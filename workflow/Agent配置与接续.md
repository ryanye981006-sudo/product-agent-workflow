# Agent 配置与接续

## 角色配置

本框架提供 product 和 qa 两个 Codex 角色样例，安装到项目 `.codex/agents/`。配置样例采用 `[agents]`、`enabled` 和 `max_concurrent_threads_per_session`，并发上限为 2。角色文件采用 name、description 和 developer_instructions 字段。

主 Agent 统一执行与交付，product 集中解决业务与设计判断，qa 在完整交付阶段独立验收。模型、权限和工具沿用当前运行环境。

配置样例沿用来源项目的结构。目标客户端的配置支持和角色加载情况，以本机实际结果为准。

## 接续检查

1. 读取项目 AGENTS.md、PROJECT.md、PROJECT_STATUS.md 和 BACKLOG.md，按任务进入正式资料。
2. 检查 `.agent-workflow/` 的公共版本，以及 `.codex/agents/` 中的角色指令。
3. 合并项目配置时逐项检查已有设置，按客户端支持情况启用角色与并发设置。
4. 有适用的真实任务时，检查角色列表及实际派发结果。工具仅支持通用子任务时，传入完整角色指令、任务目标和项目入口。
5. 将角色加载、职责执行、环境和验证缺口登记到项目状态及对应待办。

## 验证范围

配置语法、文件引用、角色可见、实际派发、职责执行分别记录证据。完成静态检查后，继续用真实项目任务验证产品评审、独立验收、主 Agent 修复与接续过程。
