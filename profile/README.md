<p align="center">
  <img src="https://raw.githubusercontent.com/mindie-agent/mindie-agent/main/assets/brand/banner.svg" alt="MindIE Agent" width="900">
</p>

# MindIE Agent

**面向昇腾（Ascend）推理工程的智能体插件、领域知识库与远程开发工具链**  
*Agent plugins, curated domain knowledge, and remote execution tooling for Ascend inference engineering.*

**[项目主入口 / Main Entry](https://github.com/mindie-agent/mindie-agent)** · **[Codex 插件](https://github.com/mindie-agent/mindie-agent-codex)** · **[Claude Code 插件](https://github.com/mindie-agent/mindie-agent-cc)** · **[Awesome MindIE Skills](https://github.com/mindie-agent/awesome-mindie-skills)** · **[vLLM-Ascend Workspace](https://github.com/mindie-agent/vllm-ascend-workspace)**

---

## 简介 / Overview

**MindIE Agent** 将昇腾推理工程（如 `vLLM-Ascend`、CANN 算子适配、远端 NPU 容器调试与精度/性能定位）所需的领域知识、经验沉淀闭环与 SSH 远端执行能力，以轻量插件的形式直接注入开发者日常使用的 AI 编程客户端（OpenAI Codex CLI、Claude Code、Kimi Code）。

**MindIE Agent** brings Ascend inference engineering capabilities—curated `vLLM-Ascend` domain knowledge, local task experience indexing, privacy-redacted community sharing, and SSH-backed remote NPU execution—directly into your daily AI coding agent (OpenAI Codex CLI, Claude Code, and Kimi Code) without taking over your local repository or breaking existing workflows.

---

## 快速体验 / Quick Start

- **使用 OpenAI Codex CLI**：前往 [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) 一行命令安装插件。
- **使用 Claude Code**：前往 [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) 一行命令安装插件。
- **按需选用独立 Agent Skills**：浏览 [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) 技能目录。
- **搭建本地多任务开发工作区**：使用 [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) 初始化 `vllm` + `vllm-ascend` 独立 Git Worktree 工作区。

---

## 仓库全景 / Repository Ecosystem

### 入口与社区生态 / Entry & Community

| 仓库 / Repository | 定位与职责 / Role |
|---|---|
| [`mindie-agent`](https://github.com/mindie-agent/mindie-agent) | 产品总入口、整体架构、领域边界、九条核心设计原则与版本发布记录 / Product entry, architecture, design principles, and release records |
| [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) | 面向昇腾推理工程的开源 Agent Skills 精选目录与质量验证规范 / Curated catalogue of Agent Skills for Ascend inference engineering |
| [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) | 面向 `vllm` 与 `vllm-ascend` 的轻量本地开发工作区脚手架（支持独立任务 Worktree）/ Lightweight local workspace scaffold for vLLM and vLLM-Ascend development |

### 宿主插件适配层 / Harness Plugins

| 仓库 / Repository | 定位与职责 / Role |
|---|---|
| [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) | OpenAI Codex CLI 原生插件（`v0.0.1` 已发布）/ Native OpenAI Codex CLI plugin (`v0.0.1` released) |
| [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) | Claude Code 原生插件（`v0.0.1` 已发布）/ Native Claude Code plugin (`v0.0.1` released) |
| [`mindie-agent-kimi`](https://github.com/mindie-agent/mindie-agent-kimi) | Kimi Code 原生适配插件（源码已对齐共享运行时）/ Native Kimi Code adapter |

### 共享运行时与领域知识 / Shared Runtimes & Knowledge

| 仓库 / Repository | 定位与职责 / Role |
|---|---|
| [`knowledge`](https://github.com/mindie-agent/knowledge) | 共享知识与经验运行时：公共知识同步、本地私有经验检索、脱敏外发与独立有用性反馈 / Shared knowledge, local experience indexing, redaction, and feedback runtime |
| [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) | `vLLM-Ascend` 公共工程知识包仓库（结构化 `PACKAGE.md` 与受控资料包）/ Curated public engineering knowledge packages for `vLLM-Ascend` |
| [`remote-dev`](https://github.com/mindie-agent/remote-dev) | 基于 SSH 的远端开发运行时与 MCP 服务（文件读写、补丁、后台作业、产物同步与安全守卫）/ SSH-backed remote development CLI and MCP server |
| [`diagnostics`](https://github.com/mindie-agent/diagnostics) | 轻量结构化故障诊断、隐私脱敏支持包导出与显式授权 Issue 上报组件 / Structured fault diagnostics, redacted support bundles, and opt-in issue reporting |
| [`npu-top`](https://github.com/mindie-agent/npu-top) | 仅监听本地回环的昇腾 NPU 集群只读观测工具（提供 TUI、Web、CLI 与 MCP 接口）/ Loopback-only Ascend NPU fleet monitor (TUI, Web, CLI, and MCP) |
| [`coordinator`](https://github.com/mindie-agent/coordinator) | 昇腾主机可选本地回环 MCP 协调器（任务租约、就绪容器池、独占 NPU 绑定与受管作业）/ Opt-in loopback MCP coordinator for Ascend runtime pools and NPU bindings |
