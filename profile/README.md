<p align="center">
  <img src="https://raw.githubusercontent.com/mindie-agent/mindie-agent/main/assets/brand/mindie-agent-logo.png" alt="MindIE Agent logo" width="128" height="128">
</p>

<h1 align="center">MindIE Agent</h1>

<p align="center">
  <b>为原生编程 Agent 提供昇腾（Ascend）领域知识、远端 NPU 执行与可追溯的工程经验</b><br/>
  <i>Ascend domain knowledge, remote NPU execution, and traceable engineering experience for native coding agents.</i>
</p>

<!-- mindie-org-versions:org-badges:start -->
<p align="center">
  <a href="https://github.com/mindie-agent/mindie-agent/blob/main/docs/releases/0.1.4.md"><img src="https://img.shields.io/github/v/release/mindie-agent/mindie-agent?label=Release&color=7045F5&style=flat-square" alt="Release v0.1.4"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-cc"><img src="https://img.shields.io/badge/Claude_Code-Plugin_Ready-D97757?style=flat-square" alt="Claude Code"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-codex"><img src="https://img.shields.io/badge/OpenAI_Codex-Plugin_Ready-10A37F?style=flat-square" alt="OpenAI Codex"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-kimi"><img src="https://img.shields.io/badge/Kimi_Code-Plugin_Ready-2563EB?style=flat-square" alt="Kimi Code"></a>
  <a href="https://github.com/mindie-agent/mindie-agent-dsh"><img src="https://img.shields.io/badge/DeepSeek_Harness-Plugin_Ready-0EA5E9?style=flat-square" alt="DeepSeek Harness"></a>
  <a href="https://github.com/mindie-agent/awesome-mindie-skills"><img src="https://img.shields.io/badge/Ascend_AI_Infra-vLLM--Ascend_%7C_AscendC_%7C_Triton-0F766E?style=flat-square" alt="Ascend AI Infra Skills"></a>
</p>

<p align="center">
  <a href="https://github.com/mindie-agent/mindie-agent"><b>项目主入口 (Main Repo)</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent/blob/main/docs/releases/0.1.4.md"><b>v0.1.4 发布说明</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent/blob/main/docs/releases/0.1.0.md"><b>v0.1.0 里程碑</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent/blob/main/docs/releases/0.1.0/design-philosophy.md"><b>作者自述</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent-cc"><b>Claude Code 插件</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent-codex"><b>Codex 插件</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent-kimi"><b>Kimi Code 插件</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-agent-dsh"><b>DSH 插件</b></a> ·
  <a href="https://github.com/mindie-agent/mindie-bench"><b>MindIE Bench</b></a> ·
  <a href="https://github.com/mindie-agent/awesome-mindie-skills"><b>Awesome MindIE Skills</b></a>
</p>
<!-- mindie-org-versions:org-badges:end -->

---

## ⚡ 一句话无感安装 / One-Sentence Agent-Native Install

不需要手动翻长篇配置文档——直接把下面这句话发给你正在使用的 **Claude Code**、**OpenAI Codex CLI**、**Kimi Code** 或 **DeepSeek Harness (DSH)**，让你的 Agent 自动完成检测、安装与工作区引导：

```text
帮我安装一下这个 https://github.com/mindie-agent/mindie-agent
```
*(English: `Please install MindIE Agent for me: https://github.com/mindie-agent/mindie-agent`)*

---

## 🔥 装好之后怎么用？ / How to Use After Installation

MindIE Agent 坚持**用户侧极简单一入口 + Agent 侧上下文按需渐进式披露**——你只需要记住 **`/mindie-agent`** 这一个入口，不需要背任何内部子命令：

- **🧠 当前会话手动输入 `/mindie-agent`（唤醒昇腾领域知识、经验与 Skill 系统）**：在做新模型 0day 接入、`vLLM-Ascend` 特性开发、`AscendC` / `Triton` 算子实现、精度测试或性能调优时，在当前会话输入一次 `/mindie-agent`（Codex 中也可输入 `$mindie-agent`）并描述需求，本会话后续轮次即持续启用按需知识检索、反馈、经验提炼与同步：
  ```text
  /mindie-agent 我准备在 vllm-ascend 中为新模型实现一个自定义融合算子（支持 Triton / AscendC），请结合现有工程规范与算子适配经验帮我梳理实现方案和单测验证点。
  ```
- **⚡ 日常对话默认自动触发 `remote-dev` 与确定性工具（无需斜杠命令，直连远端 NPU）**：`remote-dev`、`coordinator`、`profiler`、`sim` 与 `diagnostics` 作为常驻 MCP 工具默认就绪。日常对话中只要提到远端服务器、容器、NPU 选卡、Profiling 解析或性能建模，Agent 就会自动调用对应工具：
  ```text
  连上远端机器 192.0.2.21（端口 22）上的 vllm-dev 容器，把我刚写的算子代码和 tests/ 下的单测同步过去，在 NPU 上跑一下完整的 pytest 精度与性能测试。
  ```
- **🔄 研发经验按授权自动沉淀（一次授权，在 `/mindie-agent` 会话中自动运行）**：贡献授权配置一次跨会话生效。在已通过 `/mindie-agent` 启用的会话结束时，系统自动在授权项目范围内完成本地双层脱敏（确定性规则 + Gitleaks），将验证通过的排障与调优方案提炼为结构化知识单元，经审核后入库复用或按需提交社区 PR（未调用 `/mindie-agent` 的普通会话不触发采集）。

---

## 🌟 为什么需要 MindIE Agent？ / Why MindIE Agent?

通用编程大模型写常规业务代码很顺手，但在昇腾（Ascend）NPU 上开展 AI Infra 研发（从模型 0day 适配、`AscendC` / `Triton` 算子开发，到远端多卡容器验证、精度对齐与性能调优）时，往往卡在三个现实问题上：**缺少昇腾软硬件栈与版本适用条件上下文、本地写代码与远端 NPU 容器验证割裂、好不容易调通的排障与优化经验随会话结束就丢了**。

**MindIE Agent** 在你原本熟悉的编程客户端里直接补齐这三块能力：

1. **远端昇腾开发与测试闭环（`remote-dev`）**：通过 SSH 直接在远端昇腾主机和容器内读写文件、应用补丁、投递长耗时编译/测试后台作业、流式查看日志并共享用户私有 SSH 凭据与公钥。
2. **带适用条件的领域知识与经验飞轮（`knowledge` + 7 大领域知识库）**：按框架版本、硬件型号和输入条件检索 L1–L4 分级知识单元，缺失前提绝不盲目套用；研发验证通过后经本地脱敏与审核沉淀入库。
3. **实测性能剖析与五层因果仿真（`profiler` + `sim`）**：原地只读解析昇腾 `msprof` 产物、按 `mindie-model-structure/1` 对齐模型结构并自动切分 Decode/Prefill（`mindie-profiler`）；统一组合硬件资源、算子族、子图、纯模型成本与服务约束，输出 4D 效率拆解（`Cube_MFU / Vec_MFU / MBU / Link_Util / CV_Overlap`）与 SLA 硬件配比推演（`mindie-sim`）。
4. **多 Agent 资源协调与集群看板（`coordinator` + `npu-top`）**：为多 Agent 并发任务自动探测 A2/A3 双 Die/A5 拓扑、绑定容器、预检 HCCL/RoCE 并分配独占 NPU/端口租约，配合本地 Web 看板实时查看 90 天利用率热力图。
5. **确定性故障诊断与真机基准评测（`diagnostics` + `mindie-bench`）**：自动解析 CANN/`plog` 根因并隔离级联超时，通过 20 个行为级验证基准任务持续度量任务结题率、跨任务复用收益与端到端总工程成本。

---

## 🗺️ 开源仓库全景 / Repository Ecosystem

<!-- mindie-org-versions:org-ecosystem:start -->
### 1. 主入口、评测基准与开发者生态（Entry, Benchmarks & Developer Ecosystem）

| 仓库 / Repository | 当前版本 / Version | 定位与核心用途 / What It Does |
|---|---|---|
| [`mindie-agent`](https://github.com/mindie-agent/mindie-agent) | [`v0.1.4`](https://github.com/mindie-agent/mindie-agent/releases/tag/v0.1.4) | **总入口**：产品架构、工程设计原则、一句话 Agent 自动安装协议与统一版本记录 |
| [`mindie-bench`](https://github.com/mindie-agent/mindie-bench) | [`v0.4.5`](https://github.com/mindie-agent/mindie-bench/releases/tag/v0.4.5) | **真机基准与评测框架**：20 个行为级验证任务、隔离宿主运行、组件级基准、跨任务知识复用及端到端总工程成本评测 |
| [`awesome-mindie-skills`](https://github.com/mindie-agent/awesome-mindie-skills) | [`main`](https://github.com/mindie-agent/awesome-mindie-skills) | **开箱即用技能库**：覆盖昇腾 AI Infra 开发、测试、算子实现（`AscendC` / `Triton`）与 `vLLM-Ascend` 工程的精选 Agent Skills |
| [`vllm-ascend-workspace`](https://github.com/mindie-agent/vllm-ascend-workspace) | [`main`](https://github.com/mindie-agent/vllm-ascend-workspace) | **本地多任务工作区**：一键拉起 `vllm` + `vllm-ascend` 独立 Git Worktree 的开发与测试脚手架 |

### 2. 原生客户端插件（Native Agent Plugins）

| 仓库 / Repository | 适用宿主 / Host | 当前版本 / Version | 定位与核心用途 / What It Does |
|---|---|---|---|
| [`mindie-agent-cc`](https://github.com/mindie-agent/mindie-agent-cc) | **Claude Code** | [`v0.1.10`](https://github.com/mindie-agent/mindie-agent-cc/releases/tag/v0.1.10) | Claude Code 原生插件：支持 macOS、原生 Windows 与 WSL，注册 `knowledge`、`remote` 与 `components` 三大 MCP 服务 |
| [`mindie-agent-codex`](https://github.com/mindie-agent/mindie-agent-codex) | **OpenAI Codex CLI** | [`v0.1.13`](https://github.com/mindie-agent/mindie-agent-codex/releases/tag/v0.1.13) | OpenAI Codex CLI 原生插件：支持 macOS、原生 Windows 与 WSL，提供按需知识检索、远端 NPU 开发与后台静默更新 |
| [`mindie-agent-kimi`](https://github.com/mindie-agent/mindie-agent-kimi) | **Kimi Code CLI** | [`v0.1.10`](https://github.com/mindie-agent/mindie-agent-kimi/releases/tag/v0.1.10) | Kimi Code CLI 原生插件：提供 `/mindie-agent` 统一入口、旁路原子更新、远端 NPU 开发测试与经验闭环 |
| [`mindie-agent-dsh`](https://github.com/mindie-agent/mindie-agent-dsh) | **DeepSeek Harness (DSH)** | [`v0.1.9`](https://github.com/mindie-agent/mindie-agent-dsh/releases/tag/v0.1.9) | DeepSeek Harness 原生插件：复用宿主插件机制组合提供 `/mindie-agent` Skill、领域知识检索、确定性组件工具与 `remote-dev` |

### 3. 核心运行时组件（Core Runtime Components）

| 仓库 / Repository | Python 包 / Package | 当前版本 / Version | 定位与核心用途 / What It Does |
|---|---|---|---|
| [`knowledge`](https://github.com/mindie-agent/knowledge) | `mindie-knowledge` | [`v0.13.7`](https://github.com/mindie-agent/knowledge/releases/tag/v0.13.7) | **知识与经验引擎**：L1–L4 分级知识单元、按信息缺口条件检索、多领域分片路由、精确修订反馈、双层隐私脱敏与经审核的社区 PR 发布 |
| [`remote-dev`](https://github.com/mindie-agent/remote-dev) | `remote-dev` | [`v0.11.2`](https://github.com/mindie-agent/remote-dev/releases/tag/v0.11.2) | **SSH 远端开发引擎**：远端文件读写、精确补丁、跨进程共享用户私有 SSH 凭据与密钥维护、容器直连、受管后台作业与产物同步 |
| [`coordinator`](https://github.com/mindie-agent/coordinator) | `mindie-coordinator` | [`v0.7.0`](https://github.com/mindie-agent/coordinator/releases/tag/v0.7.0) | **昇腾 NPU 环境协调器**：SSH 主机/多机互通、容器池开通与绑定、NPU 拓扑探测（兼容 A2/A3 双 Die/A5）、HCCL/RoCE 预检及独占 NPU/端口租约防冲突 |
| [`profiler`](https://github.com/mindie-agent/profiler) | `mindie-profiler` | [`v0.5.3`](https://github.com/mindie-agent/profiler/releases/tag/v0.5.3) | **昇腾实测性能剖析组件**：受控采集、`msprof` 原地只读解析（`inventory / analyze / correlate / compare / sql`）、`mindie-model-structure/1` 模型结构对齐与 Decode 自动切分 |
| [`sim`](https://github.com/mindie-agent/sim) | `mindie-sim` | [`v0.8.1`](https://github.com/mindie-agent/sim/releases/tag/v0.8.1) | **五层因果性能建模组件**：统一建模硬件资源、算子族、子图、纯模型成本与服务约束，支持 4D 效率拆解（`Cube_MFU / Vec_MFU / MBU / Link_Util / CV_Overlap`）与 SLA 硬件配比推演 |
| [`npu-top`](https://github.com/mindie-agent/npu-top) | `npu-top` | [`v0.3.0`](https://github.com/mindie-agent/npu-top/releases/tag/v0.3.0) | **NPU 集群状态看板**：仅监听本地回环的昇腾 NPU 实时监控台（支持 Web 看板、TUI、CLI/MCP 与 90 天利用率热力图） |
| [`diagnostics`](https://github.com/mindie-agent/diagnostics) | `mindie-diagnostics` | [`v0.5.4`](https://github.com/mindie-agent/diagnostics/releases/tag/v0.5.4) | **结构化诊断底座**：CANN/`plog` 确定性报错解析、4×1 MiB 本地 JSONL 轮转日志、离线脱敏支持包与可选白名单去重 GitHub Issue 故障上报 |

### 4. 昇腾领域公共知识库（Public Domain Knowledge Corpora）

| 仓库 / Repository | 领域 / Domain | 知识规模 / Scale | 定位与核心用途 / What It Does |
|---|---|---|---|
| [`knowledge-vllm-ascend`](https://github.com/mindie-agent/knowledge-vllm-ascend) | `vllm-ascend` | 91 单元 · [`d3d5bf63`](https://github.com/mindie-agent/knowledge-vllm-ascend/tree/d3d5bf6320e171d4a0f131a6f746858700e0c4cc) | **`vLLM-Ascend` 与 `vLLM-Omni` 知识库**：新模型 0day 接入、PD 分离、MoE EP/MC2、量化、投机解码、ACLGraph/TorchAir 与全模态流水线调优 |
| [`knowledge-operators`](https://github.com/mindie-agent/knowledge-operators) | `operators` | 105 单元 · [`6f083f81`](https://github.com/mindie-agent/knowledge-operators/tree/6f083f810c0d8eb77b9d7992ba96b19c51dfaf74) | **昇腾算子工程知识库**：910B/910C(A3)/950(A5) 硬件约束、`AscendC`、`Triton-Ascend`、Catlass、FlashAttention/MLA、Matmul/MoE 融合与稀疏注意力算子 |
| [`knowledge-infer-core`](https://github.com/mindie-agent/knowledge-infer-core) | `infer-core` | 109 单元 · [`b319ab36`](https://github.com/mindie-agent/knowledge-infer-core/tree/b319ab36f1b2d84c5d9c33b123ca2c24e6637f80) | **推理服务与引擎核心知识库**：`cann-recipes-infer` 模型优化 Recipe、`MindIE-SD` 扩散模型稀疏注意力、跨步缓存（`DiTCache`）、3D VAE 切片解码与动态时步量化 |
| [`knowledge-infer-distributed`](https://github.com/mindie-agent/knowledge-infer-distributed) | `infer-distributed` | 39 单元 · [`4cfe3db3`](https://github.com/mindie-agent/knowledge-infer-distributed/tree/4cfe3db3f7610acbded3a4c34f7551e88aba9b77) | **分布式推理与集合通信知识库**：HCCL 通信排障、RoCE/HCCS 拓扑、SHMEM、Mooncake/Yuanrong 传输与多机 DP/TP/EP/PP/CP 并行调优 |
| [`knowledge-infer-observability`](https://github.com/mindie-agent/knowledge-infer-observability) | `infer-observability` | 39 单元 · [`13a308e3`](https://github.com/mindie-agent/knowledge-infer-observability/tree/13a308e33f3c24b7222faa296024739351771f48) | **推理可观测性、诊断与评测知识库**：CANN/`plog`/Device 故障分诊、`msprof` 性能拆解、容量/性能仿真与 `perf-gate` / `accuracy-gate` 评测规程 |
| [`knowledge-infer-ops-compat`](https://github.com/mindie-agent/knowledge-infer-ops-compat) | `infer-ops-compat` | 34 单元 · [`bc594941`](https://github.com/mindie-agent/knowledge-infer-ops-compat/tree/bc59494157f0bf000ac7d05f6719aa487d062260) | **图编译、算子注册与迁移兼容知识库**：TorchAir/ACLGraph 图捕获、`torch_npu._inductor` Pass 开发、CUDA 至昇腾迁移与容器部署 |
| [`knowledge-agent-engineering`](https://github.com/mindie-agent/knowledge-agent-engineering) | `agent-engineering` | 33 单元 · [`6cf68034`](https://github.com/mindie-agent/knowledge-agent-engineering/tree/6cf68034126486934bf96d96d809c3de1e608b5f) | **Agent 工程与治理知识库**：多 Agent 协同编排、`MindIE-SD` S0–S6 自动调优闭环、`kb-lint` 质量门禁、双层隐私脱敏与真机基准评测方法 |
<!-- mindie-org-versions:org-ecosystem:end -->

---

## 📊 开源仓库与下载统计 / Repository Statistics

<p align="center">
  <a href="https://github.com/mindie-agent/mindie-agent/blob/telemetry-data/README.md">
    <img src="https://raw.githubusercontent.com/mindie-agent/mindie-agent/telemetry-data/dashboard.zh.svg" alt="MindIE Agent 开源仓库与下载统计" width="100%">
  </a>
</p>
