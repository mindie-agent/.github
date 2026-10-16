<p align="center">
  <img src="https://raw.githubusercontent.com/mindie-agent/mindie-agent/main/assets/brand/mindie-agent-logo.png" alt="MindIE Agent logo" width="128" height="128">
</p>

<h1 align="center">MindIE Agent</h1>

<p align="center">
  <b>让你的 AI 编程助手秒懂昇腾（Ascend）NPU 与大模型推理工程</b><br/>
  <i>Turn Claude Code, OpenAI Codex CLI, and Kimi Code into battle-tested Ascend NPU & LLM inference engineers.</i>
</p>

<p align="center">
  <a href="https://github.com/mindie-agent/mindie-agent"><img src="https://img.shields.io/badge/Release-v0.0.1-blue?style=flat-square" alt="Release v0.0.1"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-cc"><img src="https://img.shields.io/badge/Claude_Code-Plugin_Ready-D97757?style=flat-square" alt="Claude Code"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-codex"><img src="https://img.shields.io/badge/OpenAI_Codex-Plugin_Ready-10A37F?style=flat-square" alt="OpenAI Codex"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-kimi"><img src="https://img.shields.io/badge/Kimi_Code-Adapter_Ready-6366F1?style=flat-square" alt="Kimi Code"></a>
  <a href="https://github.com/mindie-agent/awesome-mindie-skills"><img src="https://img.shields.io/badge/Ascend_Skills-Curated-F59E0B?style=flat-square" alt="Awesome MindIE Skills"></a>
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

## 🌟 为什么需要 MindIE Agent？ / Why MindIE Agent?

通用编程大模型写常规代码很强，但在昇腾（Ascend）NPU 上跑大模型推理（如 `vLLM-Ascend`、CANN 算子适配、远端多卡调试、精度对齐与 Profiling）时，往往会遇到**不懂昇腾报错、SSH 长任务容易断、踩过的坑下次还会再踩**三大痛点。

**MindIE Agent** 不要求你更换顺手的客户端，而是通过原生插件把四大核心能力直接装进你的终端：
1. **远端昇腾开发（`remote-dev`）**：通过 SSH 直接读写远端文件、投递后台长任务、实时流式看日志与拉回 Profiling 产物。
2. **实战知识与经验闭环（`knowledge` + `knowledge-vllm-ascend`）**：检索经过验证的 `vLLM-Ascend` 排障知识包；本地排障成功后自动通过 Gitleaks 与确定性隐私规则脱敏沉淀。
3. **NPU 集群看板与卡池调度（`npu-top` + `coordinator`）**：一眼看清多节点 NPU 显存/算力占用，并为并发任务自动分配独占 NPU 租约。
4. **可定位结构化诊断（`diagnostics`）**：有界本地诊断日志与可选、去重的白名单故障自动上报。

---

## 🗺️ 开源仓库全景 / Repository Ecosystem

### 1. 主入口与开发者生态（Entry & Developer Ecosystem）

| 仓库 / Repository | 定位与核心用途 / What It Does |
|---|---|
| [`mindie-agent`](https://github.com/mindie-agent/mindie-agent) | **总入口**：产品架构、工程设计原则、一句话 Agent 自动安装协议与统一版本记录 |
| [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) | **开箱即用技能库**：面向 `vLLM-Ascend` 排障、昇腾 NPU 运维与算子开发的精选 Agent Skills |
| [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) | **本地多任务工作区**：一键拉起 `vllm` + `vllm-ascend` 独立 Git Worktree 的开发脚手架 |

### 2. 原生客户端插件（Native Agent Plugins）

| 仓库 / Repository | 定位与核心用途 / What It Does |
|---|---|
| [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) | **Claude Code 原生插件**（`v0.0.1` 已发布）：支持 macOS、原生 Windows 与 WSL |
| [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) | **OpenAI Codex CLI 原生插件**（`v0.0.1` 已发布）：支持 macOS、原生 Windows 与 WSL |
| [`mindie-agent-kimi`](https://github.com/mindie-agent/mindie-agent-kimi) | **Kimi Code 原生适配插件**：提供 `/skill:mindie` 技能、远端开发与知识闭环 |

### 3. 核心运行时组件与公共知识库（Core Runtimes & Public Knowledge）

| 仓库 / Repository | 定位与核心用途 / What It Does |
|---|---|
| [`knowledge`](https://github.com/mindie-agent/knowledge) | **知识与经验引擎**：本地经验提取、多层隐私脱敏、小模型目录生成、双层混合检索与社区分享 |
| [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) | **`vLLM-Ascend` 公共知识库**：经审核脱敏的真实昇腾排障与推理工程 Markdown 知识包 |
| [`remote-dev`](https://github.com/mindie-agent/remote-dev) | **SSH 远端开发引擎**：远端文件读写、补丁应用、受管持久后台作业与构建产物同步 |
| [`coordinator`](https://github.com/mindie-agent/coordinator) | **昇腾 NPU 协调器**：多任务 NPU 独占租约分配、就绪容器池与受管作业调度 |
| [`npu-top`](https://github.com/mindie-agent/npu-top) | **NPU 集群状态看板**：仅监听本地回环的昇腾 NPU 实时监控（支持 TUI、Web、CLI 与 MCP） |
| [`diagnostics`](https://github.com/mindie-agent/diagnostics) | **结构化诊断组件**：有界本地日志、错误定位编号与独立授权的 GitHub Issue 故障上报 |
