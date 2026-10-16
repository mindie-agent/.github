# Contributing to MindIE Agent

[中文](CONTRIBUTING.md)

Welcome to the MindIE Agent open-source community! To make sure your Issue or Pull Request lands in the right place, please use the repository table below:

## Where to File Issues & PRs

| What You Are Working On | Target Repository |
|---|---|
| Overall architecture, engineering design principles, cross-component contracts, and release records | [`mindie-agent`](https://github.com/mindie-agent/mindie-agent) |
| Claude Code native plugin and Hook integration | [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) |
| OpenAI Codex CLI native plugin and Hook integration | [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) |
| Kimi Code adapter and command wrappers | [`mindie-agent-kimi`](https://github.com/mindie-agent/mindie-agent-kimi) |
| Knowledge sync, local experience indexing, redaction, and feedback engine | [`knowledge`](https://github.com/mindie-agent/knowledge) |
| Curated `vLLM-Ascend` public engineering knowledge packages | [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) |
| Community catalogue of standalone Agent Skills for Ascend engineering | [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) |
| Local multi-task workspace scaffold for `vllm` and `vllm-ascend` | [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) |
| SSH remote file tools, background jobs, artifact sync, and MCP server | [`remote-dev`](https://github.com/mindie-agent/remote-dev) |
| Ascend host task leases, ready-runtime pools, and exclusive NPU scheduling | [`coordinator`](https://github.com/mindie-agent/coordinator) |
| Read-only Ascend NPU fleet monitor (TUI / Web / CLI / MCP) | [`npu-top`](https://github.com/mindie-agent/npu-top) |
| Structured fault diagnostics, redacted support bundles, and opt-in Issue reporting | [`diagnostics`](https://github.com/mindie-agent/diagnostics) |

## Four Core Contribution Guidelines

1. **Keep PRs Focused & Verifiable**: Focus each PR on a single concern and describe the motivation, behavior change, and how you tested it.
2. **Complete the Design-Principles Check**: Before opening any development PR, review your diff against the [Engineering Design Principles](https://github.com/mindie-agent/mindie-agent/blob/main/docs/design-principles.en.md) and include a concise `## 设计原则 Review` summary in the PR description.
3. **Strict Privacy & Redaction**: Never include secrets, tokens, private IPs, SSH `user@host` strings, local home paths, or raw unredacted transcripts in public commits, knowledge packages, or PR descriptions.
4. **Respect the User's Environment**: Never modify unrelated user skills, plugins, MCP configurations, or business source checkouts.
