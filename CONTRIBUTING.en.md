# Contributing to MindIE Agent

[中文](CONTRIBUTING.md)

We welcome contributions to the MindIE Agent ecosystem! Please submit Issues and Pull Requests to the repository that owns the relevant capability:

## Component Ownership Boundaries

| Scope of Change | Target Repository |
|---|---|
| Overall architecture, domain boundaries, design principles, and paired-release rules | [`mindie-agent`](https://github.com/mindie-agent/mindie-agent) |
| OpenAI Codex CLI plugin integration and lifecycle hooks | [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) |
| Claude Code plugin integration and lifecycle hooks | [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) |
| Kimi Code adapter and command wrappers | [`mindie-agent-kimi`](https://github.com/mindie-agent/mindie-agent-kimi) |
| Knowledge sync, local experience indexing, redaction, and feedback runtime | [`knowledge`](https://github.com/mindie-agent/knowledge) |
| Curated `vLLM-Ascend` public engineering knowledge packages | [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) |
| Community catalogue of Agent Skills for Ascend inference engineering | [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) |
| Local development workspace scaffold for `vllm` and `vllm-ascend` | [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) |
| SSH remote file tools, background jobs, artifacts, and MCP server | [`remote-dev`](https://github.com/mindie-agent/remote-dev) |
| Ascend host task leases, ready-runtime pools, and exclusive NPU bindings | [`coordinator`](https://github.com/mindie-agent/coordinator) |
| Structured fault diagnostics, redacted support bundles, and opt-in reporting | [`diagnostics`](https://github.com/mindie-agent/diagnostics) |
| Read-only Ascend NPU fleet monitor (TUI / Web / CLI / MCP) | [`npu-top`](https://github.com/mindie-agent/npu-top) |

## Contribution Guidelines

1. **Scoped & Verifiable PRs**: Keep each PR focused on a single concern and describe the motivation, behavior change, and validation evidence.
2. **Mandatory Design-Principles Review**: Before opening any development PR, review the diff against all nine principles in [`docs/design-principles.md`](https://github.com/mindie-agent/mindie-agent/blob/main/docs/design-principles.md) and include the review table in the PR description.
3. **Strict Privacy & Redaction**: Never include credentials, private endpoints, SSH usernames/hosts, local filesystem home paths, or raw user transcripts in public commits, knowledge packages, or PR descriptions.
4. **Non-Intrusive User Experience**: Do not alter unrelated user skills, plugins, MCP configurations, or business source checkouts.
