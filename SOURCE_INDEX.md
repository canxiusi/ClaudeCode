# Claude Code 2.1.88 全量源码索引

> 这是一份基于还原后 `src/**` 源码树生成的全量目录与文件索引，按目录分组列出每个文件，并附上一条首轮作用说明，便于通读、检索和定位。

## 统计概览

- 总文件数：1902
- 总目录数：293
- 顶层重点模块：
  - `utils`：564
  - `components`：389
  - `commands`：207
  - `tools`：184
  - `services`：130
  - `hooks`：104
  - `ink`：96
  - `bridge`：31
  - `constants`：21
  - `skills`：20
  - `cli`：19
  - `.`：18
  - `keybindings`：14
  - `tasks`：12
  - `migrations`：11

## 阅读建议

- 先读 `src/main.tsx`、`src/commands.ts`、`src/tools.ts`、`src/Task.ts`、`src/Tool.ts`。
- 再按关注方向阅读 `commands/`、`tools/`、`components/`、`services/`、`utils/`。
- 这份索引覆盖全部文件，但文件作用说明仍属首轮导读级别，后续可配合专题文档继续深挖。

## 顶层结构

- `.`：18 个文件，根入口文件，负责启动、总装配、核心对象定义与跨模块桥接。
- `assistant`：1 个文件，assistant / kairos 相关能力，通常与特殊会话模式或历史管理有关。
- `bootstrap`：1 个文件，启动阶段共享状态与启动上下文初始化。
- `bridge`：31 个文件，桥接模式、桥接通信与桥接端 UI / 状态控制。
- `buddy`：6 个文件，buddy 相关角色、提示词、展示组件与辅助交互。
- `cli`：19 个文件，CLI 输出、传输和结构化终端交互适配层。
- `commands`：207 个文件，顶层命令系统，定义 CLI 可用命令与命令注册。
- `components`：389 个文件，终端 UI 组件主目录。
- `constants`：21 个文件，全局常量定义。
- `context`：9 个文件，React/Ink 上下文与共享状态入口。
- `coordinator`：1 个文件，协调模式或多代理协调相关能力。
- `entrypoints`：8 个文件，不同运行入口与初始化适配。
- `hooks`：104 个文件，通用 React/Ink hooks。
- `ink`：96 个文件，终端渲染、布局、事件和低层终端支持。
- `keybindings`：14 个文件，键位绑定与输入行为控制。
- `memdir`：8 个文件，记忆目录扫描、过滤、排序与读取。
- `migrations`：11 个文件，配置、模型、设置迁移逻辑。
- `moreright`：1 个文件，特定交互增强逻辑。
- `native-ts`：4 个文件，原生能力封装或性能敏感模块。
- `outputStyles`：1 个文件，输出样式加载。
- `plugins`：2 个文件，插件系统入口。
- `query`：4 个文件，查询构建与查询约束辅助模块。
- `remote`：4 个文件，远程会话和远程代理适配。
- `schemas`：1 个文件，Schema 定义。
- `screens`：3 个文件，终端主要页面组件。
- `server`：3 个文件，服务端连接、直连会话与服务端类型。
- `services`：130 个文件，跨模块服务层，对接外部系统或大型子系统。
- `skills`：20 个文件，技能系统入口与加载逻辑。
- `state`：6 个文件，应用状态、状态仓库与状态监听。
- `tasks`：12 个文件，任务类型与不同任务执行器。
- `tools`：184 个文件，工具系统入口与工具注册。
- `types`：11 个文件，共享类型定义。
- `upstreamproxy`：2 个文件，上游代理转发相关逻辑。
- `utils`：564 个文件，最大基础设施层，放置配置、权限、日志、Git、模型、文件系统等通用能力。
- `vim`：5 个文件，vim 风格操作和文本对象。
- `voice`：1 个文件，语音模式开关与支持逻辑。

## 目录：`.`

- 文件数：18
- 目录作用：根入口文件，负责启动、总装配、核心对象定义与跨模块桥接。

- `commands.ts`：实现 commands 相关逻辑。
- `context.ts`：定义上下文对象或上下文获取逻辑。
- `cost-tracker.ts`：实现 cost tracker 相关逻辑。
- `costHook.ts`：实现单个 hook。
- `dialogLaunchers.tsx`：定义 dialog launchers 相关界面或交互组件。
- `history.ts`：处理历史记录、会话历史或历史状态。
- `ink.ts`：实现 ink 相关逻辑。
- `interactiveHelpers.tsx`：存放该模块的辅助函数。
- `main.tsx`：定义 main 相关界面或交互组件。
- `projectOnboardingState.ts`：实现 project onboarding state 相关逻辑。
- `query.ts`：实现 query 相关逻辑。
- `QueryEngine.ts`：实现 query engine 相关逻辑。
- `replLauncher.tsx`：负责启动对应模式、界面或流程。
- `setup.ts`：实现 setup 相关逻辑。
- `Task.ts`：处理任务对象、任务状态或任务执行流程。
- `tasks.ts`：处理任务对象、任务状态或任务执行流程。
- `Tool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools.ts`：实现 tools 相关逻辑。

## 目录：`assistant`

- 文件数：1
- 目录作用：assistant / kairos 相关能力，通常与特殊会话模式或历史管理有关。

- `assistant/sessionHistory.ts`：处理历史记录、会话历史或历史状态。

## 目录：`bootstrap`

- 文件数：1
- 目录作用：启动阶段共享状态与启动上下文初始化。

- `bootstrap/state.ts`：实现 state 相关逻辑。

## 目录：`bridge`

- 文件数：31
- 目录作用：桥接模式、桥接通信与桥接端 UI / 状态控制。

- `bridge/bridgeApi.ts`：实现 bridge api 相关逻辑。
- `bridge/bridgeConfig.ts`：处理配置项、配置解析或配置结构。
- `bridge/bridgeDebug.ts`：实现 bridge debug 相关逻辑。
- `bridge/bridgeEnabled.ts`：实现 bridge enabled 相关逻辑。
- `bridge/bridgeMain.ts`：实现 bridge main 相关逻辑。
- `bridge/bridgeMessaging.ts`：实现 bridge messaging 相关逻辑。
- `bridge/bridgePermissionCallbacks.ts`：处理权限检查、权限请求或权限规则。
- `bridge/bridgePointer.ts`：实现 bridge pointer 相关逻辑。
- `bridge/bridgeStatusUtil.ts`：存放该模块的通用工具函数。
- `bridge/bridgeUI.ts`：实现 bridge ui 相关逻辑。
- `bridge/capacityWake.ts`：实现 capacity wake 相关逻辑。
- `bridge/codeSessionApi.ts`：处理会话对象、会话恢复或会话同步。
- `bridge/createSession.ts`：处理会话对象、会话恢复或会话同步。
- `bridge/debugUtils.ts`：存放该模块的通用工具函数。
- `bridge/envLessBridgeConfig.ts`：处理配置项、配置解析或配置结构。
- `bridge/flushGate.ts`：实现 flush gate 相关逻辑。
- `bridge/inboundAttachments.ts`：实现 inbound attachments 相关逻辑。
- `bridge/inboundMessages.ts`：处理消息结构、消息渲染或消息转换。
- `bridge/initReplBridge.ts`：实现 init repl bridge 相关逻辑。
- `bridge/jwtUtils.ts`：存放该模块的通用工具函数。
- `bridge/pollConfig.ts`：处理配置项、配置解析或配置结构。
- `bridge/pollConfigDefaults.ts`：处理配置项、配置解析或配置结构。
- `bridge/remoteBridgeCore.ts`：实现 remote bridge core 相关逻辑。
- `bridge/replBridge.ts`：实现 repl bridge 相关逻辑。
- `bridge/replBridgeHandle.ts`：实现 repl bridge handle 相关逻辑。
- `bridge/replBridgeTransport.ts`：实现 repl bridge transport 相关逻辑。
- `bridge/sessionIdCompat.ts`：处理会话对象、会话恢复或会话同步。
- `bridge/sessionRunner.ts`：处理会话对象、会话恢复或会话同步。
- `bridge/trustedDevice.ts`：实现 trusted device 相关逻辑。
- `bridge/types.ts`：定义这一模块相关的共享类型或结构。
- `bridge/workSecret.ts`：实现 work secret 相关逻辑。

## 目录：`buddy`

- 文件数：6
- 目录作用：buddy 相关角色、提示词、展示组件与辅助交互。

- `buddy/companion.ts`：实现 companion 相关逻辑。
- `buddy/CompanionSprite.tsx`：定义 companion sprite 相关界面或交互组件。
- `buddy/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `buddy/sprites.ts`：实现 sprites 相关逻辑。
- `buddy/types.ts`：定义这一模块相关的共享类型或结构。
- `buddy/useBuddyNotification.tsx`：定义 use buddy notification 相关界面或交互组件。

## 目录：`cli`

- 文件数：6
- 目录作用：CLI 输出、传输和结构化终端交互适配层。

- `cli/exit.ts`：实现 exit 相关逻辑。
- `cli/ndjsonSafeStringify.ts`：实现 ndjson safe stringify 相关逻辑。
- `cli/print.ts`：实现 print 相关逻辑。
- `cli/remoteIO.ts`：实现 remote io 相关逻辑。
- `cli/structuredIO.ts`：实现 structured io 相关逻辑。
- `cli/update.ts`：实现 update 相关逻辑。

## 目录：`cli/handlers`

- 文件数：6
- 目录作用：CLI 输出处理器与消息落地逻辑。

- `cli/handlers/agents.ts`：处理代理、子代理或代理展示相关逻辑。
- `cli/handlers/auth.ts`：实现 auth 相关逻辑。
- `cli/handlers/autoMode.ts`：实现 auto mode 相关逻辑。
- `cli/handlers/mcp.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `cli/handlers/plugins.ts`：处理插件发现、加载、缓存或插件命令。
- `cli/handlers/util.tsx`：存放该模块的通用工具函数。

## 目录：`cli/transports`

- 文件数：7
- 目录作用：CLI 输出 / 事件传输层。

- `cli/transports/ccrClient.ts`：实现 ccr client 相关逻辑。
- `cli/transports/HybridTransport.ts`：实现 hybrid transport 相关逻辑。
- `cli/transports/SerialBatchEventUploader.ts`：实现 serial batch event uploader 相关逻辑。
- `cli/transports/SSETransport.ts`：实现 ssetransport 相关逻辑。
- `cli/transports/transportUtils.ts`：存放该模块的通用工具函数。
- `cli/transports/WebSocketTransport.ts`：实现 web socket transport 相关逻辑。
- `cli/transports/WorkerStateUploader.ts`：实现 worker state uploader 相关逻辑。

## 目录：`commands`

- 文件数：15
- 目录作用：顶层命令系统，定义 CLI 可用命令与命令注册。

- `commands/advisor.ts`：实现 advisor 相关逻辑。
- `commands/bridge-kick.ts`：实现 bridge kick 相关逻辑。
- `commands/brief.ts`：实现 brief 相关逻辑。
- `commands/commit-push-pr.ts`：实现 commit push pr 相关逻辑。
- `commands/commit.ts`：实现 commit 相关逻辑。
- `commands/createMovedToPluginCommand.ts`：定义一个具体命令的注册与执行逻辑。
- `commands/init-verifiers.ts`：实现 init verifiers 相关逻辑。
- `commands/init.ts`：实现 init 相关逻辑。
- `commands/insights.ts`：实现 insights 相关逻辑。
- `commands/install.tsx`：定义 install 相关界面或交互组件。
- `commands/review.ts`：处理审查、评审或 review 工作流逻辑。
- `commands/security-review.ts`：处理审查、评审或 review 工作流逻辑。
- `commands/statusline.tsx`：定义 statusline 相关界面或交互组件。
- `commands/ultraplan.tsx`：定义 ultraplan 相关界面或交互组件。
- `commands/version.ts`：实现 version 相关逻辑。

## 目录：`commands/add-dir`

- 文件数：3
- 目录作用：这一目录聚合了一组与 add-dir 相关的实现。

- `commands/add-dir/add-dir.tsx`：实现 add dir 命令相关逻辑。
- `commands/add-dir/index.ts`：该目录的导出入口或聚合入口。
- `commands/add-dir/validation.ts`：实现 validation 命令相关逻辑。

## 目录：`commands/agents`

- 文件数：2
- 目录作用：这一目录聚合了一组与 agents 相关的实现。

- `commands/agents/agents.tsx`：处理代理、子代理或代理展示相关逻辑。
- `commands/agents/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/ant-trace`

- 文件数：1
- 目录作用：这一目录聚合了一组与 ant-trace 相关的实现。

- `commands/ant-trace/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/autofix-pr`

- 文件数：1
- 目录作用：这一目录聚合了一组与 autofix-pr 相关的实现。

- `commands/autofix-pr/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/backfill-sessions`

- 文件数：1
- 目录作用：这一目录聚合了一组与 backfill-sessions 相关的实现。

- `commands/backfill-sessions/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/branch`

- 文件数：2
- 目录作用：这一目录聚合了一组与 branch 相关的实现。

- `commands/branch/branch.ts`：实现 branch 命令相关逻辑。
- `commands/branch/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/break-cache`

- 文件数：1
- 目录作用：这一目录聚合了一组与 break-cache 相关的实现。

- `commands/break-cache/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/bridge`

- 文件数：2
- 目录作用：这一目录聚合了一组与 bridge 相关的实现。

- `commands/bridge/bridge.tsx`：实现 bridge 命令相关逻辑。
- `commands/bridge/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/btw`

- 文件数：2
- 目录作用：这一目录聚合了一组与 btw 相关的实现。

- `commands/btw/btw.tsx`：实现 btw 命令相关逻辑。
- `commands/btw/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/bughunter`

- 文件数：1
- 目录作用：这一目录聚合了一组与 bughunter 相关的实现。

- `commands/bughunter/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/chrome`

- 文件数：2
- 目录作用：这一目录聚合了一组与 chrome 相关的实现。

- `commands/chrome/chrome.tsx`：实现 chrome 命令相关逻辑。
- `commands/chrome/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/clear`

- 文件数：4
- 目录作用：这一目录聚合了一组与 clear 相关的实现。

- `commands/clear/caches.ts`：实现 caches 命令相关逻辑。
- `commands/clear/clear.ts`：实现 clear 命令相关逻辑。
- `commands/clear/conversation.ts`：实现 conversation 命令相关逻辑。
- `commands/clear/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/color`

- 文件数：2
- 目录作用：这一目录聚合了一组与 color 相关的实现。

- `commands/color/color.ts`：实现 color 命令相关逻辑。
- `commands/color/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/compact`

- 文件数：2
- 目录作用：这一目录聚合了一组与 compact 相关的实现。

- `commands/compact/compact.ts`：实现 compact 命令相关逻辑。
- `commands/compact/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/config`

- 文件数：2
- 目录作用：这一目录聚合了一组与 config 相关的实现。

- `commands/config/config.tsx`：处理配置项、配置解析或配置结构。
- `commands/config/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/context`

- 文件数：3
- 目录作用：这一目录聚合了一组与 context 相关的实现。

- `commands/context/context-noninteractive.ts`：实现 context noninteractive 命令相关逻辑。
- `commands/context/context.tsx`：定义上下文对象或上下文获取逻辑。
- `commands/context/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/copy`

- 文件数：2
- 目录作用：这一目录聚合了一组与 copy 相关的实现。

- `commands/copy/copy.tsx`：实现 copy 命令相关逻辑。
- `commands/copy/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/cost`

- 文件数：2
- 目录作用：这一目录聚合了一组与 cost 相关的实现。

- `commands/cost/cost.ts`：实现 cost 命令相关逻辑。
- `commands/cost/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/ctx_viz`

- 文件数：1
- 目录作用：这一目录聚合了一组与 ctx_viz 相关的实现。

- `commands/ctx_viz/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/debug-tool-call`

- 文件数：1
- 目录作用：这一目录聚合了一组与 debug-tool-call 相关的实现。

- `commands/debug-tool-call/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/desktop`

- 文件数：2
- 目录作用：这一目录聚合了一组与 desktop 相关的实现。

- `commands/desktop/desktop.tsx`：实现 desktop 命令相关逻辑。
- `commands/desktop/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/diff`

- 文件数：2
- 目录作用：这一目录聚合了一组与 diff 相关的实现。

- `commands/diff/diff.tsx`：处理差异展示、差异格式化或差异比较。
- `commands/diff/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/doctor`

- 文件数：2
- 目录作用：这一目录聚合了一组与 doctor 相关的实现。

- `commands/doctor/doctor.tsx`：实现 doctor 命令相关逻辑。
- `commands/doctor/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/effort`

- 文件数：2
- 目录作用：这一目录聚合了一组与 effort 相关的实现。

- `commands/effort/effort.tsx`：实现 effort 命令相关逻辑。
- `commands/effort/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/env`

- 文件数：1
- 目录作用：这一目录聚合了一组与 env 相关的实现。

- `commands/env/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/exit`

- 文件数：2
- 目录作用：这一目录聚合了一组与 exit 相关的实现。

- `commands/exit/exit.tsx`：实现 exit 命令相关逻辑。
- `commands/exit/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/export`

- 文件数：2
- 目录作用：这一目录聚合了一组与 export 相关的实现。

- `commands/export/export.tsx`：实现 export 命令相关逻辑。
- `commands/export/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/extra-usage`

- 文件数：4
- 目录作用：这一目录聚合了一组与 extra-usage 相关的实现。

- `commands/extra-usage/extra-usage-core.ts`：实现 extra usage core 命令相关逻辑。
- `commands/extra-usage/extra-usage-noninteractive.ts`：实现 extra usage noninteractive 命令相关逻辑。
- `commands/extra-usage/extra-usage.tsx`：实现 extra usage 命令相关逻辑。
- `commands/extra-usage/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/fast`

- 文件数：2
- 目录作用：这一目录聚合了一组与 fast 相关的实现。

- `commands/fast/fast.tsx`：实现 fast 命令相关逻辑。
- `commands/fast/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/feedback`

- 文件数：2
- 目录作用：这一目录聚合了一组与 feedback 相关的实现。

- `commands/feedback/feedback.tsx`：实现 feedback 命令相关逻辑。
- `commands/feedback/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/files`

- 文件数：2
- 目录作用：这一目录聚合了一组与 files 相关的实现。

- `commands/files/files.ts`：实现 files 命令相关逻辑。
- `commands/files/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/good-claude`

- 文件数：1
- 目录作用：这一目录聚合了一组与 good-claude 相关的实现。

- `commands/good-claude/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/heapdump`

- 文件数：2
- 目录作用：这一目录聚合了一组与 heapdump 相关的实现。

- `commands/heapdump/heapdump.ts`：实现 heapdump 命令相关逻辑。
- `commands/heapdump/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/help`

- 文件数：2
- 目录作用：这一目录聚合了一组与 help 相关的实现。

- `commands/help/help.tsx`：实现 help 命令相关逻辑。
- `commands/help/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/hooks`

- 文件数：2
- 目录作用：这一目录聚合了一组与 hooks 相关的实现。

- `commands/hooks/hooks.tsx`：实现 hooks 命令相关逻辑。
- `commands/hooks/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/ide`

- 文件数：2
- 目录作用：这一目录聚合了一组与 ide 相关的实现。

- `commands/ide/ide.tsx`：实现 ide 命令相关逻辑。
- `commands/ide/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/install-github-app`

- 文件数：14
- 目录作用：这一目录聚合了一组与 install-github-app 相关的实现。

- `commands/install-github-app/ApiKeyStep.tsx`：实现 api key step 命令相关逻辑。
- `commands/install-github-app/CheckExistingSecretStep.tsx`：实现 check existing secret step 命令相关逻辑。
- `commands/install-github-app/CheckGitHubStep.tsx`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `commands/install-github-app/ChooseRepoStep.tsx`：实现 choose repo step 命令相关逻辑。
- `commands/install-github-app/CreatingStep.tsx`：实现 creating step 命令相关逻辑。
- `commands/install-github-app/ErrorStep.tsx`：实现 error step 命令相关逻辑。
- `commands/install-github-app/ExistingWorkflowStep.tsx`：实现 existing workflow step 命令相关逻辑。
- `commands/install-github-app/index.ts`：该目录的导出入口或聚合入口。
- `commands/install-github-app/install-github-app.tsx`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `commands/install-github-app/InstallAppStep.tsx`：实现 install app step 命令相关逻辑。
- `commands/install-github-app/OAuthFlowStep.tsx`：处理 OAuth 登录或鉴权相关逻辑。
- `commands/install-github-app/setupGitHubActions.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `commands/install-github-app/SuccessStep.tsx`：实现 success step 命令相关逻辑。
- `commands/install-github-app/WarningsStep.tsx`：实现 warnings step 命令相关逻辑。

## 目录：`commands/install-slack-app`

- 文件数：2
- 目录作用：这一目录聚合了一组与 install-slack-app 相关的实现。

- `commands/install-slack-app/index.ts`：该目录的导出入口或聚合入口。
- `commands/install-slack-app/install-slack-app.ts`：实现 install slack app 命令相关逻辑。

## 目录：`commands/issue`

- 文件数：1
- 目录作用：这一目录聚合了一组与 issue 相关的实现。

- `commands/issue/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/keybindings`

- 文件数：2
- 目录作用：这一目录聚合了一组与 keybindings 相关的实现。

- `commands/keybindings/index.ts`：该目录的导出入口或聚合入口。
- `commands/keybindings/keybindings.ts`：实现 keybindings 命令相关逻辑。

## 目录：`commands/login`

- 文件数：2
- 目录作用：这一目录聚合了一组与 login 相关的实现。

- `commands/login/index.ts`：该目录的导出入口或聚合入口。
- `commands/login/login.tsx`：处理登录或登出相关逻辑。

## 目录：`commands/logout`

- 文件数：2
- 目录作用：这一目录聚合了一组与 logout 相关的实现。

- `commands/logout/index.ts`：该目录的导出入口或聚合入口。
- `commands/logout/logout.tsx`：处理登录或登出相关逻辑。

## 目录：`commands/mcp`

- 文件数：4
- 目录作用：这一目录聚合了一组与 mcp 相关的实现。

- `commands/mcp/addCommand.ts`：定义一个具体命令的注册与执行逻辑。
- `commands/mcp/index.ts`：该目录的导出入口或聚合入口。
- `commands/mcp/mcp.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `commands/mcp/xaaIdpCommand.ts`：定义一个具体命令的注册与执行逻辑。

## 目录：`commands/memory`

- 文件数：2
- 目录作用：这一目录聚合了一组与 memory 相关的实现。

- `commands/memory/index.ts`：该目录的导出入口或聚合入口。
- `commands/memory/memory.tsx`：处理记忆读取、记忆提取或记忆组织。

## 目录：`commands/mobile`

- 文件数：2
- 目录作用：这一目录聚合了一组与 mobile 相关的实现。

- `commands/mobile/index.ts`：该目录的导出入口或聚合入口。
- `commands/mobile/mobile.tsx`：实现 mobile 命令相关逻辑。

## 目录：`commands/mock-limits`

- 文件数：1
- 目录作用：这一目录聚合了一组与 mock-limits 相关的实现。

- `commands/mock-limits/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/model`

- 文件数：2
- 目录作用：这一目录聚合了一组与 model 相关的实现。

- `commands/model/index.ts`：该目录的导出入口或聚合入口。
- `commands/model/model.tsx`：处理模型选择、模型能力或模型字符串映射。

## 目录：`commands/oauth-refresh`

- 文件数：1
- 目录作用：这一目录聚合了一组与 oauth-refresh 相关的实现。

- `commands/oauth-refresh/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/onboarding`

- 文件数：1
- 目录作用：这一目录聚合了一组与 onboarding 相关的实现。

- `commands/onboarding/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/output-style`

- 文件数：2
- 目录作用：这一目录聚合了一组与 output-style 相关的实现。

- `commands/output-style/index.ts`：该目录的导出入口或聚合入口。
- `commands/output-style/output-style.tsx`：实现 output style 命令相关逻辑。

## 目录：`commands/passes`

- 文件数：2
- 目录作用：这一目录聚合了一组与 passes 相关的实现。

- `commands/passes/index.ts`：该目录的导出入口或聚合入口。
- `commands/passes/passes.tsx`：实现 passes 命令相关逻辑。

## 目录：`commands/perf-issue`

- 文件数：1
- 目录作用：这一目录聚合了一组与 perf-issue 相关的实现。

- `commands/perf-issue/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/permissions`

- 文件数：2
- 目录作用：这一目录聚合了一组与 permissions 相关的实现。

- `commands/permissions/index.ts`：该目录的导出入口或聚合入口。
- `commands/permissions/permissions.tsx`：处理权限检查、权限请求或权限规则。

## 目录：`commands/plan`

- 文件数：2
- 目录作用：这一目录聚合了一组与 plan 相关的实现。

- `commands/plan/index.ts`：该目录的导出入口或聚合入口。
- `commands/plan/plan.tsx`：实现 plan 命令相关逻辑。

## 目录：`commands/plugin`

- 文件数：17
- 目录作用：这一目录聚合了一组与 plugin 相关的实现。

- `commands/plugin/AddMarketplace.tsx`：实现 add marketplace 命令相关逻辑。
- `commands/plugin/BrowseMarketplace.tsx`：实现 browse marketplace 命令相关逻辑。
- `commands/plugin/DiscoverPlugins.tsx`：处理插件发现、加载、缓存或插件命令。
- `commands/plugin/index.tsx`：该目录的导出入口或聚合入口。
- `commands/plugin/ManageMarketplaces.tsx`：实现 manage marketplaces 命令相关逻辑。
- `commands/plugin/ManagePlugins.tsx`：处理插件发现、加载、缓存或插件命令。
- `commands/plugin/parseArgs.ts`：实现 parse args 命令相关逻辑。
- `commands/plugin/plugin.tsx`：处理插件发现、加载、缓存或插件命令。
- `commands/plugin/pluginDetailsHelpers.tsx`：存放该模块的辅助函数。
- `commands/plugin/PluginErrors.tsx`：处理插件发现、加载、缓存或插件命令。
- `commands/plugin/PluginOptionsDialog.tsx`：定义一个对话框界面。
- `commands/plugin/PluginOptionsFlow.tsx`：处理插件发现、加载、缓存或插件命令。
- `commands/plugin/PluginSettings.tsx`：处理设置读取、缓存、校验或写入。
- `commands/plugin/PluginTrustWarning.tsx`：处理插件发现、加载、缓存或插件命令。
- `commands/plugin/UnifiedInstalledCell.tsx`：实现 unified installed cell 命令相关逻辑。
- `commands/plugin/usePagination.ts`：实现 use pagination 命令相关逻辑。
- `commands/plugin/ValidatePlugin.tsx`：处理插件发现、加载、缓存或插件命令。

## 目录：`commands/pr_comments`

- 文件数：1
- 目录作用：这一目录聚合了一组与 pr_comments 相关的实现。

- `commands/pr_comments/index.ts`：该目录的导出入口或聚合入口。

## 目录：`commands/privacy-settings`

- 文件数：2
- 目录作用：这一目录聚合了一组与 privacy-settings 相关的实现。

- `commands/privacy-settings/index.ts`：该目录的导出入口或聚合入口。
- `commands/privacy-settings/privacy-settings.tsx`：处理设置读取、缓存、校验或写入。

## 目录：`commands/rate-limit-options`

- 文件数：2
- 目录作用：这一目录聚合了一组与 rate-limit-options 相关的实现。

- `commands/rate-limit-options/index.ts`：该目录的导出入口或聚合入口。
- `commands/rate-limit-options/rate-limit-options.tsx`：实现 rate limit options 命令相关逻辑。

## 目录：`commands/release-notes`

- 文件数：2
- 目录作用：这一目录聚合了一组与 release-notes 相关的实现。

- `commands/release-notes/index.ts`：该目录的导出入口或聚合入口。
- `commands/release-notes/release-notes.ts`：实现 release notes 命令相关逻辑。

## 目录：`commands/reload-plugins`

- 文件数：2
- 目录作用：这一目录聚合了一组与 reload-plugins 相关的实现。

- `commands/reload-plugins/index.ts`：该目录的导出入口或聚合入口。
- `commands/reload-plugins/reload-plugins.ts`：处理插件发现、加载、缓存或插件命令。

## 目录：`commands/remote-env`

- 文件数：2
- 目录作用：这一目录聚合了一组与 remote-env 相关的实现。

- `commands/remote-env/index.ts`：该目录的导出入口或聚合入口。
- `commands/remote-env/remote-env.tsx`：实现 remote env 命令相关逻辑。

## 目录：`commands/remote-setup`

- 文件数：3
- 目录作用：这一目录聚合了一组与 remote-setup 相关的实现。

- `commands/remote-setup/api.ts`：实现 api 命令相关逻辑。
- `commands/remote-setup/index.ts`：该目录的导出入口或聚合入口。
- `commands/remote-setup/remote-setup.tsx`：实现 remote setup 命令相关逻辑。

## 目录：`commands/rename`

- 文件数：3
- 目录作用：这一目录聚合了一组与 rename 相关的实现。

- `commands/rename/generateSessionName.ts`：处理会话对象、会话恢复或会话同步。
- `commands/rename/index.ts`：该目录的导出入口或聚合入口。
- `commands/rename/rename.ts`：实现 rename 命令相关逻辑。

## 目录：`commands/reset-limits`

- 文件数：1
- 目录作用：这一目录聚合了一组与 reset-limits 相关的实现。

- `commands/reset-limits/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/resume`

- 文件数：2
- 目录作用：这一目录聚合了一组与 resume 相关的实现。

- `commands/resume/index.ts`：该目录的导出入口或聚合入口。
- `commands/resume/resume.tsx`：实现 resume 命令相关逻辑。

## 目录：`commands/review`

- 文件数：4
- 目录作用：这一目录聚合了一组与 review 相关的实现。

- `commands/review/reviewRemote.ts`：处理审查、评审或 review 工作流逻辑。
- `commands/review/ultrareviewCommand.tsx`：定义一个具体命令的注册与执行逻辑。
- `commands/review/ultrareviewEnabled.ts`：处理审查、评审或 review 工作流逻辑。
- `commands/review/UltrareviewOverageDialog.tsx`：定义一个对话框界面。

## 目录：`commands/rewind`

- 文件数：2
- 目录作用：这一目录聚合了一组与 rewind 相关的实现。

- `commands/rewind/index.ts`：该目录的导出入口或聚合入口。
- `commands/rewind/rewind.ts`：实现 rewind 命令相关逻辑。

## 目录：`commands/sandbox-toggle`

- 文件数：2
- 目录作用：这一目录聚合了一组与 sandbox-toggle 相关的实现。

- `commands/sandbox-toggle/index.ts`：该目录的导出入口或聚合入口。
- `commands/sandbox-toggle/sandbox-toggle.tsx`：处理沙箱模式、沙箱权限或沙箱桥接。

## 目录：`commands/session`

- 文件数：2
- 目录作用：这一目录聚合了一组与 session 相关的实现。

- `commands/session/index.ts`：该目录的导出入口或聚合入口。
- `commands/session/session.tsx`：处理会话对象、会话恢复或会话同步。

## 目录：`commands/share`

- 文件数：1
- 目录作用：这一目录聚合了一组与 share 相关的实现。

- `commands/share/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/skills`

- 文件数：2
- 目录作用：这一目录聚合了一组与 skills 相关的实现。

- `commands/skills/index.ts`：该目录的导出入口或聚合入口。
- `commands/skills/skills.tsx`：处理技能加载、索引、解析或技能运行支持。

## 目录：`commands/stats`

- 文件数：2
- 目录作用：这一目录聚合了一组与 stats 相关的实现。

- `commands/stats/index.ts`：该目录的导出入口或聚合入口。
- `commands/stats/stats.tsx`：实现 stats 命令相关逻辑。

## 目录：`commands/status`

- 文件数：2
- 目录作用：这一目录聚合了一组与 status 相关的实现。

- `commands/status/index.ts`：该目录的导出入口或聚合入口。
- `commands/status/status.tsx`：实现 status 命令相关逻辑。

## 目录：`commands/stickers`

- 文件数：2
- 目录作用：这一目录聚合了一组与 stickers 相关的实现。

- `commands/stickers/index.ts`：该目录的导出入口或聚合入口。
- `commands/stickers/stickers.ts`：实现 stickers 命令相关逻辑。

## 目录：`commands/summary`

- 文件数：1
- 目录作用：这一目录聚合了一组与 summary 相关的实现。

- `commands/summary/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/tag`

- 文件数：2
- 目录作用：这一目录聚合了一组与 tag 相关的实现。

- `commands/tag/index.ts`：该目录的导出入口或聚合入口。
- `commands/tag/tag.tsx`：实现 tag 命令相关逻辑。

## 目录：`commands/tasks`

- 文件数：2
- 目录作用：这一目录聚合了一组与 tasks 相关的实现。

- `commands/tasks/index.ts`：该目录的导出入口或聚合入口。
- `commands/tasks/tasks.tsx`：处理任务对象、任务状态或任务执行流程。

## 目录：`commands/teleport`

- 文件数：1
- 目录作用：这一目录聚合了一组与 teleport 相关的实现。

- `commands/teleport/index.js`：该目录的导出入口或聚合入口。

## 目录：`commands/terminalSetup`

- 文件数：2
- 目录作用：这一目录聚合了一组与 terminalSetup 相关的实现。

- `commands/terminalSetup/index.ts`：该目录的导出入口或聚合入口。
- `commands/terminalSetup/terminalSetup.tsx`：实现 terminal setup 命令相关逻辑。

## 目录：`commands/theme`

- 文件数：2
- 目录作用：这一目录聚合了一组与 theme 相关的实现。

- `commands/theme/index.ts`：该目录的导出入口或聚合入口。
- `commands/theme/theme.tsx`：处理主题、颜色或样式切换。

## 目录：`commands/thinkback`

- 文件数：2
- 目录作用：这一目录聚合了一组与 thinkback 相关的实现。

- `commands/thinkback/index.ts`：该目录的导出入口或聚合入口。
- `commands/thinkback/thinkback.tsx`：实现 thinkback 命令相关逻辑。

## 目录：`commands/thinkback-play`

- 文件数：2
- 目录作用：这一目录聚合了一组与 thinkback-play 相关的实现。

- `commands/thinkback-play/index.ts`：该目录的导出入口或聚合入口。
- `commands/thinkback-play/thinkback-play.ts`：实现 thinkback play 命令相关逻辑。

## 目录：`commands/upgrade`

- 文件数：2
- 目录作用：这一目录聚合了一组与 upgrade 相关的实现。

- `commands/upgrade/index.ts`：该目录的导出入口或聚合入口。
- `commands/upgrade/upgrade.tsx`：实现 upgrade 命令相关逻辑。

## 目录：`commands/usage`

- 文件数：2
- 目录作用：这一目录聚合了一组与 usage 相关的实现。

- `commands/usage/index.ts`：该目录的导出入口或聚合入口。
- `commands/usage/usage.tsx`：实现 usage 命令相关逻辑。

## 目录：`commands/vim`

- 文件数：2
- 目录作用：这一目录聚合了一组与 vim 相关的实现。

- `commands/vim/index.ts`：该目录的导出入口或聚合入口。
- `commands/vim/vim.ts`：实现 vim 命令相关逻辑。

## 目录：`commands/voice`

- 文件数：2
- 目录作用：这一目录聚合了一组与 voice 相关的实现。

- `commands/voice/index.ts`：该目录的导出入口或聚合入口。
- `commands/voice/voice.ts`：实现 voice 命令相关逻辑。

## 目录：`components`

- 文件数：113
- 目录作用：终端 UI 组件主目录。

- `components/AgentProgressLine.tsx`：处理代理、子代理或代理展示相关逻辑。
- `components/App.tsx`：定义 app 相关界面或交互组件。
- `components/ApproveApiKey.tsx`：定义 approve api key 相关界面或交互组件。
- `components/AutoModeOptInDialog.tsx`：定义一个对话框界面。
- `components/AutoUpdater.tsx`：定义 auto updater 相关界面或交互组件。
- `components/AutoUpdaterWrapper.tsx`：定义 auto updater wrapper 相关界面或交互组件。
- `components/AwsAuthStatusBox.tsx`：定义 aws auth status box 相关界面或交互组件。
- `components/BaseTextInput.tsx`：定义 base text input 相关界面或交互组件。
- `components/BashModeProgress.tsx`：处理 bash 命令构造、解析或执行规则。
- `components/BridgeDialog.tsx`：定义一个对话框界面。
- `components/BypassPermissionsModeDialog.tsx`：定义一个对话框界面。
- `components/ChannelDowngradeDialog.tsx`：定义一个对话框界面。
- `components/ClaudeInChromeOnboarding.tsx`：定义 claude in chrome onboarding 相关界面或交互组件。
- `components/ClaudeMdExternalIncludesDialog.tsx`：定义一个对话框界面。
- `components/ClickableImageRef.tsx`：定义 clickable image ref 相关界面或交互组件。
- `components/CompactSummary.tsx`：定义 compact summary 相关界面或交互组件。
- `components/ConfigurableShortcutHint.tsx`：处理配置项、配置解析或配置结构。
- `components/ConsoleOAuthFlow.tsx`：处理 OAuth 登录或鉴权相关逻辑。
- `components/ContextSuggestions.tsx`：定义 context suggestions 相关界面或交互组件。
- `components/ContextVisualization.tsx`：定义 context visualization 相关界面或交互组件。
- `components/CoordinatorAgentStatus.tsx`：处理代理、子代理或代理展示相关逻辑。
- `components/CostThresholdDialog.tsx`：定义一个对话框界面。
- `components/CtrlOToExpand.tsx`：定义 ctrl oto expand 相关界面或交互组件。
- `components/DesktopHandoff.tsx`：定义 desktop handoff 相关界面或交互组件。
- `components/DevBar.tsx`：定义 dev bar 相关界面或交互组件。
- `components/DevChannelsDialog.tsx`：定义一个对话框界面。
- `components/DiagnosticsDisplay.tsx`：定义 diagnostics display 相关界面或交互组件。
- `components/EffortCallout.tsx`：定义 effort callout 相关界面或交互组件。
- `components/EffortIndicator.ts`：实现 effort indicator 相关逻辑。
- `components/ExitFlow.tsx`：定义 exit flow 相关界面或交互组件。
- `components/ExportDialog.tsx`：定义一个对话框界面。
- `components/FallbackToolUseErrorMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/FallbackToolUseRejectedMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/FastIcon.tsx`：定义 fast icon 相关界面或交互组件。
- `components/Feedback.tsx`：定义 feedback 相关界面或交互组件。
- `components/FileEditToolDiff.tsx`：处理差异展示、差异格式化或差异比较。
- `components/FileEditToolUpdatedMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/FileEditToolUseRejectedMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/FilePathLink.tsx`：定义 file path link 相关界面或交互组件。
- `components/FullscreenLayout.tsx`：定义 fullscreen layout 相关界面或交互组件。
- `components/GlobalSearchDialog.tsx`：定义一个对话框界面。
- `components/HighlightedCode.tsx`：定义 highlighted code 相关界面或交互组件。
- `components/HistorySearchDialog.tsx`：定义一个对话框界面。
- `components/IdeAutoConnectDialog.tsx`：定义一个对话框界面。
- `components/IdeOnboardingDialog.tsx`：定义一个对话框界面。
- `components/IdeStatusIndicator.tsx`：定义 ide status indicator 相关界面或交互组件。
- `components/IdleReturnDialog.tsx`：定义一个对话框界面。
- `components/InterruptedByUser.tsx`：定义 interrupted by user 相关界面或交互组件。
- `components/InvalidConfigDialog.tsx`：定义一个对话框界面。
- `components/InvalidSettingsDialog.tsx`：定义一个对话框界面。
- `components/KeybindingWarnings.tsx`：定义 keybinding warnings 相关界面或交互组件。
- `components/LanguagePicker.tsx`：定义 language picker 相关界面或交互组件。
- `components/LogSelector.tsx`：定义 log selector 相关界面或交互组件。
- `components/Markdown.tsx`：定义 markdown 相关界面或交互组件。
- `components/MarkdownTable.tsx`：定义 markdown table 相关界面或交互组件。
- `components/MCPServerApprovalDialog.tsx`：定义一个对话框界面。
- `components/MCPServerDesktopImportDialog.tsx`：定义一个对话框界面。
- `components/MCPServerDialogCopy.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `components/MCPServerMultiselectDialog.tsx`：定义一个对话框界面。
- `components/MemoryUsageIndicator.tsx`：处理记忆读取、记忆提取或记忆组织。
- `components/Message.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messageActions.tsx`：处理消息结构、消息渲染或消息转换。
- `components/MessageModel.tsx`：处理消息结构、消息渲染或消息转换。
- `components/MessageResponse.tsx`：处理消息结构、消息渲染或消息转换。
- `components/MessageRow.tsx`：处理消息结构、消息渲染或消息转换。
- `components/Messages.tsx`：处理消息结构、消息渲染或消息转换。
- `components/MessageSelector.tsx`：处理消息结构、消息渲染或消息转换。
- `components/MessageTimestamp.tsx`：处理消息结构、消息渲染或消息转换。
- `components/ModelPicker.tsx`：处理模型选择、模型能力或模型字符串映射。
- `components/NativeAutoUpdater.tsx`：定义 native auto updater 相关界面或交互组件。
- `components/NotebookEditToolUseRejectedMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/OffscreenFreeze.tsx`：定义 offscreen freeze 相关界面或交互组件。
- `components/Onboarding.tsx`：定义 onboarding 相关界面或交互组件。
- `components/OutputStylePicker.tsx`：定义 output style picker 相关界面或交互组件。
- `components/PackageManagerAutoUpdater.tsx`：定义 package manager auto updater 相关界面或交互组件。
- `components/PrBadge.tsx`：定义 pr badge 相关界面或交互组件。
- `components/PressEnterToContinue.tsx`：定义 press enter to continue 相关界面或交互组件。
- `components/QuickOpenDialog.tsx`：定义一个对话框界面。
- `components/RemoteCallout.tsx`：定义 remote callout 相关界面或交互组件。
- `components/RemoteEnvironmentDialog.tsx`：定义一个对话框界面。
- `components/ResumeTask.tsx`：处理任务对象、任务状态或任务执行流程。
- `components/SandboxViolationExpandedView.tsx`：处理沙箱模式、沙箱权限或沙箱桥接。
- `components/ScrollKeybindingHandler.tsx`：定义 scroll keybinding handler 相关界面或交互组件。
- `components/SearchBox.tsx`：定义 search box 相关界面或交互组件。
- `components/SentryErrorBoundary.ts`：实现 sentry error boundary 相关逻辑。
- `components/SessionBackgroundHint.tsx`：处理会话对象、会话恢复或会话同步。
- `components/SessionPreview.tsx`：处理会话对象、会话恢复或会话同步。
- `components/ShowInIDEPrompt.tsx`：定义提示词、说明文本或模型提示模板。
- `components/SkillImprovementSurvey.tsx`：处理技能加载、索引、解析或技能运行支持。
- `components/Spinner.tsx`：定义 spinner 相关界面或交互组件。
- `components/Stats.tsx`：定义 stats 相关界面或交互组件。
- `components/StatusLine.tsx`：定义 status line 相关界面或交互组件。
- `components/StatusNotices.tsx`：定义 status notices 相关界面或交互组件。
- `components/StructuredDiff.tsx`：处理差异展示、差异格式化或差异比较。
- `components/StructuredDiffList.tsx`：处理差异展示、差异格式化或差异比较。
- `components/TagTabs.tsx`：定义 tag tabs 相关界面或交互组件。
- `components/TaskListV2.tsx`：处理任务对象、任务状态或任务执行流程。
- `components/TeammateViewHeader.tsx`：定义 teammate view header 相关界面或交互组件。
- `components/TeleportError.tsx`：处理远程传送、远端恢复或远端会话切换。
- `components/TeleportProgress.tsx`：处理远程传送、远端恢复或远端会话切换。
- `components/TeleportRepoMismatchDialog.tsx`：定义一个对话框界面。
- `components/TeleportResumeWrapper.tsx`：处理远程传送、远端恢复或远端会话切换。
- `components/TeleportStash.tsx`：处理远程传送、远端恢复或远端会话切换。
- `components/TextInput.tsx`：定义 text input 相关界面或交互组件。
- `components/ThemePicker.tsx`：处理主题、颜色或样式切换。
- `components/ThinkingToggle.tsx`：定义 thinking toggle 相关界面或交互组件。
- `components/TokenWarning.tsx`：定义 token warning 相关界面或交互组件。
- `components/ToolUseLoader.tsx`：定义 tool use loader 相关界面或交互组件。
- `components/ValidationErrorsList.tsx`：定义 validation errors list 相关界面或交互组件。
- `components/VimTextInput.tsx`：定义 vim text input 相关界面或交互组件。
- `components/VirtualMessageList.tsx`：处理消息结构、消息渲染或消息转换。
- `components/WorkflowMultiselectDialog.tsx`：定义一个对话框界面。
- `components/WorktreeExitDialog.tsx`：定义一个对话框界面。

## 目录：`components/agents`

- 文件数：13
- 目录作用：这一目录聚合了一组与 agents 相关的实现。

- `components/agents/AgentDetail.tsx`：处理代理、子代理或代理展示相关逻辑。
- `components/agents/AgentEditor.tsx`：处理代理、子代理或代理展示相关逻辑。
- `components/agents/agentFileUtils.ts`：存放该模块的通用工具函数。
- `components/agents/AgentNavigationFooter.tsx`：处理代理、子代理或代理展示相关逻辑。
- `components/agents/AgentsList.tsx`：处理代理、子代理或代理展示相关逻辑。
- `components/agents/AgentsMenu.tsx`：处理代理、子代理或代理展示相关逻辑。
- `components/agents/ColorPicker.tsx`：定义 color picker 终端界面组件。
- `components/agents/generateAgent.ts`：处理代理、子代理或代理展示相关逻辑。
- `components/agents/ModelSelector.tsx`：处理模型选择、模型能力或模型字符串映射。
- `components/agents/ToolSelector.tsx`：定义 tool selector 终端界面组件。
- `components/agents/types.ts`：定义这一模块相关的共享类型或结构。
- `components/agents/utils.ts`：存放该模块的通用工具函数。
- `components/agents/validateAgent.ts`：处理代理、子代理或代理展示相关逻辑。

## 目录：`components/agents/new-agent-creation`

- 文件数：1
- 目录作用：这一目录聚合了一组与 new-agent-creation 相关的实现。

- `components/agents/new-agent-creation/CreateAgentWizard.tsx`：处理代理、子代理或代理展示相关逻辑。

## 目录：`components/agents/new-agent-creation/wizard-steps`

- 文件数：12
- 目录作用：这一目录聚合了一组与 wizard-steps 相关的实现。

- `components/agents/new-agent-creation/wizard-steps/ColorStep.tsx`：定义 color step 终端界面组件。
- `components/agents/new-agent-creation/wizard-steps/ConfirmStep.tsx`：定义 confirm step 终端界面组件。
- `components/agents/new-agent-creation/wizard-steps/ConfirmStepWrapper.tsx`：定义 confirm step wrapper 终端界面组件。
- `components/agents/new-agent-creation/wizard-steps/DescriptionStep.tsx`：定义 description step 终端界面组件。
- `components/agents/new-agent-creation/wizard-steps/GenerateStep.tsx`：定义 generate step 终端界面组件。
- `components/agents/new-agent-creation/wizard-steps/LocationStep.tsx`：定义 location step 终端界面组件。
- `components/agents/new-agent-creation/wizard-steps/MemoryStep.tsx`：处理记忆读取、记忆提取或记忆组织。
- `components/agents/new-agent-creation/wizard-steps/MethodStep.tsx`：定义 method step 终端界面组件。
- `components/agents/new-agent-creation/wizard-steps/ModelStep.tsx`：处理模型选择、模型能力或模型字符串映射。
- `components/agents/new-agent-creation/wizard-steps/PromptStep.tsx`：定义 prompt step 终端界面组件。
- `components/agents/new-agent-creation/wizard-steps/ToolsStep.tsx`：定义 tools step 终端界面组件。
- `components/agents/new-agent-creation/wizard-steps/TypeStep.tsx`：定义 type step 终端界面组件。

## 目录：`components/ClaudeCodeHint`

- 文件数：1
- 目录作用：这一目录聚合了一组与 ClaudeCodeHint 相关的实现。

- `components/ClaudeCodeHint/PluginHintMenu.tsx`：处理插件发现、加载、缓存或插件命令。

## 目录：`components/CustomSelect`

- 文件数：10
- 目录作用：这一目录聚合了一组与 CustomSelect 相关的实现。

- `components/CustomSelect/index.ts`：该目录的导出入口或聚合入口。
- `components/CustomSelect/option-map.ts`：定义 option map 终端界面组件。
- `components/CustomSelect/select-input-option.tsx`：定义 select input option 终端界面组件。
- `components/CustomSelect/select-option.tsx`：定义 select option 终端界面组件。
- `components/CustomSelect/select.tsx`：定义 select 终端界面组件。
- `components/CustomSelect/SelectMulti.tsx`：定义 select multi 终端界面组件。
- `components/CustomSelect/use-multi-select-state.ts`：定义 use multi select state 终端界面组件。
- `components/CustomSelect/use-select-input.ts`：定义 use select input 终端界面组件。
- `components/CustomSelect/use-select-navigation.ts`：定义 use select navigation 终端界面组件。
- `components/CustomSelect/use-select-state.ts`：定义 use select state 终端界面组件。

## 目录：`components/design-system`

- 文件数：16
- 目录作用：这一目录聚合了一组与 design-system 相关的实现。

- `components/design-system/Byline.tsx`：定义 byline 终端界面组件。
- `components/design-system/color.ts`：定义 color 终端界面组件。
- `components/design-system/Dialog.tsx`：定义一个对话框界面。
- `components/design-system/Divider.tsx`：定义 divider 终端界面组件。
- `components/design-system/FuzzyPicker.tsx`：定义 fuzzy picker 终端界面组件。
- `components/design-system/KeyboardShortcutHint.tsx`：定义 keyboard shortcut hint 终端界面组件。
- `components/design-system/ListItem.tsx`：定义 list item 终端界面组件。
- `components/design-system/LoadingState.tsx`：定义 loading state 终端界面组件。
- `components/design-system/Pane.tsx`：定义 pane 终端界面组件。
- `components/design-system/ProgressBar.tsx`：定义 progress bar 终端界面组件。
- `components/design-system/Ratchet.tsx`：定义 ratchet 终端界面组件。
- `components/design-system/StatusIcon.tsx`：定义 status icon 终端界面组件。
- `components/design-system/Tabs.tsx`：定义 tabs 终端界面组件。
- `components/design-system/ThemedBox.tsx`：处理主题、颜色或样式切换。
- `components/design-system/ThemedText.tsx`：处理主题、颜色或样式切换。
- `components/design-system/ThemeProvider.tsx`：提供上下文、依赖注入或统一 provider 封装。

## 目录：`components/DesktopUpsell`

- 文件数：1
- 目录作用：这一目录聚合了一组与 DesktopUpsell 相关的实现。

- `components/DesktopUpsell/DesktopUpsellStartup.tsx`：定义 desktop upsell startup 终端界面组件。

## 目录：`components/diff`

- 文件数：3
- 目录作用：这一目录聚合了一组与 diff 相关的实现。

- `components/diff/DiffDetailView.tsx`：处理差异展示、差异格式化或差异比较。
- `components/diff/DiffDialog.tsx`：定义一个对话框界面。
- `components/diff/DiffFileList.tsx`：处理差异展示、差异格式化或差异比较。

## 目录：`components/FeedbackSurvey`

- 文件数：9
- 目录作用：这一目录聚合了一组与 FeedbackSurvey 相关的实现。

- `components/FeedbackSurvey/FeedbackSurvey.tsx`：定义 feedback survey 终端界面组件。
- `components/FeedbackSurvey/FeedbackSurveyView.tsx`：定义 feedback survey view 终端界面组件。
- `components/FeedbackSurvey/submitTranscriptShare.ts`：定义 submit transcript share 终端界面组件。
- `components/FeedbackSurvey/TranscriptSharePrompt.tsx`：定义提示词、说明文本或模型提示模板。
- `components/FeedbackSurvey/useDebouncedDigitInput.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `components/FeedbackSurvey/useFeedbackSurvey.tsx`：定义 use feedback survey 终端界面组件。
- `components/FeedbackSurvey/useMemorySurvey.tsx`：处理记忆读取、记忆提取或记忆组织。
- `components/FeedbackSurvey/usePostCompactSurvey.tsx`：定义 use post compact survey 终端界面组件。
- `components/FeedbackSurvey/useSurveyState.tsx`：定义 use survey state 终端界面组件。

## 目录：`components/grove`

- 文件数：1
- 目录作用：这一目录聚合了一组与 grove 相关的实现。

- `components/grove/Grove.tsx`：定义 grove 终端界面组件。

## 目录：`components/HelpV2`

- 文件数：3
- 目录作用：这一目录聚合了一组与 HelpV2 相关的实现。

- `components/HelpV2/Commands.tsx`：定义 commands 终端界面组件。
- `components/HelpV2/General.tsx`：定义 general 终端界面组件。
- `components/HelpV2/HelpV2.tsx`：定义 help v2 终端界面组件。

## 目录：`components/HighlightedCode`

- 文件数：1
- 目录作用：这一目录聚合了一组与 HighlightedCode 相关的实现。

- `components/HighlightedCode/Fallback.tsx`：定义 fallback 终端界面组件。

## 目录：`components/hooks`

- 文件数：6
- 目录作用：这一目录聚合了一组与 hooks 相关的实现。

- `components/hooks/HooksConfigMenu.tsx`：处理配置项、配置解析或配置结构。
- `components/hooks/PromptDialog.tsx`：定义一个对话框界面。
- `components/hooks/SelectEventMode.tsx`：定义 select event mode 终端界面组件。
- `components/hooks/SelectHookMode.tsx`：定义 select hook mode 终端界面组件。
- `components/hooks/SelectMatcherMode.tsx`：定义 select matcher mode 终端界面组件。
- `components/hooks/ViewHookMode.tsx`：定义 view hook mode 终端界面组件。

## 目录：`components/LogoV2`

- 文件数：15
- 目录作用：这一目录聚合了一组与 LogoV2 相关的实现。

- `components/LogoV2/AnimatedAsterisk.tsx`：定义 animated asterisk 终端界面组件。
- `components/LogoV2/AnimatedClawd.tsx`：定义 animated clawd 终端界面组件。
- `components/LogoV2/ChannelsNotice.tsx`：定义 channels notice 终端界面组件。
- `components/LogoV2/Clawd.tsx`：定义 clawd 终端界面组件。
- `components/LogoV2/CondensedLogo.tsx`：定义 condensed logo 终端界面组件。
- `components/LogoV2/EmergencyTip.tsx`：定义 emergency tip 终端界面组件。
- `components/LogoV2/Feed.tsx`：定义 feed 终端界面组件。
- `components/LogoV2/FeedColumn.tsx`：定义 feed column 终端界面组件。
- `components/LogoV2/feedConfigs.tsx`：处理配置项、配置解析或配置结构。
- `components/LogoV2/GuestPassesUpsell.tsx`：定义 guest passes upsell 终端界面组件。
- `components/LogoV2/LogoV2.tsx`：定义 logo v2 终端界面组件。
- `components/LogoV2/Opus1mMergeNotice.tsx`：定义 opus1m merge notice 终端界面组件。
- `components/LogoV2/OverageCreditUpsell.tsx`：定义 overage credit upsell 终端界面组件。
- `components/LogoV2/VoiceModeNotice.tsx`：定义 voice mode notice 终端界面组件。
- `components/LogoV2/WelcomeV2.tsx`：定义 welcome v2 终端界面组件。

## 目录：`components/LspRecommendation`

- 文件数：1
- 目录作用：这一目录聚合了一组与 LspRecommendation 相关的实现。

- `components/LspRecommendation/LspRecommendationMenu.tsx`：定义 lsp recommendation menu 终端界面组件。

## 目录：`components/ManagedSettingsSecurityDialog`

- 文件数：2
- 目录作用：这一目录聚合了一组与 ManagedSettingsSecurityDialog 相关的实现。

- `components/ManagedSettingsSecurityDialog/ManagedSettingsSecurityDialog.tsx`：定义一个对话框界面。
- `components/ManagedSettingsSecurityDialog/utils.ts`：存放该模块的通用工具函数。

## 目录：`components/mcp`

- 文件数：12
- 目录作用：这一目录聚合了一组与 mcp 相关的实现。

- `components/mcp/CapabilitiesSection.tsx`：定义 capabilities section 终端界面组件。
- `components/mcp/ElicitationDialog.tsx`：定义一个对话框界面。
- `components/mcp/index.ts`：该目录的导出入口或聚合入口。
- `components/mcp/MCPAgentServerMenu.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `components/mcp/MCPListPanel.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `components/mcp/McpParsingWarnings.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `components/mcp/MCPReconnect.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `components/mcp/MCPRemoteServerMenu.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `components/mcp/MCPSettings.tsx`：处理设置读取、缓存、校验或写入。
- `components/mcp/MCPStdioServerMenu.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `components/mcp/MCPToolDetailView.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `components/mcp/MCPToolListView.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。

## 目录：`components/mcp/utils`

- 文件数：1
- 目录作用：这一目录聚合了一组与 utils 相关的实现。

- `components/mcp/utils/reconnectHelpers.tsx`：存放该模块的辅助函数。

## 目录：`components/memory`

- 文件数：2
- 目录作用：这一目录聚合了一组与 memory 相关的实现。

- `components/memory/MemoryFileSelector.tsx`：处理记忆读取、记忆提取或记忆组织。
- `components/memory/MemoryUpdateNotification.tsx`：处理记忆读取、记忆提取或记忆组织。

## 目录：`components/messages`

- 文件数：33
- 目录作用：这一目录聚合了一组与 messages 相关的实现。

- `components/messages/AdvisorMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/AssistantRedactedThinkingMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/AssistantTextMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/AssistantThinkingMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/AssistantToolUseMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/AttachmentMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/CollapsedReadSearchContent.tsx`：定义 collapsed read search content 终端界面组件。
- `components/messages/CompactBoundaryMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/GroupedToolUseContent.tsx`：定义 grouped tool use content 终端界面组件。
- `components/messages/HighlightedThinkingText.tsx`：定义 highlighted thinking text 终端界面组件。
- `components/messages/HookProgressMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/nullRenderingAttachments.ts`：处理渲染过程、渲染参数或渲染辅助逻辑。
- `components/messages/PlanApprovalMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/RateLimitMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/ShutdownMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/SystemAPIErrorMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/SystemTextMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/TaskAssignmentMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/teamMemCollapsed.tsx`：定义 team mem collapsed 终端界面组件。
- `components/messages/teamMemSaved.ts`：定义 team mem saved 终端界面组件。
- `components/messages/UserAgentNotificationMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserBashInputMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserBashOutputMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserChannelMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserCommandMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserImageMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserLocalCommandOutputMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserMemoryInputMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserPlanMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserPromptMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserResourceUpdateMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserTeammateMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserTextMessage.tsx`：处理消息结构、消息渲染或消息转换。

## 目录：`components/messages/UserToolResultMessage`

- 文件数：8
- 目录作用：这一目录聚合了一组与 UserToolResultMessage 相关的实现。

- `components/messages/UserToolResultMessage/RejectedPlanMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserToolResultMessage/RejectedToolUseMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserToolResultMessage/UserToolCanceledMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserToolResultMessage/UserToolErrorMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserToolResultMessage/UserToolRejectMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserToolResultMessage/UserToolResultMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserToolResultMessage/UserToolSuccessMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/messages/UserToolResultMessage/utils.tsx`：存放该模块的通用工具函数。

## 目录：`components/Passes`

- 文件数：1
- 目录作用：这一目录聚合了一组与 Passes 相关的实现。

- `components/Passes/Passes.tsx`：定义 passes 终端界面组件。

## 目录：`components/permissions`

- 文件数：15
- 目录作用：这一目录聚合了一组与 permissions 相关的实现。

- `components/permissions/FallbackPermissionRequest.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/hooks.ts`：定义 hooks 终端界面组件。
- `components/permissions/PermissionDecisionDebugInfo.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/PermissionDialog.tsx`：定义一个对话框界面。
- `components/permissions/PermissionExplanation.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/PermissionPrompt.tsx`：定义提示词、说明文本或模型提示模板。
- `components/permissions/PermissionRequest.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/PermissionRequestTitle.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/PermissionRuleExplanation.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/SandboxPermissionRequest.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/shellPermissionHelpers.tsx`：存放该模块的辅助函数。
- `components/permissions/useShellPermissionFeedback.ts`：处理权限检查、权限请求或权限规则。
- `components/permissions/utils.ts`：存放该模块的通用工具函数。
- `components/permissions/WorkerBadge.tsx`：定义 worker badge 终端界面组件。
- `components/permissions/WorkerPendingPermission.tsx`：处理权限检查、权限请求或权限规则。

## 目录：`components/permissions/AskUserQuestionPermissionRequest`

- 文件数：7
- 目录作用：这一目录聚合了一组与 AskUserQuestionPermissionRequest 相关的实现。

- `components/permissions/AskUserQuestionPermissionRequest/AskUserQuestionPermissionRequest.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/AskUserQuestionPermissionRequest/PreviewBox.tsx`：处理审查、评审或 review 工作流逻辑。
- `components/permissions/AskUserQuestionPermissionRequest/PreviewQuestionView.tsx`：处理审查、评审或 review 工作流逻辑。
- `components/permissions/AskUserQuestionPermissionRequest/QuestionNavigationBar.tsx`：定义 question navigation bar 终端界面组件。
- `components/permissions/AskUserQuestionPermissionRequest/QuestionView.tsx`：定义 question view 终端界面组件。
- `components/permissions/AskUserQuestionPermissionRequest/SubmitQuestionsView.tsx`：定义 submit questions view 终端界面组件。
- `components/permissions/AskUserQuestionPermissionRequest/use-multiple-choice-state.ts`：定义 use multiple choice state 终端界面组件。

## 目录：`components/permissions/BashPermissionRequest`

- 文件数：2
- 目录作用：这一目录聚合了一组与 BashPermissionRequest 相关的实现。

- `components/permissions/BashPermissionRequest/BashPermissionRequest.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/BashPermissionRequest/bashToolUseOptions.tsx`：处理 bash 命令构造、解析或执行规则。

## 目录：`components/permissions/ComputerUseApproval`

- 文件数：1
- 目录作用：这一目录聚合了一组与 ComputerUseApproval 相关的实现。

- `components/permissions/ComputerUseApproval/ComputerUseApproval.tsx`：定义 computer use approval 终端界面组件。

## 目录：`components/permissions/EnterPlanModePermissionRequest`

- 文件数：1
- 目录作用：这一目录聚合了一组与 EnterPlanModePermissionRequest 相关的实现。

- `components/permissions/EnterPlanModePermissionRequest/EnterPlanModePermissionRequest.tsx`：处理权限检查、权限请求或权限规则。

## 目录：`components/permissions/ExitPlanModePermissionRequest`

- 文件数：1
- 目录作用：这一目录聚合了一组与 ExitPlanModePermissionRequest 相关的实现。

- `components/permissions/ExitPlanModePermissionRequest/ExitPlanModePermissionRequest.tsx`：处理权限检查、权限请求或权限规则。

## 目录：`components/permissions/FileEditPermissionRequest`

- 文件数：1
- 目录作用：这一目录聚合了一组与 FileEditPermissionRequest 相关的实现。

- `components/permissions/FileEditPermissionRequest/FileEditPermissionRequest.tsx`：处理权限检查、权限请求或权限规则。

## 目录：`components/permissions/FilePermissionDialog`

- 文件数：5
- 目录作用：这一目录聚合了一组与 FilePermissionDialog 相关的实现。

- `components/permissions/FilePermissionDialog/FilePermissionDialog.tsx`：定义一个对话框界面。
- `components/permissions/FilePermissionDialog/ideDiffConfig.ts`：处理配置项、配置解析或配置结构。
- `components/permissions/FilePermissionDialog/permissionOptions.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/FilePermissionDialog/useFilePermissionDialog.ts`：定义一个对话框界面。
- `components/permissions/FilePermissionDialog/usePermissionHandler.ts`：处理权限检查、权限请求或权限规则。

## 目录：`components/permissions/FilesystemPermissionRequest`

- 文件数：1
- 目录作用：这一目录聚合了一组与 FilesystemPermissionRequest 相关的实现。

- `components/permissions/FilesystemPermissionRequest/FilesystemPermissionRequest.tsx`：处理权限检查、权限请求或权限规则。

## 目录：`components/permissions/FileWritePermissionRequest`

- 文件数：2
- 目录作用：这一目录聚合了一组与 FileWritePermissionRequest 相关的实现。

- `components/permissions/FileWritePermissionRequest/FileWritePermissionRequest.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/FileWritePermissionRequest/FileWriteToolDiff.tsx`：处理差异展示、差异格式化或差异比较。

## 目录：`components/permissions/NotebookEditPermissionRequest`

- 文件数：2
- 目录作用：这一目录聚合了一组与 NotebookEditPermissionRequest 相关的实现。

- `components/permissions/NotebookEditPermissionRequest/NotebookEditPermissionRequest.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/NotebookEditPermissionRequest/NotebookEditToolDiff.tsx`：处理差异展示、差异格式化或差异比较。

## 目录：`components/permissions/PowerShellPermissionRequest`

- 文件数：2
- 目录作用：这一目录聚合了一组与 PowerShellPermissionRequest 相关的实现。

- `components/permissions/PowerShellPermissionRequest/PowerShellPermissionRequest.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/PowerShellPermissionRequest/powershellToolUseOptions.tsx`：处理 PowerShell 命令或权限规则。

## 目录：`components/permissions/rules`

- 文件数：8
- 目录作用：这一目录聚合了一组与 rules 相关的实现。

- `components/permissions/rules/AddPermissionRules.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/rules/AddWorkspaceDirectory.tsx`：定义 add workspace directory 终端界面组件。
- `components/permissions/rules/PermissionRuleDescription.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/rules/PermissionRuleInput.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/rules/PermissionRuleList.tsx`：处理权限检查、权限请求或权限规则。
- `components/permissions/rules/RecentDenialsTab.tsx`：定义 recent denials tab 终端界面组件。
- `components/permissions/rules/RemoveWorkspaceDirectory.tsx`：定义 remove workspace directory 终端界面组件。
- `components/permissions/rules/WorkspaceTab.tsx`：定义 workspace tab 终端界面组件。

## 目录：`components/permissions/SedEditPermissionRequest`

- 文件数：1
- 目录作用：这一目录聚合了一组与 SedEditPermissionRequest 相关的实现。

- `components/permissions/SedEditPermissionRequest/SedEditPermissionRequest.tsx`：处理权限检查、权限请求或权限规则。

## 目录：`components/permissions/SkillPermissionRequest`

- 文件数：1
- 目录作用：这一目录聚合了一组与 SkillPermissionRequest 相关的实现。

- `components/permissions/SkillPermissionRequest/SkillPermissionRequest.tsx`：处理权限检查、权限请求或权限规则。

## 目录：`components/permissions/WebFetchPermissionRequest`

- 文件数：1
- 目录作用：这一目录聚合了一组与 WebFetchPermissionRequest 相关的实现。

- `components/permissions/WebFetchPermissionRequest/WebFetchPermissionRequest.tsx`：处理权限检查、权限请求或权限规则。

## 目录：`components/PromptInput`

- 文件数：21
- 目录作用：这一目录聚合了一组与 PromptInput 相关的实现。

- `components/PromptInput/HistorySearchInput.tsx`：处理历史记录、会话历史或历史状态。
- `components/PromptInput/inputModes.ts`：定义 input modes 终端界面组件。
- `components/PromptInput/inputPaste.ts`：定义 input paste 终端界面组件。
- `components/PromptInput/IssueFlagBanner.tsx`：定义 issue flag banner 终端界面组件。
- `components/PromptInput/Notifications.tsx`：定义 notifications 终端界面组件。
- `components/PromptInput/PromptInput.tsx`：定义 prompt input 终端界面组件。
- `components/PromptInput/PromptInputFooter.tsx`：定义 prompt input footer 终端界面组件。
- `components/PromptInput/PromptInputFooterLeftSide.tsx`：定义 prompt input footer left side 终端界面组件。
- `components/PromptInput/PromptInputFooterSuggestions.tsx`：定义 prompt input footer suggestions 终端界面组件。
- `components/PromptInput/PromptInputHelpMenu.tsx`：定义 prompt input help menu 终端界面组件。
- `components/PromptInput/PromptInputModeIndicator.tsx`：定义 prompt input mode indicator 终端界面组件。
- `components/PromptInput/PromptInputQueuedCommands.tsx`：定义 prompt input queued commands 终端界面组件。
- `components/PromptInput/PromptInputStashNotice.tsx`：定义 prompt input stash notice 终端界面组件。
- `components/PromptInput/SandboxPromptFooterHint.tsx`：处理沙箱模式、沙箱权限或沙箱桥接。
- `components/PromptInput/ShimmeredInput.tsx`：定义 shimmered input 终端界面组件。
- `components/PromptInput/useMaybeTruncateInput.ts`：定义 use maybe truncate input 终端界面组件。
- `components/PromptInput/usePromptInputPlaceholder.ts`：定义 use prompt input placeholder 终端界面组件。
- `components/PromptInput/useShowFastIconHint.ts`：定义 use show fast icon hint 终端界面组件。
- `components/PromptInput/useSwarmBanner.ts`：定义 use swarm banner 终端界面组件。
- `components/PromptInput/utils.ts`：存放该模块的通用工具函数。
- `components/PromptInput/VoiceIndicator.tsx`：定义 voice indicator 终端界面组件。

## 目录：`components/sandbox`

- 文件数：5
- 目录作用：这一目录聚合了一组与 sandbox 相关的实现。

- `components/sandbox/SandboxConfigTab.tsx`：处理配置项、配置解析或配置结构。
- `components/sandbox/SandboxDependenciesTab.tsx`：处理沙箱模式、沙箱权限或沙箱桥接。
- `components/sandbox/SandboxDoctorSection.tsx`：处理沙箱模式、沙箱权限或沙箱桥接。
- `components/sandbox/SandboxOverridesTab.tsx`：处理沙箱模式、沙箱权限或沙箱桥接。
- `components/sandbox/SandboxSettings.tsx`：处理设置读取、缓存、校验或写入。

## 目录：`components/Settings`

- 文件数：4
- 目录作用：这一目录聚合了一组与 Settings 相关的实现。

- `components/Settings/Config.tsx`：处理配置项、配置解析或配置结构。
- `components/Settings/Settings.tsx`：处理设置读取、缓存、校验或写入。
- `components/Settings/Status.tsx`：定义 status 终端界面组件。
- `components/Settings/Usage.tsx`：定义 usage 终端界面组件。

## 目录：`components/shell`

- 文件数：4
- 目录作用：这一目录聚合了一组与 shell 相关的实现。

- `components/shell/ExpandShellOutputContext.tsx`：定义上下文对象或上下文获取逻辑。
- `components/shell/OutputLine.tsx`：定义 output line 终端界面组件。
- `components/shell/ShellProgressMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/shell/ShellTimeDisplay.tsx`：定义 shell time display 终端界面组件。

## 目录：`components/skills`

- 文件数：1
- 目录作用：这一目录聚合了一组与 skills 相关的实现。

- `components/skills/SkillsMenu.tsx`：处理技能加载、索引、解析或技能运行支持。

## 目录：`components/Spinner`

- 文件数：12
- 目录作用：这一目录聚合了一组与 Spinner 相关的实现。

- `components/Spinner/FlashingChar.tsx`：定义 flashing char 终端界面组件。
- `components/Spinner/GlimmerMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `components/Spinner/index.ts`：该目录的导出入口或聚合入口。
- `components/Spinner/ShimmerChar.tsx`：定义 shimmer char 终端界面组件。
- `components/Spinner/SpinnerAnimationRow.tsx`：定义 spinner animation row 终端界面组件。
- `components/Spinner/SpinnerGlyph.tsx`：定义 spinner glyph 终端界面组件。
- `components/Spinner/teammateSelectHint.ts`：定义 teammate select hint 终端界面组件。
- `components/Spinner/TeammateSpinnerLine.tsx`：定义 teammate spinner line 终端界面组件。
- `components/Spinner/TeammateSpinnerTree.tsx`：定义 teammate spinner tree 终端界面组件。
- `components/Spinner/useShimmerAnimation.ts`：定义 use shimmer animation 终端界面组件。
- `components/Spinner/useStalledAnimation.ts`：定义 use stalled animation 终端界面组件。
- `components/Spinner/utils.ts`：存放该模块的通用工具函数。

## 目录：`components/StructuredDiff`

- 文件数：2
- 目录作用：这一目录聚合了一组与 StructuredDiff 相关的实现。

- `components/StructuredDiff/colorDiff.ts`：处理差异展示、差异格式化或差异比较。
- `components/StructuredDiff/Fallback.tsx`：定义 fallback 终端界面组件。

## 目录：`components/tasks`

- 文件数：12
- 目录作用：这一目录聚合了一组与 tasks 相关的实现。

- `components/tasks/AsyncAgentDetailDialog.tsx`：定义一个对话框界面。
- `components/tasks/BackgroundTask.tsx`：处理任务对象、任务状态或任务执行流程。
- `components/tasks/BackgroundTasksDialog.tsx`：定义一个对话框界面。
- `components/tasks/BackgroundTaskStatus.tsx`：处理任务对象、任务状态或任务执行流程。
- `components/tasks/DreamDetailDialog.tsx`：定义一个对话框界面。
- `components/tasks/InProcessTeammateDetailDialog.tsx`：定义一个对话框界面。
- `components/tasks/RemoteSessionDetailDialog.tsx`：定义一个对话框界面。
- `components/tasks/RemoteSessionProgress.tsx`：处理会话对象、会话恢复或会话同步。
- `components/tasks/renderToolActivity.tsx`：处理渲染过程、渲染参数或渲染辅助逻辑。
- `components/tasks/ShellDetailDialog.tsx`：定义一个对话框界面。
- `components/tasks/ShellProgress.tsx`：定义 shell progress 终端界面组件。
- `components/tasks/taskStatusUtils.tsx`：存放该模块的通用工具函数。

## 目录：`components/teams`

- 文件数：2
- 目录作用：这一目录聚合了一组与 teams 相关的实现。

- `components/teams/TeamsDialog.tsx`：定义一个对话框界面。
- `components/teams/TeamStatus.tsx`：定义 team status 终端界面组件。

## 目录：`components/TrustDialog`

- 文件数：2
- 目录作用：这一目录聚合了一组与 TrustDialog 相关的实现。

- `components/TrustDialog/TrustDialog.tsx`：定义一个对话框界面。
- `components/TrustDialog/utils.ts`：存放该模块的通用工具函数。

## 目录：`components/ui`

- 文件数：3
- 目录作用：这一目录聚合了一组与 ui 相关的实现。

- `components/ui/OrderedList.tsx`：定义 ordered list 终端界面组件。
- `components/ui/OrderedListItem.tsx`：定义 ordered list item 终端界面组件。
- `components/ui/TreeSelect.tsx`：定义 tree select 终端界面组件。

## 目录：`components/wizard`

- 文件数：5
- 目录作用：这一目录聚合了一组与 wizard 相关的实现。

- `components/wizard/index.ts`：该目录的导出入口或聚合入口。
- `components/wizard/useWizard.ts`：定义 use wizard 终端界面组件。
- `components/wizard/WizardDialogLayout.tsx`：定义 wizard dialog layout 终端界面组件。
- `components/wizard/WizardNavigationFooter.tsx`：定义 wizard navigation footer 终端界面组件。
- `components/wizard/WizardProvider.tsx`：提供上下文、依赖注入或统一 provider 封装。

## 目录：`constants`

- 文件数：21
- 目录作用：全局常量定义。

- `constants/apiLimits.ts`：实现 api limits 相关逻辑。
- `constants/betas.ts`：实现 betas 相关逻辑。
- `constants/common.ts`：实现 common 相关逻辑。
- `constants/cyberRiskInstruction.ts`：实现 cyber risk instruction 相关逻辑。
- `constants/errorIds.ts`：实现 error ids 相关逻辑。
- `constants/figures.ts`：实现 figures 相关逻辑。
- `constants/files.ts`：实现 files 相关逻辑。
- `constants/github-app.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `constants/keys.ts`：实现 keys 相关逻辑。
- `constants/messages.ts`：处理消息结构、消息渲染或消息转换。
- `constants/oauth.ts`：处理 OAuth 登录或鉴权相关逻辑。
- `constants/outputStyles.ts`：实现 output styles 相关逻辑。
- `constants/product.ts`：实现 product 相关逻辑。
- `constants/prompts.ts`：实现 prompts 相关逻辑。
- `constants/spinnerVerbs.ts`：实现 spinner verbs 相关逻辑。
- `constants/system.ts`：实现 system 相关逻辑。
- `constants/systemPromptSections.ts`：实现 system prompt sections 相关逻辑。
- `constants/toolLimits.ts`：实现 tool limits 相关逻辑。
- `constants/tools.ts`：实现 tools 相关逻辑。
- `constants/turnCompletionVerbs.ts`：实现 turn completion verbs 相关逻辑。
- `constants/xml.ts`：实现 xml 相关逻辑。

## 目录：`context`

- 文件数：9
- 目录作用：React/Ink 上下文与共享状态入口。

- `context/fpsMetrics.tsx`：定义 fps metrics 相关界面或交互组件。
- `context/mailbox.tsx`：定义 mailbox 相关界面或交互组件。
- `context/modalContext.tsx`：定义上下文对象或上下文获取逻辑。
- `context/notifications.tsx`：定义 notifications 相关界面或交互组件。
- `context/overlayContext.tsx`：定义上下文对象或上下文获取逻辑。
- `context/promptOverlayContext.tsx`：定义上下文对象或上下文获取逻辑。
- `context/QueuedMessageContext.tsx`：定义上下文对象或上下文获取逻辑。
- `context/stats.tsx`：定义 stats 相关界面或交互组件。
- `context/voice.tsx`：定义 voice 相关界面或交互组件。

## 目录：`coordinator`

- 文件数：1
- 目录作用：协调模式或多代理协调相关能力。

- `coordinator/coordinatorMode.ts`：实现 coordinator mode 相关逻辑。

## 目录：`entrypoints`

- 文件数：5
- 目录作用：不同运行入口与初始化适配。

- `entrypoints/agentSdkTypes.ts`：定义这一模块相关的共享类型或结构。
- `entrypoints/cli.tsx`：定义 cli 相关界面或交互组件。
- `entrypoints/init.ts`：实现 init 相关逻辑。
- `entrypoints/mcp.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `entrypoints/sandboxTypes.ts`：定义这一模块相关的共享类型或结构。

## 目录：`entrypoints/sdk`

- 文件数：3
- 目录作用：SDK 暴露类型与 SDK 入口适配。

- `entrypoints/sdk/controlSchemas.ts`：定义校验结构或数据 schema。
- `entrypoints/sdk/coreSchemas.ts`：定义校验结构或数据 schema。
- `entrypoints/sdk/coreTypes.ts`：定义这一模块相关的共享类型或结构。

## 目录：`hooks`

- 文件数：83
- 目录作用：通用 React/Ink hooks。

- `hooks/fileSuggestions.ts`：实现 file suggestions 相关逻辑。
- `hooks/renderPlaceholder.ts`：处理渲染过程、渲染参数或渲染辅助逻辑。
- `hooks/unifiedSuggestions.ts`：实现 unified suggestions 相关逻辑。
- `hooks/useAfterFirstRender.ts`：处理渲染过程、渲染参数或渲染辅助逻辑。
- `hooks/useApiKeyVerification.ts`：实现 use api key verification 相关逻辑。
- `hooks/useArrowKeyHistory.tsx`：处理历史记录、会话历史或历史状态。
- `hooks/useAssistantHistory.ts`：处理历史记录、会话历史或历史状态。
- `hooks/useAwaySummary.ts`：实现 use away summary 相关逻辑。
- `hooks/useBackgroundTaskNavigation.ts`：处理任务对象、任务状态或任务执行流程。
- `hooks/useBlink.ts`：实现 use blink 相关逻辑。
- `hooks/useCancelRequest.ts`：实现 use cancel request 相关逻辑。
- `hooks/useCanUseTool.tsx`：定义一个具体工具的能力、输入输出和执行逻辑。
- `hooks/useChromeExtensionNotification.tsx`：定义 use chrome extension notification 相关界面或交互组件。
- `hooks/useClaudeCodeHintRecommendation.tsx`：定义 use claude code hint recommendation 相关界面或交互组件。
- `hooks/useClipboardImageHint.ts`：实现 use clipboard image hint 相关逻辑。
- `hooks/useCommandKeybindings.tsx`：定义 use command keybindings 相关界面或交互组件。
- `hooks/useCommandQueue.ts`：实现 use command queue 相关逻辑。
- `hooks/useCopyOnSelect.ts`：实现 use copy on select 相关逻辑。
- `hooks/useDeferredHookMessages.ts`：处理消息结构、消息渲染或消息转换。
- `hooks/useDiffData.ts`：处理差异展示、差异格式化或差异比较。
- `hooks/useDiffInIDE.ts`：处理差异展示、差异格式化或差异比较。
- `hooks/useDirectConnect.ts`：实现 use direct connect 相关逻辑。
- `hooks/useDoublePress.ts`：实现 use double press 相关逻辑。
- `hooks/useDynamicConfig.ts`：处理配置项、配置解析或配置结构。
- `hooks/useElapsedTime.ts`：实现 use elapsed time 相关逻辑。
- `hooks/useExitOnCtrlCD.ts`：实现 use exit on ctrl cd 相关逻辑。
- `hooks/useExitOnCtrlCDWithKeybindings.ts`：实现 use exit on ctrl cdwith keybindings 相关逻辑。
- `hooks/useFileHistorySnapshotInit.ts`：处理历史记录、会话历史或历史状态。
- `hooks/useGlobalKeybindings.tsx`：定义 use global keybindings 相关界面或交互组件。
- `hooks/useHistorySearch.ts`：处理历史记录、会话历史或历史状态。
- `hooks/useIdeAtMentioned.ts`：实现 use ide at mentioned 相关逻辑。
- `hooks/useIdeConnectionStatus.ts`：实现 use ide connection status 相关逻辑。
- `hooks/useIDEIntegration.tsx`：定义 use ideintegration 相关界面或交互组件。
- `hooks/useIdeLogging.ts`：实现 use ide logging 相关逻辑。
- `hooks/useIdeSelection.ts`：实现 use ide selection 相关逻辑。
- `hooks/useInboxPoller.ts`：实现 use inbox poller 相关逻辑。
- `hooks/useInputBuffer.ts`：实现 use input buffer 相关逻辑。
- `hooks/useIssueFlagBanner.ts`：实现 use issue flag banner 相关逻辑。
- `hooks/useLogMessages.ts`：处理消息结构、消息渲染或消息转换。
- `hooks/useLspPluginRecommendation.tsx`：处理插件发现、加载、缓存或插件命令。
- `hooks/useMailboxBridge.ts`：实现 use mailbox bridge 相关逻辑。
- `hooks/useMainLoopModel.ts`：处理模型选择、模型能力或模型字符串映射。
- `hooks/useManagePlugins.ts`：处理插件发现、加载、缓存或插件命令。
- `hooks/useMemoryUsage.ts`：处理记忆读取、记忆提取或记忆组织。
- `hooks/useMergedClients.ts`：实现 use merged clients 相关逻辑。
- `hooks/useMergedCommands.ts`：实现 use merged commands 相关逻辑。
- `hooks/useMergedTools.ts`：实现 use merged tools 相关逻辑。
- `hooks/useMinDisplayTime.ts`：实现 use min display time 相关逻辑。
- `hooks/useNotifyAfterTimeout.ts`：实现 use notify after timeout 相关逻辑。
- `hooks/useOfficialMarketplaceNotification.tsx`：定义 use official marketplace notification 相关界面或交互组件。
- `hooks/usePasteHandler.ts`：实现 use paste handler 相关逻辑。
- `hooks/usePluginRecommendationBase.tsx`：处理插件发现、加载、缓存或插件命令。
- `hooks/usePromptsFromClaudeInChrome.tsx`：定义 use prompts from claude in chrome 相关界面或交互组件。
- `hooks/usePromptSuggestion.ts`：实现 use prompt suggestion 相关逻辑。
- `hooks/usePrStatus.ts`：实现 use pr status 相关逻辑。
- `hooks/useQueueProcessor.ts`：实现 use queue processor 相关逻辑。
- `hooks/useRemoteSession.ts`：处理会话对象、会话恢复或会话同步。
- `hooks/useReplBridge.tsx`：定义 use repl bridge 相关界面或交互组件。
- `hooks/useScheduledTasks.ts`：处理任务对象、任务状态或任务执行流程。
- `hooks/useSearchInput.ts`：实现 use search input 相关逻辑。
- `hooks/useSessionBackgrounding.ts`：处理会话对象、会话恢复或会话同步。
- `hooks/useSettings.ts`：处理设置读取、缓存、校验或写入。
- `hooks/useSettingsChange.ts`：处理设置读取、缓存、校验或写入。
- `hooks/useSkillImprovementSurvey.ts`：处理技能加载、索引、解析或技能运行支持。
- `hooks/useSkillsChange.ts`：处理技能加载、索引、解析或技能运行支持。
- `hooks/useSSHSession.ts`：处理会话对象、会话恢复或会话同步。
- `hooks/useSwarmInitialization.ts`：实现 use swarm initialization 相关逻辑。
- `hooks/useSwarmPermissionPoller.ts`：处理权限检查、权限请求或权限规则。
- `hooks/useTaskListWatcher.ts`：处理任务对象、任务状态或任务执行流程。
- `hooks/useTasksV2.ts`：处理任务对象、任务状态或任务执行流程。
- `hooks/useTeammateViewAutoExit.ts`：实现 use teammate view auto exit 相关逻辑。
- `hooks/useTeleportResume.tsx`：处理远程传送、远端恢复或远端会话切换。
- `hooks/useTerminalSize.ts`：实现 use terminal size 相关逻辑。
- `hooks/useTextInput.ts`：实现 use text input 相关逻辑。
- `hooks/useTimeout.ts`：实现 use timeout 相关逻辑。
- `hooks/useTurnDiffs.ts`：处理差异展示、差异格式化或差异比较。
- `hooks/useTypeahead.tsx`：定义 use typeahead 相关界面或交互组件。
- `hooks/useUpdateNotification.ts`：实现 use update notification 相关逻辑。
- `hooks/useVimInput.ts`：实现 use vim input 相关逻辑。
- `hooks/useVirtualScroll.ts`：实现 use virtual scroll 相关逻辑。
- `hooks/useVoice.ts`：实现 use voice 相关逻辑。
- `hooks/useVoiceEnabled.ts`：实现 use voice enabled 相关逻辑。
- `hooks/useVoiceIntegration.tsx`：定义 use voice integration 相关界面或交互组件。

## 目录：`hooks/notifs`

- 文件数：16
- 目录作用：这一目录聚合了一组与 notifs 相关的实现。

- `hooks/notifs/useAutoModeUnavailableNotification.ts`：实现 use auto mode unavailable notification 相关 hook。
- `hooks/notifs/useCanSwitchToExistingSubscription.tsx`：实现 use can switch to existing subscription 相关 hook。
- `hooks/notifs/useDeprecationWarningNotification.tsx`：实现 use deprecation warning notification 相关 hook。
- `hooks/notifs/useFastModeNotification.tsx`：实现 use fast mode notification 相关 hook。
- `hooks/notifs/useIDEStatusIndicator.tsx`：实现 use idestatus indicator 相关 hook。
- `hooks/notifs/useInstallMessages.tsx`：处理消息结构、消息渲染或消息转换。
- `hooks/notifs/useLspInitializationNotification.tsx`：实现 use lsp initialization notification 相关 hook。
- `hooks/notifs/useMcpConnectivityStatus.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `hooks/notifs/useModelMigrationNotifications.tsx`：处理模型选择、模型能力或模型字符串映射。
- `hooks/notifs/useNpmDeprecationNotification.tsx`：实现 use npm deprecation notification 相关 hook。
- `hooks/notifs/usePluginAutoupdateNotification.tsx`：处理插件发现、加载、缓存或插件命令。
- `hooks/notifs/usePluginInstallationStatus.tsx`：处理插件发现、加载、缓存或插件命令。
- `hooks/notifs/useRateLimitWarningNotification.tsx`：实现 use rate limit warning notification 相关 hook。
- `hooks/notifs/useSettingsErrors.tsx`：处理设置读取、缓存、校验或写入。
- `hooks/notifs/useStartupNotification.ts`：实现 use startup notification 相关 hook。
- `hooks/notifs/useTeammateShutdownNotification.ts`：实现 use teammate shutdown notification 相关 hook。

## 目录：`hooks/toolPermission`

- 文件数：2
- 目录作用：这一目录聚合了一组与 toolPermission 相关的实现。

- `hooks/toolPermission/PermissionContext.ts`：定义上下文对象或上下文获取逻辑。
- `hooks/toolPermission/permissionLogging.ts`：处理权限检查、权限请求或权限规则。

## 目录：`hooks/toolPermission/handlers`

- 文件数：3
- 目录作用：这一目录聚合了一组与 handlers 相关的实现。

- `hooks/toolPermission/handlers/coordinatorHandler.ts`：实现 coordinator handler 相关 hook。
- `hooks/toolPermission/handlers/interactiveHandler.ts`：实现 interactive handler 相关 hook。
- `hooks/toolPermission/handlers/swarmWorkerHandler.ts`：实现 swarm worker handler 相关 hook。

## 目录：`ink`

- 文件数：43
- 目录作用：终端渲染、布局、事件和低层终端支持。

- `ink/Ansi.tsx`：定义 ansi 相关界面或交互组件。
- `ink/bidi.ts`：实现 bidi 相关逻辑。
- `ink/clearTerminal.ts`：实现 clear terminal 相关逻辑。
- `ink/colorize.ts`：实现 colorize 相关逻辑。
- `ink/constants.ts`：定义这一模块用到的常量。
- `ink/dom.ts`：实现 dom 相关逻辑。
- `ink/focus.ts`：实现 focus 相关逻辑。
- `ink/frame.ts`：实现 frame 相关逻辑。
- `ink/get-max-width.ts`：实现 get max width 相关逻辑。
- `ink/hit-test.ts`：实现 hit test 相关逻辑。
- `ink/ink.tsx`：定义 ink 相关界面或交互组件。
- `ink/instances.ts`：实现 instances 相关逻辑。
- `ink/line-width-cache.ts`：实现 line width cache 相关逻辑。
- `ink/log-update.ts`：实现 log update 相关逻辑。
- `ink/measure-element.ts`：实现 measure element 相关逻辑。
- `ink/measure-text.ts`：实现 measure text 相关逻辑。
- `ink/node-cache.ts`：实现 node cache 相关逻辑。
- `ink/optimizer.ts`：实现 optimizer 相关逻辑。
- `ink/output.ts`：实现 output 相关逻辑。
- `ink/parse-keypress.ts`：实现 parse keypress 相关逻辑。
- `ink/reconciler.ts`：实现 reconciler 相关逻辑。
- `ink/render-border.ts`：处理渲染过程、渲染参数或渲染辅助逻辑。
- `ink/render-node-to-output.ts`：处理渲染过程、渲染参数或渲染辅助逻辑。
- `ink/render-to-screen.ts`：定义一个终端页面或主屏组件。
- `ink/renderer.ts`：处理渲染过程、渲染参数或渲染辅助逻辑。
- `ink/root.ts`：实现 root 相关逻辑。
- `ink/screen.ts`：定义一个终端页面或主屏组件。
- `ink/searchHighlight.ts`：实现 search highlight 相关逻辑。
- `ink/selection.ts`：实现 selection 相关逻辑。
- `ink/squash-text-nodes.ts`：实现 squash text nodes 相关逻辑。
- `ink/stringWidth.ts`：实现 string width 相关逻辑。
- `ink/styles.ts`：实现 styles 相关逻辑。
- `ink/supports-hyperlinks.ts`：实现 supports hyperlinks 相关逻辑。
- `ink/tabstops.ts`：实现 tabstops 相关逻辑。
- `ink/terminal-focus-state.ts`：实现 terminal focus state 相关逻辑。
- `ink/terminal-querier.ts`：实现 terminal querier 相关逻辑。
- `ink/terminal.ts`：实现 terminal 相关逻辑。
- `ink/termio.ts`：实现 termio 相关逻辑。
- `ink/useTerminalNotification.ts`：实现 use terminal notification 相关逻辑。
- `ink/warn.ts`：实现 warn 相关逻辑。
- `ink/widest-line.ts`：实现 widest line 相关逻辑。
- `ink/wrap-text.ts`：实现 wrap text 相关逻辑。
- `ink/wrapAnsi.ts`：实现 wrap ansi 相关逻辑。

## 目录：`ink/components`

- 文件数：18
- 目录作用：这一目录聚合了一组与 components 相关的实现。

- `ink/components/AlternateScreen.tsx`：定义一个终端页面或主屏组件。
- `ink/components/App.tsx`：实现 app 终端渲染支持。
- `ink/components/AppContext.ts`：定义上下文对象或上下文获取逻辑。
- `ink/components/Box.tsx`：实现 box 终端渲染支持。
- `ink/components/Button.tsx`：实现 button 终端渲染支持。
- `ink/components/ClockContext.tsx`：定义上下文对象或上下文获取逻辑。
- `ink/components/CursorDeclarationContext.ts`：定义上下文对象或上下文获取逻辑。
- `ink/components/ErrorOverview.tsx`：实现 error overview 终端渲染支持。
- `ink/components/Link.tsx`：实现 link 终端渲染支持。
- `ink/components/Newline.tsx`：实现 newline 终端渲染支持。
- `ink/components/NoSelect.tsx`：实现 no select 终端渲染支持。
- `ink/components/RawAnsi.tsx`：实现 raw ansi 终端渲染支持。
- `ink/components/ScrollBox.tsx`：实现 scroll box 终端渲染支持。
- `ink/components/Spacer.tsx`：实现 spacer 终端渲染支持。
- `ink/components/StdinContext.ts`：定义上下文对象或上下文获取逻辑。
- `ink/components/TerminalFocusContext.tsx`：定义上下文对象或上下文获取逻辑。
- `ink/components/TerminalSizeContext.tsx`：定义上下文对象或上下文获取逻辑。
- `ink/components/Text.tsx`：实现 text 终端渲染支持。

## 目录：`ink/events`

- 文件数：10
- 目录作用：这一目录聚合了一组与 events 相关的实现。

- `ink/events/click-event.ts`：实现 click event 终端渲染支持。
- `ink/events/dispatcher.ts`：实现 dispatcher 终端渲染支持。
- `ink/events/emitter.ts`：实现 emitter 终端渲染支持。
- `ink/events/event-handlers.ts`：实现 event handlers 终端渲染支持。
- `ink/events/event.ts`：实现 event 终端渲染支持。
- `ink/events/focus-event.ts`：实现 focus event 终端渲染支持。
- `ink/events/input-event.ts`：实现 input event 终端渲染支持。
- `ink/events/keyboard-event.ts`：实现 keyboard event 终端渲染支持。
- `ink/events/terminal-event.ts`：实现 terminal event 终端渲染支持。
- `ink/events/terminal-focus-event.ts`：实现 terminal focus event 终端渲染支持。

## 目录：`ink/hooks`

- 文件数：12
- 目录作用：这一目录聚合了一组与 hooks 相关的实现。

- `ink/hooks/use-animation-frame.ts`：实现 use animation frame 终端渲染支持。
- `ink/hooks/use-app.ts`：实现 use app 终端渲染支持。
- `ink/hooks/use-declared-cursor.ts`：实现 use declared cursor 终端渲染支持。
- `ink/hooks/use-input.ts`：实现 use input 终端渲染支持。
- `ink/hooks/use-interval.ts`：实现 use interval 终端渲染支持。
- `ink/hooks/use-search-highlight.ts`：实现 use search highlight 终端渲染支持。
- `ink/hooks/use-selection.ts`：实现 use selection 终端渲染支持。
- `ink/hooks/use-stdin.ts`：实现 use stdin 终端渲染支持。
- `ink/hooks/use-tab-status.ts`：实现 use tab status 终端渲染支持。
- `ink/hooks/use-terminal-focus.ts`：实现 use terminal focus 终端渲染支持。
- `ink/hooks/use-terminal-title.ts`：实现 use terminal title 终端渲染支持。
- `ink/hooks/use-terminal-viewport.ts`：实现 use terminal viewport 终端渲染支持。

## 目录：`ink/layout`

- 文件数：4
- 目录作用：这一目录聚合了一组与 layout 相关的实现。

- `ink/layout/engine.ts`：实现 engine 终端渲染支持。
- `ink/layout/geometry.ts`：实现 geometry 终端渲染支持。
- `ink/layout/node.ts`：实现 node 终端渲染支持。
- `ink/layout/yoga.ts`：实现 yoga 终端渲染支持。

## 目录：`ink/termio`

- 文件数：9
- 目录作用：这一目录聚合了一组与 termio 相关的实现。

- `ink/termio/ansi.ts`：实现 ansi 终端渲染支持。
- `ink/termio/csi.ts`：实现 csi 终端渲染支持。
- `ink/termio/dec.ts`：实现 dec 终端渲染支持。
- `ink/termio/esc.ts`：实现 esc 终端渲染支持。
- `ink/termio/osc.ts`：实现 osc 终端渲染支持。
- `ink/termio/parser.ts`：实现 parser 终端渲染支持。
- `ink/termio/sgr.ts`：实现 sgr 终端渲染支持。
- `ink/termio/tokenize.ts`：实现 tokenize 终端渲染支持。
- `ink/termio/types.ts`：定义这一模块相关的共享类型或结构。

## 目录：`keybindings`

- 文件数：14
- 目录作用：键位绑定与输入行为控制。

- `keybindings/defaultBindings.ts`：实现 default bindings 相关逻辑。
- `keybindings/KeybindingContext.tsx`：定义上下文对象或上下文获取逻辑。
- `keybindings/KeybindingProviderSetup.tsx`：定义 keybinding provider setup 相关界面或交互组件。
- `keybindings/loadUserBindings.ts`：实现 load user bindings 相关逻辑。
- `keybindings/match.ts`：实现 match 相关逻辑。
- `keybindings/parser.ts`：实现 parser 相关逻辑。
- `keybindings/reservedShortcuts.ts`：实现 reserved shortcuts 相关逻辑。
- `keybindings/resolver.ts`：实现 resolver 相关逻辑。
- `keybindings/schema.ts`：定义校验结构或数据 schema。
- `keybindings/shortcutFormat.ts`：实现 shortcut format 相关逻辑。
- `keybindings/template.ts`：实现 template 相关逻辑。
- `keybindings/useKeybinding.ts`：实现 use keybinding 相关逻辑。
- `keybindings/useShortcutDisplay.ts`：实现 use shortcut display 相关逻辑。
- `keybindings/validate.ts`：实现 validate 相关逻辑。

## 目录：`memdir`

- 文件数：8
- 目录作用：记忆目录扫描、过滤、排序与读取。

- `memdir/findRelevantMemories.ts`：实现 find relevant memories 相关逻辑。
- `memdir/memdir.ts`：实现 memdir 相关逻辑。
- `memdir/memoryAge.ts`：处理记忆读取、记忆提取或记忆组织。
- `memdir/memoryScan.ts`：处理记忆读取、记忆提取或记忆组织。
- `memdir/memoryTypes.ts`：定义这一模块相关的共享类型或结构。
- `memdir/paths.ts`：实现 paths 相关逻辑。
- `memdir/teamMemPaths.ts`：实现 team mem paths 相关逻辑。
- `memdir/teamMemPrompts.ts`：实现 team mem prompts 相关逻辑。

## 目录：`migrations`

- 文件数：11
- 目录作用：配置、模型、设置迁移逻辑。

- `migrations/migrateAutoUpdatesToSettings.ts`：处理设置读取、缓存、校验或写入。
- `migrations/migrateBypassPermissionsAcceptedToSettings.ts`：处理权限检查、权限请求或权限规则。
- `migrations/migrateEnableAllProjectMcpServersToSettings.ts`：处理设置读取、缓存、校验或写入。
- `migrations/migrateFennecToOpus.ts`：实现 migrate fennec to opus 相关逻辑。
- `migrations/migrateLegacyOpusToCurrent.ts`：实现 migrate legacy opus to current 相关逻辑。
- `migrations/migrateOpusToOpus1m.ts`：实现 migrate opus to opus1m 相关逻辑。
- `migrations/migrateReplBridgeEnabledToRemoteControlAtStartup.ts`：实现 migrate repl bridge enabled to remote control at startup 相关逻辑。
- `migrations/migrateSonnet1mToSonnet45.ts`：实现 migrate sonnet1m to sonnet45 相关逻辑。
- `migrations/migrateSonnet45ToSonnet46.ts`：实现 migrate sonnet45 to sonnet46 相关逻辑。
- `migrations/resetAutoModeOptInForDefaultOffer.ts`：实现 reset auto mode opt in for default offer 相关逻辑。
- `migrations/resetProToOpusDefault.ts`：实现 reset pro to opus default 相关逻辑。

## 目录：`moreright`

- 文件数：1
- 目录作用：特定交互增强逻辑。

- `moreright/useMoreRight.tsx`：定义 use more right 相关界面或交互组件。

## 目录：`native-ts/color-diff`

- 文件数：1
- 目录作用：这一目录聚合了一组与 color-diff 相关的实现。

- `native-ts/color-diff/index.ts`：该目录的导出入口或聚合入口。

## 目录：`native-ts/file-index`

- 文件数：1
- 目录作用：这一目录聚合了一组与 file-index 相关的实现。

- `native-ts/file-index/index.ts`：该目录的导出入口或聚合入口。

## 目录：`native-ts/yoga-layout`

- 文件数：2
- 目录作用：这一目录聚合了一组与 yoga-layout 相关的实现。

- `native-ts/yoga-layout/enums.ts`：实现 enums 相关逻辑。
- `native-ts/yoga-layout/index.ts`：该目录的导出入口或聚合入口。

## 目录：`outputStyles`

- 文件数：1
- 目录作用：输出样式加载。

- `outputStyles/loadOutputStylesDir.ts`：实现 load output styles dir 相关逻辑。

## 目录：`plugins`

- 文件数：1
- 目录作用：插件系统入口。

- `plugins/builtinPlugins.ts`：处理插件发现、加载、缓存或插件命令。

## 目录：`plugins/bundled`

- 文件数：1
- 目录作用：内置插件装载逻辑。

- `plugins/bundled/index.ts`：该目录的导出入口或聚合入口。

## 目录：`query`

- 文件数：4
- 目录作用：查询构建与查询约束辅助模块。

- `query/config.ts`：处理配置项、配置解析或配置结构。
- `query/deps.ts`：实现 deps 相关逻辑。
- `query/stopHooks.ts`：实现 stop hooks 相关逻辑。
- `query/tokenBudget.ts`：实现 token budget 相关逻辑。

## 目录：`remote`

- 文件数：4
- 目录作用：远程会话和远程代理适配。

- `remote/remotePermissionBridge.ts`：处理权限检查、权限请求或权限规则。
- `remote/RemoteSessionManager.ts`：负责管理该模块的生命周期或资源对象。
- `remote/sdkMessageAdapter.ts`：处理消息结构、消息渲染或消息转换。
- `remote/SessionsWebSocket.ts`：处理会话对象、会话恢复或会话同步。

## 目录：`schemas`

- 文件数：1
- 目录作用：Schema 定义。

- `schemas/hooks.ts`：实现 hooks 相关逻辑。

## 目录：`screens`

- 文件数：3
- 目录作用：终端主要页面组件。

- `screens/Doctor.tsx`：定义 doctor 相关界面或交互组件。
- `screens/REPL.tsx`：定义 repl 相关界面或交互组件。
- `screens/ResumeConversation.tsx`：定义 resume conversation 相关界面或交互组件。

## 目录：`server`

- 文件数：3
- 目录作用：服务端连接、直连会话与服务端类型。

- `server/createDirectConnectSession.ts`：处理会话对象、会话恢复或会话同步。
- `server/directConnectManager.ts`：负责管理该模块的生命周期或资源对象。
- `server/types.ts`：定义这一模块相关的共享类型或结构。

## 目录：`services`

- 文件数：16
- 目录作用：跨模块服务层，对接外部系统或大型子系统。

- `services/awaySummary.ts`：实现 away summary 相关逻辑。
- `services/claudeAiLimits.ts`：实现 claude ai limits 相关逻辑。
- `services/claudeAiLimitsHook.ts`：实现单个 hook。
- `services/diagnosticTracking.ts`：实现 diagnostic tracking 相关逻辑。
- `services/internalLogging.ts`：实现 internal logging 相关逻辑。
- `services/mcpServerApproval.tsx`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `services/mockRateLimits.ts`：实现 mock rate limits 相关逻辑。
- `services/notifier.ts`：实现 notifier 相关逻辑。
- `services/preventSleep.ts`：实现 prevent sleep 相关逻辑。
- `services/rateLimitMessages.ts`：处理消息结构、消息渲染或消息转换。
- `services/rateLimitMocking.ts`：实现 rate limit mocking 相关逻辑。
- `services/tokenEstimation.ts`：实现 token estimation 相关逻辑。
- `services/vcr.ts`：实现 vcr 相关逻辑。
- `services/voice.ts`：实现 voice 相关逻辑。
- `services/voiceKeyterms.ts`：实现 voice keyterms 相关逻辑。
- `services/voiceStreamSTT.ts`：实现 voice stream stt 相关逻辑。

## 目录：`services/AgentSummary`

- 文件数：1
- 目录作用：这一目录聚合了一组与 AgentSummary 相关的实现。

- `services/AgentSummary/agentSummary.ts`：处理代理、子代理或代理展示相关逻辑。

## 目录：`services/analytics`

- 文件数：9
- 目录作用：这一目录聚合了一组与 analytics 相关的实现。

- `services/analytics/config.ts`：处理配置项、配置解析或配置结构。
- `services/analytics/datadog.ts`：实现 datadog 服务层逻辑。
- `services/analytics/firstPartyEventLogger.ts`：实现 first party event logger 服务层逻辑。
- `services/analytics/firstPartyEventLoggingExporter.ts`：实现 first party event logging exporter 服务层逻辑。
- `services/analytics/growthbook.ts`：实现 growthbook 服务层逻辑。
- `services/analytics/index.ts`：该目录的导出入口或聚合入口。
- `services/analytics/metadata.ts`：实现 metadata 服务层逻辑。
- `services/analytics/sink.ts`：实现 sink 服务层逻辑。
- `services/analytics/sinkKillswitch.ts`：实现 sink killswitch 服务层逻辑。

## 目录：`services/api`

- 文件数：20
- 目录作用：这一目录聚合了一组与 api 相关的实现。

- `services/api/adminRequests.ts`：实现 admin requests 服务层逻辑。
- `services/api/bootstrap.ts`：实现 bootstrap 服务层逻辑。
- `services/api/claude.ts`：实现 claude 服务层逻辑。
- `services/api/client.ts`：实现 client 服务层逻辑。
- `services/api/dumpPrompts.ts`：实现 dump prompts 服务层逻辑。
- `services/api/emptyUsage.ts`：实现 empty usage 服务层逻辑。
- `services/api/errors.ts`：实现 errors 服务层逻辑。
- `services/api/errorUtils.ts`：存放该模块的通用工具函数。
- `services/api/filesApi.ts`：实现 files api 服务层逻辑。
- `services/api/firstTokenDate.ts`：实现 first token date 服务层逻辑。
- `services/api/grove.ts`：实现 grove 服务层逻辑。
- `services/api/logging.ts`：实现 logging 服务层逻辑。
- `services/api/metricsOptOut.ts`：实现 metrics opt out 服务层逻辑。
- `services/api/overageCreditGrant.ts`：实现 overage credit grant 服务层逻辑。
- `services/api/promptCacheBreakDetection.ts`：实现 prompt cache break detection 服务层逻辑。
- `services/api/referral.ts`：实现 referral 服务层逻辑。
- `services/api/sessionIngress.ts`：处理会话对象、会话恢复或会话同步。
- `services/api/ultrareviewQuota.ts`：处理审查、评审或 review 工作流逻辑。
- `services/api/usage.ts`：实现 usage 服务层逻辑。
- `services/api/withRetry.ts`：实现 with retry 服务层逻辑。

## 目录：`services/autoDream`

- 文件数：4
- 目录作用：这一目录聚合了一组与 autoDream 相关的实现。

- `services/autoDream/autoDream.ts`：实现 auto dream 服务层逻辑。
- `services/autoDream/config.ts`：处理配置项、配置解析或配置结构。
- `services/autoDream/consolidationLock.ts`：实现 consolidation lock 服务层逻辑。
- `services/autoDream/consolidationPrompt.ts`：定义提示词、说明文本或模型提示模板。

## 目录：`services/compact`

- 文件数：11
- 目录作用：这一目录聚合了一组与 compact 相关的实现。

- `services/compact/apiMicrocompact.ts`：实现 api microcompact 服务层逻辑。
- `services/compact/autoCompact.ts`：实现 auto compact 服务层逻辑。
- `services/compact/compact.ts`：实现 compact 服务层逻辑。
- `services/compact/compactWarningHook.ts`：实现单个 hook。
- `services/compact/compactWarningState.ts`：实现 compact warning state 服务层逻辑。
- `services/compact/grouping.ts`：实现 grouping 服务层逻辑。
- `services/compact/microCompact.ts`：实现 micro compact 服务层逻辑。
- `services/compact/postCompactCleanup.ts`：实现 post compact cleanup 服务层逻辑。
- `services/compact/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `services/compact/sessionMemoryCompact.ts`：处理会话对象、会话恢复或会话同步。
- `services/compact/timeBasedMCConfig.ts`：处理配置项、配置解析或配置结构。

## 目录：`services/extractMemories`

- 文件数：2
- 目录作用：这一目录聚合了一组与 extractMemories 相关的实现。

- `services/extractMemories/extractMemories.ts`：实现 extract memories 服务层逻辑。
- `services/extractMemories/prompts.ts`：实现 prompts 服务层逻辑。

## 目录：`services/lsp`

- 文件数：7
- 目录作用：这一目录聚合了一组与 lsp 相关的实现。

- `services/lsp/config.ts`：处理配置项、配置解析或配置结构。
- `services/lsp/LSPClient.ts`：实现 lspclient 服务层逻辑。
- `services/lsp/LSPDiagnosticRegistry.ts`：实现 lspdiagnostic registry 服务层逻辑。
- `services/lsp/LSPServerInstance.ts`：实现 lspserver instance 服务层逻辑。
- `services/lsp/LSPServerManager.ts`：负责管理该模块的生命周期或资源对象。
- `services/lsp/manager.ts`：负责管理该模块的生命周期或资源对象。
- `services/lsp/passiveFeedback.ts`：实现 passive feedback 服务层逻辑。

## 目录：`services/MagicDocs`

- 文件数：2
- 目录作用：这一目录聚合了一组与 MagicDocs 相关的实现。

- `services/MagicDocs/magicDocs.ts`：实现 magic docs 服务层逻辑。
- `services/MagicDocs/prompts.ts`：实现 prompts 服务层逻辑。

## 目录：`services/mcp`

- 文件数：23
- 目录作用：这一目录聚合了一组与 mcp 相关的实现。

- `services/mcp/auth.ts`：实现 auth 服务层逻辑。
- `services/mcp/channelAllowlist.ts`：实现 channel allowlist 服务层逻辑。
- `services/mcp/channelNotification.ts`：实现 channel notification 服务层逻辑。
- `services/mcp/channelPermissions.ts`：处理权限检查、权限请求或权限规则。
- `services/mcp/claudeai.ts`：实现 claudeai 服务层逻辑。
- `services/mcp/client.ts`：实现 client 服务层逻辑。
- `services/mcp/config.ts`：处理配置项、配置解析或配置结构。
- `services/mcp/elicitationHandler.ts`：实现 elicitation handler 服务层逻辑。
- `services/mcp/envExpansion.ts`：实现 env expansion 服务层逻辑。
- `services/mcp/headersHelper.ts`：存放该模块的辅助函数。
- `services/mcp/InProcessTransport.ts`：实现 in process transport 服务层逻辑。
- `services/mcp/MCPConnectionManager.tsx`：负责管理该模块的生命周期或资源对象。
- `services/mcp/mcpStringUtils.ts`：存放该模块的通用工具函数。
- `services/mcp/normalization.ts`：实现 normalization 服务层逻辑。
- `services/mcp/oauthPort.ts`：处理 OAuth 登录或鉴权相关逻辑。
- `services/mcp/officialRegistry.ts`：实现 official registry 服务层逻辑。
- `services/mcp/SdkControlTransport.ts`：实现 sdk control transport 服务层逻辑。
- `services/mcp/types.ts`：定义这一模块相关的共享类型或结构。
- `services/mcp/useManageMCPConnections.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `services/mcp/utils.ts`：存放该模块的通用工具函数。
- `services/mcp/vscodeSdkMcp.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `services/mcp/xaa.ts`：实现 xaa 服务层逻辑。
- `services/mcp/xaaIdpLogin.ts`：处理登录或登出相关逻辑。

## 目录：`services/oauth`

- 文件数：5
- 目录作用：这一目录聚合了一组与 oauth 相关的实现。

- `services/oauth/auth-code-listener.ts`：实现 auth code listener 服务层逻辑。
- `services/oauth/client.ts`：实现 client 服务层逻辑。
- `services/oauth/crypto.ts`：实现 crypto 服务层逻辑。
- `services/oauth/getOauthProfile.ts`：处理 OAuth 登录或鉴权相关逻辑。
- `services/oauth/index.ts`：该目录的导出入口或聚合入口。

## 目录：`services/plugins`

- 文件数：3
- 目录作用：这一目录聚合了一组与 plugins 相关的实现。

- `services/plugins/pluginCliCommands.ts`：处理插件发现、加载、缓存或插件命令。
- `services/plugins/PluginInstallationManager.ts`：负责管理该模块的生命周期或资源对象。
- `services/plugins/pluginOperations.ts`：处理插件发现、加载、缓存或插件命令。

## 目录：`services/policyLimits`

- 文件数：2
- 目录作用：这一目录聚合了一组与 policyLimits 相关的实现。

- `services/policyLimits/index.ts`：该目录的导出入口或聚合入口。
- `services/policyLimits/types.ts`：定义这一模块相关的共享类型或结构。

## 目录：`services/PromptSuggestion`

- 文件数：2
- 目录作用：这一目录聚合了一组与 PromptSuggestion 相关的实现。

- `services/PromptSuggestion/promptSuggestion.ts`：实现 prompt suggestion 服务层逻辑。
- `services/PromptSuggestion/speculation.ts`：实现 speculation 服务层逻辑。

## 目录：`services/remoteManagedSettings`

- 文件数：5
- 目录作用：这一目录聚合了一组与 remoteManagedSettings 相关的实现。

- `services/remoteManagedSettings/index.ts`：该目录的导出入口或聚合入口。
- `services/remoteManagedSettings/securityCheck.tsx`：实现 security check 服务层逻辑。
- `services/remoteManagedSettings/syncCache.ts`：实现 sync cache 服务层逻辑。
- `services/remoteManagedSettings/syncCacheState.ts`：实现 sync cache state 服务层逻辑。
- `services/remoteManagedSettings/types.ts`：定义这一模块相关的共享类型或结构。

## 目录：`services/SessionMemory`

- 文件数：3
- 目录作用：这一目录聚合了一组与 SessionMemory 相关的实现。

- `services/SessionMemory/prompts.ts`：实现 prompts 服务层逻辑。
- `services/SessionMemory/sessionMemory.ts`：处理会话对象、会话恢复或会话同步。
- `services/SessionMemory/sessionMemoryUtils.ts`：存放该模块的通用工具函数。

## 目录：`services/settingsSync`

- 文件数：2
- 目录作用：这一目录聚合了一组与 settingsSync 相关的实现。

- `services/settingsSync/index.ts`：该目录的导出入口或聚合入口。
- `services/settingsSync/types.ts`：定义这一模块相关的共享类型或结构。

## 目录：`services/teamMemorySync`

- 文件数：5
- 目录作用：这一目录聚合了一组与 teamMemorySync 相关的实现。

- `services/teamMemorySync/index.ts`：该目录的导出入口或聚合入口。
- `services/teamMemorySync/secretScanner.ts`：实现 secret scanner 服务层逻辑。
- `services/teamMemorySync/teamMemSecretGuard.ts`：实现 team mem secret guard 服务层逻辑。
- `services/teamMemorySync/types.ts`：定义这一模块相关的共享类型或结构。
- `services/teamMemorySync/watcher.ts`：实现 watcher 服务层逻辑。

## 目录：`services/tips`

- 文件数：3
- 目录作用：这一目录聚合了一组与 tips 相关的实现。

- `services/tips/tipHistory.ts`：处理历史记录、会话历史或历史状态。
- `services/tips/tipRegistry.ts`：实现 tip registry 服务层逻辑。
- `services/tips/tipScheduler.ts`：实现 tip scheduler 服务层逻辑。

## 目录：`services/tools`

- 文件数：4
- 目录作用：这一目录聚合了一组与 tools 相关的实现。

- `services/tools/StreamingToolExecutor.ts`：实现 streaming tool executor 服务层逻辑。
- `services/tools/toolExecution.ts`：实现 tool execution 服务层逻辑。
- `services/tools/toolHooks.ts`：实现 tool hooks 服务层逻辑。
- `services/tools/toolOrchestration.ts`：实现 tool orchestration 服务层逻辑。

## 目录：`services/toolUseSummary`

- 文件数：1
- 目录作用：这一目录聚合了一组与 toolUseSummary 相关的实现。

- `services/toolUseSummary/toolUseSummaryGenerator.ts`：实现 tool use summary generator 服务层逻辑。

## 目录：`skills`

- 文件数：3
- 目录作用：技能系统入口与加载逻辑。

- `skills/bundledSkills.ts`：处理技能加载、索引、解析或技能运行支持。
- `skills/loadSkillsDir.ts`：处理技能加载、索引、解析或技能运行支持。
- `skills/mcpSkillBuilders.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。

## 目录：`skills/bundled`

- 文件数：17
- 目录作用：内置技能与内置技能索引。

- `skills/bundled/batch.ts`：实现 batch 技能逻辑。
- `skills/bundled/claudeApi.ts`：实现 claude api 技能逻辑。
- `skills/bundled/claudeApiContent.ts`：实现 claude api content 技能逻辑。
- `skills/bundled/claudeInChrome.ts`：实现 claude in chrome 技能逻辑。
- `skills/bundled/debug.ts`：实现 debug 技能逻辑。
- `skills/bundled/index.ts`：该目录的导出入口或聚合入口。
- `skills/bundled/keybindings.ts`：实现 keybindings 技能逻辑。
- `skills/bundled/loop.ts`：实现 loop 技能逻辑。
- `skills/bundled/loremIpsum.ts`：实现 lorem ipsum 技能逻辑。
- `skills/bundled/remember.ts`：实现 remember 技能逻辑。
- `skills/bundled/scheduleRemoteAgents.ts`：处理代理、子代理或代理展示相关逻辑。
- `skills/bundled/simplify.ts`：实现 simplify 技能逻辑。
- `skills/bundled/skillify.ts`：处理技能加载、索引、解析或技能运行支持。
- `skills/bundled/stuck.ts`：实现 stuck 技能逻辑。
- `skills/bundled/updateConfig.ts`：处理配置项、配置解析或配置结构。
- `skills/bundled/verify.ts`：实现 verify 技能逻辑。
- `skills/bundled/verifyContent.ts`：实现 verify content 技能逻辑。

## 目录：`state`

- 文件数：6
- 目录作用：应用状态、状态仓库与状态监听。

- `state/AppState.tsx`：定义 app state 相关界面或交互组件。
- `state/AppStateStore.ts`：定义状态存储或状态容器逻辑。
- `state/onChangeAppState.ts`：实现 on change app state 相关逻辑。
- `state/selectors.ts`：实现 selectors 相关逻辑。
- `state/store.ts`：定义状态存储或状态容器逻辑。
- `state/teammateViewHelpers.ts`：存放该模块的辅助函数。

## 目录：`tasks`

- 文件数：4
- 目录作用：任务类型与不同任务执行器。

- `tasks/LocalMainSessionTask.ts`：处理会话对象、会话恢复或会话同步。
- `tasks/pillLabel.ts`：实现 pill label 相关逻辑。
- `tasks/stopTask.ts`：处理任务对象、任务状态或任务执行流程。
- `tasks/types.ts`：定义这一模块相关的共享类型或结构。

## 目录：`tasks/DreamTask`

- 文件数：1
- 目录作用：这一目录聚合了一组与 DreamTask 相关的实现。

- `tasks/DreamTask/DreamTask.ts`：处理任务对象、任务状态或任务执行流程。

## 目录：`tasks/InProcessTeammateTask`

- 文件数：2
- 目录作用：这一目录聚合了一组与 InProcessTeammateTask 相关的实现。

- `tasks/InProcessTeammateTask/InProcessTeammateTask.tsx`：处理任务对象、任务状态或任务执行流程。
- `tasks/InProcessTeammateTask/types.ts`：定义这一模块相关的共享类型或结构。

## 目录：`tasks/LocalAgentTask`

- 文件数：1
- 目录作用：这一目录聚合了一组与 LocalAgentTask 相关的实现。

- `tasks/LocalAgentTask/LocalAgentTask.tsx`：处理任务对象、任务状态或任务执行流程。

## 目录：`tasks/LocalShellTask`

- 文件数：3
- 目录作用：这一目录聚合了一组与 LocalShellTask 相关的实现。

- `tasks/LocalShellTask/guards.ts`：实现 guards 任务流程。
- `tasks/LocalShellTask/killShellTasks.ts`：处理任务对象、任务状态或任务执行流程。
- `tasks/LocalShellTask/LocalShellTask.tsx`：处理任务对象、任务状态或任务执行流程。

## 目录：`tasks/RemoteAgentTask`

- 文件数：1
- 目录作用：这一目录聚合了一组与 RemoteAgentTask 相关的实现。

- `tasks/RemoteAgentTask/RemoteAgentTask.tsx`：处理任务对象、任务状态或任务执行流程。

## 目录：`tools`

- 文件数：1
- 目录作用：工具系统入口与工具注册。

- `tools/utils.ts`：存放该模块的通用工具函数。

## 目录：`tools/AgentTool`

- 文件数：14
- 目录作用：这一目录聚合了一组与 AgentTool 相关的实现。

- `tools/AgentTool/agentColorManager.ts`：负责管理该模块的生命周期或资源对象。
- `tools/AgentTool/agentDisplay.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/agentMemory.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/agentMemorySnapshot.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/AgentTool.tsx`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/AgentTool/agentToolUtils.ts`：存放该模块的通用工具函数。
- `tools/AgentTool/builtInAgents.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/constants.ts`：定义这一模块用到的常量。
- `tools/AgentTool/forkSubagent.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/loadAgentsDir.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/AgentTool/resumeAgent.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/runAgent.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/AgentTool/built-in`

- 文件数：6
- 目录作用：这一目录聚合了一组与 built-in 相关的实现。

- `tools/AgentTool/built-in/claudeCodeGuideAgent.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/built-in/exploreAgent.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/built-in/generalPurposeAgent.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/built-in/planAgent.ts`：处理代理、子代理或代理展示相关逻辑。
- `tools/AgentTool/built-in/statuslineSetup.ts`：实现 statusline setup 工具相关逻辑。
- `tools/AgentTool/built-in/verificationAgent.ts`：处理代理、子代理或代理展示相关逻辑。

## 目录：`tools/AskUserQuestionTool`

- 文件数：2
- 目录作用：这一目录聚合了一组与 AskUserQuestionTool 相关的实现。

- `tools/AskUserQuestionTool/AskUserQuestionTool.tsx`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/AskUserQuestionTool/prompt.ts`：定义提示词、说明文本或模型提示模板。

## 目录：`tools/BashTool`

- 文件数：18
- 目录作用：这一目录聚合了一组与 BashTool 相关的实现。

- `tools/BashTool/bashCommandHelpers.ts`：存放该模块的辅助函数。
- `tools/BashTool/bashPermissions.ts`：处理权限检查、权限请求或权限规则。
- `tools/BashTool/bashSecurity.ts`：处理 bash 命令构造、解析或执行规则。
- `tools/BashTool/BashTool.tsx`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/BashTool/BashToolResultMessage.tsx`：处理消息结构、消息渲染或消息转换。
- `tools/BashTool/commandSemantics.ts`：实现 command semantics 工具相关逻辑。
- `tools/BashTool/commentLabel.ts`：实现 comment label 工具相关逻辑。
- `tools/BashTool/destructiveCommandWarning.ts`：实现 destructive command warning 工具相关逻辑。
- `tools/BashTool/modeValidation.ts`：实现 mode validation 工具相关逻辑。
- `tools/BashTool/pathValidation.ts`：实现 path validation 工具相关逻辑。
- `tools/BashTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/BashTool/readOnlyValidation.ts`：实现 read only validation 工具相关逻辑。
- `tools/BashTool/sedEditParser.ts`：实现 sed edit parser 工具相关逻辑。
- `tools/BashTool/sedValidation.ts`：实现 sed validation 工具相关逻辑。
- `tools/BashTool/shouldUseSandbox.ts`：处理沙箱模式、沙箱权限或沙箱桥接。
- `tools/BashTool/toolName.ts`：实现 tool name 工具相关逻辑。
- `tools/BashTool/UI.tsx`：实现 ui 工具相关逻辑。
- `tools/BashTool/utils.ts`：存放该模块的通用工具函数。

## 目录：`tools/BriefTool`

- 文件数：5
- 目录作用：这一目录聚合了一组与 BriefTool 相关的实现。

- `tools/BriefTool/attachments.ts`：实现 attachments 工具相关逻辑。
- `tools/BriefTool/BriefTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/BriefTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/BriefTool/UI.tsx`：实现 ui 工具相关逻辑。
- `tools/BriefTool/upload.ts`：实现 upload 工具相关逻辑。

## 目录：`tools/ConfigTool`

- 文件数：5
- 目录作用：这一目录聚合了一组与 ConfigTool 相关的实现。

- `tools/ConfigTool/ConfigTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/ConfigTool/constants.ts`：定义这一模块用到的常量。
- `tools/ConfigTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/ConfigTool/supportedSettings.ts`：处理设置读取、缓存、校验或写入。
- `tools/ConfigTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/EnterPlanModeTool`

- 文件数：4
- 目录作用：这一目录聚合了一组与 EnterPlanModeTool 相关的实现。

- `tools/EnterPlanModeTool/constants.ts`：定义这一模块用到的常量。
- `tools/EnterPlanModeTool/EnterPlanModeTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/EnterPlanModeTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/EnterPlanModeTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/EnterWorktreeTool`

- 文件数：4
- 目录作用：这一目录聚合了一组与 EnterWorktreeTool 相关的实现。

- `tools/EnterWorktreeTool/constants.ts`：定义这一模块用到的常量。
- `tools/EnterWorktreeTool/EnterWorktreeTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/EnterWorktreeTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/EnterWorktreeTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/ExitPlanModeTool`

- 文件数：4
- 目录作用：这一目录聚合了一组与 ExitPlanModeTool 相关的实现。

- `tools/ExitPlanModeTool/constants.ts`：定义这一模块用到的常量。
- `tools/ExitPlanModeTool/ExitPlanModeV2Tool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/ExitPlanModeTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/ExitPlanModeTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/ExitWorktreeTool`

- 文件数：4
- 目录作用：这一目录聚合了一组与 ExitWorktreeTool 相关的实现。

- `tools/ExitWorktreeTool/constants.ts`：定义这一模块用到的常量。
- `tools/ExitWorktreeTool/ExitWorktreeTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/ExitWorktreeTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/ExitWorktreeTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/FileEditTool`

- 文件数：6
- 目录作用：这一目录聚合了一组与 FileEditTool 相关的实现。

- `tools/FileEditTool/constants.ts`：定义这一模块用到的常量。
- `tools/FileEditTool/FileEditTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/FileEditTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/FileEditTool/types.ts`：定义这一模块相关的共享类型或结构。
- `tools/FileEditTool/UI.tsx`：实现 ui 工具相关逻辑。
- `tools/FileEditTool/utils.ts`：存放该模块的通用工具函数。

## 目录：`tools/FileReadTool`

- 文件数：5
- 目录作用：这一目录聚合了一组与 FileReadTool 相关的实现。

- `tools/FileReadTool/FileReadTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/FileReadTool/imageProcessor.ts`：实现 image processor 工具相关逻辑。
- `tools/FileReadTool/limits.ts`：实现 limits 工具相关逻辑。
- `tools/FileReadTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/FileReadTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/FileWriteTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 FileWriteTool 相关的实现。

- `tools/FileWriteTool/FileWriteTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/FileWriteTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/FileWriteTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/GlobTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 GlobTool 相关的实现。

- `tools/GlobTool/GlobTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/GlobTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/GlobTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/GrepTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 GrepTool 相关的实现。

- `tools/GrepTool/GrepTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/GrepTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/GrepTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/ListMcpResourcesTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 ListMcpResourcesTool 相关的实现。

- `tools/ListMcpResourcesTool/ListMcpResourcesTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/ListMcpResourcesTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/ListMcpResourcesTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/LSPTool`

- 文件数：6
- 目录作用：这一目录聚合了一组与 LSPTool 相关的实现。

- `tools/LSPTool/formatters.ts`：实现 formatters 工具相关逻辑。
- `tools/LSPTool/LSPTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/LSPTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/LSPTool/schemas.ts`：定义校验结构或数据 schema。
- `tools/LSPTool/symbolContext.ts`：定义上下文对象或上下文获取逻辑。
- `tools/LSPTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/McpAuthTool`

- 文件数：1
- 目录作用：这一目录聚合了一组与 McpAuthTool 相关的实现。

- `tools/McpAuthTool/McpAuthTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`tools/MCPTool`

- 文件数：4
- 目录作用：这一目录聚合了一组与 MCPTool 相关的实现。

- `tools/MCPTool/classifyForCollapse.ts`：实现 classify for collapse 工具相关逻辑。
- `tools/MCPTool/MCPTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/MCPTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/MCPTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/NotebookEditTool`

- 文件数：4
- 目录作用：这一目录聚合了一组与 NotebookEditTool 相关的实现。

- `tools/NotebookEditTool/constants.ts`：定义这一模块用到的常量。
- `tools/NotebookEditTool/NotebookEditTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/NotebookEditTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/NotebookEditTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/PowerShellTool`

- 文件数：14
- 目录作用：这一目录聚合了一组与 PowerShellTool 相关的实现。

- `tools/PowerShellTool/clmTypes.ts`：定义这一模块相关的共享类型或结构。
- `tools/PowerShellTool/commandSemantics.ts`：实现 command semantics 工具相关逻辑。
- `tools/PowerShellTool/commonParameters.ts`：实现 common parameters 工具相关逻辑。
- `tools/PowerShellTool/destructiveCommandWarning.ts`：实现 destructive command warning 工具相关逻辑。
- `tools/PowerShellTool/gitSafety.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `tools/PowerShellTool/modeValidation.ts`：实现 mode validation 工具相关逻辑。
- `tools/PowerShellTool/pathValidation.ts`：实现 path validation 工具相关逻辑。
- `tools/PowerShellTool/powershellPermissions.ts`：处理权限检查、权限请求或权限规则。
- `tools/PowerShellTool/powershellSecurity.ts`：处理 PowerShell 命令或权限规则。
- `tools/PowerShellTool/PowerShellTool.tsx`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/PowerShellTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/PowerShellTool/readOnlyValidation.ts`：实现 read only validation 工具相关逻辑。
- `tools/PowerShellTool/toolName.ts`：实现 tool name 工具相关逻辑。
- `tools/PowerShellTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/ReadMcpResourceTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 ReadMcpResourceTool 相关的实现。

- `tools/ReadMcpResourceTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/ReadMcpResourceTool/ReadMcpResourceTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/ReadMcpResourceTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/RemoteTriggerTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 RemoteTriggerTool 相关的实现。

- `tools/RemoteTriggerTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/RemoteTriggerTool/RemoteTriggerTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/RemoteTriggerTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/REPLTool`

- 文件数：2
- 目录作用：这一目录聚合了一组与 REPLTool 相关的实现。

- `tools/REPLTool/constants.ts`：定义这一模块用到的常量。
- `tools/REPLTool/primitiveTools.ts`：实现 primitive tools 工具相关逻辑。

## 目录：`tools/ScheduleCronTool`

- 文件数：5
- 目录作用：这一目录聚合了一组与 ScheduleCronTool 相关的实现。

- `tools/ScheduleCronTool/CronCreateTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/ScheduleCronTool/CronDeleteTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/ScheduleCronTool/CronListTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/ScheduleCronTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/ScheduleCronTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/SendMessageTool`

- 文件数：4
- 目录作用：这一目录聚合了一组与 SendMessageTool 相关的实现。

- `tools/SendMessageTool/constants.ts`：定义这一模块用到的常量。
- `tools/SendMessageTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/SendMessageTool/SendMessageTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/SendMessageTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/shared`

- 文件数：2
- 目录作用：这一目录聚合了一组与 shared 相关的实现。

- `tools/shared/gitOperationTracking.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `tools/shared/spawnMultiAgent.ts`：处理代理、子代理或代理展示相关逻辑。

## 目录：`tools/SkillTool`

- 文件数：4
- 目录作用：这一目录聚合了一组与 SkillTool 相关的实现。

- `tools/SkillTool/constants.ts`：定义这一模块用到的常量。
- `tools/SkillTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/SkillTool/SkillTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/SkillTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/SleepTool`

- 文件数：1
- 目录作用：这一目录聚合了一组与 SleepTool 相关的实现。

- `tools/SleepTool/prompt.ts`：定义提示词、说明文本或模型提示模板。

## 目录：`tools/SyntheticOutputTool`

- 文件数：1
- 目录作用：这一目录聚合了一组与 SyntheticOutputTool 相关的实现。

- `tools/SyntheticOutputTool/SyntheticOutputTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`tools/TaskCreateTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 TaskCreateTool 相关的实现。

- `tools/TaskCreateTool/constants.ts`：定义这一模块用到的常量。
- `tools/TaskCreateTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/TaskCreateTool/TaskCreateTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`tools/TaskGetTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 TaskGetTool 相关的实现。

- `tools/TaskGetTool/constants.ts`：定义这一模块用到的常量。
- `tools/TaskGetTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/TaskGetTool/TaskGetTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`tools/TaskListTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 TaskListTool 相关的实现。

- `tools/TaskListTool/constants.ts`：定义这一模块用到的常量。
- `tools/TaskListTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/TaskListTool/TaskListTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`tools/TaskOutputTool`

- 文件数：2
- 目录作用：这一目录聚合了一组与 TaskOutputTool 相关的实现。

- `tools/TaskOutputTool/constants.ts`：定义这一模块用到的常量。
- `tools/TaskOutputTool/TaskOutputTool.tsx`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`tools/TaskStopTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 TaskStopTool 相关的实现。

- `tools/TaskStopTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/TaskStopTool/TaskStopTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/TaskStopTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/TaskUpdateTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 TaskUpdateTool 相关的实现。

- `tools/TaskUpdateTool/constants.ts`：定义这一模块用到的常量。
- `tools/TaskUpdateTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/TaskUpdateTool/TaskUpdateTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`tools/TeamCreateTool`

- 文件数：4
- 目录作用：这一目录聚合了一组与 TeamCreateTool 相关的实现。

- `tools/TeamCreateTool/constants.ts`：定义这一模块用到的常量。
- `tools/TeamCreateTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/TeamCreateTool/TeamCreateTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/TeamCreateTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/TeamDeleteTool`

- 文件数：4
- 目录作用：这一目录聚合了一组与 TeamDeleteTool 相关的实现。

- `tools/TeamDeleteTool/constants.ts`：定义这一模块用到的常量。
- `tools/TeamDeleteTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/TeamDeleteTool/TeamDeleteTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `tools/TeamDeleteTool/UI.tsx`：实现 ui 工具相关逻辑。

## 目录：`tools/testing`

- 文件数：1
- 目录作用：这一目录聚合了一组与 testing 相关的实现。

- `tools/testing/TestingPermissionTool.tsx`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`tools/TodoWriteTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 TodoWriteTool 相关的实现。

- `tools/TodoWriteTool/constants.ts`：定义这一模块用到的常量。
- `tools/TodoWriteTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/TodoWriteTool/TodoWriteTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`tools/ToolSearchTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 ToolSearchTool 相关的实现。

- `tools/ToolSearchTool/constants.ts`：定义这一模块用到的常量。
- `tools/ToolSearchTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/ToolSearchTool/ToolSearchTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`tools/WebFetchTool`

- 文件数：5
- 目录作用：这一目录聚合了一组与 WebFetchTool 相关的实现。

- `tools/WebFetchTool/preapproved.ts`：实现 preapproved 工具相关逻辑。
- `tools/WebFetchTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/WebFetchTool/UI.tsx`：实现 ui 工具相关逻辑。
- `tools/WebFetchTool/utils.ts`：存放该模块的通用工具函数。
- `tools/WebFetchTool/WebFetchTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`tools/WebSearchTool`

- 文件数：3
- 目录作用：这一目录聚合了一组与 WebSearchTool 相关的实现。

- `tools/WebSearchTool/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `tools/WebSearchTool/UI.tsx`：实现 ui 工具相关逻辑。
- `tools/WebSearchTool/WebSearchTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。

## 目录：`types`

- 文件数：7
- 目录作用：共享类型定义。

- `types/command.ts`：定义一个具体命令的注册与执行逻辑。
- `types/hooks.ts`：实现 hooks 相关逻辑。
- `types/ids.ts`：实现 ids 相关逻辑。
- `types/logs.ts`：实现 logs 相关逻辑。
- `types/permissions.ts`：处理权限检查、权限请求或权限规则。
- `types/plugin.ts`：处理插件发现、加载、缓存或插件命令。
- `types/textInputTypes.ts`：定义这一模块相关的共享类型或结构。

## 目录：`types/generated/events_mono/claude_code/v1`

- 文件数：1
- 目录作用：这一目录聚合了一组与 v1 相关的实现。

- `types/generated/events_mono/claude_code/v1/claude_code_internal_event.ts`：定义 claude code internal event 类型。

## 目录：`types/generated/events_mono/common/v1`

- 文件数：1
- 目录作用：这一目录聚合了一组与 v1 相关的实现。

- `types/generated/events_mono/common/v1/auth.ts`：定义 auth 类型。

## 目录：`types/generated/events_mono/growthbook/v1`

- 文件数：1
- 目录作用：这一目录聚合了一组与 v1 相关的实现。

- `types/generated/events_mono/growthbook/v1/growthbook_experiment_event.ts`：定义 growthbook experiment event 类型。

## 目录：`types/generated/google/protobuf`

- 文件数：1
- 目录作用：这一目录聚合了一组与 protobuf 相关的实现。

- `types/generated/google/protobuf/timestamp.ts`：定义 timestamp 类型。

## 目录：`upstreamproxy`

- 文件数：2
- 目录作用：上游代理转发相关逻辑。

- `upstreamproxy/relay.ts`：实现 relay 相关逻辑。
- `upstreamproxy/upstreamproxy.ts`：实现 upstreamproxy 相关逻辑。

## 目录：`utils`

- 文件数：298
- 目录作用：最大基础设施层，放置配置、权限、日志、Git、模型、文件系统等通用能力。

- `utils/abortController.ts`：实现 abort controller 相关逻辑。
- `utils/activityManager.ts`：负责管理该模块的生命周期或资源对象。
- `utils/advisor.ts`：实现 advisor 相关逻辑。
- `utils/agentContext.ts`：定义上下文对象或上下文获取逻辑。
- `utils/agenticSessionSearch.ts`：处理会话对象、会话恢复或会话同步。
- `utils/agentId.ts`：处理代理、子代理或代理展示相关逻辑。
- `utils/agentSwarmsEnabled.ts`：处理代理、子代理或代理展示相关逻辑。
- `utils/analyzeContext.ts`：定义上下文对象或上下文获取逻辑。
- `utils/ansiToPng.ts`：实现 ansi to png 相关逻辑。
- `utils/ansiToSvg.ts`：实现 ansi to svg 相关逻辑。
- `utils/api.ts`：实现 api 相关逻辑。
- `utils/apiPreconnect.ts`：实现 api preconnect 相关逻辑。
- `utils/appleTerminalBackup.ts`：实现 apple terminal backup 相关逻辑。
- `utils/argumentSubstitution.ts`：实现 argument substitution 相关逻辑。
- `utils/array.ts`：实现 array 相关逻辑。
- `utils/asciicast.ts`：实现 asciicast 相关逻辑。
- `utils/attachments.ts`：实现 attachments 相关逻辑。
- `utils/attribution.ts`：实现 attribution 相关逻辑。
- `utils/auth.ts`：实现 auth 相关逻辑。
- `utils/authFileDescriptor.ts`：实现 auth file descriptor 相关逻辑。
- `utils/authPortable.ts`：实现 auth portable 相关逻辑。
- `utils/autoModeDenials.ts`：实现 auto mode denials 相关逻辑。
- `utils/autoRunIssue.tsx`：定义 auto run issue 相关界面或交互组件。
- `utils/autoUpdater.ts`：实现 auto updater 相关逻辑。
- `utils/aws.ts`：实现 aws 相关逻辑。
- `utils/awsAuthStatusManager.ts`：负责管理该模块的生命周期或资源对象。
- `utils/backgroundHousekeeping.ts`：实现 background housekeeping 相关逻辑。
- `utils/betas.ts`：实现 betas 相关逻辑。
- `utils/billing.ts`：实现 billing 相关逻辑。
- `utils/binaryCheck.ts`：实现 binary check 相关逻辑。
- `utils/browser.ts`：实现 browser 相关逻辑。
- `utils/bufferedWriter.ts`：实现 buffered writer 相关逻辑。
- `utils/bundledMode.ts`：实现 bundled mode 相关逻辑。
- `utils/caCerts.ts`：实现 ca certs 相关逻辑。
- `utils/caCertsConfig.ts`：处理配置项、配置解析或配置结构。
- `utils/cachePaths.ts`：实现 cache paths 相关逻辑。
- `utils/CircularBuffer.ts`：实现 circular buffer 相关逻辑。
- `utils/classifierApprovals.ts`：实现 classifier approvals 相关逻辑。
- `utils/classifierApprovalsHook.ts`：实现单个 hook。
- `utils/claudeCodeHints.ts`：实现 claude code hints 相关逻辑。
- `utils/claudeDesktop.ts`：实现 claude desktop 相关逻辑。
- `utils/claudemd.ts`：实现 claudemd 相关逻辑。
- `utils/cleanup.ts`：实现 cleanup 相关逻辑。
- `utils/cleanupRegistry.ts`：实现 cleanup registry 相关逻辑。
- `utils/cliArgs.ts`：实现 cli args 相关逻辑。
- `utils/cliHighlight.ts`：实现 cli highlight 相关逻辑。
- `utils/codeIndexing.ts`：实现 code indexing 相关逻辑。
- `utils/collapseBackgroundBashNotifications.ts`：处理 bash 命令构造、解析或执行规则。
- `utils/collapseHookSummaries.ts`：实现 collapse hook summaries 相关逻辑。
- `utils/collapseReadSearch.ts`：实现 collapse read search 相关逻辑。
- `utils/collapseTeammateShutdowns.ts`：实现 collapse teammate shutdowns 相关逻辑。
- `utils/combinedAbortSignal.ts`：实现 combined abort signal 相关逻辑。
- `utils/commandLifecycle.ts`：实现 command lifecycle 相关逻辑。
- `utils/commitAttribution.ts`：实现 commit attribution 相关逻辑。
- `utils/completionCache.ts`：实现 completion cache 相关逻辑。
- `utils/concurrentSessions.ts`：处理会话对象、会话恢复或会话同步。
- `utils/config.ts`：处理配置项、配置解析或配置结构。
- `utils/configConstants.ts`：定义这一模块用到的常量。
- `utils/contentArray.ts`：实现 content array 相关逻辑。
- `utils/context.ts`：定义上下文对象或上下文获取逻辑。
- `utils/contextAnalysis.ts`：实现 context analysis 相关逻辑。
- `utils/contextSuggestions.ts`：实现 context suggestions 相关逻辑。
- `utils/controlMessageCompat.ts`：处理消息结构、消息渲染或消息转换。
- `utils/conversationRecovery.ts`：实现 conversation recovery 相关逻辑。
- `utils/cron.ts`：实现 cron 相关逻辑。
- `utils/cronJitterConfig.ts`：处理配置项、配置解析或配置结构。
- `utils/cronScheduler.ts`：实现 cron scheduler 相关逻辑。
- `utils/cronTasks.ts`：处理任务对象、任务状态或任务执行流程。
- `utils/cronTasksLock.ts`：处理任务对象、任务状态或任务执行流程。
- `utils/crossProjectResume.ts`：实现 cross project resume 相关逻辑。
- `utils/crypto.ts`：实现 crypto 相关逻辑。
- `utils/Cursor.ts`：实现 cursor 相关逻辑。
- `utils/cwd.ts`：实现 cwd 相关逻辑。
- `utils/debug.ts`：实现 debug 相关逻辑。
- `utils/debugFilter.ts`：实现 debug filter 相关逻辑。
- `utils/desktopDeepLink.ts`：实现 desktop deep link 相关逻辑。
- `utils/detectRepository.ts`：实现 detect repository 相关逻辑。
- `utils/diagLogs.ts`：实现 diag logs 相关逻辑。
- `utils/diff.ts`：处理差异展示、差异格式化或差异比较。
- `utils/directMemberMessage.ts`：处理消息结构、消息渲染或消息转换。
- `utils/displayTags.ts`：实现 display tags 相关逻辑。
- `utils/doctorContextWarnings.ts`：实现 doctor context warnings 相关逻辑。
- `utils/doctorDiagnostic.ts`：实现 doctor diagnostic 相关逻辑。
- `utils/earlyInput.ts`：实现 early input 相关逻辑。
- `utils/editor.ts`：实现 editor 相关逻辑。
- `utils/effort.ts`：实现 effort 相关逻辑。
- `utils/embeddedTools.ts`：实现 embedded tools 相关逻辑。
- `utils/env.ts`：实现 env 相关逻辑。
- `utils/envDynamic.ts`：实现 env dynamic 相关逻辑。
- `utils/envUtils.ts`：存放该模块的通用工具函数。
- `utils/envValidation.ts`：实现 env validation 相关逻辑。
- `utils/errorLogSink.ts`：实现 error log sink 相关逻辑。
- `utils/errors.ts`：实现 errors 相关逻辑。
- `utils/exampleCommands.ts`：实现 example commands 相关逻辑。
- `utils/execFileNoThrow.ts`：实现 exec file no throw 相关逻辑。
- `utils/execFileNoThrowPortable.ts`：实现 exec file no throw portable 相关逻辑。
- `utils/execSyncWrapper.ts`：实现 exec sync wrapper 相关逻辑。
- `utils/exportRenderer.tsx`：处理渲染过程、渲染参数或渲染辅助逻辑。
- `utils/extraUsage.ts`：实现 extra usage 相关逻辑。
- `utils/fastMode.ts`：实现 fast mode 相关逻辑。
- `utils/file.ts`：实现 file 相关逻辑。
- `utils/fileHistory.ts`：处理历史记录、会话历史或历史状态。
- `utils/fileOperationAnalytics.ts`：处理埋点、实验、指标或统计分析。
- `utils/fileRead.ts`：实现 file read 相关逻辑。
- `utils/fileReadCache.ts`：实现 file read cache 相关逻辑。
- `utils/fileStateCache.ts`：实现 file state cache 相关逻辑。
- `utils/findExecutable.ts`：实现 find executable 相关逻辑。
- `utils/fingerprint.ts`：实现 fingerprint 相关逻辑。
- `utils/forkedAgent.ts`：处理代理、子代理或代理展示相关逻辑。
- `utils/format.ts`：实现 format 相关逻辑。
- `utils/formatBriefTimestamp.ts`：实现 format brief timestamp 相关逻辑。
- `utils/fpsTracker.ts`：实现 fps tracker 相关逻辑。
- `utils/frontmatterParser.ts`：实现 frontmatter parser 相关逻辑。
- `utils/fsOperations.ts`：实现 fs operations 相关逻辑。
- `utils/fullscreen.ts`：定义一个终端页面或主屏组件。
- `utils/generatedFiles.ts`：实现 generated files 相关逻辑。
- `utils/generators.ts`：实现 generators 相关逻辑。
- `utils/genericProcessUtils.ts`：存放该模块的通用工具函数。
- `utils/getWorktreePaths.ts`：实现 get worktree paths 相关逻辑。
- `utils/getWorktreePathsPortable.ts`：实现 get worktree paths portable 相关逻辑。
- `utils/ghPrStatus.ts`：实现 gh pr status 相关逻辑。
- `utils/git.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `utils/gitDiff.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `utils/githubRepoPathMapping.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `utils/gitSettings.ts`：处理设置读取、缓存、校验或写入。
- `utils/glob.ts`：实现 glob 相关逻辑。
- `utils/gracefulShutdown.ts`：实现 graceful shutdown 相关逻辑。
- `utils/groupToolUses.ts`：实现 group tool uses 相关逻辑。
- `utils/handlePromptSubmit.ts`：实现 handle prompt submit 相关逻辑。
- `utils/hash.ts`：实现 hash 相关逻辑。
- `utils/headlessProfiler.ts`：实现 headless profiler 相关逻辑。
- `utils/heapDumpService.ts`：实现 heap dump service 相关逻辑。
- `utils/heatmap.ts`：实现 heatmap 相关逻辑。
- `utils/highlightMatch.tsx`：定义 highlight match 相关界面或交互组件。
- `utils/hooks.ts`：实现 hooks 相关逻辑。
- `utils/horizontalScroll.ts`：实现 horizontal scroll 相关逻辑。
- `utils/http.ts`：实现 http 相关逻辑。
- `utils/hyperlink.ts`：实现 hyperlink 相关逻辑。
- `utils/ide.ts`：实现 ide 相关逻辑。
- `utils/idePathConversion.ts`：实现 ide path conversion 相关逻辑。
- `utils/idleTimeout.ts`：实现 idle timeout 相关逻辑。
- `utils/imagePaste.ts`：实现 image paste 相关逻辑。
- `utils/imageResizer.ts`：实现 image resizer 相关逻辑。
- `utils/imageStore.ts`：定义状态存储或状态容器逻辑。
- `utils/imageValidation.ts`：实现 image validation 相关逻辑。
- `utils/immediateCommand.ts`：定义一个具体命令的注册与执行逻辑。
- `utils/ink.ts`：实现 ink 相关逻辑。
- `utils/inProcessTeammateHelpers.ts`：存放该模块的辅助函数。
- `utils/intl.ts`：实现 intl 相关逻辑。
- `utils/iTermBackup.ts`：实现 i term backup 相关逻辑。
- `utils/jetbrains.ts`：实现 jetbrains 相关逻辑。
- `utils/json.ts`：实现 json 相关逻辑。
- `utils/jsonRead.ts`：实现 json read 相关逻辑。
- `utils/keyboardShortcuts.ts`：实现 keyboard shortcuts 相关逻辑。
- `utils/lazySchema.ts`：定义校验结构或数据 schema。
- `utils/listSessionsImpl.ts`：处理会话对象、会话恢复或会话同步。
- `utils/localInstaller.ts`：实现 local installer 相关逻辑。
- `utils/lockfile.ts`：实现 lockfile 相关逻辑。
- `utils/log.ts`：实现 log 相关逻辑。
- `utils/logoV2Utils.ts`：存放该模块的通用工具函数。
- `utils/mailbox.ts`：实现 mailbox 相关逻辑。
- `utils/managedEnv.ts`：实现 managed env 相关逻辑。
- `utils/managedEnvConstants.ts`：定义这一模块用到的常量。
- `utils/markdown.ts`：实现 markdown 相关逻辑。
- `utils/markdownConfigLoader.ts`：处理配置项、配置解析或配置结构。
- `utils/mcpInstructionsDelta.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `utils/mcpOutputStorage.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `utils/mcpValidation.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `utils/mcpWebSocketTransport.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `utils/memoize.ts`：实现 memoize 相关逻辑。
- `utils/memoryFileDetection.ts`：处理记忆读取、记忆提取或记忆组织。
- `utils/messagePredicates.ts`：处理消息结构、消息渲染或消息转换。
- `utils/messageQueueManager.ts`：负责管理该模块的生命周期或资源对象。
- `utils/messages.ts`：处理消息结构、消息渲染或消息转换。
- `utils/modelCost.ts`：处理模型选择、模型能力或模型字符串映射。
- `utils/modifiers.ts`：实现 modifiers 相关逻辑。
- `utils/mtls.ts`：实现 mtls 相关逻辑。
- `utils/notebook.ts`：实现 notebook 相关逻辑。
- `utils/objectGroupBy.ts`：实现 object group by 相关逻辑。
- `utils/pasteStore.ts`：定义状态存储或状态容器逻辑。
- `utils/path.ts`：实现 path 相关逻辑。
- `utils/pdf.ts`：实现 pdf 相关逻辑。
- `utils/pdfUtils.ts`：存放该模块的通用工具函数。
- `utils/peerAddress.ts`：实现 peer address 相关逻辑。
- `utils/planModeV2.ts`：实现 plan mode v2 相关逻辑。
- `utils/plans.ts`：实现 plans 相关逻辑。
- `utils/platform.ts`：实现 platform 相关逻辑。
- `utils/preflightChecks.tsx`：定义 preflight checks 相关界面或交互组件。
- `utils/privacyLevel.ts`：实现 privacy level 相关逻辑。
- `utils/process.ts`：实现 process 相关逻辑。
- `utils/profilerBase.ts`：实现 profiler base 相关逻辑。
- `utils/promptCategory.ts`：实现 prompt category 相关逻辑。
- `utils/promptEditor.ts`：实现 prompt editor 相关逻辑。
- `utils/promptShellExecution.ts`：实现 prompt shell execution 相关逻辑。
- `utils/proxy.ts`：实现 proxy 相关逻辑。
- `utils/queryContext.ts`：定义上下文对象或上下文获取逻辑。
- `utils/QueryGuard.ts`：实现 query guard 相关逻辑。
- `utils/queryHelpers.ts`：存放该模块的辅助函数。
- `utils/queryProfiler.ts`：实现 query profiler 相关逻辑。
- `utils/queueProcessor.ts`：实现 queue processor 相关逻辑。
- `utils/readEditContext.ts`：定义上下文对象或上下文获取逻辑。
- `utils/readFileInRange.ts`：实现 read file in range 相关逻辑。
- `utils/releaseNotes.ts`：实现 release notes 相关逻辑。
- `utils/renderOptions.ts`：处理渲染过程、渲染参数或渲染辅助逻辑。
- `utils/ripgrep.ts`：实现 ripgrep 相关逻辑。
- `utils/sanitization.ts`：实现 sanitization 相关逻辑。
- `utils/screenshotClipboard.ts`：实现 screenshot clipboard 相关逻辑。
- `utils/sdkEventQueue.ts`：实现 sdk event queue 相关逻辑。
- `utils/semanticBoolean.ts`：实现 semantic boolean 相关逻辑。
- `utils/semanticNumber.ts`：实现 semantic number 相关逻辑。
- `utils/semver.ts`：实现 semver 相关逻辑。
- `utils/sequential.ts`：实现 sequential 相关逻辑。
- `utils/sessionActivity.ts`：处理会话对象、会话恢复或会话同步。
- `utils/sessionEnvironment.ts`：处理会话对象、会话恢复或会话同步。
- `utils/sessionEnvVars.ts`：处理会话对象、会话恢复或会话同步。
- `utils/sessionFileAccessHooks.ts`：处理会话对象、会话恢复或会话同步。
- `utils/sessionIngressAuth.ts`：处理会话对象、会话恢复或会话同步。
- `utils/sessionRestore.ts`：定义状态存储或状态容器逻辑。
- `utils/sessionStart.ts`：处理会话对象、会话恢复或会话同步。
- `utils/sessionState.ts`：处理会话对象、会话恢复或会话同步。
- `utils/sessionStorage.ts`：处理会话对象、会话恢复或会话同步。
- `utils/sessionStoragePortable.ts`：处理会话对象、会话恢复或会话同步。
- `utils/sessionTitle.ts`：处理会话对象、会话恢复或会话同步。
- `utils/sessionUrl.ts`：处理会话对象、会话恢复或会话同步。
- `utils/set.ts`：实现 set 相关逻辑。
- `utils/Shell.ts`：实现 shell 相关逻辑。
- `utils/ShellCommand.ts`：定义一个具体命令的注册与执行逻辑。
- `utils/shellConfig.ts`：处理配置项、配置解析或配置结构。
- `utils/sideQuery.ts`：实现 side query 相关逻辑。
- `utils/sideQuestion.ts`：实现 side question 相关逻辑。
- `utils/signal.ts`：实现 signal 相关逻辑。
- `utils/sinks.ts`：实现 sinks 相关逻辑。
- `utils/slashCommandParsing.ts`：实现 slash command parsing 相关逻辑。
- `utils/sleep.ts`：实现 sleep 相关逻辑。
- `utils/sliceAnsi.ts`：实现 slice ansi 相关逻辑。
- `utils/slowOperations.ts`：实现 slow operations 相关逻辑。
- `utils/standaloneAgent.ts`：处理代理、子代理或代理展示相关逻辑。
- `utils/startupProfiler.ts`：实现 startup profiler 相关逻辑。
- `utils/staticRender.tsx`：处理渲染过程、渲染参数或渲染辅助逻辑。
- `utils/stats.ts`：实现 stats 相关逻辑。
- `utils/statsCache.ts`：实现 stats cache 相关逻辑。
- `utils/status.tsx`：定义 status 相关界面或交互组件。
- `utils/statusNoticeDefinitions.tsx`：定义 status notice definitions 相关界面或交互组件。
- `utils/statusNoticeHelpers.ts`：存放该模块的辅助函数。
- `utils/stream.ts`：实现 stream 相关逻辑。
- `utils/streamJsonStdoutGuard.ts`：实现 stream json stdout guard 相关逻辑。
- `utils/streamlinedTransform.ts`：实现 streamlined transform 相关逻辑。
- `utils/stringUtils.ts`：存放该模块的通用工具函数。
- `utils/subprocessEnv.ts`：实现 subprocess env 相关逻辑。
- `utils/systemDirectories.ts`：实现 system directories 相关逻辑。
- `utils/systemPrompt.ts`：定义提示词、说明文本或模型提示模板。
- `utils/systemPromptType.ts`：定义这一模块相关的共享类型或结构。
- `utils/systemTheme.ts`：处理主题、颜色或样式切换。
- `utils/taggedId.ts`：实现 tagged id 相关逻辑。
- `utils/tasks.ts`：处理任务对象、任务状态或任务执行流程。
- `utils/teamDiscovery.ts`：实现 team discovery 相关逻辑。
- `utils/teammate.ts`：实现 teammate 相关逻辑。
- `utils/teammateContext.ts`：定义上下文对象或上下文获取逻辑。
- `utils/teammateMailbox.ts`：实现 teammate mailbox 相关逻辑。
- `utils/teamMemoryOps.ts`：处理记忆读取、记忆提取或记忆组织。
- `utils/telemetryAttributes.ts`：实现 telemetry attributes 相关逻辑。
- `utils/teleport.tsx`：处理远程传送、远端恢复或远端会话切换。
- `utils/tempfile.ts`：实现 tempfile 相关逻辑。
- `utils/terminal.ts`：实现 terminal 相关逻辑。
- `utils/terminalPanel.ts`：实现 terminal panel 相关逻辑。
- `utils/textHighlighting.ts`：实现 text highlighting 相关逻辑。
- `utils/theme.ts`：处理主题、颜色或样式切换。
- `utils/thinking.ts`：实现 thinking 相关逻辑。
- `utils/timeouts.ts`：实现 timeouts 相关逻辑。
- `utils/tmuxSocket.ts`：实现 tmux socket 相关逻辑。
- `utils/tokenBudget.ts`：实现 token budget 相关逻辑。
- `utils/tokens.ts`：实现 tokens 相关逻辑。
- `utils/toolErrors.ts`：实现 tool errors 相关逻辑。
- `utils/toolPool.ts`：实现 tool pool 相关逻辑。
- `utils/toolResultStorage.ts`：实现 tool result storage 相关逻辑。
- `utils/toolSchemaCache.ts`：定义校验结构或数据 schema。
- `utils/toolSearch.ts`：实现 tool search 相关逻辑。
- `utils/transcriptSearch.ts`：实现 transcript search 相关逻辑。
- `utils/treeify.ts`：实现 treeify 相关逻辑。
- `utils/truncate.ts`：实现 truncate 相关逻辑。
- `utils/unaryLogging.ts`：实现 unary logging 相关逻辑。
- `utils/undercover.ts`：实现 undercover 相关逻辑。
- `utils/user.ts`：实现 user 相关逻辑。
- `utils/userAgent.ts`：处理代理、子代理或代理展示相关逻辑。
- `utils/userPromptKeywords.ts`：实现 user prompt keywords 相关逻辑。
- `utils/uuid.ts`：实现 uuid 相关逻辑。
- `utils/warningHandler.ts`：实现 warning handler 相关逻辑。
- `utils/which.ts`：实现 which 相关逻辑。
- `utils/windowsPaths.ts`：实现 windows paths 相关逻辑。
- `utils/withResolvers.ts`：实现 with resolvers 相关逻辑。
- `utils/words.ts`：实现 words 相关逻辑。
- `utils/workloadContext.ts`：定义上下文对象或上下文获取逻辑。
- `utils/worktree.ts`：实现 worktree 相关逻辑。
- `utils/worktreeModeEnabled.ts`：实现 worktree mode enabled 相关逻辑。
- `utils/xdg.ts`：实现 xdg 相关逻辑。
- `utils/xml.ts`：实现 xml 相关逻辑。
- `utils/yaml.ts`：实现 yaml 相关逻辑。
- `utils/zodToJsonSchema.ts`：定义校验结构或数据 schema。

## 目录：`utils/background/remote`

- 文件数：2
- 目录作用：这一目录聚合了一组与 remote 相关的实现。

- `utils/background/remote/preconditions.ts`：提供 preconditions 相关的通用辅助能力。
- `utils/background/remote/remoteSession.ts`：处理会话对象、会话恢复或会话同步。

## 目录：`utils/bash`

- 文件数：15
- 目录作用：这一目录聚合了一组与 bash 相关的实现。

- `utils/bash/ast.ts`：提供 ast 相关的通用辅助能力。
- `utils/bash/bashParser.ts`：处理 bash 命令构造、解析或执行规则。
- `utils/bash/bashPipeCommand.ts`：定义一个具体命令的注册与执行逻辑。
- `utils/bash/commands.ts`：提供 commands 相关的通用辅助能力。
- `utils/bash/heredoc.ts`：提供 heredoc 相关的通用辅助能力。
- `utils/bash/ParsedCommand.ts`：定义一个具体命令的注册与执行逻辑。
- `utils/bash/parser.ts`：提供 parser 相关的通用辅助能力。
- `utils/bash/prefix.ts`：提供 prefix 相关的通用辅助能力。
- `utils/bash/registry.ts`：提供 registry 相关的通用辅助能力。
- `utils/bash/shellCompletion.ts`：提供 shell completion 相关的通用辅助能力。
- `utils/bash/shellPrefix.ts`：提供 shell prefix 相关的通用辅助能力。
- `utils/bash/shellQuote.ts`：提供 shell quote 相关的通用辅助能力。
- `utils/bash/shellQuoting.ts`：提供 shell quoting 相关的通用辅助能力。
- `utils/bash/ShellSnapshot.ts`：提供 shell snapshot 相关的通用辅助能力。
- `utils/bash/treeSitterAnalysis.ts`：提供 tree sitter analysis 相关的通用辅助能力。

## 目录：`utils/bash/specs`

- 文件数：8
- 目录作用：这一目录聚合了一组与 specs 相关的实现。

- `utils/bash/specs/alias.ts`：提供 alias 相关的通用辅助能力。
- `utils/bash/specs/index.ts`：该目录的导出入口或聚合入口。
- `utils/bash/specs/nohup.ts`：提供 nohup 相关的通用辅助能力。
- `utils/bash/specs/pyright.ts`：提供 pyright 相关的通用辅助能力。
- `utils/bash/specs/sleep.ts`：提供 sleep 相关的通用辅助能力。
- `utils/bash/specs/srun.ts`：提供 srun 相关的通用辅助能力。
- `utils/bash/specs/time.ts`：提供 time 相关的通用辅助能力。
- `utils/bash/specs/timeout.ts`：提供 timeout 相关的通用辅助能力。

## 目录：`utils/claudeInChrome`

- 文件数：7
- 目录作用：这一目录聚合了一组与 claudeInChrome 相关的实现。

- `utils/claudeInChrome/chromeNativeHost.ts`：提供 chrome native host 相关的通用辅助能力。
- `utils/claudeInChrome/common.ts`：提供 common 相关的通用辅助能力。
- `utils/claudeInChrome/mcpServer.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `utils/claudeInChrome/prompt.ts`：定义提示词、说明文本或模型提示模板。
- `utils/claudeInChrome/setup.ts`：提供 setup 相关的通用辅助能力。
- `utils/claudeInChrome/setupPortable.ts`：提供 setup portable 相关的通用辅助能力。
- `utils/claudeInChrome/toolRendering.tsx`：处理渲染过程、渲染参数或渲染辅助逻辑。

## 目录：`utils/computerUse`

- 文件数：15
- 目录作用：这一目录聚合了一组与 computerUse 相关的实现。

- `utils/computerUse/appNames.ts`：提供 app names 相关的通用辅助能力。
- `utils/computerUse/cleanup.ts`：提供 cleanup 相关的通用辅助能力。
- `utils/computerUse/common.ts`：提供 common 相关的通用辅助能力。
- `utils/computerUse/computerUseLock.ts`：提供 computer use lock 相关的通用辅助能力。
- `utils/computerUse/drainRunLoop.ts`：提供 drain run loop 相关的通用辅助能力。
- `utils/computerUse/escHotkey.ts`：提供 esc hotkey 相关的通用辅助能力。
- `utils/computerUse/executor.ts`：提供 executor 相关的通用辅助能力。
- `utils/computerUse/gates.ts`：提供 gates 相关的通用辅助能力。
- `utils/computerUse/hostAdapter.ts`：提供 host adapter 相关的通用辅助能力。
- `utils/computerUse/inputLoader.ts`：提供 input loader 相关的通用辅助能力。
- `utils/computerUse/mcpServer.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `utils/computerUse/setup.ts`：提供 setup 相关的通用辅助能力。
- `utils/computerUse/swiftLoader.ts`：提供 swift loader 相关的通用辅助能力。
- `utils/computerUse/toolRendering.tsx`：处理渲染过程、渲染参数或渲染辅助逻辑。
- `utils/computerUse/wrapper.tsx`：提供 wrapper 相关的通用辅助能力。

## 目录：`utils/deepLink`

- 文件数：6
- 目录作用：这一目录聚合了一组与 deepLink 相关的实现。

- `utils/deepLink/banner.ts`：提供 banner 相关的通用辅助能力。
- `utils/deepLink/parseDeepLink.ts`：提供 parse deep link 相关的通用辅助能力。
- `utils/deepLink/protocolHandler.ts`：提供 protocol handler 相关的通用辅助能力。
- `utils/deepLink/registerProtocol.ts`：提供 register protocol 相关的通用辅助能力。
- `utils/deepLink/terminalLauncher.ts`：负责启动对应模式、界面或流程。
- `utils/deepLink/terminalPreference.ts`：提供 terminal preference 相关的通用辅助能力。

## 目录：`utils/dxt`

- 文件数：2
- 目录作用：这一目录聚合了一组与 dxt 相关的实现。

- `utils/dxt/helpers.ts`：存放该模块的辅助函数。
- `utils/dxt/zip.ts`：提供 zip 相关的通用辅助能力。

## 目录：`utils/filePersistence`

- 文件数：2
- 目录作用：这一目录聚合了一组与 filePersistence 相关的实现。

- `utils/filePersistence/filePersistence.ts`：提供 file persistence 相关的通用辅助能力。
- `utils/filePersistence/outputsScanner.ts`：提供 outputs scanner 相关的通用辅助能力。

## 目录：`utils/git`

- 文件数：3
- 目录作用：这一目录聚合了一组与 git 相关的实现。

- `utils/git/gitConfigParser.ts`：处理配置项、配置解析或配置结构。
- `utils/git/gitFilesystem.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `utils/git/gitignore.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。

## 目录：`utils/github`

- 文件数：1
- 目录作用：这一目录聚合了一组与 github 相关的实现。

- `utils/github/ghAuthStatus.ts`：提供 gh auth status 相关的通用辅助能力。

## 目录：`utils/hooks`

- 文件数：17
- 目录作用：这一目录聚合了一组与 hooks 相关的实现。

- `utils/hooks/apiQueryHookHelper.ts`：存放该模块的辅助函数。
- `utils/hooks/AsyncHookRegistry.ts`：提供 async hook registry 相关的通用辅助能力。
- `utils/hooks/execAgentHook.ts`：实现单个 hook。
- `utils/hooks/execHttpHook.ts`：实现单个 hook。
- `utils/hooks/execPromptHook.ts`：实现单个 hook。
- `utils/hooks/fileChangedWatcher.ts`：提供 file changed watcher 相关的通用辅助能力。
- `utils/hooks/hookEvents.ts`：提供 hook events 相关的通用辅助能力。
- `utils/hooks/hookHelpers.ts`：存放该模块的辅助函数。
- `utils/hooks/hooksConfigManager.ts`：负责管理该模块的生命周期或资源对象。
- `utils/hooks/hooksConfigSnapshot.ts`：处理配置项、配置解析或配置结构。
- `utils/hooks/hooksSettings.ts`：处理设置读取、缓存、校验或写入。
- `utils/hooks/postSamplingHooks.ts`：提供 post sampling hooks 相关的通用辅助能力。
- `utils/hooks/registerFrontmatterHooks.ts`：提供 register frontmatter hooks 相关的通用辅助能力。
- `utils/hooks/registerSkillHooks.ts`：处理技能加载、索引、解析或技能运行支持。
- `utils/hooks/sessionHooks.ts`：处理会话对象、会话恢复或会话同步。
- `utils/hooks/skillImprovement.ts`：处理技能加载、索引、解析或技能运行支持。
- `utils/hooks/ssrfGuard.ts`：提供 ssrf guard 相关的通用辅助能力。

## 目录：`utils/mcp`

- 文件数：2
- 目录作用：这一目录聚合了一组与 mcp 相关的实现。

- `utils/mcp/dateTimeParser.ts`：提供 date time parser 相关的通用辅助能力。
- `utils/mcp/elicitationValidation.ts`：提供 elicitation validation 相关的通用辅助能力。

## 目录：`utils/memory`

- 文件数：2
- 目录作用：这一目录聚合了一组与 memory 相关的实现。

- `utils/memory/types.ts`：定义这一模块相关的共享类型或结构。
- `utils/memory/versions.ts`：提供 versions 相关的通用辅助能力。

## 目录：`utils/messages`

- 文件数：2
- 目录作用：这一目录聚合了一组与 messages 相关的实现。

- `utils/messages/mappers.ts`：提供 mappers 相关的通用辅助能力。
- `utils/messages/systemInit.ts`：提供 system init 相关的通用辅助能力。

## 目录：`utils/model`

- 文件数：16
- 目录作用：这一目录聚合了一组与 model 相关的实现。

- `utils/model/agent.ts`：处理代理、子代理或代理展示相关逻辑。
- `utils/model/aliases.ts`：提供 aliases 相关的通用辅助能力。
- `utils/model/antModels.ts`：处理模型选择、模型能力或模型字符串映射。
- `utils/model/bedrock.ts`：提供 bedrock 相关的通用辅助能力。
- `utils/model/check1mAccess.ts`：提供 check1m access 相关的通用辅助能力。
- `utils/model/configs.ts`：处理配置项、配置解析或配置结构。
- `utils/model/contextWindowUpgradeCheck.ts`：提供 context window upgrade check 相关的通用辅助能力。
- `utils/model/deprecation.ts`：提供 deprecation 相关的通用辅助能力。
- `utils/model/model.ts`：处理模型选择、模型能力或模型字符串映射。
- `utils/model/modelAllowlist.ts`：处理模型选择、模型能力或模型字符串映射。
- `utils/model/modelCapabilities.ts`：处理模型选择、模型能力或模型字符串映射。
- `utils/model/modelOptions.ts`：处理模型选择、模型能力或模型字符串映射。
- `utils/model/modelStrings.ts`：处理模型选择、模型能力或模型字符串映射。
- `utils/model/modelSupportOverrides.ts`：处理模型选择、模型能力或模型字符串映射。
- `utils/model/providers.ts`：提供 providers 相关的通用辅助能力。
- `utils/model/validateModel.ts`：处理模型选择、模型能力或模型字符串映射。

## 目录：`utils/nativeInstaller`

- 文件数：5
- 目录作用：这一目录聚合了一组与 nativeInstaller 相关的实现。

- `utils/nativeInstaller/download.ts`：提供 download 相关的通用辅助能力。
- `utils/nativeInstaller/index.ts`：该目录的导出入口或聚合入口。
- `utils/nativeInstaller/installer.ts`：提供 installer 相关的通用辅助能力。
- `utils/nativeInstaller/packageManagers.ts`：提供 package managers 相关的通用辅助能力。
- `utils/nativeInstaller/pidLock.ts`：提供 pid lock 相关的通用辅助能力。

## 目录：`utils/permissions`

- 文件数：24
- 目录作用：这一目录聚合了一组与 permissions 相关的实现。

- `utils/permissions/autoModeState.ts`：提供 auto mode state 相关的通用辅助能力。
- `utils/permissions/bashClassifier.ts`：处理 bash 命令构造、解析或执行规则。
- `utils/permissions/bypassPermissionsKillswitch.ts`：处理权限检查、权限请求或权限规则。
- `utils/permissions/classifierDecision.ts`：提供 classifier decision 相关的通用辅助能力。
- `utils/permissions/classifierShared.ts`：提供 classifier shared 相关的通用辅助能力。
- `utils/permissions/dangerousPatterns.ts`：提供 dangerous patterns 相关的通用辅助能力。
- `utils/permissions/denialTracking.ts`：提供 denial tracking 相关的通用辅助能力。
- `utils/permissions/filesystem.ts`：提供 filesystem 相关的通用辅助能力。
- `utils/permissions/getNextPermissionMode.ts`：处理权限检查、权限请求或权限规则。
- `utils/permissions/pathValidation.ts`：提供 path validation 相关的通用辅助能力。
- `utils/permissions/permissionExplainer.ts`：处理权限检查、权限请求或权限规则。
- `utils/permissions/PermissionMode.ts`：处理权限检查、权限请求或权限规则。
- `utils/permissions/PermissionPromptToolResultSchema.ts`：定义校验结构或数据 schema。
- `utils/permissions/PermissionResult.ts`：处理权限检查、权限请求或权限规则。
- `utils/permissions/PermissionRule.ts`：处理权限检查、权限请求或权限规则。
- `utils/permissions/permissionRuleParser.ts`：处理权限检查、权限请求或权限规则。
- `utils/permissions/permissions.ts`：处理权限检查、权限请求或权限规则。
- `utils/permissions/permissionSetup.ts`：处理权限检查、权限请求或权限规则。
- `utils/permissions/permissionsLoader.ts`：处理权限检查、权限请求或权限规则。
- `utils/permissions/PermissionUpdate.ts`：处理权限检查、权限请求或权限规则。
- `utils/permissions/PermissionUpdateSchema.ts`：定义校验结构或数据 schema。
- `utils/permissions/shadowedRuleDetection.ts`：提供 shadowed rule detection 相关的通用辅助能力。
- `utils/permissions/shellRuleMatching.ts`：提供 shell rule matching 相关的通用辅助能力。
- `utils/permissions/yoloClassifier.ts`：提供 yolo classifier 相关的通用辅助能力。

## 目录：`utils/plugins`

- 文件数：44
- 目录作用：这一目录聚合了一组与 plugins 相关的实现。

- `utils/plugins/addDirPluginSettings.ts`：处理设置读取、缓存、校验或写入。
- `utils/plugins/cacheUtils.ts`：存放该模块的通用工具函数。
- `utils/plugins/dependencyResolver.ts`：提供 dependency resolver 相关的通用辅助能力。
- `utils/plugins/fetchTelemetry.ts`：提供 fetch telemetry 相关的通用辅助能力。
- `utils/plugins/gitAvailability.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。
- `utils/plugins/headlessPluginInstall.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/hintRecommendation.ts`：提供 hint recommendation 相关的通用辅助能力。
- `utils/plugins/installCounts.ts`：提供 install counts 相关的通用辅助能力。
- `utils/plugins/installedPluginsManager.ts`：负责管理该模块的生命周期或资源对象。
- `utils/plugins/loadPluginAgents.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/loadPluginCommands.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/loadPluginHooks.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/loadPluginOutputStyles.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/lspPluginIntegration.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/lspRecommendation.ts`：提供 lsp recommendation 相关的通用辅助能力。
- `utils/plugins/managedPlugins.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/marketplaceHelpers.ts`：存放该模块的辅助函数。
- `utils/plugins/marketplaceManager.ts`：负责管理该模块的生命周期或资源对象。
- `utils/plugins/mcpbHandler.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `utils/plugins/mcpPluginIntegration.ts`：处理 MCP 协议、MCP 资源或 MCP 服务器对接。
- `utils/plugins/officialMarketplace.ts`：提供 official marketplace 相关的通用辅助能力。
- `utils/plugins/officialMarketplaceGcs.ts`：提供 official marketplace gcs 相关的通用辅助能力。
- `utils/plugins/officialMarketplaceStartupCheck.ts`：提供 official marketplace startup check 相关的通用辅助能力。
- `utils/plugins/orphanedPluginFilter.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/parseMarketplaceInput.ts`：提供 parse marketplace input 相关的通用辅助能力。
- `utils/plugins/performStartupChecks.tsx`：提供 perform startup checks 相关的通用辅助能力。
- `utils/plugins/pluginAutoupdate.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/pluginBlocklist.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/pluginDirectories.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/pluginFlagging.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/pluginIdentifier.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/pluginInstallationHelpers.ts`：存放该模块的辅助函数。
- `utils/plugins/pluginLoader.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/pluginOptionsStorage.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/pluginPolicy.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/pluginStartupCheck.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/pluginVersioning.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/reconciler.ts`：提供 reconciler 相关的通用辅助能力。
- `utils/plugins/refresh.ts`：提供 refresh 相关的通用辅助能力。
- `utils/plugins/schemas.ts`：定义校验结构或数据 schema。
- `utils/plugins/validatePlugin.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/walkPluginMarkdown.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/plugins/zipCache.ts`：提供 zip cache 相关的通用辅助能力。
- `utils/plugins/zipCacheAdapters.ts`：提供 zip cache adapters 相关的通用辅助能力。

## 目录：`utils/powershell`

- 文件数：3
- 目录作用：这一目录聚合了一组与 powershell 相关的实现。

- `utils/powershell/dangerousCmdlets.ts`：提供 dangerous cmdlets 相关的通用辅助能力。
- `utils/powershell/parser.ts`：提供 parser 相关的通用辅助能力。
- `utils/powershell/staticPrefix.ts`：提供 static prefix 相关的通用辅助能力。

## 目录：`utils/processUserInput`

- 文件数：4
- 目录作用：这一目录聚合了一组与 processUserInput 相关的实现。

- `utils/processUserInput/processBashCommand.tsx`：定义一个具体命令的注册与执行逻辑。
- `utils/processUserInput/processSlashCommand.tsx`：定义一个具体命令的注册与执行逻辑。
- `utils/processUserInput/processTextPrompt.ts`：定义提示词、说明文本或模型提示模板。
- `utils/processUserInput/processUserInput.ts`：提供 process user input 相关的通用辅助能力。

## 目录：`utils/sandbox`

- 文件数：2
- 目录作用：这一目录聚合了一组与 sandbox 相关的实现。

- `utils/sandbox/sandbox-adapter.ts`：处理沙箱模式、沙箱权限或沙箱桥接。
- `utils/sandbox/sandbox-ui-utils.ts`：存放该模块的通用工具函数。

## 目录：`utils/secureStorage`

- 文件数：6
- 目录作用：这一目录聚合了一组与 secureStorage 相关的实现。

- `utils/secureStorage/fallbackStorage.ts`：提供 fallback storage 相关的通用辅助能力。
- `utils/secureStorage/index.ts`：该目录的导出入口或聚合入口。
- `utils/secureStorage/keychainPrefetch.ts`：提供 keychain prefetch 相关的通用辅助能力。
- `utils/secureStorage/macOsKeychainHelpers.ts`：存放该模块的辅助函数。
- `utils/secureStorage/macOsKeychainStorage.ts`：提供 mac os keychain storage 相关的通用辅助能力。
- `utils/secureStorage/plainTextStorage.ts`：提供 plain text storage 相关的通用辅助能力。

## 目录：`utils/settings`

- 文件数：16
- 目录作用：这一目录聚合了一组与 settings 相关的实现。

- `utils/settings/allErrors.ts`：提供 all errors 相关的通用辅助能力。
- `utils/settings/applySettingsChange.ts`：处理设置读取、缓存、校验或写入。
- `utils/settings/changeDetector.ts`：提供 change detector 相关的通用辅助能力。
- `utils/settings/constants.ts`：定义这一模块用到的常量。
- `utils/settings/internalWrites.ts`：提供 internal writes 相关的通用辅助能力。
- `utils/settings/managedPath.ts`：提供 managed path 相关的通用辅助能力。
- `utils/settings/permissionValidation.ts`：处理权限检查、权限请求或权限规则。
- `utils/settings/pluginOnlyPolicy.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/settings/schemaOutput.ts`：定义校验结构或数据 schema。
- `utils/settings/settings.ts`：处理设置读取、缓存、校验或写入。
- `utils/settings/settingsCache.ts`：处理设置读取、缓存、校验或写入。
- `utils/settings/toolValidationConfig.ts`：处理配置项、配置解析或配置结构。
- `utils/settings/types.ts`：定义这一模块相关的共享类型或结构。
- `utils/settings/validateEditTool.ts`：定义一个具体工具的能力、输入输出和执行逻辑。
- `utils/settings/validation.ts`：提供 validation 相关的通用辅助能力。
- `utils/settings/validationTips.ts`：提供 validation tips 相关的通用辅助能力。

## 目录：`utils/settings/mdm`

- 文件数：3
- 目录作用：这一目录聚合了一组与 mdm 相关的实现。

- `utils/settings/mdm/constants.ts`：定义这一模块用到的常量。
- `utils/settings/mdm/rawRead.ts`：提供 raw read 相关的通用辅助能力。
- `utils/settings/mdm/settings.ts`：处理设置读取、缓存、校验或写入。

## 目录：`utils/shell`

- 文件数：10
- 目录作用：这一目录聚合了一组与 shell 相关的实现。

- `utils/shell/bashProvider.ts`：提供上下文、依赖注入或统一 provider 封装。
- `utils/shell/outputLimits.ts`：提供 output limits 相关的通用辅助能力。
- `utils/shell/powershellDetection.ts`：处理 PowerShell 命令或权限规则。
- `utils/shell/powershellProvider.ts`：提供上下文、依赖注入或统一 provider 封装。
- `utils/shell/prefix.ts`：提供 prefix 相关的通用辅助能力。
- `utils/shell/readOnlyCommandValidation.ts`：提供 read only command validation 相关的通用辅助能力。
- `utils/shell/resolveDefaultShell.ts`：提供 resolve default shell 相关的通用辅助能力。
- `utils/shell/shellProvider.ts`：提供上下文、依赖注入或统一 provider 封装。
- `utils/shell/shellToolUtils.ts`：存放该模块的通用工具函数。
- `utils/shell/specPrefix.ts`：提供 spec prefix 相关的通用辅助能力。

## 目录：`utils/skills`

- 文件数：1
- 目录作用：这一目录聚合了一组与 skills 相关的实现。

- `utils/skills/skillChangeDetector.ts`：处理技能加载、索引、解析或技能运行支持。

## 目录：`utils/suggestions`

- 文件数：5
- 目录作用：这一目录聚合了一组与 suggestions 相关的实现。

- `utils/suggestions/commandSuggestions.ts`：提供 command suggestions 相关的通用辅助能力。
- `utils/suggestions/directoryCompletion.ts`：提供 directory completion 相关的通用辅助能力。
- `utils/suggestions/shellHistoryCompletion.ts`：处理历史记录、会话历史或历史状态。
- `utils/suggestions/skillUsageTracking.ts`：处理技能加载、索引、解析或技能运行支持。
- `utils/suggestions/slackChannelSuggestions.ts`：提供 slack channel suggestions 相关的通用辅助能力。

## 目录：`utils/swarm`

- 文件数：13
- 目录作用：这一目录聚合了一组与 swarm 相关的实现。

- `utils/swarm/constants.ts`：定义这一模块用到的常量。
- `utils/swarm/inProcessRunner.ts`：提供 in process runner 相关的通用辅助能力。
- `utils/swarm/It2SetupPrompt.tsx`：定义提示词、说明文本或模型提示模板。
- `utils/swarm/leaderPermissionBridge.ts`：处理权限检查、权限请求或权限规则。
- `utils/swarm/permissionSync.ts`：处理权限检查、权限请求或权限规则。
- `utils/swarm/reconnection.ts`：提供 reconnection 相关的通用辅助能力。
- `utils/swarm/spawnInProcess.ts`：提供 spawn in process 相关的通用辅助能力。
- `utils/swarm/spawnUtils.ts`：存放该模块的通用工具函数。
- `utils/swarm/teamHelpers.ts`：存放该模块的辅助函数。
- `utils/swarm/teammateInit.ts`：提供 teammate init 相关的通用辅助能力。
- `utils/swarm/teammateLayoutManager.ts`：负责管理该模块的生命周期或资源对象。
- `utils/swarm/teammateModel.ts`：处理模型选择、模型能力或模型字符串映射。
- `utils/swarm/teammatePromptAddendum.ts`：提供 teammate prompt addendum 相关的通用辅助能力。

## 目录：`utils/swarm/backends`

- 文件数：9
- 目录作用：这一目录聚合了一组与 backends 相关的实现。

- `utils/swarm/backends/detection.ts`：提供 detection 相关的通用辅助能力。
- `utils/swarm/backends/InProcessBackend.ts`：提供 in process backend 相关的通用辅助能力。
- `utils/swarm/backends/it2Setup.ts`：提供 it2 setup 相关的通用辅助能力。
- `utils/swarm/backends/ITermBackend.ts`：提供 iterm backend 相关的通用辅助能力。
- `utils/swarm/backends/PaneBackendExecutor.ts`：提供 pane backend executor 相关的通用辅助能力。
- `utils/swarm/backends/registry.ts`：提供 registry 相关的通用辅助能力。
- `utils/swarm/backends/teammateModeSnapshot.ts`：提供 teammate mode snapshot 相关的通用辅助能力。
- `utils/swarm/backends/TmuxBackend.ts`：提供 tmux backend 相关的通用辅助能力。
- `utils/swarm/backends/types.ts`：定义这一模块相关的共享类型或结构。

## 目录：`utils/task`

- 文件数：5
- 目录作用：这一目录聚合了一组与 task 相关的实现。

- `utils/task/diskOutput.ts`：提供 disk output 相关的通用辅助能力。
- `utils/task/framework.ts`：提供 framework 相关的通用辅助能力。
- `utils/task/outputFormatting.ts`：提供 output formatting 相关的通用辅助能力。
- `utils/task/sdkProgress.ts`：提供 sdk progress 相关的通用辅助能力。
- `utils/task/TaskOutput.ts`：处理任务对象、任务状态或任务执行流程。

## 目录：`utils/telemetry`

- 文件数：9
- 目录作用：这一目录聚合了一组与 telemetry 相关的实现。

- `utils/telemetry/betaSessionTracing.ts`：处理会话对象、会话恢复或会话同步。
- `utils/telemetry/bigqueryExporter.ts`：提供 bigquery exporter 相关的通用辅助能力。
- `utils/telemetry/events.ts`：提供 events 相关的通用辅助能力。
- `utils/telemetry/instrumentation.ts`：提供 instrumentation 相关的通用辅助能力。
- `utils/telemetry/logger.ts`：提供 logger 相关的通用辅助能力。
- `utils/telemetry/perfettoTracing.ts`：提供 perfetto tracing 相关的通用辅助能力。
- `utils/telemetry/pluginTelemetry.ts`：处理插件发现、加载、缓存或插件命令。
- `utils/telemetry/sessionTracing.ts`：处理会话对象、会话恢复或会话同步。
- `utils/telemetry/skillLoadedEvent.ts`：处理技能加载、索引、解析或技能运行支持。

## 目录：`utils/teleport`

- 文件数：4
- 目录作用：这一目录聚合了一组与 teleport 相关的实现。

- `utils/teleport/api.ts`：提供 api 相关的通用辅助能力。
- `utils/teleport/environments.ts`：提供 environments 相关的通用辅助能力。
- `utils/teleport/environmentSelection.ts`：提供 environment selection 相关的通用辅助能力。
- `utils/teleport/gitBundle.ts`：处理 Git 仓库、分支、ignore 或 Git 配置。

## 目录：`utils/todo`

- 文件数：1
- 目录作用：这一目录聚合了一组与 todo 相关的实现。

- `utils/todo/types.ts`：定义这一模块相关的共享类型或结构。

## 目录：`utils/ultraplan`

- 文件数：2
- 目录作用：这一目录聚合了一组与 ultraplan 相关的实现。

- `utils/ultraplan/ccrSession.ts`：处理会话对象、会话恢复或会话同步。
- `utils/ultraplan/keyword.ts`：提供 keyword 相关的通用辅助能力。

## 目录：`vim`

- 文件数：5
- 目录作用：vim 风格操作和文本对象。

- `vim/motions.ts`：实现 motions 相关逻辑。
- `vim/operators.ts`：实现 operators 相关逻辑。
- `vim/textObjects.ts`：实现 text objects 相关逻辑。
- `vim/transitions.ts`：实现 transitions 相关逻辑。
- `vim/types.ts`：定义这一模块相关的共享类型或结构。

## 目录：`voice`

- 文件数：1
- 目录作用：语音模式开关与支持逻辑。

- `voice/voiceModeEnabled.ts`：实现 voice mode enabled 相关逻辑。
