# Paper and Project Catalog

[中文](../zh/CATALOG.md) | **English**

[Home](../../README.en.md) · [Survey](SURVEYS.md) · [Benchmarks](../../docs/en/05-Voice-Agent-Benchmarks.md)

⭐ Suggested first readings include a reason. See the [label guide](../../README.en.md#labels).

[🧠 LLM post-training and reinforcement learning](#llm) · [🎧 ALM / Omni and speech models](#omni) · [💬 Voice agents and interaction systems](#voice) · [🤖 Embodied interaction and language feedback](#embodied) · [🦾 Actions, data, and deployment](#robotics) · [📏 Evaluation](#evaluation) · [🏭 Industry demonstrations](#industry)

<a id="llm"></a>

## 🧠 LLM post-training and reinforcement learning

<a id="e75"></a>

### ⭐ PPO

[![arXiv 2017](https://img.shields.io/badge/arXiv%202017-475569?style=flat-square)](https://arxiv.org/abs/1707.06347) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/1707.06347)

[📄 Paper](https://arxiv.org/abs/1707.06347) · [💻 Repository](https://github.com/openai/baselines) · [![★ 16,775](https://img.shields.io/badge/%E2%98%85%2016%2C775-eab308?style=flat-square)](https://github.com/openai/baselines) [![Cite OA 10,618](https://img.shields.io/badge/Cite%20OA%2010%2C618-0284c7?style=flat-square)](https://openalex.org/W2736601468)

Optimizes rewards on sampled trajectories while constraining policy updates; a foundation for subsequent RLHF methods.

📌 Priority rationale: Introduces policies, rewards, advantage estimates, and the clipped objective as background for PPO in language models.

Organizations / maintainers: OpenAI

<sub>Count snapshot: 2026-11-03</sub>

<a id="e76"></a>

### ⭐ InstructGPT / RLHF

[![NeurIPS 2022](https://img.shields.io/badge/NeurIPS%202022-475569?style=flat-square)](https://arxiv.org/abs/2203.02155) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2203.02155)

[📄 Paper](https://arxiv.org/abs/2203.02155) · [![Cite OA 4,208](https://img.shields.io/badge/Cite%20OA%204%2C208-0284c7?style=flat-square)](https://openalex.org/W4226278401)

Combines supervised demonstrations, a reward model trained on human rankings, and PPO optimization.

📌 Priority rationale: Establish the SFT → preferences → reward model → RL pipeline.

Organizations / maintainers: OpenAI

<sub>Count snapshot: 2026-11-03</sub>

<a id="e77"></a>

### ⭐ DPO

[![NeurIPS 2023](https://img.shields.io/badge/NeurIPS%202023-475569?style=flat-square)](https://arxiv.org/abs/2305.18290) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2305.18290)

[📄 Paper](https://arxiv.org/abs/2305.18290) · [💻 Repository](https://github.com/eric-mitchell/direct-preference-optimization) · [![★ 2,922](https://img.shields.io/badge/%E2%98%85%202%2C922-eab308?style=flat-square)](https://github.com/eric-mitchell/direct-preference-optimization) Cite —

Optimizes relative response probabilities from preference pairs, providing an offline alternative to online RL.

📌 Priority rationale: Understand how the same preference data supports different post-training methods.

DPO itself does not require online environment rollouts.

Organizations / maintainers: Stanford University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e78"></a>

### ⭐ DeepSeekMath / GRPO

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2402.03300) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2402.03300)

[📄 Paper](https://arxiv.org/abs/2402.03300) · [💻 Repository](https://github.com/deepseek-ai/DeepSeek-Math) · [![★ 3,478](https://img.shields.io/badge/%E2%98%85%203%2C478-eab308?style=flat-square)](https://github.com/deepseek-ai/DeepSeek-Math) [![Cite OA 101](https://img.shields.io/badge/Cite%20OA%20101-0284c7?style=flat-square)](https://openalex.org/W4391631327)

Introduces GRPO for mathematical reasoning, deriving relative advantages from groups of sampled answers.

📌 Priority rationale: Study group rewards, advantage estimation, and KL regularization for verifiable-reward training.

Organizations / maintainers: DeepSeek-AI; Tsinghua University; Peking University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e79"></a>

### DeepSeek-R1

[![Nature 2025](https://img.shields.io/badge/Nature%202025-475569?style=flat-square)](https://www.nature.com/articles/s41586-025-09422-z) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2501.12948)

[📄 Paper](https://arxiv.org/abs/2501.12948) · [💻 Repository](https://github.com/deepseek-ai/DeepSeek-R1) · [![★ 91,995](https://img.shields.io/badge/%E2%98%85%2091%2C995-eab308?style=flat-square)](https://github.com/deepseek-ai/DeepSeek-R1) [![Cite OA 1,701](https://img.shields.io/badge/Cite%20OA%201%2C701-0284c7?style=flat-square)](https://openalex.org/W4414281281)

Studies reasoning RL, cold starts, multistage post-training, and distillation into smaller models.

Distilled checkpoints support adaptation; released weights and the complete original RL training pipeline are distinct resources.

Organizations / maintainers: DeepSeek-AI

<sub>Count snapshot: 2026-11-03</sub>

<a id="omni"></a>

## 🎧 ALM / Omni and speech models

<a id="e01"></a>

### ⭐ MiniCPM-o 4.5

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.27393) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V)

[📄 Paper](https://arxiv.org/abs/2604.27393) · [💻 Repository](https://github.com/OpenBMB/MiniCPM-V) · [![★ 27,047](https://img.shields.io/badge/%E2%98%85%2027%2C047-eab308?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W7159670352)

Organizes continuous audio/video input and text/speech output on a shared timeline, including proactive responses.

📌 Priority rationale: Study continuous audiovisual input, full-duplex output, and deployment requirements.

Use the official requirements for each full-duplex mode; distinguish model memory from total system memory.

Organizations / maintainers: Tsinghua University / THUNLP; ModelBest; OpenBMB

<sub>Count snapshot: 2026-11-02</sub>

<a id="e02"></a>

### ⭐ Qwen2.5-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.20215) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni)

[📄 Paper](https://arxiv.org/abs/2503.20215) · [💻 Repository](https://github.com/QwenLM/Qwen2.5-Omni) · [![★ 4,092](https://img.shields.io/badge/%E2%98%85%204%2C092-eab308?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni) [![Cite OA 14](https://img.shields.io/badge/Cite%20OA%2014-0284c7?style=flat-square)](https://openalex.org/W4409051416)

Accepts audio, video, images, and text, and jointly generates text and speech; a reference for the Thinker–Talker architecture.

📌 Priority rationale: Establish a reference for Thinker–Talker architecture, data, and staged training.

Streaming speech output and native full-duplex interaction are evaluated separately; MNN support depends on the deployment mode.

Organizations / maintainers: Qwen Team / Alibaba

<sub>Count snapshot: 2026-11-02</sub>

<a id="e03"></a>

### Qwen3-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.17765) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni)

[📄 Paper](https://arxiv.org/abs/2509.17765) · [💻 Repository](https://github.com/QwenLM/Qwen3-Omni) · [![★ 4,093](https://img.shields.io/badge/%E2%98%85%204%2C093-eab308?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4415255153)

An MoE Thinker–Talker approach covering multimodal understanding and real-time speech generation.

Organizations / maintainers: Qwen Team / Alibaba

<sub>Count snapshot: 2026-11-02</sub>

<a id="e04"></a>

### InteractiveOmni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.13747) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2510.13747)

[📄 Paper](https://arxiv.org/abs/2510.13747) · [💻 Repository](https://github.com/OpenSenseNova/InteractiveOmni) · [![★ 9](https://img.shields.io/badge/%E2%98%85%209-eab308?style=flat-square)](https://github.com/OpenSenseNova/InteractiveOmni) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415277372)

Targets audiovisual multi-turn interaction, with 4B and 8B models and multi-turn evaluation.

Organizations / maintainers: SenseTime Research

<sub>Count snapshot: 2026-11-02</sub>

<a id="e05"></a>

### VITA-1.5

[![NeurIPS 2025](https://img.shields.io/badge/NeurIPS%202025-475569?style=flat-square)](https://arxiv.org/abs/2501.01957) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2501.01957)

[📄 Paper](https://arxiv.org/abs/2501.01957) · [💻 Repository](https://github.com/VITA-MLLM/VITA) · [![★ 2,539](https://img.shields.io/badge/%E2%98%85%202%2C539-eab308?style=flat-square)](https://github.com/VITA-MLLM/VITA) [![Cite OA 11](https://img.shields.io/badge/Cite%20OA%2011-0284c7?style=flat-square)](https://openalex.org/W4406093559)

A multimodal model for real-time visual and speech interaction, with training and inference workflows.

Organizations / maintainers: Nanjing University; Xiamen University; CASIA; Tencent Youtu Lab

<sub>Count snapshot: 2026-11-02</sub>

<a id="e06"></a>

### Mini-Omni2

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.11190) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2410.11190)

[📄 Paper](https://arxiv.org/abs/2410.11190) · [💻 Repository](https://github.com/gpt-omni/mini-omni2) · [![★ 1,936](https://img.shields.io/badge/%E2%98%85%201%2C936-eab308?style=flat-square)](https://github.com/gpt-omni/mini-omni2) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4403576555)

An early open experimental system supporting image, speech, and text inputs with real-time speech output.

Organizations / maintainers: Tsinghua University; Inspirai

<sub>Count snapshot: 2026-11-02</sub>

<a id="e07"></a>

### ⭐ Moshi

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.00037) [![Independent Lab](https://img.shields.io/badge/Independent%20Lab-b45309?style=flat-square)](https://arxiv.org/html/2410.00037)

[📄 Paper](https://arxiv.org/abs/2410.00037) · [💻 Repository](https://github.com/kyutai-labs/moshi) · [![★ 11,361](https://img.shields.io/badge/%E2%98%85%2011%2C361-eab308?style=flat-square)](https://github.com/kyutai-labs/moshi) [![Cite OA 9](https://img.shields.io/badge/Cite%20OA%209-0284c7?style=flat-square)](https://openalex.org/W4403883071) [![Cite S2 875](https://img.shields.io/badge/Cite%20S2%20875-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/ae4aa7b0c5a327dae63ad20e00b58bcc6176b3b8)

Models two-way speech streams together with text, providing an open research foundation for continuous listening and speaking.

📌 Priority rationale: Understand bidirectional speech streams, text assistance, and low-latency generation.

Organizations / maintainers: Kyutai

<sub>Count snapshot: 2026-11-02</sub>

<a id="e08"></a>

### Freeze-Omni

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2411.00774) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2411.00774)

[📄 Paper](https://arxiv.org/abs/2411.00774) · [💻 Repository](https://github.com/VITA-MLLM/Freeze-Omni) · [![★ 403](https://img.shields.io/badge/%E2%98%85%20403-eab308?style=flat-square)](https://github.com/VITA-MLLM/Freeze-Omni) [![Cite OA 4](https://img.shields.io/badge/Cite%20OA%204-0284c7?style=flat-square)](https://openalex.org/W4404390495)

Combines a frozen language model with streaming speech encoding/decoding and chunk-level state prediction.

Organizations / maintainers: Northwestern Polytechnical University; Nanjing University; Tencent Youtu Lab

<sub>Count snapshot: 2026-11-02</sub>

<a id="e80"></a>

### ⭐ Qwen2-Audio

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2407.10759) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2407.10759)

[📄 Paper](https://arxiv.org/abs/2407.10759) · [💻 Repository](https://github.com/QwenLM/Qwen2-Audio) · [![★ 2,101](https://img.shields.io/badge/%E2%98%85%202%2C101-eab308?style=flat-square)](https://github.com/QwenLM/Qwen2-Audio) [![Cite OA 8](https://img.shields.io/badge/Cite%20OA%208-0284c7?style=flat-square)](https://openalex.org/W4400717319)

A 7B audio language model for speech, sound, and music understanding with text responses.

📌 Priority rationale: Start with connecting an audio encoder to an LLM and establishing an audio-understanding baseline.

Organizations / maintainers: Alibaba / Qwen Team

<sub>Count snapshot: 2026-11-03</sub>

<a id="e81"></a>

### GLM-4-Voice

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2412.02612) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2412.02612)

[📄 Paper](https://arxiv.org/abs/2412.02612) · [💻 Repository](https://github.com/zai-org/GLM-4-Voice) · [![★ 3,243](https://img.shields.io/badge/%E2%98%85%203%2C243-eab308?style=flat-square)](https://github.com/zai-org/GLM-4-Voice) [![Cite OA 4](https://img.shields.io/badge/Cite%20OA%204-0284c7?style=flat-square)](https://openalex.org/W4405057125)

A 9B spoken-dialogue model with discrete speech tokens, interleaved speech/text modeling, and streaming decoding.

Organizations / maintainers: Tsinghua University; Zhipu.AI

<sub>Count snapshot: 2026-11-03</sub>

<a id="e82"></a>

### ⭐ Audio Flamingo 3

[![NeurIPS Spotlight 2025](https://img.shields.io/badge/NeurIPS%20Spotlight%202025-475569?style=flat-square)](https://openreview.net/forum?id=FjByDpDVIO) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2507.08128)

[📄 Paper](https://arxiv.org/abs/2507.08128) · [💻 Repository](https://github.com/NVIDIA/audio-flamingo) · [🔗 Training](https://github.com/NVIDIA/audio-flamingo/tree/audio_flamingo_3) · [![★ 1,219](https://img.shields.io/badge/%E2%98%85%201%2C219-eab308?style=flat-square)](https://github.com/NVIDIA/audio-flamingo) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W6929354950)

A 7B audio language model for speech, sound, music, and audio reasoning, with training, data, and inference resources.

📌 Priority rationale: Read data construction and staged training alongside the released training branch.

Check model and data licenses separately; the weights use a noncommercial research license.

Organizations / maintainers: NVIDIA; University of Maryland

<sub>Count snapshot: 2026-11-03</sub>

<a id="e83"></a>

### Audio Flamingo Next

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.10905) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2604.10905)

[📄 Paper](https://arxiv.org/abs/2604.10905) · [🔗 Weights](https://huggingface.co/nvidia/audio-flamingo-next-hf) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7154207876)

Extends long-audio understanding, temporal grounding, speaker attribution, and multi-speaker reasoning.

The released HF checkpoint takes audio/text and outputs text; streaming speech generation is not part of that checkpoint.

Organizations / maintainers: NVIDIA; University of Maryland

<sub>Count snapshot: 2026-11-03</sub>

<a id="e84"></a>

### ⭐ MiMo-Audio

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2512.23808) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2512.23808)

[📄 Paper](https://arxiv.org/abs/2512.23808) · [💻 Repository](https://github.com/XiaomiMiMo/MiMo-Audio) · [🔗 Training](https://github.com/XiaomiMiMo/MiMo-Audio-Training) · [![★ 1,088](https://img.shields.io/badge/%E2%98%85%201%2C088-eab308?style=flat-square)](https://github.com/XiaomiMiMo/MiMo-Audio) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W7117988839)

7B speech base and instruction models with an official fine-tuning toolkit for ASR, TTS, audio understanding, and spoken dialogue.

📌 Priority rationale: Inspect task data formats and SFT scripts as an entry point to adapting an existing speech base.

Organizations / maintainers: Xiaomi MiMo

<sub>Count snapshot: 2026-11-03</sub>

<a id="e85"></a>

### Step-Audio 2

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2507.16632) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2507.16632)

[📄 Paper](https://arxiv.org/abs/2507.16632) · [💻 Repository](https://github.com/stepfun-ai/Step-Audio2) · [![★ 1,526](https://img.shields.io/badge/%E2%98%85%201%2C526-eab308?style=flat-square)](https://github.com/stepfun-ai/Step-Audio2) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4415202956)

Targets multimodal speech interaction, audio reasoning, and tool use, with Mini-series checkpoints and inference code.

Organizations / maintainers: StepFun

<sub>Count snapshot: 2026-11-03</sub>

<a id="e86"></a>

### ⭐ SALMONN

[![ICLR 2024](https://img.shields.io/badge/ICLR%202024-475569?style=flat-square)](https://github.com/bytedance/SALMONN/tree/salmonn) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2310.13289)

[📄 Paper](https://arxiv.org/abs/2310.13289) · [💻 Repository](https://github.com/bytedance/SALMONN) · [🔗 Training](https://github.com/bytedance/SALMONN/tree/salmonn) · [![★ 1,564](https://img.shields.io/badge/%E2%98%85%201%2C564-eab308?style=flat-square)](https://github.com/bytedance/SALMONN) [![Cite OA 67](https://img.shields.io/badge/Cite%20OA%2067-0284c7?style=flat-square)](https://openalex.org/W4387891768)

Combines speech and general-audio encoders with an adapter and an LLM for speech, sound, and music tasks.

📌 Priority rationale: Understand how dual encoders, an adapter, and multitask training retain information beyond ASR.

Organizations / maintainers: Tsinghua University; ByteDance

<sub>Count snapshot: 2026-11-03</sub>

<a id="e87"></a>

### ⭐ SpeechGPT

[![EMNLP Findings 2023](https://img.shields.io/badge/EMNLP%20Findings%202023-475569?style=flat-square)](https://aclanthology.org/2023.findings-emnlp.1055/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2305.11000)

[📄 Paper](https://arxiv.org/abs/2305.11000) · [💻 Repository](https://github.com/0nutation/SpeechGPT) · [![★ 1,401](https://img.shields.io/badge/%E2%98%85%201%2C401-eab308?style=flat-square)](https://github.com/0nutation/SpeechGPT) [![Cite OA 189](https://img.shields.io/badge/Cite%20OA%20189-0284c7?style=flat-square)](https://openalex.org/W4389524500)

Extends a text LLM to speech input/output using discrete speech units and SpeechInstruct.

📌 Priority rationale: Organizes data and training into modality adaptation, cross-modal instruction tuning, and chain-of-modality tuning.

Organizations / maintainers: Fudan University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e88"></a>

### ⭐ BLSP

[![arXiv 2023](https://img.shields.io/badge/arXiv%202023-475569?style=flat-square)](https://arxiv.org/abs/2309.00916) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2309.00916)

[📄 Paper](https://arxiv.org/abs/2309.00916) · [💻 Repository](https://github.com/cwang621/blsp) · [![★ 59](https://img.shields.io/badge/%E2%98%85%2059-eab308?style=flat-square)](https://github.com/cwang621/blsp) [![Cite OA 9](https://img.shields.io/badge/Cite%20OA%209-0284c7?style=flat-square)](https://openalex.org/W4386552581)

Trains a lightweight adapter between a frozen speech encoder and LLM by aligning continuations from speech and transcripts.

📌 Priority rationale: A clear training objective and trainable module make it useful for understanding lightweight speech adaptation.

Organizations / maintainers: CASIA; UCAS; Alibaba DAMO Academy

<sub>Count snapshot: 2026-11-03</sub>

<a id="e89"></a>

### ⭐ LLaMA-Omni2

[![ACL 2025](https://img.shields.io/badge/ACL%202025-475569?style=flat-square)](https://aclanthology.org/2025.acl-long.912/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2505.02625)

[📄 Paper](https://arxiv.org/abs/2505.02625) · [💻 Repository](https://github.com/ictnlp/LLaMA-Omni2) · [![★ 281](https://img.shields.io/badge/%E2%98%85%20281-eab308?style=flat-square)](https://github.com/ictnlp/LLaMA-Omni2) [![Cite OA 11](https://img.shields.io/badge/Cite%20OA%2011-0284c7?style=flat-square)](https://openalex.org/W4412944968)

Builds bilingual spoken dialogue and streaming speech generation on Qwen2.5, with multiple model sizes and inference code.

📌 Priority rationale: Provides 0.5B–3B variants for studying speech-instruction data, alignment, and streaming output.

Code and models have different licenses; models are for research use.

Organizations / maintainers: Institute of Computing Technology, CAS; UCAS

<sub>Count snapshot: 2026-11-03</sub>

<a id="e90"></a>

### PersonaPlex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.06053) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2602.06053)

[📄 Paper](https://arxiv.org/abs/2602.06053) · [💻 Repository](https://github.com/NVIDIA/personaplex) · [![★ 12,018](https://img.shields.io/badge/%E2%98%85%2012%2C018-eab308?style=flat-square)](https://github.com/NVIDIA/personaplex) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W7128377012)

A Moshi-based 7B full-duplex model with voice and text prompts for speaker and role control.

The official release provides weights and inference; read DuplexGen for a related training workflow.

Organizations / maintainers: NVIDIA

<sub>Count snapshot: 2026-11-03</sub>

<a id="voice"></a>

## 💬 Voice agents and interaction systems

<a id="e29"></a>

### ⭐ FireRedChat

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.06502) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/abs/2509.06502)

[📄 Paper](https://arxiv.org/abs/2509.06502) · [💻 Repository](https://github.com/FireRedTeam/FireRedChat) · [![★ 597](https://img.shields.io/badge/%E2%98%85%20597-eab308?style=flat-square)](https://github.com/FireRedTeam/FireRedChat) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4414757003)

A full-duplex speech system covering turn control, target-speaker interruption, dialogue management, and tool calling.

📌 Priority rationale: Use the modular implementation to understand interruption control, dialogue state, and tool use.

Organizations / maintainers: Xiaohongshu / FireRed Team

<sub>Count snapshot: 2026-11-03</sub>

<a id="e30"></a>

### Qwen Audio Agent

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent)

[💻 Repository](https://github.com/QwenAudio/qwen-audio-agent) · [![★ 3,112](https://img.shields.io/badge/%E2%98%85%203%2C112-eab308?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent)

An engineering entry point for asynchronous task coordination and cancellation between a speech frontend and a backend agent.

Organizations / maintainers: Qwen / Alibaba

<sub>Count snapshot: 2026-11-03</sub>

<a id="e09"></a>

### DuplexSLA

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2605.20755) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2605.20755)

[📄 Paper](https://arxiv.org/abs/2605.20755) · [💻 Repository](https://github.com/hyzhang24/DuplexSLA) · [![★ 147](https://img.shields.io/badge/%E2%98%85%20147-eab308?style=flat-square)](https://github.com/hyzhang24/DuplexSLA) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7161968102)

Produces speech and a structured action channel on a shared timeline, studying planning and tool use during conversation.

The action channel represents structured planning and tool operations; joint control belongs to the downstream execution system.

Organizations / maintainers: StepFun; Peking University; Nanyang Technological University; Shanghai Jiao Tong University; University of New South Wales; Imperial College London

<sub>Count snapshot: 2026-11-02</sub>

<a id="e31"></a>

### Jarvis

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.23804) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2610.23804)

[📄 Paper](https://arxiv.org/abs/2610.23804) · [💻 Repository](https://github.com/JensenYX/Jarvis) · [![★ 18](https://img.shields.io/badge/%E2%98%85%2018-eab308?style=flat-square)](https://github.com/JensenYX/Jarvis) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7222979632)

Trains a coordinator between the interaction frontend and background tasks to manage switching, state, and stale results.

The study concerns software-agent coordination; gains on physical robot tasks require separate validation.

Organizations / maintainers: CUHK Shenzhen; Tencent Hunyuan; Amphion Technology

<sub>Count snapshot: 2026-11-03</sub>

<a id="e36"></a>

### TEN Framework

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/TEN-framework/ten-framework) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/TEN-framework/ten-framework)

[💻 Repository](https://github.com/TEN-framework/ten-framework) · [![★ 11,219](https://img.shields.io/badge/%E2%98%85%2011%2C219-eab308?style=flat-square)](https://github.com/TEN-framework/ten-framework)

A framework for engineering real-time audiovisual agents and applications.

The LICENSE includes conditions beyond Apache-2.0, including provisions on endpoint-device hosting; read the official LICENSE before deployment.

Organizations / maintainers: Agora; Contributor community

<sub>Count snapshot: 2026-11-03</sub>

<a id="e37"></a>

### ⭐ VoxMind

[![ACL 2026](https://img.shields.io/badge/ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.acl-long.459/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2604.15710)

[📄 Paper](https://arxiv.org/abs/2604.15710) · [💻 Repository](https://github.com/MM-Speech/VoxMind) · [![★ 46](https://img.shields.io/badge/%E2%98%85%2046-eab308?style=flat-square)](https://github.com/MM-Speech/VoxMind) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7155019877)

Uses AgentChat data, Think-before-Speak, and dynamic tool retrieval to learn a reasoning–tool-call–feedback loop for spoken agents.

📌 Priority rationale: AgentChat formats, training objectives, and tool experiments show how speech interaction supports task execution.

Asynchronous tool management and simultaneous listening/speaking are evaluated in different experiments; results depend on the task and interaction conditions.

Organizations / maintainers: Zhejiang University; China University of Petroleum–Beijing at Karamay; Xiamen University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e38"></a>

### ⭐ F-Actor

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.242/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2601.11329)

[📄 Paper](https://arxiv.org/abs/2601.11329) · [💻 Repository](https://github.com/MaikeZuefle/f-actor) · [![★ 33](https://img.shields.io/badge/%E2%98%85%2033-eab308?style=flat-square)](https://github.com/MaikeZuefle/f-actor) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7124734178)

Controls voice, topic, backchannels, interruptions, and conversation initiation through instructions, using a frozen audio encoder and single-stage training.

📌 Priority rationale: Represents interaction behaviors such as interruption and feedback as supervised, controllable instructions.

Organizations / maintainers: Karlsruhe Institute of Technology; University of Edinburgh; NatWest

<sub>Count snapshot: 2026-11-03</sub>

<a id="e39"></a>

### ⭐ SOMMELIER

[![ACL Industry Track 2026](https://img.shields.io/badge/ACL%20Industry%20Track%202026-475569?style=flat-square)](https://aclanthology.org/2026.acl-industry.18/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2603.25750)

[📄 Paper](https://arxiv.org/abs/2603.25750) · [💻 Repository](https://github.com/Anonymous-2001-j/Sommelier) · [![★ 0](https://img.shields.io/badge/%E2%98%85%200-eab308?style=flat-square)](https://github.com/Anonymous-2001-j/Sommelier) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7143443580)

Converts real multiparty recordings into temporally aligned two-channel training data through separation, diarization, transcription, and quality filtering.

📌 Priority rationale: Shows temporal alignment, overlap handling, and filtering when converting real recordings into full-duplex training data.

Organizations / maintainers: KAIST; NAVER Cloud

<sub>Count snapshot: 2026-11-03</sub>

<a id="e40"></a>

### CF-Duplex / XA-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2605.10199) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2605.10199)

[📄 Paper](https://arxiv.org/abs/2605.10199) · [🔗 Project](https://light1726.github.io/duplex-demo/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7160904488)

Compares controlled fusion and cross-attention for routing the user audio stream into an actively generating model.

Organizations / maintainers: The Chinese University of Hong Kong; Tsinghua University; SenseTime

<sub>Count snapshot: 2026-11-03</sub>

<a id="e41"></a>

### ⭐ DuplexGen

[![EMNLP 2026](https://img.shields.io/badge/EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.emnlp-main.2618/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2607.26178)

[📄 Paper](https://arxiv.org/abs/2607.26178) · [💻 Repository](https://github.com/duplexgen/duplexgen-code) · [🔗 Project](https://duplexgen.github.io/) · [![★ 29](https://img.shields.io/badge/%E2%98%85%2029-eab308?style=flat-square)](https://github.com/duplexgen/duplexgen-code) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7171803236)

Calibrates turn-taking predictions with a small amount of human preference data, then synthesizes scenario-specific human–AI dialogue for full-duplex fine-tuning.

📌 Priority rationale: Explains the relationship between target interaction behaviors and data construction, including human preferences in synthesis and fine-tuning.

Organizations / maintainers: University of Illinois Urbana-Champaign; Seoul National University; University of California Berkeley; Georgia Institute of Technology; Columbia University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e42"></a>

### BayLing-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.14528) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2606.14528)

[📄 Paper](https://arxiv.org/abs/2606.14528) · [💻 Repository](https://github.com/BayLing-Models/BayLing-Duplex) · [![★ 96](https://img.shields.io/badge/%E2%98%85%2096-eab308?style=flat-square)](https://github.com/BayLing-Models/BayLing-Duplex) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7164829614)

Uses a single autoregressive LLM and a small set of state tokens to jointly model listening, speaking, and stopping, with SFT and DPO.

Organizations / maintainers: Institute of Computing Technology, Chinese Academy of Sciences; University of Chinese Academy of Sciences

<sub>Count snapshot: 2026-11-03</sub>

<a id="e43"></a>

### MultiTalk / MultiTalkBench

[![NeurIPS 2026 · author-reported](https://img.shields.io/badge/NeurIPS%202026%20%C2%B7%20author--reported-475569?style=flat-square)](https://arxiv.org/abs/2609.36903) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.36903)

[📄 Paper](https://arxiv.org/abs/2609.36903) · [🔗 Pretraining data](https://huggingface.co/datasets/MultiTalk/MultiTalkPT) · [🔗 Fine-tuning data](https://huggingface.co/datasets/MultiTalk/MultiTalkFT) · [🔗 Benchmark](https://huggingface.co/datasets/MultiTalk/MultiTalkBench) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214898838)

Extends full-duplex speech modeling to long, multiparty, bilingual conversations, releasing pretraining/fine-tuning data and a benchmark based on real recordings.

NeurIPS 2026 is reported by the authors on arXiv. Keep MultiTalkBench separate from model training data.

Organizations / maintainers: The Chinese University of Hong Kong; Centre for Perceptual and Interactive Intelligence (InnoHK)

<sub>Count snapshot: 2026-11-03</sub>

<a id="e44"></a>

### ⭐ Self-Listening / LoopSpeech

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.05592) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.05592)

[📄 Paper](https://arxiv.org/abs/2609.05592) · [💻 Repository](https://github.com/FreedomIntelligence/LoopSpeech) · [![★ 8](https://img.shields.io/badge/%E2%98%85%208-eab308?style=flat-square)](https://github.com/FreedomIntelligence/LoopSpeech) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212059771)

Adds actually played speech to the history, distinguishing intended speech from what the user has heard, to study continuity after interruption.

📌 Priority rationale: Analyzes post-interruption dialogue state and subsequent responses conditioned on played-back history.

Organizations / maintainers: Shenzhen Loop Area Institute; The Chinese University of Hong Kong, Shenzhen

<sub>Count snapshot: 2026-11-03</sub>

<a id="e45"></a>

### D2: Dialogue-to-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.17124) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2610.17124)

[📄 Paper](https://arxiv.org/abs/2610.17124) · [💻 Repository](https://github.com/penguinfish1688/D2-dialogue-to-duplex) · [🔗 Project](https://d2-duplex-demo.github.io/) · [![★ 11](https://img.shields.io/badge/%E2%98%85%2011-eab308?style=flat-square)](https://github.com/penguinfish1688/D2-dialogue-to-duplex) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221777691)

Adapts half-duplex speech backbones to full duplex, examining the quality, latency, and compute trade-offs of audio chunk intervals.

The repository currently offers a Qwen3-Omni 80 ms checkpoint. Reported acoustic latency excludes some compute and service overhead.

Organizations / maintainers: MIT CSAIL; MIT–IBM Watson AI Lab

<sub>Count snapshot: 2026-11-03</sub>

<a id="e46"></a>

### TASTE2

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.08956) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.08956)

[📄 Paper](https://arxiv.org/abs/2609.08956) · [💻 Repository](https://github.com/GitYCC/TASTE-SpokenLM-2) · [🔗 Project](https://gitycc.github.io/TASTE2-Homepage/) · [🔗 Voice application](https://github.com/GitYCC/TASTE-Voice-Bot) · [![★ 2](https://img.shields.io/badge/%E2%98%85%202-eab308?style=flat-square)](https://github.com/GitYCC/TASTE-SpokenLM-2) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212080144)

Combines text-aligned speech modeling with deployment design for full-duplex interaction, including paralinguistic signals and real-time operation.

Organizations / maintainers: MediaTek Research; National Taiwan University; NVIDIA AI Technology Center

<sub>Count snapshot: 2026-11-03</sub>

<a id="e47"></a>

### IRAF

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.06559) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2606.06559)

[📄 Paper](https://arxiv.org/abs/2606.06559) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7163910264)

Estimates target-speaker reliability frame by frame and adaptively fuses audio to improve full-duplex robustness against interfering speakers.

Organizations / maintainers: The Chinese University of Hong Kong; Huawei Leibniz Research Center; Nanyang Technological University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e48"></a>

### ⭐ MoshiRAG

[![ICML 2026 · author-reported](https://img.shields.io/badge/ICML%202026%20%C2%B7%20author--reported-475569?style=flat-square)](https://arxiv.org/abs/2604.12928) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.12928)

[📄 Paper](https://arxiv.org/abs/2604.12928) · [💻 Repository](https://github.com/kyutai-labs/moshi-rag) · [![★ 195](https://img.shields.io/badge/%E2%98%85%20195-eab308?style=flat-square)](https://github.com/kyutai-labs/moshi-rag) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7154507545)

Triggers retrieval asynchronously and injects knowledge into ongoing full-duplex conversation.

📌 Priority rationale: Study the interfaces, triggers, and result injection linking continuous speech interaction with slower retrieval.

ICML 2026 acceptance is reported by the authors on arXiv. Retrieval tasks differ in scope from general tool execution.

Organizations / maintainers: Toyota Technological Institute at Chicago; Kyutai; Gradium

<sub>Count snapshot: 2026-11-03</sub>

<a id="e49"></a>

### Frontend–Backend Tool Calling

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.19334) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.19334)

[📄 Paper](https://arxiv.org/abs/2609.19334) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213611583)

Separates a real-time speech frontend from a text-based tool backend, connecting streaming transcription, tool execution, and prefill-and-repeat result delivery.

Publication status is currently preprint; ICASSP 2027 is listed by the authors as a submission plan.

Organizations / maintainers: NVIDIA

<sub>Count snapshot: 2026-11-03</sub>

<a id="e50"></a>

### DiffuPlex · Rolling Masked Diffusion

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.12214) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2610.12214)

[📄 Paper](https://arxiv.org/abs/2610.12214) · [🔗 Project](https://diffuplex.github.io/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221088445)

Uses rolling masked diffusion to predict interaction frames, reducing backbone calls while studying interaction quality.

Distinct from NVIDIA's discrete-diffusion paper; use full titles to disambiguate the shared project name.

Organizations / maintainers: University of Seoul

<sub>Count snapshot: 2026-11-03</sub>

<a id="e51"></a>

### Diffuplex · Discrete Diffusion

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.17780) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2610.17780)

[📄 Paper](https://arxiv.org/abs/2610.17780) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221757954)

Uses autoregression to decide when to speak and discrete diffusion to generate content in parallel, studying full-duplex generation efficiency.

The paper announces code and checkpoint releases; a downloadable version has not been verified for this entry.

Organizations / maintainers: NVIDIA

<sub>Count snapshot: 2026-11-03</sub>

<a id="e52"></a>

### Voice-Light

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.20995)

[📄 Paper](https://arxiv.org/abs/2609.20995) · [💻 Repository](https://github.com/BertilBraun/Voice-Light) · [![★ 10](https://img.shields.io/badge/%E2%98%85%2010-eab308?style=flat-square)](https://github.com/BertilBraun/Voice-Light) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213934747)

A cascaded system with causal turn-taking, speculative generation, and reversible playback; playback acknowledgments update durable conversation history.

The online experiment comprises three operator runs totaling 36 turns, providing an engineering case; broader user effects require further evaluation. Institutional affiliation is unverified.

Organizations / maintainers: Bertil Braun

<sub>Count snapshot: 2026-11-03</sub>

<a id="e53"></a>

### AdaptDuplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.29217) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.29217)

[📄 Paper](https://arxiv.org/abs/2609.29217) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214079271)

Combines adaptive perception windows, non-blocking cognitive consolidation, and external reasoning for dynamic full-duplex interaction and staged post-training.

The verified resource is the technical paper; availability of model weights and the complete training pipeline remains unverified.

Organizations / maintainers: Zuoyebang Education Technology

<sub>Count snapshot: 2026-11-03</sub>

<a id="e54"></a>

### Realtime-Venus

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.13814) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.13814)

[📄 Paper](https://arxiv.org/abs/2609.13814) · [💻 Repository](https://github.com/inclusionAI/Realtime-Venus) · [![★ 252](https://img.shields.io/badge/%E2%98%85%20252-eab308?style=flat-square)](https://github.com/inclusionAI/Realtime-Venus) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213284145)

A real-time interaction layer delegates background tasks asynchronously and incorporates returned results, connecting multimodal input, trained policies, and runtime design.

Organizations / maintainers: Ant Group; Tsinghua University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e55"></a>

### NemotronLabs VoiceChat

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.21967) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.21967)

[📄 Paper](https://arxiv.org/abs/2609.21967) · [💻 Repository](https://github.com/NVIDIA-NeMo/Speech/tree/nemotron-labs-voicechat) · [🔗 Model](https://huggingface.co/nvidia/NVIDIA-NemotronLabs-VoiceChat-11B) · [![★ 18,685](https://img.shields.io/badge/%E2%98%85%2018%2C685-eab308?style=flat-square)](https://github.com/NVIDIA-NeMo/Speech/tree/nemotron-labs-voicechat) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213936344)

An open full-duplex speech model using a separate tool channel for action calls and interruptible speech output.

Code is linked to the nemotron-labs-voicechat branch of NVIDIA-NeMo/Speech. Stars refer to the entire Speech repository.

Organizations / maintainers: NVIDIA

<sub>Count snapshot: 2026-11-03</sub>

<a id="e56"></a>

### StepAudio 3 Realtime

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.14005) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.14005)

[📄 Paper](https://arxiv.org/abs/2609.14005) · [🔗 Project](https://stepaudiollm.github.io/step-audio-3-realtime/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213371127)

Organizes real-time speech interaction around listening, conversing, thinking, and acting, with Think-While-Speaking and asynchronous tool execution.

This entry links the paper and demonstration for this version; availability of a complete implementation is verified separately for this release.

Organizations / maintainers: StepFun

<sub>Count snapshot: 2026-11-03</sub>

<a id="e57"></a>

### Qwen-Audio-3.1-Realtime

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.25176) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.25176)

[📄 Paper](https://arxiv.org/abs/2609.25176) · [💻 Repository](https://github.com/QwenAudio/qwen-audio-agent) · [![★ 3,112](https://img.shields.io/badge/%E2%98%85%203%2C112-eab308?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214103824)

Uses Agent GRPO in executable environments and multimodal policy distillation to study task reliability and interaction post-training.

qwen-audio-agent provides the companion runtime; model-weight and training-code availability are recorded separately.

Organizations / maintainers: Alibaba / Qwen

<sub>Count snapshot: 2026-11-03</sub>

<a id="e58"></a>

### ⭐ DuplexOmni

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.09186) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2606.09186)

[📄 Paper](https://arxiv.org/abs/2606.09186) · [💻 Repository](https://github.com/MuyeHuang/DuplexOmni) · [![★ 145](https://img.shields.io/badge/%E2%98%85%20145-eab308?style=flat-square)](https://github.com/MuyeHuang/DuplexOmni) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7164028919)

Coordinates real-time interaction with asynchronous reasoning, using a Writer–Director synthesis pipeline for concurrent listening, seeing, thinking, and speaking.

📌 Priority rationale: Trace the relationship between real-time interaction, asynchronous reasoning, and synthetic data as a reference for end-to-end design.

Organizations / maintainers: Xi’an Jiaotong University; Peking University; Meituan

<sub>Count snapshot: 2026-11-03</sub>

<a id="embodied"></a>

## 🤖 Embodied interaction and language feedback

<a id="e13"></a>

### Interactive Language / Language Table

[![IEEE RA-L 2024](https://img.shields.io/badge/IEEE%20RA--L%202024-475569?style=flat-square)](https://doi.org/10.1109/LRA.2023.3295255) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2210.06407)

[📄 Paper](https://arxiv.org/abs/2210.06407) · [💻 Repository](https://github.com/google-research/language-table) · [![★ 367](https://img.shields.io/badge/%E2%98%85%20367-eab308?style=flat-square)](https://github.com/google-research/language-table) [![Cite OA 113](https://img.shields.io/badge/Cite%20OA%20113-0284c7?style=flat-square)](https://openalex.org/W4391759936)

Uses real-time language guidance to steer visuomotor policies, allowing people to adjust a robot's behavior during a task.

Organizations / maintainers: Robotics at Google

<sub>Count snapshot: 2026-11-02</sub>

<a id="e25"></a>

### ⭐ Hi Robot

[![ICML 2025](https://img.shields.io/badge/ICML%202025-475569?style=flat-square)](https://proceedings.mlr.press/v267/shi25d.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.19417)

[📄 Paper](https://arxiv.org/abs/2502.19417) · [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4416045178) [![Cite S2 319](https://img.shields.io/badge/Cite%20S2%20319-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/69afd10d387423a03617d461c3f47a5f3033cc54)

High-level vision-language reasoning converts complex requests and execution-time feedback into the next task; a lower-level VLA executes actions.

📌 Priority rationale: Shows how execution feedback changes task decomposition through high-level language reasoning and a low-level action policy.

Language feedback reaches the action policy through high-level planning; contributions from raw speech features require a separate ablation.

Organizations / maintainers: Physical Intelligence; Stanford University; UC Berkeley

<sub>Count snapshot: 2026-11-02</sub>

<a id="e26"></a>

### Yell At Your Robot / YAY Robot

[![RSS 2024](https://img.shields.io/badge/RSS%202024-475569?style=flat-square)](https://roboticsproceedings.org/rss20/p025.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2403.12910)

[📄 Paper](https://arxiv.org/abs/2403.12910) · [💻 Repository](https://github.com/yay-robot/yay_robot) · [![★ 166](https://img.shields.io/badge/%E2%98%85%20166-eab308?style=flat-square)](https://github.com/yay-robot/yay_robot) [![Cite OA 47](https://img.shields.io/badge/Cite%20OA%2047-0284c7?style=flat-square)](https://openalex.org/W4402354098) [![Cite S2 179](https://img.shields.io/badge/Cite%20S2%20179-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/f213d0cb84b6afca9a4d5722081ba3052e7e89bc)

Uses spoken corrections during long robot tasks for immediate adjustment and subsequent high-level policy training.

Reading focus: Understand how execution-time corrections support both current control and later learning.

Spoken corrections primarily enter control and learning through language representations.

Organizations / maintainers: Stanford University; UC Berkeley

<sub>Count snapshot: 2026-11-02</sub>

<a id="e24"></a>

### ⭐ VLAS

[![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2025/hash/804a1a9de5787e3597b4bb64e1a48ec3-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.13508)

[📄 Paper](https://arxiv.org/abs/2502.13508) · [💻 Repository](https://github.com/whichwhichgone/VLAS) · [![★ 50](https://img.shields.io/badge/%E2%98%85%2050-eab308?style=flat-square)](https://github.com/whichwhichgone/VLAS) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4407764312) [![Cite S2 68](https://img.shields.io/badge/Cite%20S2%2068-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/f6075ce4db8dcc359c3ac97b85f2644dc5cadda6)

Conditions visuomotor action on raw speech and retrieves speaker-specific information for personalized manipulation.

📌 Priority rationale: Provides a concrete example of adding a speech encoder to a visuomotor model and studying speech-instruction adaptation and speaker-conditioned manipulation.

Evaluation focuses on spoken instructions and speaker-based personalization; full-duplex speech/action interaction requires separate evaluation.

Organizations / maintainers: Westlake University; Zhejiang University; Xi’an Jiaotong University

<sub>Count snapshot: 2026-11-02</sub>

<a id="e21"></a>

### RoboOmni (OpenMOSS)

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/33610fba262d7b6fed0810b89f55e147-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2510.23763)

[📄 Paper](https://arxiv.org/abs/2510.23763) · [💻 Repository](https://github.com/OpenMOSS/RoboOmni) · [![★ 124](https://img.shields.io/badge/%E2%98%85%20124-eab308?style=flat-square)](https://github.com/OpenMOSS/RoboOmni) [![Cite S2 12](https://img.shields.io/badge/Cite%20S2%2012-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/37cd1e4cbfbfdadc2a898a703ab46bc0e1c83dd3)

Infers intent from dialogue, environmental sound, and vision, then produces manipulation actions after confirmation; studies proactive assistance from implicit contextual instructions.

Reading focus: Understand how environmental sounds and implicit intent enter manipulation tasks.

This entry refers to RoboOmni by the OpenMOSS team.

Organizations / maintainers: Fudan University; Shanghai Innovation Institute; National University of Singapore

<sub>Count snapshot: 2026-11-02</sub>

<a id="e22"></a>

### ⭐ ELLSA

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/6d8af672c0bca7a4be6f0cd0d229c05c-Abstract-Conference.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.16756)

[📄 Paper](https://arxiv.org/abs/2510.16756) · [💻 Repository](https://github.com/bytedance/SALMONN) · [![★ 1,564](https://img.shields.io/badge/%E2%98%85%201%2C564-eab308?style=flat-square)](https://github.com/bytedance/SALMONN) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415958597) [![Cite S2 7](https://img.shields.io/badge/Cite%20S2%207-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/3af611e47c30a439f8acad312f16cf7837ddbce7)

Processes vision, text, speech, and action in a unified architecture, supporting concurrent speech/action, action interruption, and grounded question answering.

📌 Priority rationale: Provides a concrete example of joint speech/action expert training, concurrent speaking and acting, action interruption, and staged adaptation.

Star counts cover the entire SALMONN repository; ELLSA weights and training resources are listed in its dedicated branch and model page.

Organizations / maintainers: Tsinghua University; ByteDance

<sub>Count snapshot: 2026-11-02</sub>

<a id="e23"></a>

### VITA-E

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.21817) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.21817)

[📄 Paper](https://arxiv.org/abs/2510.21817) · [💻 Repository](https://github.com/Tencent/VITA) · [![★ 166](https://img.shields.io/badge/%E2%98%85%20166-eab308?style=flat-square)](https://github.com/Tencent/VITA) [![Cite S2 2](https://img.shields.io/badge/Cite%20S2%202-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/62d932e380f9ec7de5d43c17bc933a05887b0007)

Uses parallel active/listening models and control tokens to schedule speech and action, supporting interruption, task switching, and concurrent speech/action.

Organizations / maintainers: Nanjing University; CASIA; Tencent Youtu Lab; Fourier Intelligence

<sub>Count snapshot: 2026-11-02</sub>

<a id="e95"></a>

### NaVILA

[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://navila-bot.github.io/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2412.04453)

[📄 Paper](https://arxiv.org/abs/2412.04453) · [💻 Repository](https://github.com/AnjieCheng/NaVILA) · [🔗 Locomotion](https://github.com/yang-zj1026/legged-loco) · [![★ 731](https://img.shields.io/badge/%E2%98%85%20731-eab308?style=flat-square)](https://github.com/AnjieCheng/NaVILA) [![Cite OA 55](https://img.shields.io/badge/Cite%20OA%2055-0284c7?style=flat-square)](https://openalex.org/W4414050442)

A high-level VLA emits spatial-language commands for a low-level visual locomotion policy, with experiments on Go2 and other platforms.

Reading focus: Explains the relationship between language navigation goals, the high/low-level policy interface, and execution feedback.

Organizations / maintainers: UC San Diego; University of Southern California; NVIDIA

<sub>Count snapshot: 2026-11-03</sub>

<a id="e11"></a>

### Reachy Mini Conversation App

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)

[💻 Repository](https://github.com/pollen-robotics/reachy_mini_conversation_app) · [![★ 348](https://img.shields.io/badge/%E2%98%85%20348-eab308?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)

Connects real-time speech, camera tools, and robot motion within a conversation application.

The application primarily covers head and antenna expression and visual tool use.

Organizations / maintainers: Pollen Robotics / Hugging Face

<sub>Count snapshot: 2026-11-02</sub>

<a id="e12"></a>

### EMAGE / BEAT2

[![CVPR 2024](https://img.shields.io/badge/CVPR%202024-475569?style=flat-square)](https://pantomatrix.github.io/EMAGE/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2401.00374)

[📄 Paper](https://arxiv.org/abs/2401.00374) · [💻 Repository](https://github.com/haiyangliu0/character-policy) · [![★ 1,312](https://img.shields.io/badge/%E2%98%85%201%2C312-eab308?style=flat-square)](https://github.com/haiyangliu0/character-policy) [![Cite OA 95](https://img.shields.io/badge/Cite%20OA%2095-0284c7?style=flat-square)](https://openalex.org/W4402727140)

Generates coordinated body and facial motion from speech and text, connecting co-speech gesture methods with expressive motion data.

The scope is co-speech gestures and character expression; physical robot manipulation requires separate evaluation.

Organizations / maintainers: The University of Tokyo; Keio University; Max Planck Institute for Intelligent Systems; JAIST; Tsinghua University

<sub>Count snapshot: 2026-11-02</sub>

<a id="robotics"></a>

## 🦾 Actions, data, and deployment

<a id="e19"></a>

### LeRobot

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.22818) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2602.22818)

[📄 Paper](https://arxiv.org/abs/2602.22818) · [💻 Repository](https://github.com/huggingface/lerobot) · [![★ 28,653](https://img.shields.io/badge/%E2%98%85%2028%2C653-eab308?style=flat-square)](https://github.com/huggingface/lerobot) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7131860508)

An open toolkit for robot datasets, policy training, hardware control, and evaluation.

Reading focus: Covers demonstration collection, data inspection, policy training, and real-robot execution in one workflow.

Organizations / maintainers: Hugging Face; University of Oxford

<sub>Count snapshot: 2026-11-02 / 2026-11-03</sub>

<a id="e32"></a>

### ACT / ALOHA

[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://www.roboticsproceedings.org/rss19/p016.pdf) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2304.13705)

[📄 Paper](https://arxiv.org/abs/2304.13705) · [💻 Repository](https://github.com/tonyzhaozh/act) · [![★ 2,318](https://img.shields.io/badge/%E2%98%85%202%2C318-eab308?style=flat-square)](https://github.com/tonyzhaozh/act) [![Cite OA 674](https://img.shields.io/badge/Cite%20OA%20674-0284c7?style=flat-square)](https://openalex.org/W4385430674)

Learns action chunks from teleoperated demonstrations, establishing a visuomotor imitation-learning baseline.

Reading focus: Introduces imitation learning through observations, demonstrations, and action-chunk prediction.

Standard ACT predicts actions conditioned on observations; multi-goal tasks can use a skill selector or additional goal conditioning.

Organizations / maintainers: Stanford University; Meta; UC Berkeley

<sub>Count snapshot: 2026-11-03</sub>

<a id="e33"></a>

### Diffusion Policy

[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![IJRR 2024](https://img.shields.io/badge/IJRR%202024-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2303.04137)

[📄 Paper](https://arxiv.org/abs/2303.04137v4) · [💻 Repository](https://github.com/real-stanford/diffusion_policy) · [![★ 4,698](https://img.shields.io/badge/%E2%98%85%204%2C698-eab308?style=flat-square)](https://github.com/real-stanford/diffusion_policy) [![Cite OA 12](https://img.shields.io/badge/Cite%20OA%2012-0284c7?style=flat-square)](https://openalex.org/W4323651335)

Models conditional action distributions through denoising to generate continuous action sequences.

The linked paper is the RSS 2023 version; IJRR 2024 is an extension. Citation counts refer to the linked database record.

Organizations / maintainers: Columbia University; Toyota Research Institute; MIT

<sub>Count snapshot: 2026-11-03</sub>

<a id="e34"></a>

### SmolVLA

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2506.01844) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2506.01844)

[📄 Paper](https://arxiv.org/abs/2506.01844) · [💻 Repository](https://github.com/huggingface/lerobot) · [![★ 28,653](https://img.shields.io/badge/%E2%98%85%2028%2C653-eab308?style=flat-square)](https://github.com/huggingface/lerobot) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4414898213)

An efficient pretrained VLA reference for adapting language-conditioned actions to robot demonstrations.

Reading focus: Provides an official tutorial and implementation for adapting a pretrained VLA to robot data.

The policy is conditioned on text instructions. Stars cover the entire LeRobot repository; end-to-end real-time performance includes perception and control.

Organizations / maintainers: Hugging Face; Sorbonne University; valeo.ai; ENS Paris-Saclay

<sub>Count snapshot: 2026-11-03</sub>

<a id="e20"></a>

### OpenVLA

[![CoRL 2024](https://img.shields.io/badge/CoRL%202024-475569?style=flat-square)](https://proceedings.mlr.press/v270/kim25c.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2406.09246)

[📄 Paper](https://arxiv.org/abs/2406.09246) · [💻 Repository](https://github.com/openvla/openvla) · [![★ 7,250](https://img.shields.io/badge/%E2%98%85%207%2C250-eab308?style=flat-square)](https://github.com/openvla/openvla) [![Cite OA 62](https://img.shields.io/badge/Cite%20OA%2062-0284c7?style=flat-square)](https://openalex.org/W4399695759)

A vision-language-conditioned robot action model, providing a foundation for connecting interaction layers with action policies.

A vision/language-to-action foundation; native speech and real-time interruption need additional system design.

Organizations / maintainers: Stanford University; UC Berkeley; MIT; Toyota Research Institute; Google DeepMind; Physical Intelligence

<sub>Count snapshot: 2026-11-02</sub>

<a id="e91"></a>

### ⭐ openpi / π0 · π0.5

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2504.16054) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2504.16054)

[📄 Paper](https://arxiv.org/abs/2504.16054) · [💻 Repository](https://github.com/Physical-Intelligence/openpi) · [🔗 π0 paper](https://arxiv.org/abs/2410.24164) · [🔗 π0.5 blog](https://www.physicalintelligence.company/blog/pi05) · [![★ 14,510](https://img.shields.io/badge/%E2%98%85%2014%2C510-eab308?style=flat-square)](https://github.com/Physical-Intelligence/openpi) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4414674749)

Releases π0, π0-FAST, and π0.5 weights, inference, and adaptation code, connecting VLMs to continuous actions and multi-robot data.

📌 Priority rationale: π0 introduces the VLM–action-expert interface; π0.5 extends the discussion to heterogeneous co-training and generalization to new environments.

Citation counts in this entry refer to π0.5; stars refer to openpi. The original π0 paper is linked separately. LoRA uses the JAX implementation; see official documentation for the PyTorch feature set.

Organizations / maintainers: Physical Intelligence

<sub>Count snapshot: 2026-11-03</sub>

<a id="e92"></a>

### Isaac GR00T N1.7

[![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T)

[💻 Repository](https://github.com/NVIDIA/Isaac-GR00T) · [🔗 N1 background paper](https://arxiv.org/abs/2503.14734) · [![★ 8,308](https://img.shields.io/badge/%E2%98%85%208%2C308-eab308?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T)

A 3B vision-language-action base with pretrained weights, new-embodiment data adaptation, and fine-tuning workflows.

Reading focus: Read embodiment configuration, action spaces, and custom-data fine-tuning to compare industrial adaptation costs.

The current repository is N1.7; the background paper describes the earlier N1. Read configurations and results by version.

Organizations / maintainers: NVIDIA

<sub>Count snapshot: 2026-11-03</sub>

<a id="e93"></a>

### OpenVLA-OFT

[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://roboticsproceedings.org/rss21/p017.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.19645)

[📄 Paper](https://arxiv.org/abs/2502.19645) · [💻 Repository](https://github.com/moojink/openvla-oft) · [🔗 Project](https://openvla-oft.github.io/) · [![★ 1,440](https://img.shields.io/badge/%E2%98%85%201%2C440-eab308?style=flat-square)](https://github.com/moojink/openvla-oft) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W6948104436)

Builds on OpenVLA with parallel decoding, action chunks, continuous actions, L1 training, and FiLM for language control.

Reading focus: A clear base, open training, and explicit compute requirements make it useful for studying adaptation methods.

Organizations / maintainers: Stanford University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e94"></a>

### SimpleVLA-RL

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/cbfbcb4da14235bd69b134070898ae9d-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2509.09674)

[📄 Paper](https://arxiv.org/abs/2509.09674) · [💻 Repository](https://github.com/PRIME-RL/SimpleVLA-RL) · [![★ 1,903](https://img.shields.io/badge/%E2%98%85%201%2C903-eab308?style=flat-square)](https://github.com/PRIME-RL/SimpleVLA-RL) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W7081569152)

Applies RL to VLAs including OpenVLA-OFT, with training, rollout, and evaluation workflows for LIBERO and RoboTwin.

Reading focus: Read after SFT to examine environment rewards, rollout cost, and generalization evaluation.

Organizations / maintainers: Tsinghua University; Shanghai AI Lab; Shanghai Jiao Tong University; Peking University; University of Hong Kong

<sub>Count snapshot: 2026-11-03</sub>

<a id="e97"></a>

### Unitree SDK2 / MuJoCo

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/unitreerobotics/unitree_sdk2) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/unitreerobotics/unitree_sdk2)

[💻 Repository](https://github.com/unitreerobotics/unitree_sdk2) · [🔗 Python SDK](https://github.com/unitreerobotics/unitree_sdk2_python) · [🔗 MuJoCo](https://github.com/unitreerobotics/unitree_mujoco) · [![★ 1,431](https://img.shields.io/badge/%E2%98%85%201%2C431-eab308?style=flat-square)](https://github.com/unitreerobotics/unitree_sdk2)

Unitree communication/control interfaces and a MuJoCo simulation entry point based on SDK2.

Reading focus: Provides state, command, and device interfaces for connecting the task layer to executable skills.

unitree_mujoco primarily targets low-level control; check interface support for the specific robot and firmware.

Organizations / maintainers: Unitree Robotics

<sub>Count snapshot: 2026-11-03</sub>

<a id="e98"></a>

### Unitree RL mjlab

[![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab)

[💻 Repository](https://github.com/unitreerobotics/unitree_rl_mjlab) · [![★ 719](https://img.shields.io/badge/%E2%98%85%20719-eab308?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab)

MuJoCo/mjlab locomotion-policy training and deployment tools, including Go2 configurations.

Reading focus: Use official configurations to understand training, simulation playback, and deployment.

Organizations / maintainers: Unitree Robotics

<sub>Count snapshot: 2026-11-03</sub>

<a id="e99"></a>

### ASAP

[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://agile.human2humanoid.com/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.01143)

[📄 Paper](https://arxiv.org/abs/2502.01143) · [💻 Repository](https://github.com/LeCAR-Lab/ASAP) · [![★ 2,138](https://img.shields.io/badge/%E2%98%85%202%2C138-eab308?style=flat-square)](https://github.com/LeCAR-Lab/ASAP) [![Cite OA 58](https://img.shields.io/badge/Cite%20OA%2058-0284c7?style=flat-square)](https://openalex.org/W4414051111)

Learns discrepancies between simulated and real dynamics from robot data to adapt whole-body motion policies.

Organizations / maintainers: Carnegie Mellon University; NVIDIA

<sub>Count snapshot: 2026-11-03</sub>

<a id="e100"></a>

### TWIST2

[![ICRA 2026](https://img.shields.io/badge/ICRA%202026-475569?style=flat-square)](https://yanjieze.com/projects/TWIST2/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2511.02832)

[📄 Paper](https://arxiv.org/abs/2511.02832) · [💻 Repository](https://github.com/amazon-far/TWIST2) · [🔗 TWIST](https://yanjieze.com/projects/TWIST/) · [![★ 894](https://img.shields.io/badge/%E2%98%85%20894-eab308?style=flat-square)](https://github.com/amazon-far/TWIST2) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7103984447)

Whole-body teleoperation and motion tracking for collecting humanoid data with contact and bimanual coordination.

Controller training and teleoperation are released; check the separate release status of the high-level visuomotor policy.

Organizations / maintainers: Amazon FAR; Stanford University; University of Southern California; UC Berkeley; Carnegie Mellon University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e101"></a>

### RoboTwin 2.0

[![ICML 2026](https://img.shields.io/badge/ICML%202026-475569?style=flat-square)](https://github.com/RoboTwin-Platform/RoboTwin) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2506.18088)

[📄 Paper](https://arxiv.org/abs/2506.18088) · [💻 Repository](https://github.com/RoboTwin-Platform/RoboTwin) · [![★ 3,032](https://img.shields.io/badge/%E2%98%85%203%2C032-eab308?style=flat-square)](https://github.com/RoboTwin-Platform/RoboTwin) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W6929480010)

Builds bimanual tasks through automated simulation data generation and domain randomization, with pre-collected trajectories.

Reading focus: Provides data for policy training and evaluation, with task generation and domain randomization.

Organizations / maintainers: Shanghai AI Lab; Shenzhen University; Nanjing University; SJTU; HKU; TeleAI; D-Robotics

<sub>Count snapshot: 2026-11-03</sub>

<a id="e102"></a>

### RDT-1B

[![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://github.com/thu-ml/RoboticsDiffusionTransformer) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2410.07864)

[📄 Paper](https://arxiv.org/abs/2410.07864) · [💻 Repository](https://github.com/thu-ml/RoboticsDiffusionTransformer) · [![★ 1,816](https://img.shields.io/badge/%E2%98%85%201%2C816-eab308?style=flat-square)](https://github.com/thu-ml/RoboticsDiffusionTransformer) [![Cite OA 5](https://img.shields.io/badge/Cite%20OA%205-0284c7?style=flat-square)](https://openalex.org/W4403364995)

A diffusion base for bimanual manipulation with a unified action representation and a lighter 170M variant.

Organizations / maintainers: Tsinghua University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e17"></a>

### llama.cpp ecosystem

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/OpenBMB/llama.cpp-omni) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/ggml-org/llama.cpp/discussions/19759)

[💻 Repository](https://github.com/ggml-org/llama.cpp) · [![★ 133,116](https://img.shields.io/badge/%E2%98%85%20133%2C116-eab308?style=flat-square)](https://github.com/ggml-org/llama.cpp)

A local inference toolchain offering quantization and execution across platforms.

Complete Omni modes may require a dedicated branch such as OpenBMB/llama.cpp-omni.

Organizations / maintainers: ggml.ai / Hugging Face; llama.cpp contributor community

<sub>Count snapshot: 2026-11-02</sub>

<a id="e18"></a>

### MNN

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni#deployment-with-mnn) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/alibaba/MNN)

[💻 Repository](https://github.com/alibaba/MNN) · [![★ 16,336](https://img.shields.io/badge/%E2%98%85%2016%2C336-eab308?style=flat-square)](https://github.com/alibaba/MNN)

An inference framework for mobile and edge devices, with an official integration entry point for Qwen2.5-Omni.

Organizations / maintainers: Alibaba

<sub>Count snapshot: 2026-11-02</sub>

<a id="evaluation"></a>

## 📏 Evaluation

<a id="e14"></a>

### Daily-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2505.17862) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2505.17862)

[📄 Paper](https://arxiv.org/abs/2505.17862) · [💻 Repository](https://github.com/Lliar-liar/Daily-Omni) · [![★ 53](https://img.shields.io/badge/%E2%98%85%2053-eab308?style=flat-square)](https://github.com/Lliar-liar/Daily-Omni) Cite —

A benchmark for temporally aligned audiovisual reasoning in everyday video.

Organizations / maintainers: Fudan University

<sub>Count snapshot: 2026-11-02</sub>

<a id="e15"></a>

### OmniBench (m-a-p)

[![NeurIPS 2025](https://img.shields.io/badge/NeurIPS%202025-475569?style=flat-square)](https://arxiv.org/abs/2409.15272) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2409.15272)

[📄 Paper](https://arxiv.org/abs/2409.15272) · [💻 Repository](https://github.com/multimodal-art-projection/OmniBench) · [![★ 62](https://img.shields.io/badge/%E2%98%85%2062-eab308?style=flat-square)](https://github.com/multimodal-art-projection/OmniBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4403885114) [![Cite S2 111](https://img.shields.io/badge/Cite%20S2%20111-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/bde43a6356341b68a675582cf964fd9725fb40fb)

A benchmark for joint image, audio, and text understanding, accompanied by OmniInstruct.

Organizations / maintainers: M-A-P; University of Manchester; Queen Mary University of London; 01.ai; HKUST; Nanjing University; Dartmouth College

<sub>Count snapshot: 2026-11-02</sub>

<a id="e16"></a>

### ⭐ Full-Duplex-Bench

[![ASRU 2025](https://img.shields.io/badge/ASRU%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.04721) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2503.04721)

[📄 Paper](https://arxiv.org/abs/2503.04721) · [💻 Repository](https://github.com/DanielLin94144/Full-Duplex-Bench) · [![★ 335](https://img.shields.io/badge/%E2%98%85%20335-eab308?style=flat-square)](https://github.com/DanielLin94144/Full-Duplex-Bench) [![Cite OA 8](https://img.shields.io/badge/Cite%20OA%208-0284c7?style=flat-square)](https://openalex.org/W7148492801)

Evaluates pauses, backchannels, turn transitions, and interruptions; later versions extend to overlap, dynamic multi-turn interaction, and tool use.

📌 Priority rationale: Translate interruptions, turn transitions, and interaction timing into measurable outcomes.

Organizations / maintainers: National Taiwan University; UC Berkeley; University of Washington; MIT CSAIL

<sub>Count snapshot: 2026-11-02 / 2026-11-03</sub>

<a id="e35"></a>

### LIBERO

[![NeurIPS Datasets and Benchmarks 2023](https://img.shields.io/badge/NeurIPS%20Datasets%20and%20Benchmarks%202023-475569?style=flat-square)](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8c3c666820ea055a77726d66fc7d447f-Abstract-Datasets_and_Benchmarks.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2306.03310)

[📄 Paper](https://arxiv.org/abs/2306.03310) · [💻 Repository](https://github.com/Lifelong-Robot-Learning/LIBERO) · [![★ 2,508](https://img.shields.io/badge/%E2%98%85%202%2C508-eab308?style=flat-square)](https://github.com/Lifelong-Robot-Learning/LIBERO) [![Cite OA 136](https://img.shields.io/badge/Cite%20OA%20136-0284c7?style=flat-square)](https://openalex.org/W7133220882)

A simulation benchmark for language-conditioned robot manipulation and lifelong learning.

Evaluates language-conditioned manipulation; speech interaction and human collaboration require additional evaluations.

Organizations / maintainers: UT Austin; Tsinghua University; Sony AI

<sub>Count snapshot: 2026-11-03</sub>

<a id="e59"></a>

### ⭐ VoiceBench

[![TACL 2026](https://img.shields.io/badge/TACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.tacl-1.18/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2410.17196)

[📄 Paper](https://arxiv.org/abs/2410.17196) · [💻 Repository](https://github.com/MatthewCYM/VoiceBench) · [![★ 407](https://img.shields.io/badge/%E2%98%85%20407-eab308?style=flat-square)](https://github.com/MatthewCYM/VoiceBench) [![Cite OA 12](https://img.shields.io/badge/Cite%20OA%2012-0284c7?style=flat-square)](https://openalex.org/W4404261856)

Evaluates voice-assistant knowledge, instruction following, safety, and response robustness under accents, noise, and other perturbations.

📌 Priority rationale: Establish a basic voice-assistant reference before comparing interaction and task outcomes separately.

Primarily evaluates responses to spoken input; continuous full-duplex interaction and tool tasks use their respective evaluations.

Organizations / maintainers: National University of Singapore

<sub>Count snapshot: 2026-11-03</sub>

<a id="e60"></a>

### VocalBench

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2505.15727) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2505.15727)

[📄 Paper](https://arxiv.org/abs/2505.15727) · [💻 Repository](https://github.com/SJTU-OmniAgent/VocalBench) · [![★ 8](https://img.shields.io/badge/%E2%98%85%208-eab308?style=flat-square)](https://github.com/SJTU-OmniAgent/VocalBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4415329203)

Covers semantic, acoustic, conversational, and robustness dimensions across single-turn and multi-turn speech interaction.

Release status and venues are recorded separately for each subset, language, and extension.

Organizations / maintainers: Shanghai Jiao Tong University; Ant Group

<sub>Count snapshot: 2026-11-03</sub>

<a id="e61"></a>

### VCB Bench

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.1659/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2510.11098)

[📄 Paper](https://arxiv.org/abs/2510.11098) · [💻 Repository](https://github.com/Tencent/VCB-Bench) · [![★ 5](https://img.shields.io/badge/%E2%98%85%205-eab308?style=flat-square)](https://github.com/Tencent/VCB-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4417101201)

Uses real Chinese speech to evaluate instruction following, knowledge understanding, and robustness to acoustic and content perturbations.

The core contribution concerns real Chinese speech; report later language extensions separately from the original protocol.

Organizations / maintainers: Wuhan University; Tencent

<sub>Count snapshot: 2026-11-03</sub>

<a id="e62"></a>

### ⭐ VoiceAgentBench

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.07978) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2510.07978)

[📄 Paper](https://arxiv.org/abs/2510.07978) · [💻 Repository](https://github.com/ola-krutrim/VoiceAgentBench) · [🔗 Data](https://huggingface.co/datasets/krutrim-ai-labs/VoiceAgentBench) · [![★ 6](https://img.shields.io/badge/%E2%98%85%206-eab308?style=flat-square)](https://github.com/ola-krutrim/VoiceAgentBench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415318706)

Connects multilingual speech input to single, parallel, sequential, and multi-turn tool tasks, testing function choice, arguments, and other agent capabilities.

📌 Priority rationale: Defines function, argument, and multi-step structure in speech tool use as a foundation for task-level evaluation.

Evaluation focuses on speech-conditioned tool structure and arguments; timing naturalness in continuous speech output is a separate metric.

Organizations / maintainers: OLA Electric / Krutrim AI

<sub>Count snapshot: 2026-11-03</sub>

<a id="e63"></a>

### ⭐ τ-Voice

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2603.13686) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2603.13686)

[📄 Paper](https://arxiv.org/abs/2603.13686) · [💻 Repository](https://github.com/sierra-research/tau2-bench) · [![★ 2,382](https://img.shields.io/badge/%E2%98%85%202%2C382-eab308?style=flat-square)](https://github.com/sierra-research/tau2-bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7138316890)

Uses domain policies and environment state to evaluate multi-turn tool use and final task completion by full-duplex voice agents.

📌 Priority rationale: Judge completion from final environment state and compare text agents with voice agents.

The tau2-bench repository continues to evolve, including later τ³ development. Pin the paper's version, environment, and user simulator.

Organizations / maintainers: Sierra; Princeton University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e64"></a>

### ⭐ Full-Duplex-Bench-v3

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.04847) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.04847)

[📄 Paper](https://arxiv.org/abs/2604.04847) · [💻 Repository](https://github.com/DanielLin94144/Full-Duplex-Bench) · [🔗 Project](https://daniellin94144.github.io/FDB-v3-demo/) · [![★ 335](https://img.shields.io/badge/%E2%98%85%20335-eab308?style=flat-square)](https://github.com/DanielLin94144/Full-Duplex-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7151544009)

Combines real spoken hesitations, repetitions, and corrections with multi-step tool use to evaluate task execution during interaction.

📌 Priority rationale: Test whether spoken corrections and other interaction disturbances cause tool-task errors.

Shares a repository with v1, v1.5, and v2 but evaluates a different task; v3 is a preprint, while v1 was published at ASRU 2025.

Organizations / maintainers: National Taiwan University; NVIDIA

<sub>Count snapshot: 2026-11-03</sub>

<a id="e65"></a>

### ⭐ MTR-DuplexBench

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.263/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2511.10262)

[📄 Paper](https://arxiv.org/abs/2511.10262) · [💻 Repository](https://github.com/ZhangHe0918/MTR-DuplexBench) · [![★ 9](https://img.shields.io/badge/%E2%98%85%209-eab308?style=flat-square)](https://github.com/ZhangHe0918/MTR-DuplexBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4416238789)

Analyzes full-duplex conversations turn by turn, combining interaction dynamics, response quality, instruction following, and safety.

📌 Priority rationale: Covers error accumulation and context dependencies across multiple interaction turns.

Organizations / maintainers: Tsinghua University; The Chinese University of Hong Kong; Huawei

<sub>Count snapshot: 2026-11-03</sub>

<a id="e66"></a>

### HumDial-FDBench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.21406) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.21406)

[📄 Paper](https://arxiv.org/abs/2604.21406) · [💻 Repository](https://github.com/ASLP-lab/HumDial-FDBench) · [![★ 44](https://img.shields.io/badge/%E2%98%85%2044-eab308?style=flat-square)](https://github.com/ASLP-lab/HumDial-FDBench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7155525302)

Uses real two-channel human dialogue to evaluate overlap, interruption, and backchannels, with a HumDial challenge and leaderboard.

The paper discusses the ICASSP 2026 HumDial challenge; this entry records the paper as a preprint.

Organizations / maintainers: Northwestern Polytechnical University / ASLP Lab; Nanjing University; AISHELL

<sub>Count snapshot: 2026-11-03</sub>

<a id="e67"></a>

### MP-Bench

[![Findings of EMNLP 2026](https://img.shields.io/badge/Findings%20of%20EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-emnlp.1437/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.13076)

[📄 Paper](https://arxiv.org/abs/2609.13076) · [💻 Repository](https://github.com/atosystem/MP-Bench) · [![★ 1](https://img.shields.io/badge/%E2%98%85%201-eab308?style=flat-square)](https://github.com/atosystem/MP-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212688662)

Evaluates a voice agent as a multiparty conversation participant, including comprehension, turn timing, and response appropriateness.

Organizations / maintainers: The University of Texas at Austin; National Taiwan University; MIT; Carnegie Mellon University; Meta AI

<sub>Count snapshot: 2026-11-03</sub>

<a id="e68"></a>

### Duplex-MPE

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.31948) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.31948)

[📄 Paper](https://arxiv.org/abs/2609.31948) · [🔗 Project](https://step-out.github.io/Duplex-MPE-Page/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214781414)

Tests participation decisions in multiparty scenes, including explicit address, implicit requests, proactive responses, and appropriate silence.

Organizations / maintainers: Peking University; Renmin University of China; Tsinghua University; National Taiwan University; Xiamen University; Fudan University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e69"></a>

### Instruct-FD

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2607.20460) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2607.20460)

[📄 Paper](https://arxiv.org/abs/2607.20460) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7170334618)

Tests whether full-duplex systems can follow instructions governing turn-taking, interruption, backchannels, and proactivity.

Organizations / maintainers: Boson AI

<sub>Count snapshot: 2026-11-03</sub>

<a id="e70"></a>

### DuplexAct-Bench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.39446) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.39446)

[📄 Paper](https://arxiv.org/abs/2609.39446) · [💻 Repository](https://github.com/Alita-xky/DuplexAct-Bench) · [🔗 Project](https://alitaxky.icu/DuplexAct-Bench/) · [![★ 1](https://img.shields.io/badge/%E2%98%85%201-eab308?style=flat-square)](https://github.com/Alita-xky/DuplexAct-Bench) Cite —

Covers interruption, yielding, resisting interruption, active silence, proactive initiation, and backchannels, evaluating timing and content separately.

The linked repository primarily contains the project website. Check the project release for complete evaluators and data.

Organizations / maintainers: Beijing Institute for General Artificial Intelligence; Peking University; Shanghai Jiao Tong University

<sub>Count snapshot: 2026-11-03</sub>

<a id="e71"></a>

### ⭐ EVA-Bench

[![Findings of EMNLP 2026](https://img.shields.io/badge/Findings%20of%20EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-emnlp.2182/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2605.13841)

[📄 Paper](https://arxiv.org/abs/2605.13841) · [💻 Repository](https://github.com/ServiceNow/eva) · [🔗 Project](https://servicenow.github.io/eva/) · [![★ 235](https://img.shields.io/badge/%E2%98%85%20235-eab308?style=flat-square)](https://github.com/ServiceNow/eva) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7161175665)

Uses dynamic bot-to-bot simulation to evaluate complete tasks and interaction experience, separating task/factual fidelity from timing and experience.

📌 Priority rationale: Learn to evaluate task correctness and experience separately, and inspect the validity of the simulated user.

Organizations / maintainers: ServiceNow AI Research

<sub>Count snapshot: 2026-11-03</sub>

<a id="e72"></a>

### VAmoS Bench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2607.27453) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2607.27453)

[📄 Paper](https://arxiv.org/abs/2607.27453) · [💻 Repository](https://github.com/veris-ai/riley-agent) · [![★ 18](https://img.shields.io/badge/%E2%98%85%2018-eab308?style=flat-square)](https://github.com/veris-ai/riley-agent) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7172022530)

Simulates voice agents in financial-service scenarios, checking complete dialogues, tool traces, and domain facts.

The evaluation domain is financial services; riley-agent provides a reference agent implementation, with complete grader availability verified separately.

Organizations / maintainers: Veris AI

<sub>Count snapshot: 2026-11-03</sub>

<a id="e73"></a>

### FD-Bench

[![Interspeech 2025](https://img.shields.io/badge/Interspeech%202025-475569?style=flat-square)](https://www.isca-archive.org/interspeech_2025/peng25b_interspeech.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2507.19040)

[📄 Paper](https://arxiv.org/abs/2507.19040) · [💻 Repository](https://github.com/pengyizhou/FD-Bench) · [![★ 27](https://img.shields.io/badge/%E2%98%85%2027-eab308?style=flat-square)](https://github.com/pengyizhou/FD-Bench) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4415433582)

A full-duplex evaluation pipeline with multi-turn interaction, interruptions, and noise, measuring generation quality and latency.

A separate project from DanielLin94144/Full-Duplex-Bench, with its own versions and scoring protocols.

Organizations / maintainers: Nanyang Technological University; Alibaba

<sub>Count snapshot: 2026-11-03</sub>

<a id="e74"></a>

### TurnBench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2608.25218) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2608.25218)

[📄 Paper](https://arxiv.org/abs/2608.25218) · [💻 Repository](https://github.com/SesameAILabs/turnbench) · [🔗 Project](https://turnbench.sesame.com/) · [![★ 57](https://img.shields.io/badge/%E2%98%85%2057-eab308?style=flat-square)](https://github.com/SesameAILabs/turnbench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7204453739)

Evaluates end-of-turn and interruption detectors through recall and latency at specified false-positive budgets.

Evaluates the turn-decision component; response content, tool use, and final task completion require additional system-level evaluation.

Organizations / maintainers: Sesame AI; Mundo AI; Oto; Carnegie Mellon University; National Taiwan University; Academia Sinica; Brno University of Technology

<sub>Count snapshot: 2026-11-03</sub>

<a id="industry"></a>

## 🏭 Industry demonstrations

<a id="e10"></a>

### WITA-Omni

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://www.agibot.com/article/231/detail/122.html) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.agibot.com/article/231/detail/122.html)

[🔗 Official page](https://www.agibot.com/article/231/detail/122.html) · —

AGIBOT's embodied interaction demonstration combines scene understanding, speech, and bodily expression.

Public material primarily presents system demonstrations; availability of action models, training data, and the complete system follows official releases.

Organizations / maintainers: AGIBOT

<a id="e27"></a>

### Gemini Live API × Robotics demo

[![Technical Demo 2025](https://img.shields.io/badge/Technical%20Demo%202025-475569?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/)

[🔗 Official page](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) · —

An official Google example feeds speech and robot-camera input into the Live API, then connects function calls to robot control interfaces.

Provides an engineering example connecting Live API to robot interfaces; Gemini Robotics releases and controlled robot success-rate studies are separate resources.

Organizations / maintainers: Google / Google DeepMind

<a id="e28"></a>

### Figure Helix 02

[![Technical Demo 2026](https://img.shields.io/badge/Technical%20Demo%202026-475569?style=flat-square)](https://www.figure.ai/news/helix-02) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.figure.ai/news/helix-02)

[🔗 Official page](https://www.figure.ai/news/helix-02) · —

Figure connects language goals with mobile manipulation through S2 semantic planning, S1 visuomotor policies, and S0 whole-body control.

Public material is a system demonstration useful for studying hierarchical design; training code and reproducible experiments depend on official releases.

Organizations / maintainers: Figure AI

<a id="e96"></a>

### Qwen-RobotNav

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.18112) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2606.18112)

[📄 Paper](https://arxiv.org/abs/2606.18112) · [💻 Repository](https://github.com/QwenLM/Qwen-RobotNav) · [![★ 198](https://img.shields.io/badge/%E2%98%85%20198-eab308?style=flat-square)](https://github.com/QwenLM/Qwen-RobotNav) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7165037828)

A Qwen3-VL navigation-system report covering task modes, context, waypoint interfaces, and Go2 deployment.

The official repository states there is no current plan to release weights; public material supports system-design and deployment reference.

Organizations / maintainers: Alibaba / Qwen Team

<sub>Count snapshot: 2026-11-03</sub>
