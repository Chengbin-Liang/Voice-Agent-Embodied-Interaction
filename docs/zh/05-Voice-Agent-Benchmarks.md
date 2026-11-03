# 05 · Voice Agent Benchmarks

**中文** | [English](../en/05-Voice-Agent-Benchmarks.md)

[返回首页](../../README.md) · [完整索引](../../resources/zh/CATALOG.md) · [Survey 对照](../../resources/zh/SURVEYS.md) · [Voice Agent 论文](03-Voice-Agent.md)

按“评测目标、实验协议与适用范围”选择评测。下列 18 个评测入口包含独立 benchmark、Full-Duplex-Bench 的不同任务版本和 MultiTalk 的配套测试集，不视为 18 套互不重叠的数据。核对日期：2026-11-03。

[🎧 基础回答、中文与声学鲁棒性](#foundations) · [⏱️ 轮次、打断与全双工行为](#turn) · [👥 多轮、长时与多人交互](#multi) · [🎛️ 交互指令与主动行为](#instructions) · [🧰 工具调用与最终任务完成](#tasks) · [🧭 选型](#selection)

<a id="selection"></a>
## 🧭 评测组合示例

| 目标 | 建议组合 | 分开报告的结果 |
|---|---|---|
| 通用语音助手 / 中文助手 | [VoiceBench](../../resources/zh/CATALOG.md#e59) + [VCB Bench](../../resources/zh/CATALOG.md#e61) | 内容能力、指令遵循、鲁棒性 |
| 连续全双工聊天 | [Full-Duplex-Bench](../../resources/zh/CATALOG.md#e16) + [MTR-DuplexBench](../../resources/zh/CATALOG.md#e65) | 交接/打断时序、多轮质量 |
| 能执行工具的语音 Agent | [VoiceAgentBench](../../resources/zh/CATALOG.md#e62) + [Full-Duplex-Bench-v3](../../resources/zh/CATALOG.md#e64) + [τ-Voice](../../resources/zh/CATALOG.md#e63) | 函数参数、口语干扰下的调用、环境终态成功 |
| 可控、主动或多人交互 | [Instruct-FD](../../resources/zh/CATALOG.md#e69) / [DuplexAct-Bench](../../resources/zh/CATALOG.md#e70) + [MP-Bench](../../resources/zh/CATALOG.md#e67) / [Duplex-MPE](../../resources/zh/CATALOG.md#e68) | 遵循指令、适时参与、适时沉默 |
| 业务语音系统的端到端体验 | [EVA-Bench](../../resources/zh/CATALOG.md#e71) + 固定真人任务 | 任务正确性、体验、端到端时延与失败恢复 |

<a id="foundations"></a>
## 🎧 基础回答、中文与声学鲁棒性

| Benchmark / 发表与归属 | 评测目标 | 数据与交互协议 | 适用边界 |
|---|---|---|---|
| ⭐ [VoiceBench](../../resources/zh/CATALOG.md#e59)<br>[![TACL 2026](https://img.shields.io/badge/TACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.tacl-1.18/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2410.17196)<br>[📄 论文](https://arxiv.org/abs/2410.17196) · [💻 仓库](https://github.com/MatthewCYM/VoiceBench) | 知识、指令遵循、安全；口音、噪声、混响等扰动。 | 真实与合成口语指令；以回答能力为主。 | 不直接测连续交互时序或工具任务完成。 |
| [VCB Bench](../../resources/zh/CATALOG.md#e61)<br>[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.1659/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2510.11098)<br>[📄 论文](https://arxiv.org/abs/2510.11098) · [💻 仓库](https://github.com/Tencent/VCB-Bench) | 真实中文语音指令、知识理解与鲁棒性。 | 真实人声为核心；区分原始中文协议与后续扩展。 | 不覆盖完整 Agent 环境终态。 |
| [VocalBench](../../resources/zh/CATALOG.md#e60)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2505.15727) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2505.15727)<br>[📄 论文](https://arxiv.org/abs/2505.15727) · [💻 仓库](https://github.com/SJTU-OmniAgent/VocalBench) | 语义、声学、对话、鲁棒性多个维度。 | 含单轮和多轮任务；各子集与语言分别报告。 | 高分不自动说明全双工自然或工具调用可靠。 |

<a id="turn"></a>
## ⏱️ 轮次、打断与全双工行为

| Benchmark / 发表与归属 | 评测目标 | 数据与交互协议 | 适用边界 |
|---|---|---|---|
| ⭐ [Full-Duplex-Bench](../../resources/zh/CATALOG.md#e16)<br>[![ASRU 2025](https://img.shields.io/badge/ASRU%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.04721) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2503.04721)<br>[📄 论文](https://arxiv.org/abs/2503.04721) · [💻 仓库](https://github.com/DanielLin94144/Full-Duplex-Bench) | 停顿、反馈、交接、打断；v2 扩展多轮。 | 按 v1 / v1.5 / v2 固定协议；v3 工具任务另列。 | v1 论文 ASRU 2025；共享仓库不表示所有版本同一论文。 |
| [FD-Bench](../../resources/zh/CATALOG.md#e73)<br>[![Interspeech 2025](https://img.shields.io/badge/Interspeech%202025-475569?style=flat-square)](https://www.isca-archive.org/interspeech_2025/peng25b_interspeech.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2507.19040)<br>[📄 论文](https://arxiv.org/abs/2507.19040) · [💻 仓库](https://github.com/pengyizhou/FD-Bench) | 多轮交互、打断、噪声与延迟。 | 合成全双工对话测试流程。 | 与 Full-Duplex-Bench 为不同团队的不同项目。 |
| [HumDial-FDBench](../../resources/zh/CATALOG.md#e66)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.21406) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.21406)<br>[📄 论文](https://arxiv.org/abs/2604.21406) · [💻 仓库](https://github.com/ASLP-lab/HumDial-FDBench) | 真实对话中的重叠、打断与反馈。 | 真实双声道人类会话；HumDial 挑战与公开榜单。 | 挑战名称与论文正式发表状态分开记录。 |
| [TurnBench](../../resources/zh/CATALOG.md#e74)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2608.25218) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2608.25218)<br>[📄 论文](https://arxiv.org/abs/2608.25218) · [💻 仓库](https://github.com/SesameAILabs/turnbench) · [🔗 项目](https://turnbench.sesame.com/) | 轮次结束与打断检测的召回、误报、决策延迟。 | 人类标注的双声道多域对话；固定误报预算。 | 组件级评价，不直接测生成内容与任务成功。 |

<a id="multi"></a>
## 👥 多轮、长时与多人交互

| Benchmark / 发表与归属 | 评测目标 | 数据与交互协议 | 适用边界 |
|---|---|---|---|
| ⭐ [MTR-DuplexBench](../../resources/zh/CATALOG.md#e65)<br>[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.263/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2511.10262)<br>[📄 论文](https://arxiv.org/abs/2511.10262) · [💻 仓库](https://github.com/ZhangHe0918/MTR-DuplexBench) | 逐轮交互动态、回答质量、指令遵循与安全。 | 将较长会话分段评价，观察随轮次累积的变化。 | 会话来源与数据使用条件按官方说明。 |
| [MultiTalk / MultiTalkBench](../../resources/zh/CATALOG.md#e43)<br>[![NeurIPS 2026 · 作者标注](https://img.shields.io/badge/NeurIPS%202026%20%C2%B7%20%E4%BD%9C%E8%80%85%E6%A0%87%E6%B3%A8-475569?style=flat-square)](https://arxiv.org/abs/2609.36903) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.36903)<br>[📄 论文](https://arxiv.org/abs/2609.36903) · [🔗 预训练数据](https://huggingface.co/datasets/MultiTalk/MultiTalkPT) · [🔗 微调数据](https://huggingface.co/datasets/MultiTalk/MultiTalkFT) · [🔗 Benchmark](https://huggingface.co/datasets/MultiTalk/MultiTalkBench) | 长时、多方、双语会话能力。 | MultiTalkBench 来自真实录音，平均会话约 32.6 分钟。 | 与 MultiTalkPT / FT 训练数据区分；不代表工具任务完成。 |
| [MP-Bench](../../resources/zh/CATALOG.md#e67)<br>[![Findings of EMNLP 2026](https://img.shields.io/badge/Findings%20of%20EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-emnlp.1437/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.13076)<br>[📄 论文](https://arxiv.org/abs/2609.13076) · [💻 仓库](https://github.com/atosystem/MP-Bench) | 作为多人参与者理解上下文、适时接话、合理回应。 | 多人会话参与协议。 | 本条为 atosystem/MP-Bench，勿与同名其他 benchmark 混淆。 |
| [Duplex-MPE](../../resources/zh/CATALOG.md#e68)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.31948) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.31948)<br>[📄 论文](https://arxiv.org/abs/2609.31948) · [🔗 项目](https://step-out.github.io/Duplex-MPE-Page/) | 明确点名、隐含求助、主动回应与保持沉默。 | 3–4 位人类与助手的场景，强调“是否应该参与”。 | 版本可能调整场景和基线，固定论文与数据版本。 |

<a id="instructions"></a>
## 🎛️ 交互指令与主动行为

| Benchmark / 发表与归属 | 评测目标 | 数据与交互协议 | 适用边界 |
|---|---|---|---|
| [Instruct-FD](../../resources/zh/CATALOG.md#e69)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2607.20460) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2607.20460)<br>[📄 论文](https://arxiv.org/abs/2607.20460) | 按指令改变接话、打断、反馈和主动性。 | 以交互指令遵循分数及相对变化评价行为。 | 依据论文协议；不将指标判分器当作真人体验。 |
| [DuplexAct-Bench](../../resources/zh/CATALOG.md#e70)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.39446) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.39446)<br>[📄 论文](https://arxiv.org/abs/2609.39446) · [💻 仓库](https://github.com/Alita-xky/DuplexAct-Bench) · [🔗 项目](https://alitaxky.icu/DuplexAct-Bench/) | 六类交互行为；时机与内容分别评价。 | 中英双语 1,290 个试次；含主动沉默与抵抗打断。 | 代码链接主要是项目页，完整评测器开放情况另核。 |

<a id="tasks"></a>
## 🧰 工具调用与最终任务完成

| Benchmark / 发表与归属 | 评测目标 | 数据与交互协议 | 适用边界 |
|---|---|---|---|
| ⭐ [VoiceAgentBench](../../resources/zh/CATALOG.md#e62)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.07978) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2510.07978)<br>[📄 论文](https://arxiv.org/abs/2510.07978) · [💻 仓库](https://github.com/ola-krutrim/VoiceAgentBench) · [🔗 数据](https://huggingface.co/datasets/krutrim-ai-labs/VoiceAgentBench) | 单步、并行、顺序工具调用，多轮和安全。 | 英语及六种印度语言的语音代理任务，检查函数和参数。 | 工具结构准确率与环境终态成功率分别报告。 |
| ⭐ [Full-Duplex-Bench-v3](../../resources/zh/CATALOG.md#e64)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.04847) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.04847)<br>[📄 论文](https://arxiv.org/abs/2604.04847) · [💻 仓库](https://github.com/DanielLin94144/Full-Duplex-Bench) · [🔗 项目](https://daniellin94144.github.io/FDB-v3-demo/) | 真实口语不流利条件下的多步工具使用。 | 真实人声中的重复、犹豫和自我修正；小规模诊断集。 | 与原版 FDB 的交互指标分开；不沿用 ASRU 2025 标签。 |
| ⭐ [τ-Voice](../../resources/zh/CATALOG.md#e63)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2603.13686) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2603.13686)<br>[📄 论文](https://arxiv.org/abs/2603.13686) · [💻 仓库](https://github.com/sierra-research/tau2-bench) | 领域规则、工具执行、环境终态的任务完成。 | 动态全双工用户模拟，含噪声和口音；可对照文本 Agent。 | 固定 tau2 对应版本，不混用后续 τ³ 开发协议。 |
| ⭐ [EVA-Bench](../../resources/zh/CATALOG.md#e71)<br>[![Findings of EMNLP 2026](https://img.shields.io/badge/Findings%20of%20EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-emnlp.2182/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2605.13841)<br>[📄 论文](https://arxiv.org/abs/2605.13841) · [💻 仓库](https://github.com/ServiceNow/eva) · [🔗 项目](https://servicenow.github.io/eva/) | EVA-A：任务与事实；EVA-X：时序与交互体验。 | 动态 bot-to-bot 模拟，检查用户模拟有效性和重复试验。 | 任务成功、体验评分及不同重复采样指标分别报告。 |
| [VAmoS Bench](../../resources/zh/CATALOG.md#e72)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2607.27453) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2607.27453)<br>[📄 论文](https://arxiv.org/abs/2607.27453) · [💻 仓库](https://github.com/veris-ai/riley-agent) | 金融服务任务、领域事实与工具执行轨迹。 | 模拟完整会话，按任务轨迹和领域规则评分。 | 结果适用于指定行业；参考代理与完整评分器分别核实。 |

## 🌐 补充在线评测入口

| 入口 | 使用方式 |
|---|---|
| [Artificial Analysis Speech Agent Arena](https://artificialanalysis.ai/articles/announcing-the-speech-agent-arena) | 参考人类对话偏好和真实任务体验；核对任务、模型版本及是否报告工具任务完成。 |
| [Pipecat Benchmarks](https://www.pipecat.ai/benchmarks) | 查看 PhoneBench 和语音组件测试；比较时保留服务配置、电话链路和 benchmark 版本。 |

## 📐 比较结果时保留的条件

1. **时延口径**：声学间隔、模型推理时延、包含网络和音频播放的端到端时延分别记录。
2. **因果输入**：在线系统只能看到当时已到达的音频；离线回放与实时服务结果分别报告。
3. **成功层级**：函数名/参数正确、工具真实执行、环境终态成功，以及用户听到正确反馈分开统计。
4. **实验协议**：固定模型、提示、工具环境、数据 split、模拟用户、判分器及运行次数；pass@k 与连续重复成功等指标不可混用。
5. **泛化范围**：合成语音、真人录音和真人在线交互分别报告；多人、噪声、口音、长对话以及打断恢复需要对应证据。

具身任务还需记录动作是否完成、目标是否正确、取消是否生效与人工接管；上述语音 benchmark 不能直接替代[机器人与真人协作评测](04-Edge-Embodied-Interaction.md)。
