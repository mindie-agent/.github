# 参与贡献（Contributing to MindIE Agent）

[English](CONTRIBUTING.en.md)

欢迎参与 MindIE Agent 开源社区建设！为了让你的 Issue 或 Pull Request 得到最快响应，请根据改动所属的功能模块，提交到对应的仓库：

## 仓库职责速查表

| 你想贡献或修改的内容 | 请提交到该仓库 |
|---|---|
| 总体架构、工程设计原则、跨组件契约与统一版本记录 | [`mindie-agent`](https://github.com/mindie-agent/mindie-agent) |
| 真机基准套件、行为级判分器（Oracle）与评测运行器 | [`mindie-bench`](https://github.com/mindie-agent/mindie-bench) |
| Claude Code 原生插件与 Hook / MCP 集成 | [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) |
| OpenAI Codex CLI 原生插件与 Hook / MCP 集成 | [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) |
| Kimi Code 原生适配插件与旁路原子更新 | [`mindie-agent-kimi`](https://github.com/mindie-agent/mindie-agent-kimi) |
| DeepSeek Harness (DSH) 原生插件与工具桥接 | [`mindie-agent-dsh`](https://github.com/mindie-agent/mindie-agent-dsh) |
| 知识同步、按信息缺口条件检索、隐私脱敏与反馈引擎 | [`knowledge`](https://github.com/mindie-agent/knowledge) |
| SSH 远端文件工具、共享 SSH 凭据、容器执行与后台长作业 | [`remote-dev`](https://github.com/mindie-agent/remote-dev) |
| 昇腾主机任务租约、就绪容器池与独占 NPU/端口调度服务 | [`coordinator`](https://github.com/mindie-agent/coordinator) |
| 昇腾 `msprof` 原地只读解析、模型结构对齐与跨版本对比 | [`profiler`](https://github.com/mindie-agent/profiler) |
| 五层因果性能建模、4D 效率拆解与 SLA 硬件配比推演 | [`sim`](https://github.com/mindie-agent/sim) |
| 昇腾 NPU 集群只读状态监控（Web / TUI / CLI / MCP） | [`npu-top`](https://github.com/mindie-agent/npu-top) |
| 结构化故障诊断、CANN/`plog` 分诊与可选白名单故障上报 | [`diagnostics`](https://github.com/mindie-agent/diagnostics) |
| 昇腾领域公共知识库（`vLLM-Ascend` / 算子 / 推理核心 / 分布式 / 可观测 / 图编译兼容 / Agent 工程） | [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) · [`knowledge-operators`](https://github.com/mindie-agent/knowledge-operators) · [`knowledge-infer-core`](https://github.com/mindie-agent/knowledge-infer-core) · [`knowledge-infer-distributed`](https://github.com/mindie-agent/knowledge-infer-distributed) · [`knowledge-infer-observability`](https://github.com/mindie-agent/knowledge-infer-observability) · [`knowledge-infer-ops-compat`](https://github.com/mindie-agent/knowledge-infer-ops-compat) · [`knowledge-agent-engineering`](https://github.com/mindie-agent/knowledge-agent-engineering) |
| 昇腾 AI Infra 独立 Agent Skills 精选目录 | [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) |
| `vllm` / `vllm-ascend` 本地多任务开发工作区脚手架 | [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) |

## 提交 Pull Request 的四条基本准则

1. **小步快跑，职责单一**：每个 PR 聚焦解决一个具体问题，并在描述中写明背景、改动点与验证方式。
2. **完成工程设计原则与 Pre-PR Checklist 自查**：动手写代码前请先阅读目标仓库的 `AGENTS.md` 与 [`docs/design-principles.md`](https://github.com/mindie-agent/mindie-agent/blob/main/docs/design-principles.md)；提交 PR 时对照 `.github/pull_request_template.md` 完成逐项自检（含强制 Unix `LF` 换行格式检查）。
3. **严守隐私脱敏红线**：任何公开提交、知识包、测试样例或 PR 描述中，严禁包含密钥、Token、内网 IP、SSH 用户名/主机名、个人主目录路径或未脱敏的原始会话记录。
4. **尊重用户本地环境**：绝不篡改用户无关的全局配置、其他插件、MCP 服务或业务源码仓库。
