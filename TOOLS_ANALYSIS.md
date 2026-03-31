# Claude Code 2.1.88 工具系统分析

## 定位

工具系统的核心入口是 `src/tools.ts`，抽象定义在 `src/Tool.ts`。

命令系统负责“用户怎么进入能力”，工具系统负责“模型真正能执行什么动作”。这也是 Claude Code 这类 agent 型 CLI 的核心层。

## 关键文件

- `src/Tool.ts`
  定义工具模型、权限上下文、工具执行上下文和工具查找机制。

- `src/tools.ts`
  汇总所有基础工具，并按权限、环境、feature flag、模式进行筛选。

- `src/utils/toolPool.ts`
  负责 REPL 路径中的工具合并、MCP 工具注入和 coordinator 模式过滤。

- `src/hooks/useMergedTools.ts`
  在交互式 REPL 中组装最终工具池。

## 工具装配机制

`src/tools.ts` 的逻辑可以概括为四步：

1. 收集所有基础工具定义
2. 根据 feature flag 和环境决定哪些工具可见
3. 根据权限上下文做 blanket deny 过滤
4. 在 REPL 里再与 MCP 工具池合并，形成最终可调用工具集合

也就是说，工具系统不是固定集合，而是一个“分阶段收缩和扩展”的工具池。

## 工具能力分层

### A. 文件与工作区操作

- `FileReadTool`
- `FileEditTool`
- `FileWriteTool`
- `GlobTool`
- `GrepTool`
- `NotebookEditTool`

这类工具负责：

- 读取文件
- 修改文件
- 写入新文件
- 文件匹配
- 内容搜索
- Notebook 编辑

这是最核心的一组本地代码操作工具。

### B. 终端与系统执行

- `BashTool`
- `PowerShellTool`
- `TerminalCaptureTool`（条件启用）
- `REPLTool`（特定环境启用）

这类工具负责：

- 执行系统命令
- 读取命令输出
- 捕获终端上下文
- 在特定模式下访问更底层的交互执行能力

这是风险最高、能力最强的一组工具。

### C. Web 与外部信息获取

- `WebFetchTool`
- `WebSearchTool`
- `WebBrowserTool`（条件启用）

这类工具负责：

- 抓取网页内容
- 做搜索查询
- 在更高级模式下与浏览器能力联动

### D. 任务与代理协作

- `AgentTool`
- `TaskCreateTool`
- `TaskGetTool`
- `TaskUpdateTool`
- `TaskListTool`
- `TaskOutputTool`
- `TaskStopTool`
- `SendMessageTool`
- `TeamCreateTool`
- `TeamDeleteTool`
- `RemoteTriggerTool`

这类工具负责：

- 创建子代理
- 管理任务对象
- 获取任务输出
- 停止任务
- 进行代理间通信
- 创建团队/协作结构

这是 Claude Code 从“单次问答工具”变成“任务型 agent 系统”的关键。

### E. 模式与会话控制

- `EnterPlanModeTool`
- `ExitPlanModeV2Tool`
- `EnterWorktreeTool`
- `ExitWorktreeTool`
- `SleepTool`
- `BriefTool`
- `SyntheticOutputTool`

这类工具负责：

- 模式切换
- 工作树切换
- 计划模式控制
- brief 输出控制
- 睡眠/等待
- 结构化输出包装

### F. MCP 与外部资源

- `ListMcpResourcesTool`
- `ReadMcpResourceTool`
- `MCPTool`
- `McpAuthTool`

这类工具负责：

- 枚举 MCP 资源
- 读取 MCP 资源
- 对接 MCP 能力
- 处理 MCP 鉴权

### G. 辅助与元能力

- `SkillTool`
- `ToolSearchTool`
- `ConfigTool`
- `TodoWriteTool`
- `LSPTool`
- `TestingPermissionTool`
- `TungstenTool`

这类工具负责：

- 技能调用
- 工具搜索
- 配置查看或修改
- TODO 写入
- LSP 集成
- 测试环境权限模拟
- 特定环境下的实验能力

## 工具能力矩阵

| 工具 | 类别 | 默认/条件 | 核心能力 | 风险面 |
| --- | --- | --- | --- | --- |
| `AgentTool` | 代理协作 | 默认 | 生成或调用子代理 | 高 |
| `AskUserQuestionTool` | 交互 | 默认 | 向用户发起补充提问 | 低 |
| `BashTool` | 系统执行 | 默认 | 执行 shell 命令 | 高 |
| `BriefTool` | 输出控制 | 默认 | 控制 brief 模式输出 | 低 |
| `ConfigTool` | 配置 | 条件 | 配置读取与修改 | 中 |
| `EnterPlanModeTool` | 模式控制 | 默认 | 进入计划模式 | 中 |
| `ExitPlanModeV2Tool` | 模式控制 | 默认 | 退出计划模式 | 中 |
| `EnterWorktreeTool` | 工作区控制 | 条件 | 进入 worktree 模式 | 中 |
| `ExitWorktreeTool` | 工作区控制 | 条件 | 退出 worktree 模式 | 中 |
| `FileEditTool` | 文件操作 | 默认 | 定点编辑现有文件 | 高 |
| `FileReadTool` | 文件操作 | 默认 | 读取文件内容 | 中 |
| `FileWriteTool` | 文件操作 | 默认 | 新建/覆盖文件 | 高 |
| `GlobTool` | 搜索 | 默认 | 文件路径匹配 | 中 |
| `GrepTool` | 搜索 | 默认 | 内容搜索 | 中 |
| `ListMcpResourcesTool` | MCP | 默认 | 列出 MCP 资源 | 中 |
| `LSPTool` | IDE/LSP | 条件 | 调用 LSP 信息 | 中 |
| `NotebookEditTool` | 文件操作 | 默认 | 修改 notebook | 高 |
| `PowerShellTool` | 系统执行 | 条件 | PowerShell 命令执行 | 高 |
| `ReadMcpResourceTool` | MCP | 默认 | 读取 MCP 资源 | 中 |
| `RemoteTriggerTool` | 远程/调度 | 条件 | 触发远程任务 | 高 |
| `REPLTool` | 终端控制 | 条件 | 特定环境下的 REPL 能力 | 高 |
| `ScheduleCronTool` | 调度 | 条件 | 创建/列出/删除 cron 任务 | 高 |
| `SendMessageTool` | 代理协作 | 条件 | 给代理/协作者发消息 | 中 |
| `SkillTool` | 扩展能力 | 默认 | 调用技能系统 | 中 |
| `SleepTool` | 模式控制 | 条件 | 等待/挂起型动作 | 低 |
| `SyntheticOutputTool` | 输出包装 | 内部 | 结构化输出工具 | 低 |
| `TaskCreateTool` | 任务 | 条件 | 创建任务 | 中 |
| `TaskGetTool` | 任务 | 条件 | 获取任务详情 | 低 |
| `TaskListTool` | 任务 | 条件 | 枚举任务 | 低 |
| `TaskOutputTool` | 任务 | 默认 | 输出任务产物 | 中 |
| `TaskStopTool` | 任务 | 默认 | 停止任务 | 中 |
| `TaskUpdateTool` | 任务 | 条件 | 更新任务状态 | 中 |
| `TeamCreateTool` | 多代理 | 条件 | 创建团队协作结构 | 中 |
| `TeamDeleteTool` | 多代理 | 条件 | 删除团队结构 | 中 |
| `TodoWriteTool` | 规划辅助 | 默认 | 写入 todo | 低 |
| `ToolSearchTool` | 元能力 | 条件 | 在工具池里搜索工具 | 低 |
| `TungstenTool` | 实验/内部 | 条件 | 特定环境实验能力 | 中 |
| `WebFetchTool` | Web | 默认 | 拉取网页内容 | 中 |
| `WebSearchTool` | Web | 默认 | 发起搜索查询 | 中 |
| `WebBrowserTool` | Web/浏览器 | 条件 | 浏览器级交互 | 高 |

## 条件启用机制

`tools.ts` 中大量工具不是默认全开，而是受以下因素控制：

- `feature('...')`
- `process.env.USER_TYPE`
- `isTodoV2Enabled()`
- `isWorktreeModeEnabled()`
- `isAgentSwarmsEnabled()`
- `isPowerShellToolEnabled()`
- `isToolSearchEnabledOptimistic()`

这说明：

- 工具系统是分发行形态和运行模式裁剪的
- 外部构建看到的工具集合，并不一定等于内部环境的工具集合
- 真正提供给模型的工具清单，是“环境相关结果”

## 工具池的两条主路径

### 1. Headless / 非交互路径

在 `main.tsx` 中直接调用：

- `getTools(toolPermissionContext)`

然后在 headless 模式下直接进入主流程。

### 2. REPL / 交互路径

在 `screens/REPL.tsx` 中：

1. 先调用 `getTools(toolPermissionContext)` 得到本地基础工具
2. 再将本地工具与 MCP 工具集合并
3. 通过 `useMergedTools` 与 `mergeAndFilterTools` 做最终过滤
4. 若主线程代理定义存在，再通过 `resolveAgentTools` 进一步裁剪

因此 REPL 路径中的最终工具集，比 `main.tsx` 里的初始工具集更动态、更依赖运行态。

## 架构判断

工具系统体现出几个非常明显的设计取向：

- 工具是第一等公民，不是命令的附属品
- 权限控制是工具池裁剪的一部分，而不是事后补丁
- 模式切换本身也被抽象成工具
- 多代理、任务、MCP、计划模式都建立在工具抽象之上

## 最值得继续深挖的工具目录

如果要继续深入工具系统，优先级最高的通常是：

1. `src/tools/AgentTool/`
2. `src/tools/BashTool/`
3. `src/tools/FileEditTool/`
4. `src/tools/PowerShellTool/`
5. `src/tools/WebSearchTool/`
6. `src/tools/ListMcpResourcesTool/`
7. `src/tools/TaskCreateTool/`
8. `src/tools/EnterPlanModeTool/`
