<p align="center">
  <img src="https://raw.githubusercontent.com/mindie-agent/mindie-agent/main/assets/brand/mindie-agent-logo.png" alt="MindIE Agent logo" width="128" height="128">
</p>

# MindIE Agent Organization Repository (`.github`)

[中文](README.md)

This repository maintains the public GitHub organization profile, organization-wide contribution guidelines, and cross-repository issue templates for `@mindie-agent`.

## Repository Contents

- [`profile/README.md`](profile/README.md): Organization profile rendered on [github.com/mindie-agent](https://github.com/mindie-agent), including the 26-repository ecosystem and version tables synchronized with [`channels/0.1.json`](https://github.com/mindie-agent/mindie-agent/blob/main/channels/0.1.json) via [`.github/scripts/sync_org_versions.py`](https://github.com/mindie-agent/mindie-agent/blob/main/.github/scripts/sync_org_versions.py).
- [`CONTRIBUTING.en.md`](CONTRIBUTING.en.md) / [`CONTRIBUTING.md`](CONTRIBUTING.md): Organization-wide contribution guidelines and component ownership boundaries.
- [`.github/ISSUE_TEMPLATE/cross-repo-change.md`](.github/ISSUE_TEMPLATE/cross-repo-change.md): Issue template for coordinating contract changes across multiple repositories.

## Primary Entry Points & Current Formal Versions

<!-- mindie-org-versions:org-readme-en:start -->
- Product Entry & Architecture: [mindie-agent/mindie-agent](https://github.com/mindie-agent/mindie-agent) ([`v0.1.8`](https://github.com/mindie-agent/mindie-agent/releases/tag/v0.1.8))
- Claude Code Plugin: [mindie-agent/mindie-agent-cc](https://github.com/mindie-agent/mindie-agent-cc) ([`v0.1.15`](https://github.com/mindie-agent/mindie-agent-cc/releases/tag/v0.1.15))
- OpenAI Codex Plugin: [mindie-agent/mindie-agent-codex](https://github.com/mindie-agent/mindie-agent-codex) ([`v0.1.19`](https://github.com/mindie-agent/mindie-agent-codex/releases/tag/v0.1.19))
- Kimi Code Plugin: [mindie-agent/mindie-agent-kimi](https://github.com/mindie-agent/mindie-agent-kimi) ([`v0.1.15`](https://github.com/mindie-agent/mindie-agent-kimi/releases/tag/v0.1.15))
- DeepSeek Harness (DSH) Plugin: [mindie-agent/mindie-agent-dsh](https://github.com/mindie-agent/mindie-agent-dsh) ([`v0.1.14`](https://github.com/mindie-agent/mindie-agent-dsh/releases/tag/v0.1.14))
- Google Antigravity Plugin: [mindie-agent/mindie-agent-agy](https://github.com/mindie-agent/mindie-agent-agy) ([`v0.1.5`](https://github.com/mindie-agent/mindie-agent-agy/releases/tag/v0.1.5))
- Tencent WorkBuddy Plugin: [mindie-agent/mindie-agent-wb](https://github.com/mindie-agent/mindie-agent-wb) ([`v0.1.4`](https://github.com/mindie-agent/mindie-agent-wb/releases/tag/v0.1.4))
- Core Runtime Components: [`knowledge`](https://github.com/mindie-agent/knowledge) ([`v0.13.12`](https://github.com/mindie-agent/knowledge/releases/tag/v0.13.12)) · [`remote-dev`](https://github.com/mindie-agent/remote-dev) ([`v0.11.5`](https://github.com/mindie-agent/remote-dev/releases/tag/v0.11.5)) · [`coordinator`](https://github.com/mindie-agent/coordinator) ([`v0.7.4`](https://github.com/mindie-agent/coordinator/releases/tag/v0.7.4)) · [`profiler`](https://github.com/mindie-agent/profiler) ([`v0.5.6`](https://github.com/mindie-agent/profiler/releases/tag/v0.5.6)) · [`sim`](https://github.com/mindie-agent/sim) ([`v0.9.3`](https://github.com/mindie-agent/sim/releases/tag/v0.9.3)) · [`npu-top`](https://github.com/mindie-agent/npu-top) ([`v0.3.1`](https://github.com/mindie-agent/npu-top/releases/tag/v0.3.1)) · [`diagnostics`](https://github.com/mindie-agent/diagnostics) ([`v0.5.6`](https://github.com/mindie-agent/diagnostics/releases/tag/v0.5.6)) · [`debugger`](https://github.com/mindie-agent/debugger) ([`v0.1.0`](https://github.com/mindie-agent/debugger/releases/tag/v0.1.0))
- Evaluation & Live NPU Benchmark Suite: [mindie-agent/mindie-bench](https://github.com/mindie-agent/mindie-bench) ([`v0.4.6`](https://github.com/mindie-agent/mindie-bench/releases/tag/v0.4.6))
- Ascend Agent Skills Catalogue: [mindie-agent/awesome-mindie-skills](https://github.com/mindie-agent/awesome-mindie-skills)
<!-- mindie-org-versions:org-readme-en:end -->
