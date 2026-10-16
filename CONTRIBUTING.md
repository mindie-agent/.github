# 参与贡献（Contributing to MindIE Agent）

[English](CONTRIBUTING.en.md)

欢迎参与 MindIE Agent 开源生态建设！请根据改动所属的职责边界，将 Issue 或 Pull Request 提交至对应的所属仓库：

## 仓库职责边界

| 改动类型 | 所属仓库 |
|---|---|
| 总体架构、领域边界、九条设计原则、配套发布规范 | [`mindie-agent`](https://github.com/mindie-agent/mindie-agent) |
| OpenAI Codex CLI 插件集成与生命周期钩子 | [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) |
| Claude Code 插件集成与生命周期钩子 | [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) |
| Kimi Code 适配层与命令包装 | [`mindie-agent-kimi`](https://github.com/mindie-agent/mindie-agent-kimi) |
| 知识同步、本地经验检索、隐私脱敏与反馈运行时 | [`knowledge`](https://github.com/mindie-agent/knowledge) |
| `vLLM-Ascend` 公共工程知识包内容 | [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) |
| 昇腾推理工程独立 Agent Skills 精选目录 | [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) |
| `vllm` / `vllm-ascend` 本地开发工作区脚手架 | [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) |
| SSH 远端文件工具、后台作业、产物同步与 MCP 服务 | [`remote-dev`](https://github.com/mindie-agent/remote-dev) |
| 昇腾主机任务租约、就绪容器池与独占 NPU 协调服务 | [`coordinator`](https://github.com/mindie-agent/coordinator) |
| 结构化故障诊断、支持包导出与故障上报组件 | [`diagnostics`](https://github.com/mindie-agent/diagnostics) |
| 昇腾 NPU 集群只读状态监控（TUI / Web / CLI / MCP） | [`npu-top`](https://github.com/mindie-agent/npu-top) |

## 提交要求

1. **职责单一与可验证**：保持每个 PR 聚焦单一主题，并在 PR 描述中说明触发背景、行为变化与实际验证结果。
2. **遵循九条设计原则**：所有开发类 PR 在提交前必须对照 [`docs/design-principles.md`](https://github.com/mindie-agent/mindie-agent/blob/main/docs/design-principles.md) 完成九条设计原则逐条审查，并在 PR 描述中记录审查结论。
3. **严格的隐私与脱敏边界**：任何公开提交、知识包、诊断片段或 PR 描述中严禁包含凭证、私钥、内网主机地址、SSH 用户名或未脱敏的原始任务对话内容。
4. **保持对用户环境的非侵入性**：不得篡改用户无关的全局配置、其他插件、MCP 服务或本地业务源码树。
