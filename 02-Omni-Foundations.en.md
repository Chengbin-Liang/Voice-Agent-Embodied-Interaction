# 02 · ALM / Omni Foundations

[中文](02-Omni-Foundations.md) | **English**

[Home](README.en.md) · [Catalog](CATALOG.en.md#omni) · [Surveys](SURVEYS.en.md)

Start with Audio Language Models (ALMs), then move to speech generation, real-time dialogue, and audiovisual understanding.

[Reading route](#route) · [Industry and joint bases](#bases) · [Academic methods](#methods) · [Real-time and audiovisual models](#realtime) · [Data and training](#training) · [Evaluation](#evaluation)

<a id="route"></a>
## 🧭 Four concepts to establish first

| Question | First readings | What to explain afterward |
|---|---|---|
| How does audio enter an LLM? | ⭐ [Qwen2-Audio](CATALOG.en.md#e80) → [SALMONN](CATALOG.en.md#e86) / [BLSP](CATALOG.en.md#e88) | Audio encoders, adapters, continuous representations, and information lost in transcripts. |
| How does an LLM generate speech? | ⭐ [SpeechGPT](CATALOG.en.md#e87) → [GLM-4-Voice](CATALOG.en.md#e81) / [LLaMA-Omni2](CATALOG.en.md#e89) | Discrete units, codecs, text/speech prediction order, and waveform decoding. |
| How can a model listen while speaking? | ⭐ [Moshi](CATALOG.en.md#e07) → [PersonaPlex](CATALOG.en.md#e90) → [Full-duplex training](03-Voice-Agent.en.md#academic) | Input/output audio streams, turns, time alignment, interruptions, and role control. |
| How are vision and continuous video added? | ⭐ [Qwen2.5-Omni](CATALOG.en.md#e02) → [MiniCPM-o](CATALOG.en.md#e01) / [Qwen3-Omni](CATALOG.en.md#e03) | Modality encoders, shared timelines, Thinker–Talker, and concurrent inference. |

Components: [Whisper](https://github.com/openai/whisper) (speech encoding/recognition) · [SpeechTokenizer](https://github.com/ZhangXInFD/SpeechTokenizer) (speech tokens) · [Moshi / Mimi](https://github.com/kyutai-labs/moshi) (streaming codec) · [CosyVoice](https://github.com/FunAudioLLM/CosyVoice) (speech generation).

<a id="bases"></a>
## 🏭 Industry and joint bases: capabilities and usable interfaces

| Paper / project | Publication and affiliation | Reading focus and resources |
|---|---|---|
| ⭐ [Qwen2-Audio](CATALOG.en.md#e80) | [![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2407.10759) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2407.10759) | A 7B audio language model for speech, sound, and music understanding with text responses.<br>[📄 Paper](https://arxiv.org/abs/2407.10759) · [💻 Repository](https://github.com/QwenLM/Qwen2-Audio) |
| [GLM-4-Voice](CATALOG.en.md#e81) | [![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2412.02612) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2412.02612) | A 9B spoken-dialogue model with discrete speech tokens, interleaved speech/text modeling, and streaming decoding.<br>[📄 Paper](https://arxiv.org/abs/2412.02612) · [💻 Repository](https://github.com/zai-org/GLM-4-Voice) |
| ⭐ [Audio Flamingo 3](CATALOG.en.md#e82) | [![NeurIPS Spotlight 2025](https://img.shields.io/badge/NeurIPS%20Spotlight%202025-475569?style=flat-square)](https://openreview.net/forum?id=FjByDpDVIO) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2507.08128) | A 7B audio language model for speech, sound, music, and audio reasoning, with training, data, and inference resources.<br>[📄 Paper](https://arxiv.org/abs/2507.08128) · [💻 Repository](https://github.com/NVIDIA/audio-flamingo) · [🔗 Training](https://github.com/NVIDIA/audio-flamingo/tree/audio_flamingo_3) |
| [Audio Flamingo Next](CATALOG.en.md#e83) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.10905) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2604.10905) | Extends long-audio understanding, temporal grounding, speaker attribution, and multi-speaker reasoning.<br>[📄 Paper](https://arxiv.org/abs/2604.10905) · [🔗 Weights](https://huggingface.co/nvidia/audio-flamingo-next-hf) |
| ⭐ [MiMo-Audio](CATALOG.en.md#e84) | [![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2512.23808) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2512.23808) | 7B speech base and instruction models with an official fine-tuning toolkit for ASR, TTS, audio understanding, and spoken dialogue.<br>[📄 Paper](https://arxiv.org/abs/2512.23808) · [💻 Repository](https://github.com/XiaomiMiMo/MiMo-Audio) · [🔗 Training](https://github.com/XiaomiMiMo/MiMo-Audio-Training) |
| [Step-Audio 2](CATALOG.en.md#e85) | [![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2507.16632) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2507.16632) | Targets multimodal speech interaction, audio reasoning, and tool use, with Mini-series checkpoints and inference code.<br>[📄 Paper](https://arxiv.org/abs/2507.16632) · [💻 Repository](https://github.com/stepfun-ai/Step-Audio2) |
| [PersonaPlex](CATALOG.en.md#e90) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.06053) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2602.06053) | A Moshi-based 7B full-duplex model with voice and text prompts for speaker and role control.<br>[📄 Paper](https://arxiv.org/abs/2602.06053) · [💻 Repository](https://github.com/NVIDIA/personaplex) |

Adaptation entry points: ⭐ [Official MiMo-Audio SFT toolkit](https://github.com/XiaomiMiMo/MiMo-Audio-Training); ⭐ [Audio Flamingo 3 training branch](https://github.com/NVIDIA/audio-flamingo/tree/audio_flamingo_3). Audio Flamingo Next's HF checkpoint outputs text; PersonaPlex's official entry point focuses on inference and role control.

Training framework: [SLAM-LLM](https://github.com/X-LANCE/SLAM-LLM) provides examples combining speech encoders, adapters, and LLMs.

<a id="methods"></a>
## 🎓 Academic methods and base-model adaptation

| Paper / project | Publication and affiliation | Reading focus and resources |
|---|---|---|
| ⭐ [SALMONN](CATALOG.en.md#e86) | [![ICLR 2024](https://img.shields.io/badge/ICLR%202024-475569?style=flat-square)](https://github.com/bytedance/SALMONN/tree/salmonn) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2310.13289) | Combines speech and general-audio encoders with an adapter and an LLM for speech, sound, and music tasks.<br>[📄 Paper](https://arxiv.org/abs/2310.13289) · [💻 Repository](https://github.com/bytedance/SALMONN) · [🔗 Training](https://github.com/bytedance/SALMONN/tree/salmonn) |
| ⭐ [SpeechGPT](CATALOG.en.md#e87) | [![EMNLP Findings 2023](https://img.shields.io/badge/EMNLP%20Findings%202023-475569?style=flat-square)](https://aclanthology.org/2023.findings-emnlp.1055/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2305.11000) | Extends a text LLM to speech input/output using discrete speech units and SpeechInstruct.<br>[📄 Paper](https://arxiv.org/abs/2305.11000) · [💻 Repository](https://github.com/0nutation/SpeechGPT) |
| ⭐ [BLSP](CATALOG.en.md#e88) | [![arXiv 2023](https://img.shields.io/badge/arXiv%202023-475569?style=flat-square)](https://arxiv.org/abs/2309.00916) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2309.00916) | Trains a lightweight adapter between a frozen speech encoder and LLM by aligning continuations from speech and transcripts.<br>[📄 Paper](https://arxiv.org/abs/2309.00916) · [💻 Repository](https://github.com/cwang621/blsp) |
| ⭐ [LLaMA-Omni2](CATALOG.en.md#e89) | [![ACL 2025](https://img.shields.io/badge/ACL%202025-475569?style=flat-square)](https://aclanthology.org/2025.acl-long.912/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2505.02625) | Builds bilingual spoken dialogue and streaming speech generation on Qwen2.5, with multiple model sizes and inference code.<br>[📄 Paper](https://arxiv.org/abs/2505.02625) · [💻 Repository](https://github.com/ictnlp/LLaMA-Omni2) |

| Method | Initialization and changes | Minimal reproduction question |
|---|---|---|
| BLSP | Existing speech encoder + LLM; train a lightweight adapter | Do speech and text inputs produce consistent task behavior? |
| SALMONN | Speech and general-audio encoders + LLM | Which tasks benefit from non-speech audio information? |
| SpeechGPT | Text LLM + discrete speech units + staged instruction tuning | What do modality adaptation and instruction data each contribute? |
| LLaMA-Omni2 | Qwen2.5 + speech input modules + streaming speech output | How do smaller models balance content accuracy, speech quality, and first-audio latency? |

<a id="realtime"></a>
## 🎧 Real-time speech and audiovisual modeling

| Paper / project | Publication and affiliation | Reading focus and resources |
|---|---|---|
| ⭐ [Moshi](CATALOG.en.md#e07) | [![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.00037) [![Independent Lab](https://img.shields.io/badge/Independent%20Lab-b45309?style=flat-square)](https://arxiv.org/html/2410.00037) | Models two-way speech streams together with text, providing an open research foundation for continuous listening and speaking.<br>[📄 Paper](https://arxiv.org/abs/2410.00037) · [💻 Repository](https://github.com/kyutai-labs/moshi) |
| ⭐ [Qwen2.5-Omni](CATALOG.en.md#e02) | [![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.20215) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni) | Accepts audio, video, images, and text, and jointly generates text and speech; a reference for the Thinker–Talker architecture.<br>[📄 Paper](https://arxiv.org/abs/2503.20215) · [💻 Repository](https://github.com/QwenLM/Qwen2.5-Omni) |
| [Qwen3-Omni](CATALOG.en.md#e03) | [![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.17765) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni) | An MoE Thinker–Talker approach covering multimodal understanding and real-time speech generation.<br>[📄 Paper](https://arxiv.org/abs/2509.17765) · [💻 Repository](https://github.com/QwenLM/Qwen3-Omni) |
| ⭐ [MiniCPM-o 4.5](CATALOG.en.md#e01) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.27393) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V) | Organizes continuous audio/video input and text/speech output on a shared timeline, including proactive responses.<br>[📄 Paper](https://arxiv.org/abs/2604.27393) · [💻 Repository](https://github.com/OpenBMB/MiniCPM-V) |

Further reading: [Freeze-Omni](CATALOG.en.md#e08) · [Mini-Omni2](CATALOG.en.md#e06) · [VITA-1.5](CATALOG.en.md#e05) · [InteractiveOmni](CATALOG.en.md#e04). Continue to [Voice Agents](03-Voice-Agent.en.md) for interaction policies, data synthesis, and tool use.

<a id="training"></a>
## 🗂️ Connecting data, models, and training

| Stage | Questions to answer | References |
|---|---|---|
| Data production | How are real/synthetic speech, sound descriptions, and dialogue mixed? How are audio and text aligned? | [SpeechGPT](CATALOG.en.md#e87), [Audio Flamingo 3](CATALOG.en.md#e82), [SOMMELIER](CATALOG.en.md#e39) |
| Model design | Continuous features or discrete tokens? One stream or several? Shared understanding/generation model? | [SALMONN](CATALOG.en.md#e86), [GLM-4-Voice](CATALOG.en.md#e81), [Moshi](CATALOG.en.md#e07) |
| Supervised training | Which base is inherited, which modules are frozen, and which positions receive loss? | [BLSP](CATALOG.en.md#e88), [LLaMA-Omni2](CATALOG.en.md#e89), [MiMo-Audio](CATALOG.en.md#e84) |
| Preferences and RL | Are content, speech quality, turn decisions, or task outcomes optimized? How are rewards validated? | [LLM RL basics](01-LLM-Foundations.en.md#rl), [BayLing-Duplex](CATALOG.en.md#e42), [VoxMind](CATALOG.en.md#e37) |
| Real-time deployment | First-audio latency, sustained throughput, interruption response, and multimodal input overhead | [MiniCPM-o](CATALOG.en.md#e01), [Moshi](CATALOG.en.md#e07), [Edge deployment](04-Edge-Embodied-Interaction.en.md#evaluation) |

<a id="evaluation"></a>
## 📏 Measure capabilities and interaction separately

| Evaluation target | Entry points |
|---|---|
| Spoken QA, instructions, and robustness | [VoiceBench](CATALOG.en.md#e59), [VocalBench](CATALOG.en.md#e60), [VCB Bench](CATALOG.en.md#e61) |
| Everyday audiovisual and cross-modal information | [Daily-Omni](CATALOG.en.md#e14), [OmniBench](CATALOG.en.md#e15) |
| Turns and full-duplex interaction | [Full-Duplex-Bench](CATALOG.en.md#e16), [MTR-DuplexBench](CATALOG.en.md#e65) |
| Tools and task completion | [VoiceAgentBench](CATALOG.en.md#e62), [τ-Voice](CATALOG.en.md#e63); more in the [benchmark guide](05-Voice-Agent-Benchmarks.en.md) |

Next: [Voice Agents →](03-Voice-Agent.en.md)
