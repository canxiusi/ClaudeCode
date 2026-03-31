# Claude Code 2.1.88 命令系统分析

## 定位

命令系统的核心入口是 `src/commands.ts`。它承担三件事：

1. 汇总内置命令模块
2. 根据 feature flag、用户类型和运行环境决定哪些命令生效
3. 把内置命令、技能命令、插件命令、MCP 命令统一整理成最终命令池

从架构上看，命令系统是“用户入口层”，主要解决“用户能在 CLI 里触发什么能力”的问题；真正执行动作时，很多命令还会进一步调用工具系统、服务层或 REPL 查询主循环。

## 关键文件

- `src/commands.ts`
  顶层命令注册表与统一导出入口。

- `src/types/command.ts`
  命令模型、命令类型和启用逻辑的核心类型定义。

- `src/skills/loadSkillsDir.ts`
  动态技能命令的加载入口。

- `src/utils/plugins/loadPluginCommands.ts`
  插件命令与插件技能命令的加载入口。

## 命令系统分层

### 1. 注册层

`src/commands.ts` 直接导入一批命令实现，例如：

- `commands/config/index.js`
- `commands/doctor/index.js`
- `commands/review.js`
- `commands/mcp/index.js`
- `commands/tasks/index.js`
- `commands/plugin/index.js`

并通过以下机制进行筛选：

- `USER_TYPE === 'ant'`
- `feature('...')`
- 是否使用第三方服务
- 当前配置和运行模式

### 2. 聚合层

最终命令集合并不只来自内置命令，还会叠加：

- 技能目录里的动态命令
- 内置插件带来的命令
- 已安装插件带来的命令
- MCP 暴露出来的命令

因此在 REPL 中看到的命令列表，是“内置 + 动态扩展”的结果，而不是一个固定死表。

### 3. 执行层

命令的执行形态大致分三类：

- 立即执行型
  典型如 `/config`、`/doctor` 这类更偏本地 UI 或本地逻辑的命令。

- prompt 型
  将命令转成提示、上下文或查询任务，再交给主查询流程执行。

- 混合型
  既修改本地状态，又影响后续查询行为或工具集。

## 命令分类

下面按职责对内置命令做更适合阅读的分类。

### A. 会话与交互控制

这类命令主要负责当前 REPL 会话、历史、状态或交互模式切换。

- `resume`
- `session`
- `clear`
- `exit`
- `rewind`
- `summary`
- `status`
- `statusline`
- `tag`
- `rename`
- `thinkback`
- `thinkback-play`

作用特点：

- 操作当前会话状态
- 管理历史记录或会话恢复
- 影响界面呈现或当前会话元信息

### B. 配置与运行参数

这类命令主要面向配置、模型、权限、风格和环境设置。

- `config`
- `model`
- `permissions`
- `output-style`
- `theme`
- `color`
- `fast`
- `effort`
- `privacy-settings`
- `rate-limit-options`
- `env`
- `remote-env`
- `sandbox-toggle`
- `vim`
- `keybindings`

作用特点：

- 决定查询行为
- 决定工具权限和模式
- 决定终端输出与交互风格

### C. 项目与工作区操作

这类命令围绕当前代码仓库、文件、上下文和工作目录展开。

- `add-dir`
- `files`
- `context`
- `diff`
- `branch`
- `copy`
- `compact`
- `memory`
- `passes`

作用特点：

- 改变可见上下文范围
- 管理输入给模型的仓库信息
- 提供面向代码库的快捷操作

### D. 账户、安装与接入

这类命令围绕账户身份、集成安装和设备接入展开。

- `login`
- `logout`
- `oauth-refresh`
- `install-github-app`
- `install-slack-app`
- `desktop`
- `mobile`
- `ide`
- `terminalSetup`
- `chrome`

作用特点：

- 处理鉴权
- 处理外部客户端接入
- 处理桌面、移动端、IDE 或浏览器联动

### E. 插件、技能与 MCP 扩展

这类命令负责扩展机制，是系统可扩展性的核心入口。

- `mcp`
- `skills`
- `plugin`
- `reload-plugins`
- `hooks`
- `agents`
- `plan`
- `tasks`

作用特点：

- 让系统接入外部能力
- 管理命令、工具、资源与自动化组件
- 与多代理、计划模式、任务模式联动

### F. 审查、分析与诊断

这类命令主要面向审查、问题定位、数据分析和自检。

- `review`
- `security-review`
- `doctor`
- `usage`
- `insights`
- `stats`
- `cost`
- `feedback`
- `release-notes`
- `upgrade`

作用特点：

- 帮助定位问题
- 帮助分析使用情况
- 帮助审查代码或系统状态

### G. Git 与协作工作流

这类命令与 Git、PR、协作流程更强绑定。

- `commit`
- `commit-push-pr`
- `pr_comments`
- `share`
- `autofix-pr`

作用特点：

- 将模型能力接入代码提交流程
- 把审查、修复和 PR 工作流串起来

### H. 内部、实验与调试命令

这类命令更多面向 Anthropic 内部环境、实验特性或开发调试。

- `backfill-sessions`
- `break-cache`
- `bughunter`
- `ctx_viz`
- `good-claude`
- `issue`
- `init-verifiers`
- `mock-limits`
- `bridge-kick`
- `version`
- `ant-trace`
- `perf-issue`
- `debug-tool-call`
- `onboarding`
- `teleport`

作用特点：

- 很多不会在外部构建中完整保留
- 常与 feature flag 或内部用户类型绑定

## 命令清单

以下命令可从 `src/commands.ts` 直接看到其注册来源：

| 命令 | 实现位置 | 主要职责 |
| --- | --- | --- |
| `add-dir` | `src/commands/add-dir/` | 将目录加入上下文或项目工作范围 |
| `advisor` | `src/commands/advisor.js` | 与 advisor 模式或 advisor 配置相关 |
| `agents` | `src/commands/agents/` | 代理定义与代理相关命令 |
| `ant-trace` | `src/commands/ant-trace/` | 内部跟踪/诊断命令 |
| `autofix-pr` | `src/commands/autofix-pr/` | 自动修复 PR 相关问题 |
| `branch` | `src/commands/branch/` | 分支工作流辅助 |
| `break-cache` | `src/commands/break-cache/` | 内部缓存调试 |
| `bughunter` | `src/commands/bughunter/` | 问题定位或内部调试 |
| `chrome` | `src/commands/chrome/` | 浏览器或 Claude in Chrome 集成 |
| `clear` | `src/commands/clear/` | 清空当前会话或界面状态 |
| `color` | `src/commands/color/` | 颜色或终端显示相关设置 |
| `commit` | `src/commands/commit.js` | Git commit 工作流 |
| `commit-push-pr` | `src/commands/commit-push-pr.js` | 提交、推送、PR 一体化流程 |
| `compact` | `src/commands/compact/` | 压缩上下文或会话内容 |
| `config` | `src/commands/config/` | 配置查看与编辑 |
| `context` | `src/commands/context/` | 上下文查看与控制 |
| `copy` | `src/commands/copy/` | 复制输出或内容处理 |
| `cost` | `src/commands/cost/` | 使用成本与统计 |
| `ctx_viz` | `src/commands/ctx_viz/` | 上下文可视化 |
| `debug-tool-call` | `src/commands/debug-tool-call/` | 工具调用调试 |
| `desktop` | `src/commands/desktop/` | 桌面端能力或接入 |
| `diff` | `src/commands/diff/` | 代码差异查看 |
| `doctor` | `src/commands/doctor/` | 环境检查与故障诊断 |
| `effort` | `src/commands/effort/` | 推理强度设置 |
| `env` | `src/commands/env/` | 环境变量与环境信息 |
| `exit` | `src/commands/exit/` | 退出流程 |
| `export` | `src/commands/export/` | 导出会话或结果 |
| `extra-usage` | `src/commands/extra-usage/` | 额外使用统计 |
| `fast` | `src/commands/fast/` | 快速模式切换 |
| `feedback` | `src/commands/feedback/` | 反馈提交流程 |
| `files` | `src/commands/files/` | 文件与上下文文件相关操作 |
| `good-claude` | `src/commands/good-claude/` | 内部或实验命令 |
| `heapdump` | `src/commands/heapdump/` | 堆内存诊断 |
| `help` | `src/commands/help/` | 帮助系统 |
| `hooks` | `src/commands/hooks/` | hooks 配置或查看 |
| `ide` | `src/commands/ide/` | IDE 集成 |
| `init` | `src/commands/init.js` | 初始化工作流 |
| `init-verifiers` | `src/commands/init-verifiers.js` | 初始化校验器 |
| `install-github-app` | `src/commands/install-github-app/` | GitHub App 安装 |
| `install-slack-app` | `src/commands/install-slack-app/` | Slack App 安装 |
| `issue` | `src/commands/issue/` | issue 工作流 |
| `keybindings` | `src/commands/keybindings/` | 键位设置 |
| `login` | `src/commands/login/` | 登录 |
| `logout` | `src/commands/logout/` | 登出 |
| `mcp` | `src/commands/mcp/` | MCP 配置、连接和资源管理 |
| `memory` | `src/commands/memory/` | 记忆系统相关操作 |
| `mobile` | `src/commands/mobile/` | 移动端接入 |
| `mock-limits` | `src/commands/mock-limits/` | 限额模拟 |
| `model` | `src/commands/model/` | 模型切换与查看 |
| `oauth-refresh` | `src/commands/oauth-refresh/` | OAuth 刷新 |
| `onboarding` | `src/commands/onboarding/` | 新手引导 |
| `output-style` | `src/commands/output-style/` | 输出样式设置 |
| `passes` | `src/commands/passes/` | passes 相关能力 |
| `perf-issue` | `src/commands/perf-issue/` | 性能问题收集 |
| `permissions` | `src/commands/permissions/` | 权限模式管理 |
| `plan` | `src/commands/plan/` | 计划模式相关入口 |
| `plugin` | `src/commands/plugin/` | 插件管理 |
| `pr_comments` | `src/commands/pr_comments/` | PR 评论工作流 |
| `privacy-settings` | `src/commands/privacy-settings/` | 隐私设置 |
| `rate-limit-options` | `src/commands/rate-limit-options/` | 速率/额度设置 |
| `release-notes` | `src/commands/release-notes/` | 版本说明展示 |
| `reload-plugins` | `src/commands/reload-plugins/` | 重新加载插件 |
| `remote-env` | `src/commands/remote-env/` | 远程环境设置 |
| `resume` | `src/commands/resume/` | 恢复会话 |
| `review` | `src/commands/review.js` | 代码审查工作流 |
| `rewind` | `src/commands/rewind/` | 回滚到先前状态 |
| `sandbox-toggle` | `src/commands/sandbox-toggle/` | 沙箱模式切换 |
| `security-review` | `src/commands/security-review.js` | 安全审查 |
| `session` | `src/commands/session/` | 会话元数据与状态操作 |
| `share` | `src/commands/share/` | 分享会话或结果 |
| `skills` | `src/commands/skills/` | 技能管理 |
| `stats` | `src/commands/stats/` | 状态或指标统计 |
| `status` | `src/commands/status/` | 当前状态展示 |
| `stickers` | `src/commands/stickers/` | 贴纸/辅助展示类命令 |
| `summary` | `src/commands/summary/` | 摘要信息 |
| `tag` | `src/commands/tag/` | 标签管理 |
| `tasks` | `src/commands/tasks/` | 任务模式与任务管理 |
| `teleport` | `src/commands/teleport/` | 远程传送/远端恢复 |
| `terminalSetup` | `src/commands/terminalSetup/` | 终端环境设置 |
| `theme` | `src/commands/theme/` | 主题切换 |
| `thinkback` | `src/commands/thinkback/` | 回溯式分析 |
| `thinkback-play` | `src/commands/thinkback-play/` | thinkback 重放 |
| `upgrade` | `src/commands/upgrade/` | 升级相关逻辑 |
| `usage` | `src/commands/usage/` | 使用量与报告 |
| `vim` | `src/commands/vim/` | vim 模式与键位 |
| `voice` | `src/commands/voice/` | 语音模式 |

## 架构判断

从命令系统的组织方式可以看出几个明显特征：

- 命令系统不是孤立层，而是“前台入口层”
- 许多命令本身不直接完成复杂工作，而是切换状态、构造上下文、触发工具或查询
- 命令集合是动态扩展的，插件、技能和 MCP 都能向这层注入能力
- `commands.ts` 的价值不是“实现命令”，而是“统一定义系统外部接口面”

## 最值得继续深挖的命令目录

如果要继续深读命令系统，优先级最高的通常是：

1. `src/commands/config/`
2. `src/commands/mcp/`
3. `src/commands/tasks/`
4. `src/commands/plugin/`
5. `src/commands/review.js`
6. `src/commands/doctor/`
7. `src/commands/resume/`
