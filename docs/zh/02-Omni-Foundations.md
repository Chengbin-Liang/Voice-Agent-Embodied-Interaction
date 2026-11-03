# 02 · ALM / Omni 基础

**中文** | [English](../en/02-Omni-Foundations.md)

[返回首页](../../README.md) · [完整索引](../../resources/zh/CATALOG.md#omni) · [Survey 对照](../../resources/zh/SURVEYS.md)

从音频语言模型（Audio Language Model, ALM）进入语音生成、实时对话与音视频联合理解。

[阅读路线](#route) · [工业与联合基座](#bases) · [学术方法与适配](#methods) · [实时与音视频](#realtime) · [数据与训练](#training) · [评测](#evaluation)

<a id="route"></a>
## 🧭 四项基础概念

| 问题 | 优先阅读 | 核心概念 |
|---|---|---|
| 音频怎样进入 LLM？ | ⭐ [Qwen2-Audio](../../resources/zh/CATALOG.md#e80) → [SALMONN](../../resources/zh/CATALOG.md#e86) / [BLSP](../../resources/zh/CATALOG.md#e88) | 音频编码器、适配器、连续表示，以及转写遗漏的声音信息。 |
| LLM 怎样生成语音？ | ⭐ [SpeechGPT](../../resources/zh/CATALOG.md#e87) → [GLM-4-Voice](../../resources/zh/CATALOG.md#e81) / [LLaMA-Omni2](../../resources/zh/CATALOG.md#e89) | 离散单元、语音 codec、文本与语音的预测顺序、波形解码。 |
| 全双工语音交互如何建模？ | ⭐ [Moshi](../../resources/zh/CATALOG.md#e07) → [PersonaPlex](../../resources/zh/CATALOG.md#e90) → [全双工训练](03-Voice-Agent.md#academic) | 输入和输出音频流、轮次、时间对齐、打断与角色控制。 |
| 怎样接入视觉与持续视频？ | ⭐ [Qwen2.5-Omni](../../resources/zh/CATALOG.md#e02) → [MiniCPM-o](../../resources/zh/CATALOG.md#e01) / [Qwen3-Omni](../../resources/zh/CATALOG.md#e03) | 模态编码、共享时间轴、Thinker–Talker 与并发推理。 |

组件入口：[Whisper](https://github.com/openai/whisper)（语音编码/识别）· [SpeechTokenizer](https://github.com/ZhangXInFD/SpeechTokenizer)（语音 token）· [Moshi / Mimi](https://github.com/kyutai-labs/moshi)（流式 codec）· [CosyVoice](https://github.com/FunAudioLLM/CosyVoice)（语音生成）。

<a id="bases"></a>
## 🏭 工业与联合基座：理解能力与可用接口

| 论文 / 项目 | 发表与来源 | 阅读重点与入口 |
|---|---|---|
| ⭐ [Qwen2-Audio](../../resources/zh/CATALOG.md#e80) | [![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2407.10759) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2407.10759) | 7B 音频语言模型，以音频理解和文本回答为主，覆盖语音、声音与音乐。<br>[📄 论文](https://arxiv.org/abs/2407.10759) · [💻 仓库](https://github.com/QwenLM/Qwen2-Audio) |
| [GLM-4-Voice](../../resources/zh/CATALOG.md#e81) | [![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2412.02612) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2412.02612) | 9B 语音对话模型，结合离散语音 token、语音文本交错建模与流式解码。<br>[📄 论文](https://arxiv.org/abs/2412.02612) · [💻 仓库](https://github.com/zai-org/GLM-4-Voice) |
| ⭐ [Audio Flamingo 3](../../resources/zh/CATALOG.md#e82) | [![NeurIPS Spotlight 2025](https://img.shields.io/badge/NeurIPS%20Spotlight%202025-475569?style=flat-square)](https://openreview.net/forum?id=FjByDpDVIO) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2507.08128) | 7B 音频语言模型，研究语音、声音、音乐理解与音频推理，提供训练、数据和推理入口。<br>[📄 论文](https://arxiv.org/abs/2507.08128) · [💻 仓库](https://github.com/NVIDIA/audio-flamingo) · [🔗 Training / 训练](https://github.com/NVIDIA/audio-flamingo/tree/audio_flamingo_3) |
| [Audio Flamingo Next](../../resources/zh/CATALOG.md#e83) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.10905) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2604.10905) | 扩展长音频、时间定位、说话人归属和多说话人推理。<br>[📄 论文](https://arxiv.org/abs/2604.10905) · [🔗 Weights / 权重](https://huggingface.co/nvidia/audio-flamingo-next-hf) |
| ⭐ [MiMo-Audio](../../resources/zh/CATALOG.md#e84) | [![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2512.23808) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2512.23808) | 7B 语音基座与指令模型；官方微调工具支持识别、合成、音频理解和口语对话。<br>[📄 论文](https://arxiv.org/abs/2512.23808) · [💻 仓库](https://github.com/XiaomiMiMo/MiMo-Audio) · [🔗 Training / 训练](https://github.com/XiaomiMiMo/MiMo-Audio-Training) |
| [Step-Audio 2](../../resources/zh/CATALOG.md#e85) | [![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2507.16632) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2507.16632) | 面向多模态语音交互、音频推理与工具使用；提供 Mini 系列检查点和推理实现。<br>[📄 论文](https://arxiv.org/abs/2507.16632) · [💻 仓库](https://github.com/stepfun-ai/Step-Audio2) |
| [PersonaPlex](../../resources/zh/CATALOG.md#e90) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.06053) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2602.06053) | 基于 Moshi 的 7B 全双工对话模型，通过声音与文本提示控制说话人和角色。<br>[📄 论文](https://arxiv.org/abs/2602.06053) · [💻 仓库](https://github.com/NVIDIA/personaplex) |

适配入口：⭐ [MiMo-Audio 官方 SFT](https://github.com/XiaomiMiMo/MiMo-Audio-Training)；⭐ [Audio Flamingo 3 训练分支](https://github.com/NVIDIA/audio-flamingo/tree/audio_flamingo_3)。Audio Flamingo Next 的 HF 检查点输出文本；PersonaPlex 的官方入口侧重推理与角色控制。

训练框架补充：[SLAM-LLM](https://github.com/X-LANCE/SLAM-LLM)，查看语音编码器、适配器与 LLM 的组合训练示例。

<a id="methods"></a>
## 🎓 学术方法与基座适配

| 论文 / 项目 | 发表与来源 | 阅读重点与入口 |
|---|---|---|
| ⭐ [SALMONN](../../resources/zh/CATALOG.md#e86) | [![ICLR 2024](https://img.shields.io/badge/ICLR%202024-475569?style=flat-square)](https://github.com/bytedance/SALMONN/tree/salmonn) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2310.13289) | 融合语音与通用音频编码器，通过适配器与 LLM 连接语音、声音和音乐任务。<br>[📄 论文](https://arxiv.org/abs/2310.13289) · [💻 仓库](https://github.com/bytedance/SALMONN) · [🔗 Training / 训练](https://github.com/bytedance/SALMONN/tree/salmonn) |
| ⭐ [SpeechGPT](../../resources/zh/CATALOG.md#e87) | [![EMNLP Findings 2023](https://img.shields.io/badge/EMNLP%20Findings%202023-475569?style=flat-square)](https://aclanthology.org/2023.findings-emnlp.1055/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2305.11000) | 利用离散语音单元与 SpeechInstruct，将文本 LLM 扩展到语音输入输出。<br>[📄 论文](https://arxiv.org/abs/2305.11000) · [💻 仓库](https://github.com/0nutation/SpeechGPT) |
| ⭐ [BLSP](../../resources/zh/CATALOG.md#e88) | [![arXiv 2023](https://img.shields.io/badge/arXiv%202023-475569?style=flat-square)](https://arxiv.org/abs/2309.00916) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2309.00916) | 通过语音和转写的续写行为对齐，训练冻结语音编码器与 LLM 之间的轻量适配器。<br>[📄 论文](https://arxiv.org/abs/2309.00916) · [💻 仓库](https://github.com/cwang621/blsp) |
| ⭐ [LLaMA-Omni2](../../resources/zh/CATALOG.md#e89) | [![ACL 2025](https://img.shields.io/badge/ACL%202025-475569?style=flat-square)](https://aclanthology.org/2025.acl-long.912/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2505.02625) | 在 Qwen2.5 上构建双语语音对话与流式语音生成，公开多种模型规模与推理代码。<br>[📄 论文](https://arxiv.org/abs/2505.02625) · [💻 仓库](https://github.com/ictnlp/LLaMA-Omni2) |

| 方法线索 | 初始化与改动 | 可复现的研究问题 |
|---|---|---|
| BLSP | 现有语音编码器 + LLM，训练轻量适配器 | 语音输入和文本输入是否产生一致的任务行为？ |
| SALMONN | 语音与通用音频编码器 + LLM | 加入非语音声音信息，哪些任务因此改善？ |
| SpeechGPT | 文本 LLM + 离散语音单元 + 分阶段指令训练 | 模态适配与指令数据分别带来什么？ |
| LLaMA-Omni2 | Qwen2.5 + 语音输入模块 + 流式语音输出 | 小模型如何平衡内容正确性、音质和首包延迟？ |

<a id="realtime"></a>
## 🎧 实时语音与音视频联合建模

| 论文 / 项目 | 发表与来源 | 阅读重点与入口 |
|---|---|---|
| ⭐ [Moshi](../../resources/zh/CATALOG.md#e07) | [![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.00037) [![Independent Lab](https://img.shields.io/badge/Independent%20Lab-b45309?style=flat-square)](https://arxiv.org/html/2410.00037) | 双向语音流与文本协同建模，为连续听说提供开源研究基础。<br>[📄 论文](https://arxiv.org/abs/2410.00037) · [💻 仓库](https://github.com/kyutai-labs/moshi) |
| ⭐ [Qwen2.5-Omni](../../resources/zh/CATALOG.md#e02) | [![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.20215) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni) | 音视频、图像和文本输入，联合生成文本与语音；提供 Thinker–Talker 架构参照。<br>[📄 论文](https://arxiv.org/abs/2503.20215) · [💻 仓库](https://github.com/QwenLM/Qwen2.5-Omni) |
| [Qwen3-Omni](../../resources/zh/CATALOG.md#e03) | [![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.17765) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni) | MoE Thinker–Talker 路线，覆盖多模态理解和实时语音生成。<br>[📄 论文](https://arxiv.org/abs/2509.17765) · [💻 仓库](https://github.com/QwenLM/Qwen3-Omni) |
| ⭐ [MiniCPM-o 4.5](../../resources/zh/CATALOG.md#e01) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.27393) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V) | 以共享时间轴组织持续音视频输入与文本、语音输出，并研究主动回应。<br>[📄 论文](https://arxiv.org/abs/2604.27393) · [💻 仓库](https://github.com/OpenBMB/MiniCPM-V) |

扩展阅读：[Freeze-Omni](../../resources/zh/CATALOG.md#e08) · [Mini-Omni2](../../resources/zh/CATALOG.md#e06) · [VITA-1.5](../../resources/zh/CATALOG.md#e05) · [InteractiveOmni](../../resources/zh/CATALOG.md#e04)。交互策略、数据合成与工具使用继续见 [Voice Agent](03-Voice-Agent.md)。

<a id="training"></a>
## 🗂️ 数据、模型与训练目标

| 环节 | 需要读清的问题 | 代表入口 |
|---|---|---|
| 数据生产 | 真实语音、合成语音、声音描述、对话如何混合？音频与文字怎样对齐？ | [SpeechGPT](../../resources/zh/CATALOG.md#e87)、[Audio Flamingo 3](../../resources/zh/CATALOG.md#e82)、[SOMMELIER](../../resources/zh/CATALOG.md#e39) |
| 模型设计 | 连续特征还是离散 token？单流还是多流？理解与生成是否共享模型？ | [SALMONN](../../resources/zh/CATALOG.md#e86)、[GLM-4-Voice](../../resources/zh/CATALOG.md#e81)、[Moshi](../../resources/zh/CATALOG.md#e07) |
| 监督训练 | 继承哪个基座，冻结什么，哪些位置计算损失？ | [BLSP](../../resources/zh/CATALOG.md#e88)、[LLaMA-Omni2](../../resources/zh/CATALOG.md#e89)、[MiMo-Audio](../../resources/zh/CATALOG.md#e84) |
| 偏好与强化学习 | 优化内容、音质、轮次还是任务结果？奖励怎样验证？ | [Happy-LLM 第 8 章](https://github.com/datawhalechina/happy-llm/blob/main/docs/chapter8/%E7%AC%AC%E5%85%AB%E7%AB%A0%20%E5%A4%A7%E6%A8%A1%E5%9E%8B%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0.md)、[BayLing-Duplex](../../resources/zh/CATALOG.md#e42)、[VoxMind](../../resources/zh/CATALOG.md#e37) |
| 实时部署 | 首个音频包、持续吞吐、打断响应和多模态输入开销分别是多少？ | [MiniCPM-o](../../resources/zh/CATALOG.md#e01)、[Moshi](../../resources/zh/CATALOG.md#e07)、[端侧部署](04-Edge-Embodied-Interaction.md#evaluation) |

<a id="evaluation"></a>
## 📏 模型能力与交互评测

| 评测对象 | 入口 |
|---|---|
| 语音问答、指令与鲁棒性 | [VoiceBench](../../resources/zh/CATALOG.md#e59)、[VocalBench](../../resources/zh/CATALOG.md#e60)、[VCB Bench](../../resources/zh/CATALOG.md#e61) |
| 日常音视频与跨模态信息 | [Daily-Omni](../../resources/zh/CATALOG.md#e14)、[OmniBench](../../resources/zh/CATALOG.md#e15) |
| 轮次与全双工 | [Full-Duplex-Bench](../../resources/zh/CATALOG.md#e16)、[MTR-DuplexBench](../../resources/zh/CATALOG.md#e65) |
| 工具与任务完成 | [VoiceAgentBench](../../resources/zh/CATALOG.md#e62)、[τ-Voice](../../resources/zh/CATALOG.md#e63)；更多见 [Benchmark 导航](05-Voice-Agent-Benchmarks.md) |

下一步：[Voice Agent →](03-Voice-Agent.md)
