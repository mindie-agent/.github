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
| Knowledge sync, information-gap retrieval, redaction, and feedback engine | [`knowledge`](https://github.com/mindie-agent/knowledge) |
| SSH remote file tools, shared SSH credentials, container execution, and background jobs | [`remote-dev`](https://github.com/mindie-agent/remote-dev) |
| Ascend host task leases, ready-runtime pools, and exclusive NPU/port scheduling | [`coordinator`](https://github.com/mindie-agent/coordinator) |
| In-place Ascend `msprof` trace analysis, structure alignment, and cross-run comparison | [`profiler`](https://github.com/mindie-agent/profiler) |
| 5-layer causal performance modeling, 4D efficiency breakdown, and SLA hardware scaling | [`sim`](https://github.com/mindie-agent/sim) |
| Read-only Ascend NPU fleet monitor (Web / TUI / CLI / MCP) | [`npu-top`](https://github.com/mindie-agent/npu-top) |
| Structured fault diagnostics, CANN/`plog` triage, and opt-in Issue reporting | [`diagnostics`](https://github.com/mindie-agent/diagnostics) |
| Public Ascend domain knowledge corpora (`vLLM-Ascend` / Operators / Infer Core / Distributed / Observability / Ops Compat / Agent Engineering) | [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) · [`knowledge-operators`](https://github.com/mindie-agent/knowledge-operators) · [`knowledge-infer-core`](https://github.com/mindie-agent/knowledge-infer-core) · [`knowledge-infer-distributed`](https://github.com/mindie-agent/knowledge-infer-distributed) · [`knowledge-infer-observability`](https://github.com/mindie-agent/knowledge-infer-observability) · [`knowledge-infer-ops-compat`](https://github.com/mindie-agent/knowledge-infer-ops-compat) · [`knowledge-agent-engineering`](https://github.com/mindie-agent/knowledge-agent-engineering) |
| Community catalogue of standalone Agent Skills for Ascend engineering | [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) |
| Local multi-task workspace scaffold for `vllm` and `vllm-ascend` | [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) |

## Four Core Contribution Guidelines

1. **Keep PRs Focused & Verifiable**: Focus each PR on a single concern and describe the motivation, behavior change, and how you tested it.
2. **Complete the Design-Principles & Pre-PR Checklist Review**: Read `AGENTS.md` and the [Engineering Design Principles](https://github.com/mindie-agent/mindie-agent/blob/main/docs/design-principles.en.md) before writing code, and complete every item in `.github/pull_request_template.md` (including mandatory Unix `LF` line endings) when opening a PR.
3. **Strict Privacy & Redaction**: Never include secrets, tokens, private IPs, SSH `user@host` strings, local home paths, or raw unredacted transcripts in public commits, knowledge packages, or PR descriptions.
4. **Respect the User's Environment**: Never modify unrelated user skills, plugins, MCP configurations, or business source checkouts.
