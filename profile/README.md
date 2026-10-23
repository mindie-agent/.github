<p align="center">
  <img src="https://raw.githubusercontent.com/mindie-agent/mindie-agent/main/assets/brand/mindie-agent-logo.png" alt="MindIE Agent logo" width="128" height="128">
</p>

<h1 align="center">MindIE Agent</h1>

<p align="center">
  <b>面向昇腾（Ascend）NPU AI Infra 研发、设计与测试全流程的统一 Agent 能力底座</b><br/>
  <i>The unified AI Agent capability platform for Ascend NPU AI Infra — across architecture design, feature development, AscendC/Triton kernels, testing, and tuning.</i>
</p>

<p align="center">
  <a href="https://github.com/mindie-agent/mindie-agent/blob/main/docs/releases/0.1.0.md"><img src="https://img.shields.io/badge/Release-v0.1.0-7045F5?style=flat-square" alt="Release v0.1.0"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-cc"><img src="https://img.shields.io/badge/Claude_Code-Plugin_Ready-D97757?style=flat-square" alt="Claude Code"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-codex"><img src="https://img.shields.io/badge/OpenAI_Codex-Plugin_Ready-10A37F?style=flat-square" alt="OpenAI Codex"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-kimi"><img src="https://img.shields.io/badge/Kimi_Code-Plugin_Ready-2563EB?style=flat-square" alt="Kimi Code"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-dsh"><img src="https://img.shields.io/badge/DeepSeek_Harness-Plugin_Ready-0EA5E9?style=flat-square" alt="DeepSeek Harness"></a>
  <a href="https://github.com/mindie-agent/awesome-mindie-skills"><img src="https://img.shields.io/badge/Ascend_AI_Infra-vLLM--Ascend_%7C_AscendC_%7C_Triton-F59E0B?style=flat-square" alt="Ascend AI Infra Skills"></a>
</p>

<p align="center">
  <a href="https://github.com/mindie-agent/mindie-agent"><b>项目主入口 (Main Repo)</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent/blob/main/docs/releases/0.1.0.md"><b>v0.1.0 发布说明</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent/blob/main/docs/releases/0.1.0/design-philosophy.md"><b>作者自述</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent-cc"><b>Claude Code 插件</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent-codex"><b>Codex 插件</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent-kimi"><b>Kimi Code 插件</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent-dsh"><b>DSH 插件</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-bench"><b>MindIE Bench</b></a> ·
  <a href="https://github.com/mindie-agent/awesome-mindie-skills"><b>Awesome MindIE Skills</b></a>
</p>

---

## ⚡ 一句话无感安装 / One-Sentence Agent-Native Install

不需要手翻长篇配置文档——直接把下面这句话发给你正在使用的 **Claude Code**、**OpenAI Codex CLI**、**Kimi Code** 或 **DeepSeek Harness (DSH)**，让你的 Agent 自动完成检测、安装与配置：

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

1. **远端昇腾开发与测试闭环（`remote-dev`）**：通过 SSH 直接在远端昇腾容器内读写文件、应用补丁、投递长耗时编译/测试作业、流式查看日志并拉回构建与测试产物。
2. **领域知识与研发经验飞轮（`knowledge` + `knowledge-vllm-ascend` / `knowledge-operators`）**：按框架版本、硬件与适用条件检索分级知识单元；本地研发完成后通过确定性隐私规则脱敏提炼，经审核沉淀入库。
3. **实测性能剖析与四层理论仿真求解（`profiler` + `sim`）**：原地只读解析昇腾 Profiling 产物、关联 Host-Device 异步调用与跨 Run 对比（`mindie-profiler`），并结合多型号 SKU 硬件规格、算子微阶段流水、子图融合与整网并行开展四层理论边界求解（`mindie-sim`）。
4. **NPU 集群看板与卡池调度（`npu-top` + `coordinator`）**：一眼看清多节点 NPU 显存/算力占用与 90 天利用率热力图，并为多 Agent 并发任务自动探测环境、绑定容器与分配独占 NPU/端口租约。
5. **可定位结构化诊断与真机基准评测（`diagnostics` + `mindie-bench`）**：提供有界本地诊断日志与可选白名单去重故障上报，并通过固定任务与真机基准持续度量任务结题率、跨任务复用收益与端到端总工程成本。

---

## 🗺️ 开源仓库全景 / Repository Ecosystem

### 1. 主入口、评测基准与开发者生态（Entry, Benchmarks & Developer Ecosystem）

| 仓库 / Repository | 定位与核心用途 / What It Does |
|---|---|
| [`mindie-agent`](https://github.com/mindie-agent/mindie-agent) | **总入口**：产品架构、工程设计原则、一句话 Agent 自动安装协议与统一版本记录 |
| [`mindie-bench`](https://github.com/mindie-agent/mindie-bench) | **真机基准与评测框架**：固定任务与 Oracle、隔离宿主运行、组件级基准、跨任务知识复用及端到端总工程成本评测 |
| [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) | **开箱即用技能库**：覆盖昇腾 AI Infra 开发、测试、算子实现（`AscendC` / `Triton`）与 `vLLM-Ascend` 工程的精选 Agent Skills（持续扩展中） |
| [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) | **本地多任务工作区**：一键拉起 `vllm` + `vllm-ascend` 独立 Git Worktree 的开发与测试脚手架 |

### 2. 原生客户端插件（Native Agent Plugins）

| 仓库 / Repository | 定位与核心用途 / What It Does |
|---|---|
| [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) | **Claude Code 原生插件**（配套 `v0.1.0` 已发布）：支持 macOS、原生 Windows 与 WSL |
| [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) | **OpenAI Codex CLI 原生插件**（配套 `v0.1.0` 已发布）：支持 macOS、原生 Windows 与 WSL |
| [`mindie-agent-kimi`](https://github.com/mindie-agent/mindie-agent-kimi) | **Kimi Code CLI 原生插件**（配套 `v0.1.0` 已发布）：提供 `/mindie-agent` 统一入口、代数原子更新、远端 NPU 开发测试与知识闭环 |
| [`mindie-agent-dsh`](https://github.com/mindie-agent/mindie-agent-dsh) | **DeepSeek Harness (DSH) 原生插件**（配套 `v0.1.0` 已发布）：复用宿主插件机制组合提供 `/mindie-agent` Skill、领域知识检索、生命周期桥接与 `remote-dev` |

### 3. 核心运行时组件（Core Runtime Components）

| 仓库 / Repository | 定位与核心用途 / What It Does |
|---|---|
| [`knowledge`](https://github.com/mindie-agent/knowledge) | **知识与经验引擎（`mindie-knowledge`）**：L1–L4 分级知识单元、条件检索、多领域分片路由、精确修订反馈、双层隐私脱敏与经审核的社区发布闭环 |
| [`remote-dev`](https://github.com/mindie-agent/remote-dev) | **SSH 远端开发引擎（`remote-dev`）**：远端文件读写、精确补丁、容器直连、受管持久后台作业与构建/测试产物同步 |
| [`coordinator`](https://github.com/mindie-agent/coordinator) | **昇腾 NPU 环境协调器（`mindie-coordinator`）**：SSH 主机/免密/多机互通、就绪容器池绑定与开通、NPU/挂载探测（`mindie_probe`）、独占 NPU/端口租约仲裁（`mindie_lease`）与受管任务调度 |
| [`profiler`](https://github.com/mindie-agent/profiler) | **昇腾实测性能剖析组件（`mindie-profiler`）**：昇腾 Profiling 受控采集、`inventory / analyze / correlate / compare / sql` 原地只读解析、显存证据提取与跨 Run 对比 CLI |
| [`sim`](https://github.com/mindie-agent/sim) | **昇腾四层仿真与边界求解器（`mindie-sim`）**：多型号 A2/A3/A5 `DeviceCapabilityProfile`、7 类全路径 `D2D`/`H2D`/`D2H`/`RH2D`/`RD2H` 传输边界、算子微阶段周期依赖图求解、Phase 0 子图融合分析与整网并行推演 |
| [`npu-top`](https://github.com/mindie-agent/npu-top) | **NPU 集群状态看板（`npu-top`）**：仅监听本地回环的昇腾 NPU 实时监控台（支持 Web 看板、TUI、CLI/MCP 与 90 天利用率热力图） |
| [`diagnostics`](https://github.com/mindie-agent/diagnostics) | **结构化诊断底座（`mindie-diagnostics`）**：CANN/`plog` 确定性报错解析、4×1 MiB 本地 JSONL 轮转日志、离线脱敏支持包与可选白名单去重 GitHub Issue 故障上报 |

### 4. 昇腾领域公共知识库（Public Domain Knowledge Corpora）

| 仓库 / Repository | 定位与核心用途 / What It Does |
|---|---|
| [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) | **`vLLM-Ascend` 领域公共知识库（`vllm-ascend`）**：新模型 0day 接入、PD 分离、MoE EP/MC2、量化、投机解码与 ACLGraph/TorchAir 调优知识单元 |
| [`knowledge-operators`](https://github.com/mindie-agent/knowledge-operators) | **昇腾算子领域公共知识库（`operators`）**：910B/910C/950 硬件约束、`AscendC`、`Triton-Ascend`、TBE/AKG 编译排障与融合调优知识单元 |
| [`knowledge-infer-core`](https://github.com/mindie-agent/knowledge-infer-core) | **推理服务与引擎核心知识库（`infer-core`）**：MindIE Server / Service / LLM / Motor 部署配置、Batch 调度、KV Cache 管理与多模态服务知识单元 |
| [`knowledge-infer-distributed`](https://github.com/mindie-agent/knowledge-infer-distributed) | **分布式推理与集合通信知识库（`infer-distributed`）**：HCCL 通信排障、RoCE/HCCS 拓扑与 Ranktable 校验、SHMEM 及多机 DP/TP/EP/PP/CP 并行知识单元 |
| [`knowledge-infer-observability`](https://github.com/mindie-agent/knowledge-infer-observability) | **推理可观测性、诊断与评测知识库（`infer-observability`）**：CANN/`plog`/Device 故障诊断、`msprof` 性能拆解、精度对齐与基准测量知识单元 |
| [`knowledge-infer-ops-compat`](https://github.com/mindie-agent/knowledge-infer-ops-compat) | **图编译、算子注册与迁移兼容知识库（`infer-ops-compat`）**：TorchAir/ACLGraph 图捕获排障、自定义算子注册、CUDA 迁移适配与运行时兼容知识单元 |
| [`knowledge-agent-engineering`](https://github.com/mindie-agent/knowledge-agent-engineering) | **Agent 工程与治理知识库（`agent-engineering`）**：多 Agent 协同编排、知识提炼治理、双层隐私脱敏门禁、CI 发布校验与基准评测知识单元 |

---

## 📊 开源仓库与下载统计 / Repository Statistics

<p align="center">
  <a href="https://github.com/mindie-agent/mindie-agent/blob/telemetry-data/README.md">
    <img src="https://raw.githubusercontent.com/mindie-agent/mindie-agent/telemetry-data/dashboard.zh.svg" alt="MindIE Agent 开源仓库与下载统计" width="100%">
  </a>
</p>
