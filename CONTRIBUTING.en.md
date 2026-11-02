# Contributing to MindIE Agent

[中文](CONTRIBUTING.md)

Welcome to the MindIE Agent open-source community! To make sure your Issue or Pull Request lands in the right place, please use the repository table below:

## Where to File Issues & PRs

| What You Are Working On | Target Repository |
|---|---|
| Overall architecture, engineering design principles, cross-component contracts, and release records | [`mindie-agent`](https://github.com/mindie-agent/mindie-agent) |
| Live NPU benchmark suite, behavioral task oracles, and evaluation runner | [`mindie-bench`](https://github.com/mindie-agent/mindie-bench) |
| Claude Code native plugin and Hook / MCP integration | [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) |
| OpenAI Codex CLI native plugin and Hook / MCP integration | [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) |
| Kimi Code native plugin and side-by-side atomic updates | [`mindie-agent-kimi`](https://github.com/mindie-agent/mindie-agent-kimi) |
| DeepSeek Harness (DSH) native plugin and tool bridging | [`mindie-agent-dsh`](https://github.com/mindie-agent/mindie-agent-dsh) |
| Google Antigravity native plugin and tool bridging | [`mindie-agent-agy`](https://github.com/mindie-agent/mindie-agent-agy) |
| Tencent WorkBuddy (CodeBuddy Agent CLI) native plugin and connector bridging | [`mindie-agent-wb`](https://github.com/mindie-agent/mindie-agent-wb) |
| Knowledge sync, information-gap retrieval, batch `refs` / `known_refs` / `token_budget` explanation, `rejected_history` / `affected_components` provenance, and redaction engine | [`knowledge`](https://github.com/mindie-agent/knowledge) |
| SSH remote file tools, shared `~/.mindie/ssh/id_ed25519` credential fallback, destructive-command safety guards, container execution, and background jobs | [`remote-dev`](https://github.com/mindie-agent/remote-dev) |
| Ascend A2/A3/A5 topology probing, HCCL/RoCE preflight, per-Die HBM lease & compile slot budgets, and exclusive NPU/port scheduling | [`coordinator`](https://github.com/mindie-agent/coordinator) |
| In-place Ascend `msprof` trace analysis, `analyze_profiling --structure` 3-state topology alignment, and `auto_segment_decode_forwards` Decode segmentation | [`profiler`](https://github.com/mindie-agent/profiler) |
| 5-layer causal performance modeling (`DP × TP × EP × PP × DCP / DSA-CP / PCP`, AFD, DeepEP, hierarchical KV offload, and configurable network/hardware SKUs), 4D efficiency breakdown, SLA hardware scaling solver, and fleet calibration | [`sim`](https://github.com/mindie-agent/sim) |
| Read-only Ascend A2/A3/A5 NPU fleet monitor (Web / TUI / CLI / MCP, with shared `~/.mindie/ssh` credential fallback) | [`npu-top`](https://github.com/mindie-agent/npu-top) |
| Agent internal fault logs (4×1 MiB rotation), offline redacted bundles, and opt-in Issue reporting with bounded 2-attempt outbound reconciliation | [`diagnostics`](https://github.com/mindie-agent/diagnostics) |
| Target Ascend NPU fault triage (`npu_fault_triage`), 3-primitive precision/memory-stomp localization (`precision`), and `ACLGraph` static-graph debugging (`aclgraph`) | [`debugger`](https://github.com/mindie-agent/debugger) |
| Public Ascend domain knowledge corpora (`vLLM-Ascend` / `xLLM` / `MindIE-SD` / Operators / Infer Core / Distributed / Observability / Ops Compat / Agent Engineering) | [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) · [`knowledge-xllm`](https://github.com/mindie-agent/knowledge-xllm) · [`knowledge-mindie-sd`](https://github.com/mindie-agent/knowledge-mindie-sd) · [`knowledge-operators`](https://github.com/mindie-agent/knowledge-operators) · [`knowledge-infer-core`](https://github.com/mindie-agent/knowledge-infer-core) · [`knowledge-infer-distributed`](https://github.com/mindie-agent/knowledge-infer-distributed) · [`knowledge-infer-observability`](https://github.com/mindie-agent/knowledge-infer-observability) · [`knowledge-infer-ops-compat`](https://github.com/mindie-agent/knowledge-infer-ops-compat) · [`knowledge-agent-engineering`](https://github.com/mindie-agent/knowledge-agent-engineering) |
| Community catalogue of standalone Agent Skills for Ascend engineering | [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) |
| Local multi-task workspace scaffold for `vllm` and `vllm-ascend` | [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) |

## Four Core Contribution Guidelines

1. **Keep PRs Focused & Verifiable**: Focus each PR on a single concern and describe the motivation, behavior change, and how you tested it.
2. **Complete the Design-Principles & Pre-PR Checklist Review**: Read `AGENTS.md` and the [Engineering Design Principles](https://github.com/mindie-agent/mindie-agent/blob/main/docs/design-principles.en.md) before writing code, and complete every item in `.github/pull_request_template.md` (including mandatory Unix `LF` line endings) when opening a PR.
3. **Strict Privacy & Redaction**: Never include secrets, tokens, private IPs, SSH `user@host` strings, local home paths, or raw unredacted transcripts in public commits, knowledge packages, or PR descriptions.
4. **Respect the User's Environment**: Never modify unrelated user skills, plugins, MCP configurations, or business source checkouts.
