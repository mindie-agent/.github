# 参与贡献（Contributing to MindIE Agent）

[English](CONTRIBUTING.en.md)

欢迎参与 MindIE Agent 开源社区建设！为了让你的 Issue 或 Pull Request 得到最快响应，请根据改动所属的功能模块，提交到对应的仓库：

## 仓库职责速查表

| 你想贡献或修改的内容 | 请提交到该仓库 |
|---|---|
| 总体架构、工程设计原则、跨组件契约与统一版本记录 | [`mindie-agent`](https://github.com/mindie-agent/mindie-agent) |
| Claude Code 原生插件与 Hook 集成 | [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) |
| OpenAI Codex CLI 原生插件与 Hook 集成 | [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) |
| Kimi Code 原生适配插件与命令包装 | [`mindie-agent-kimi`](https://github.com/mindie-agent/mindie-agent-kimi) |
| 知识同步、本地经验检索、隐私脱敏与反馈引擎 | [`knowledge`](https://github.com/mindie-agent/knowledge) |
| `vLLM-Ascend` 公共工程知识包内容 | [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) |
| 昇腾推理工程独立 Agent Skills 精选目录 | [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) |
| `vllm` / `vllm-ascend` 本地多任务开发工作区脚手架 | [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) |
| SSH 远端文件工具、后台长作业、产物同步与 MCP 服务 | [`remote-dev`](https://github.com/mindie-agent/remote-dev) |
| 昇腾主机任务租约、就绪容器池与独占 NPU 调度服务 | [`coordinator`](https://github.com/mindie-agent/coordinator) |
| 昇腾 NPU 集群只读状态监控（TUI / Web / CLI / MCP） | [`npu-top`](https://github.com/mindie-agent/npu-top) |
| 结构化故障诊断、支持包导出与故障上报组件 | [`diagnostics`](https://github.com/mindie-agent/diagnostics) |

## 提交 Pull Request 的四条基本准则

1. **小步快跑，职责单一**：每个 PR 聚焦解决一个具体问题，并在描述中写明背景、改动点与验证方式。
2. **完成工程设计原则自查**：所有开发类 PR 在提交前请对照 [`docs/design-principles.md`](https://github.com/mindie-agent/mindie-agent/blob/main/docs/design-principles.md) 完成自查，并在 PR 描述中附上简明的 `## 设计原则 Review` 小结。
3. **严守隐私脱敏红线**：任何公开提交、知识包、测试样例或 PR 描述中，严禁包含密钥、Token、内网 IP、SSH 用户名/主机名、个人主目录路径或未脱敏的原始会话记录。
4. **尊重用户本地环境**：绝不篡改用户无关的全局配置、其他插件、MCP 服务或业务源码仓库。
