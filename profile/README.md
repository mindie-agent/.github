# MindIE Agent

Domain-focused agents, reliable remote tools, and a knowledge and experience feedback loop for Ascend development.

**[Get started with the Codex plugin](https://github.com/mindie-agent/mindie-agent-codex)** · [Architecture](https://github.com/mindie-agent/mindie-agent/issues/195) · [Real NPU acceptance](https://github.com/mindie-agent/mindie-agent-codex/blob/main/docs/real-acceptance-2026-09-18.md)

Codex and the knowledge service run locally. Remote Ascend containers provide device execution through remote-dev. A normal task's final reply can produce reusable experience; independent tasks apply it, and a separate judge's usefulness feedback affects later retrieval.

| Repository | Role |
|---|---|
| [mindie-agent](https://github.com/mindie-agent/mindie-agent) | Architecture, domain boundaries and delivery entry |
| [mindie-agent-codex](https://github.com/mindie-agent/mindie-agent-codex) | First Harness adapter and plugin |
| [knowledge](https://github.com/mindie-agent/knowledge) | Retrieval, collection, distribution and independent feedback |
| [knowledge-vllm-ascend](https://github.com/mindie-agent/knowledge-vllm-ascend) | Domain content |
| [remote-dev](https://github.com/mindie-agent/remote-dev) | Remote files, commands, owned jobs and artifacts |
| [coordinator](https://github.com/mindie-agent/coordinator) | Managed environments, resources and execution |
| [diagnostics](https://github.com/mindie-agent/diagnostics) | Component diagnostics |
| [npu-top](https://github.com/mindie-agent/npu-top) | Optional device observation |

Renamed in place on 2026-09-18; repository IDs, issues, PRs and history remain intact. Packages, imports and owned configuration now use the new names; the former workspace entry and aliases are removed.

The first single-domain loop has actual CLI/MCP/hook and NPU evidence. Grok event delivery and cross-domain Desktop controls still need acceptance. The current feed remains on the knowledge repository's knowledge/vllm-ascend branch; consolidating domain publication is next.
