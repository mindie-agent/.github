<p align="center">
  <img src="https://raw.githubusercontent.com/mindie-agent/mindie-agent/main/assets/brand/mindie-agent-logo.png" alt="MindIE Agent logo" width="128" height="128">
</p>

# MindIE Agent 组织配置仓库（`.github`）

[English](README.en.md)

本仓库维护 `@mindie-agent` GitHub 组织的公共主页简介、跨仓库贡献指南以及组织级 Issue 模板。

## 目录结构

- [`profile/README.md`](profile/README.md)：展示在 [github.com/mindie-agent](https://github.com/mindie-agent) 组织主页的公开简介与 26 仓库生态版本导航表（由主仓 [`.github/scripts/sync_org_versions.py`](https://github.com/mindie-agent/mindie-agent/blob/main/.github/scripts/sync_org_versions.py) 根据 [`channels/0.1.json`](https://github.com/mindie-agent/mindie-agent/blob/main/channels/0.1.json) 自动同步校验）。
- [`CONTRIBUTING.md`](CONTRIBUTING.md) / [`CONTRIBUTING.en.md`](CONTRIBUTING.en.md)：跨仓库贡献原则、职责边界与提交流程说明。
- [`.github/ISSUE_TEMPLATE/cross-repo-change.md`](.github/ISSUE_TEMPLATE/cross-repo-change.md)：涉及多个组件仓库的契约演进与联动变更 Issue 模板。

## 核心入口与当前正式版本

<!-- mindie-org-versions:org-readme-zh:start -->
- 产品总入口与架构文档：[mindie-agent/mindie-agent](https://github.com/mindie-agent/mindie-agent)（[`v0.1.8`](https://github.com/mindie-agent/mindie-agent/releases/tag/v0.1.8)）
- Claude Code 插件：[mindie-agent/mindie-agent-cc](https://github.com/mindie-agent/mindie-agent-cc)（[`v0.1.15`](https://github.com/mindie-agent/mindie-agent-cc/releases/tag/v0.1.15)）
- OpenAI Codex 插件：[mindie-agent/mindie-agent-codex](https://github.com/mindie-agent/mindie-agent-codex)（[`v0.1.19`](https://github.com/mindie-agent/mindie-agent-codex/releases/tag/v0.1.19)）
- Kimi Code 插件：[mindie-agent/mindie-agent-kimi](https://github.com/mindie-agent/mindie-agent-kimi)（[`v0.1.15`](https://github.com/mindie-agent/mindie-agent-kimi/releases/tag/v0.1.15)）
- DeepSeek Harness (DSH) 插件：[mindie-agent/mindie-agent-dsh](https://github.com/mindie-agent/mindie-agent-dsh)（[`v0.1.14`](https://github.com/mindie-agent/mindie-agent-dsh/releases/tag/v0.1.14)）
- Google Antigravity 插件：[mindie-agent/mindie-agent-agy](https://github.com/mindie-agent/mindie-agent-agy)（[`v0.1.5`](https://github.com/mindie-agent/mindie-agent-agy/releases/tag/v0.1.5)）
- Tencent WorkBuddy 插件：[mindie-agent/mindie-agent-wb](https://github.com/mindie-agent/mindie-agent-wb)（[`v0.1.4`](https://github.com/mindie-agent/mindie-agent-wb/releases/tag/v0.1.4)）
- 核心运行时组件：[`knowledge`](https://github.com/mindie-agent/knowledge)（[`v0.13.12`](https://github.com/mindie-agent/knowledge/releases/tag/v0.13.12)）· [`remote-dev`](https://github.com/mindie-agent/remote-dev)（[`v0.11.5`](https://github.com/mindie-agent/remote-dev/releases/tag/v0.11.5)）· [`coordinator`](https://github.com/mindie-agent/coordinator)（[`v0.7.4`](https://github.com/mindie-agent/coordinator/releases/tag/v0.7.4)）· [`profiler`](https://github.com/mindie-agent/profiler)（[`v0.5.6`](https://github.com/mindie-agent/profiler/releases/tag/v0.5.6)）· [`sim`](https://github.com/mindie-agent/sim)（[`v0.9.3`](https://github.com/mindie-agent/sim/releases/tag/v0.9.3)）· [`npu-top`](https://github.com/mindie-agent/npu-top)（[`v0.3.1`](https://github.com/mindie-agent/npu-top/releases/tag/v0.3.1)）· [`diagnostics`](https://github.com/mindie-agent/diagnostics)（[`v0.5.6`](https://github.com/mindie-agent/diagnostics/releases/tag/v0.5.6)）· [`debugger`](https://github.com/mindie-agent/debugger)（[`v0.1.0`](https://github.com/mindie-agent/debugger/releases/tag/v0.1.0)）
- 真机评测与基准套件：[mindie-agent/mindie-bench](https://github.com/mindie-agent/mindie-bench)（[`v0.4.6`](https://github.com/mindie-agent/mindie-bench/releases/tag/v0.4.6)）
- 昇腾 AI Infra 技能目录：[mindie-agent/awesome-mindie-skills](https://github.com/mindie-agent/awesome-mindie-skills)
<!-- mindie-org-versions:org-readme-zh:end -->
