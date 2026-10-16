<p align="center">
  <img src="https://raw.githubusercontent.com/mindie-agent/mindie-agent/main/assets/brand/mindie-agent-logo.png" alt="MindIE Agent logo" width="128" height="128">
</p>

<h1 align="center">MindIE Agent</h1>

<p align="center">
  <b>面向昇腾（Ascend）NPU AI Infra 研发、设计与测试全流程的统一 Agent 能力底座</b><br/>
  <i>The unified AI Agent capability platform for Ascend NPU AI Infra — across architecture design, feature development, AscendC/Triton kernels, testing, and tuning.</i>
</p>

<p align="center">
  <a href="https://github.com/mindie-agent/mindie-agent"><img src="https://img.shields.io/badge/Release-v0.0.1-blue?style=flat-square" alt="Release v0.0.1"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-cc"><img src="https://img.shields.io/badge/Claude_Code-Plugin_Ready-D97757?style=flat-square" alt="Claude Code"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-codex"><img src="https://img.shields.io/badge/OpenAI_Codex-Plugin_Ready-10A37F?style=flat-square" alt="OpenAI Codex"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-kimi"><img src="https://img.shields.io/badge/Kimi_Code-Adapter_Ready-6366F1?style=flat-square" alt="Kimi Code"></a>
  <a href="https://github.com/mindie-agent/awesome-mindie-skills"><img src="https://img.shields.io/badge/Ascend_AI_Infra-vLLM--Ascend_%7C_AscendC_%7C_Triton-F59E0B?style=flat-square" alt="Ascend AI Infra Skills"></a>
</p>

<p align="center">
  <a href="https://github.com/mindie-agent/mindie-agent"><b>项目主入口 (Main Repo)</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent-cc"><b>Claude Code 插件</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent-codex"><b>Codex 插件</b></a> ·
  <a href="https://github.com/mindie-agent/awesome-mindie-skills"><b>Awesome MindIE Skills</b></a> ·
  <a href="https://github.com/mindie-agent/vllm-ascend-workspace"><b>vLLM-Ascend Workspace</b></a>
</p>

---

## ⚡ 一句话无感安装 / One-Sentence Agent-Native Install

不需要手翻长篇配置文档——直接把下面这句话发给你正在使用的 **Claude Code**、**Codex CLI** 或 **Kimi Code**，让你的 Agent 自动完成检测、安装与配置：

```text
帮我安装一下这个 https://github.com/mindie-agent/mindie-agent
```
*(English: `Please install https://github.com/mindie-agent/mindie-agent for me`)*

---

## 🔥 装好之后怎么用？ / How to Use After Installation

MindIE Agent 坚持**用户侧极简单一入口 + Agent 侧上下文渐进式披露**的设计理念——你只需要知道 **`/mindie-agent`** 这一个入口，无需记忆任何复杂的子命令：

- **🧠 手动输入 `/mindie-agent`（唤醒昇腾 Infra 领域知识、经验与 Skill 系统）**：无论是做新特性方案设计、`vLLM-Ascend` 开发、`AscendC` / `Triton` 算子编写、单测/集成测试构建，还是性能调优与问题定位，直接输入 `/mindie-agent`（Codex 中也可使用 `$mindie-agent`）并描述需求（配置与状态查看也同样包裹在 `/mindie-agent` 中，由 Agent 按需渐进式加载上下文处理）：
  ```text
  /mindie-agent 我准备在 vllm-ascend 中为新模型设计并接入一个融合算子（支持 Triton / AscendC 实现），帮我结合现有的架构规范与开发经验梳理设计方案和单测验证点。
  ```
- **⚡ 默认自动触发 `remote-dev`（无需斜杠命令，日常对话直连远端 NPU）**：`remote-dev` 作为常驻 MCP 工具默认就绪。日常对话中只要提到远端服务器或容器，Agent 就会自动调用远端读写、代码同步与后台测试工具：
  ```text
  连上远端机器 192.0.2.21 上的 vllm-dev 容器，把我刚写的算子代码和测试用例同步过去，在 NPU 上跑一下完整的 pytest 精度与性能测试。
  ```
- **🔄 研发经验后台静默沉淀（一次开启，全程无感）**：首次配置时开启社区贡献后，每次会话结束时都会在后台自动完成本地隐私脱敏（确定性规则 + Gitleaks）并将架构设计、算子开发或测试排障经验整理为知识库 PR，日常开发零打扰。

---

## 🌟 为什么需要 MindIE Agent？ / Why MindIE Agent?

通用编程大模型写常规代码很强，但在昇腾（Ascend）NPU 上开展 AI Infra 研发（从系统架构设计、框架特性开发、`AscendC` / `Triton` 算子开发，到远端多卡测试验证、精度对齐与性能调优）时，往往面临**缺乏昇腾软硬件栈上下文、本地写代码与远端 NPU 容器验证割裂、宝贵的研发与设计经验随会话结束而流失**三大痛点。

**MindIE Agent** 的核心目标是为**昇腾 NPU 上的 AI Infra 全流程（设计 / 开发 / 测试 / 调优）提供统一的 Agent 能力底座**。目前生态已率先沉淀了面向 **`vLLM-Ascend`、`AscendC` 与 `Triton` 算子开发及测试**的知识库与技能体系，并正在持续扩展至更广泛的昇腾基础软件领域：

1. **远端昇腾开发与测试闭环（`remote-dev`）**：通过 SSH 直接在远端昇腾容器内读写文件、应用补丁、投递长耗时编译/测试作业、流式查看日志并拉回 Profiling 产物。
2. **领域知识与研发经验飞轮（`knowledge` + `knowledge-vllm-ascend`）**：检索经过实机验证的设计规范、开发实践与测试案例；本地研发完成后自动通过 Gitleaks 与确定性隐私规则脱敏沉淀。
3. **NPU 集群看板与卡池调度（`npu-top` + `coordinator`）**：一眼看清多节点 NPU 显存/算力占用，并为并发开发与测试任务自动分配独占 NPU 租约。
4. **可定位结构化诊断（`diagnostics`）**：有界本地诊断日志与可选、去重的白名单故障自动上报。

---

## 🗺️ 开源仓库全景 / Repository Ecosystem

### 1. 主入口与开发者生态（Entry & Developer Ecosystem）

| 仓库 / Repository | 定位与核心用途 / What It Does |
|---|---|
| [`mindie-agent`](https://github.com/mindie-agent/mindie-agent) | **总入口**：产品架构、工程设计原则、一句话 Agent 自动安装协议与统一版本记录 |
| [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) | **开箱即用技能库**：覆盖昇腾 AI Infra 开发、测试、算子实现（`AscendC` / `Triton`）与 `vLLM-Ascend` 工程的精选 Agent Skills（持续扩展中） |
| [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) | **本地多任务工作区**：一键拉起 `vllm` + `vllm-ascend` 独立 Git Worktree 的开发与测试脚手架 |

### 2. 原生客户端插件（Native Agent Plugins）

| 仓库 / Repository | 定位与核心用途 / What It Does |
|---|---|
| [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) | **Claude Code 原生插件**（`v0.0.1` 已发布）：支持 macOS、原生 Windows 与 WSL |
| [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) | **OpenAI Codex CLI 原生插件**（`v0.0.1` 已发布）：支持 macOS、原生 Windows 与 WSL |
| [`mindie-agent-kimi`](https://github.com/mindie-agent/mindie-agent-kimi) | **Kimi Code 原生适配插件**：提供 `/mindie-agent` 统一入口、远端 NPU 开发测试与知识闭环 |

### 3. 核心运行时组件与公共知识库（Core Runtimes & Public Knowledge）

| 仓库 / Repository | 定位与核心用途 / What It Does |
|---|---|
| [`knowledge`](https://github.com/mindie-agent/knowledge) | **知识与经验引擎**：本地经验提取、双层隐私脱敏、小模型目录生成、BM25 检索与社区共建 |
| [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) | **昇腾领域公共知识库**：经审核脱敏的 `vLLM-Ascend`、算子开发与 NPU 测试实战 Markdown 知识包（更多领域持续接入） |
| [`remote-dev`](https://github.com/mindie-agent/remote-dev) | **SSH 远端开发引擎**：远端文件读写、补丁应用、受管持久后台作业与构建/测试产物同步 |
| [`coordinator`](https://github.com/mindie-agent/coordinator) | **昇腾 NPU 协调器**：多任务 NPU 独占租约分配、就绪容器池与受管作业调度 |
| [`npu-top`](https://github.com/mindie-agent/npu-top) | **NPU 集群状态看板**：仅监听本地回环的昇腾 NPU 实时监控（支持 TUI、Web、CLI 与 MCP） |
| [`diagnostics`](https://github.com/mindie-agent/diagnostics) | **结构化诊断组件**：有界本地日志、错误定位编号与独立授权的 GitHub Issue 故障上报 |
