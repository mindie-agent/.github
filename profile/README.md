<p align="center">
  <img src="https://raw.githubusercontent.com/mindie-agent/mindie-agent/main/assets/brand/mindie-agent-logo.png" alt="MindIE Agent logo" width="128" height="128">
</p>

# MindIE Agent

Domain-focused agents, reliable remote tools, and a knowledge and experience feedback loop for Ascend development.

**[Get started with the Codex plugin](https://github.com/mindie-agent/mindie-agent-codex)** · [Architecture](https://github.com/mindie-agent/mindie-agent/blob/main/docs/architecture.md) · [Real NPU acceptance](https://github.com/mindie-agent/mindie-agent-codex/blob/main/docs/real-acceptance-2026-09-18.md)

Codex and the knowledge service run locally. Remote Ascend containers provide device execution through remote-dev. Eligible native tasks use existing contribution choice and project scope. Complete redacted public messages are the body authority; an internal model supplies retrieval navigation. Later tasks optionally read experience or give usefulness feedback, without mandatory retrieval or judging steps.

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

The current feed is [knowledge-vllm-ascend/main](https://github.com/mindie-agent/knowledge-vllm-ascend/tree/main). Codex and its upstream/downstream components are undergoing systematic prerelease review. Earlier native, NPU and Bot results apply only to their recorded versions; see [current implementation status](https://github.com/mindie-agent/mindie-agent/blob/main/docs/implementation-status.md). Kimi and Claude Code retain independent older pins and require their own port and acceptance.
