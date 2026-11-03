# Paper and Project Catalog

[中文](CATALOG.md) | **English**

[Home](README.en.md) · [Catalog](CATALOG.en.md) · [Surveys](SURVEYS.en.md) · [Benchmarks](05-Voice-Agent-Benchmarks.en.md)

Browse by technical topic. ⭐ marks suggested first readings. See the [label guide](README.en.md#labels) for counting conventions.

[🎧 Omni and speech models](#omni) · [💬 Voice agents and interaction systems](#voice) · [🤖 Embodied interaction and language feedback](#embodied) · [🦾 Actions, data, and deployment](#robotics) · [📏 Evaluation](#evaluation) · [🏭 Industry demonstrations](#industry)

<a id="omni"></a>

## 🎧 Omni and speech models

<a id="e01"></a>

### ⭐ MiniCPM-o 4.5

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.27393) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V)

[📄 Paper](https://arxiv.org/abs/2604.27393) · [💻 Repository](https://github.com/OpenBMB/MiniCPM-V) · [![★ 27,047](https://img.shields.io/badge/%E2%98%85%2027%2C047-eab308?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W7159670352)

Organizes continuous audio/video input and text/speech output on a shared timeline, including proactive responses.

📌 Why read first: Study continuous audiovisual input, full-duplex output, and deployment requirements.

Scope: Use the official requirements for each full-duplex mode; distinguish model memory from total system memory.

Organizations / maintainers: Tsinghua University / THUNLP; ModelBest; OpenBMB.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e02"></a>

### ⭐ Qwen2.5-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.20215) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni)

[📄 Paper](https://arxiv.org/abs/2503.20215) · [💻 Repository](https://github.com/QwenLM/Qwen2.5-Omni) · [![★ 4,092](https://img.shields.io/badge/%E2%98%85%204%2C092-eab308?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni) [![Cite OA 14](https://img.shields.io/badge/Cite%20OA%2014-0284c7?style=flat-square)](https://openalex.org/W4409051416)

Accepts audio, video, images, and text, and jointly generates text and speech; a reference for the Thinker–Talker architecture.

📌 Why read first: Establish a reference for Thinker–Talker architecture, data, and staged training.

Scope: Streaming speech output does not imply native simultaneous listening and speaking; MNN support depends on the deployment mode.

Organizations / maintainers: Qwen Team / Alibaba.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e03"></a>

### Qwen3-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.17765) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni)

[📄 Paper](https://arxiv.org/abs/2509.17765) · [💻 Repository](https://github.com/QwenLM/Qwen3-Omni) · [![★ 4,093](https://img.shields.io/badge/%E2%98%85%204%2C093-eab308?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4415255153)

An MoE Thinker–Talker approach covering multimodal understanding and real-time speech generation.

Organizations / maintainers: Qwen Team / Alibaba.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e04"></a>

### InteractiveOmni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.13747) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2510.13747)

[📄 Paper](https://arxiv.org/abs/2510.13747) · [💻 Repository](https://github.com/OpenSenseNova/InteractiveOmni) · [![★ 9](https://img.shields.io/badge/%E2%98%85%209-eab308?style=flat-square)](https://github.com/OpenSenseNova/InteractiveOmni) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415277372)

Targets audiovisual multi-turn interaction, with 4B and 8B models and multi-turn evaluation.

Organizations / maintainers: SenseTime Research.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e05"></a>

### VITA-1.5

[![NeurIPS 2025](https://img.shields.io/badge/NeurIPS%202025-475569?style=flat-square)](https://arxiv.org/abs/2501.01957) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2501.01957)

[📄 Paper](https://arxiv.org/abs/2501.01957) · [💻 Repository](https://github.com/VITA-MLLM/VITA) · [![★ 2,539](https://img.shields.io/badge/%E2%98%85%202%2C539-eab308?style=flat-square)](https://github.com/VITA-MLLM/VITA) [![Cite OA 11](https://img.shields.io/badge/Cite%20OA%2011-0284c7?style=flat-square)](https://openalex.org/W4406093559)

A multimodal model for real-time visual and speech interaction, with training and inference workflows.

Organizations / maintainers: Nanjing University; Xiamen University; CASIA; Tencent Youtu Lab.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e06"></a>

### Mini-Omni2

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.11190) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2410.11190)

[📄 Paper](https://arxiv.org/abs/2410.11190) · [💻 Repository](https://github.com/gpt-omni/mini-omni2) · [![★ 1,936](https://img.shields.io/badge/%E2%98%85%201%2C936-eab308?style=flat-square)](https://github.com/gpt-omni/mini-omni2) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4403576555)

An early open experimental system supporting image, speech, and text inputs with real-time speech output.

Organizations / maintainers: Tsinghua University; Inspirai.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e07"></a>

### ⭐ Moshi

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.00037) [![Independent Lab](https://img.shields.io/badge/Independent%20Lab-b45309?style=flat-square)](https://arxiv.org/html/2410.00037)

[📄 Paper](https://arxiv.org/abs/2410.00037) · [💻 Repository](https://github.com/kyutai-labs/moshi) · [![★ 11,361](https://img.shields.io/badge/%E2%98%85%2011%2C361-eab308?style=flat-square)](https://github.com/kyutai-labs/moshi) [![Cite OA 9](https://img.shields.io/badge/Cite%20OA%209-0284c7?style=flat-square)](https://openalex.org/W4403883071) [![Cite S2 875](https://img.shields.io/badge/Cite%20S2%20875-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/ae4aa7b0c5a327dae63ad20e00b58bcc6176b3b8)

Models two-way speech streams together with text, providing an open research foundation for continuous listening and speaking.

📌 Why read first: Understand bidirectional speech streams, text assistance, and low-latency generation.

Organizations / maintainers: Kyutai.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e08"></a>

### Freeze-Omni

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2411.00774) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2411.00774)

[📄 Paper](https://arxiv.org/abs/2411.00774) · [💻 Repository](https://github.com/VITA-MLLM/Freeze-Omni) · [![★ 403](https://img.shields.io/badge/%E2%98%85%20403-eab308?style=flat-square)](https://github.com/VITA-MLLM/Freeze-Omni) [![Cite OA 4](https://img.shields.io/badge/Cite%20OA%204-0284c7?style=flat-square)](https://openalex.org/W4404390495)

Combines a frozen language model with streaming speech encoding/decoding and chunk-level state prediction.

Organizations / maintainers: Northwestern Polytechnical University; Nanjing University; Tencent Youtu Lab.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="voice"></a>

## 💬 Voice agents and interaction systems

<a id="e29"></a>

### ⭐ FireRedChat

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.06502) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/abs/2509.06502)

[📄 Paper](https://arxiv.org/abs/2509.06502) · [💻 Repository](https://github.com/FireRedTeam/FireRedChat) · [![★ 597](https://img.shields.io/badge/%E2%98%85%20597-eab308?style=flat-square)](https://github.com/FireRedTeam/FireRedChat) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4414757003)

A full-duplex speech system covering turn control, target-speaker interruption, dialogue management, and tool calling.

📌 Why read first: Use the modular implementation to understand interruption control, dialogue state, and tool use.

Organizations / maintainers: Xiaohongshu / FireRed Team.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e30"></a>

### Qwen Audio Agent

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent)

[💻 Repository](https://github.com/QwenAudio/qwen-audio-agent) · [![★ 3,112](https://img.shields.io/badge/%E2%98%85%203%2C112-eab308?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent)

An engineering entry point for asynchronous task coordination and cancellation between a speech frontend and a backend agent.

Organizations / maintainers: Qwen / Alibaba.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e09"></a>

### DuplexSLA

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2605.20755) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2605.20755)

[📄 Paper](https://arxiv.org/abs/2605.20755) · [💻 Repository](https://github.com/hyzhang24/DuplexSLA) · [![★ 147](https://img.shields.io/badge/%E2%98%85%20147-eab308?style=flat-square)](https://github.com/hyzhang24/DuplexSLA) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7161968102)

Produces speech and a structured action channel on a shared timeline, studying planning and tool use during conversation.

Scope: The action channel primarily represents structured planning and tool operations, not direct joint control.

Organizations / maintainers: StepFun; Peking University; Nanyang Technological University; Shanghai Jiao Tong University; University of New South Wales; Imperial College London.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e31"></a>

### Jarvis

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.23804) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2610.23804)

[📄 Paper](https://arxiv.org/abs/2610.23804) · [💻 Repository](https://github.com/JensenYX/Jarvis) · [![★ 18](https://img.shields.io/badge/%E2%98%85%2018-eab308?style=flat-square)](https://github.com/JensenYX/Jarvis) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7222979632)

Trains a coordinator between the interaction frontend and background tasks to manage switching, state, and stale results.

Scope: Research on software-agent coordination does not by itself establish gains on physical robot tasks.

Organizations / maintainers: CUHK Shenzhen; Tencent Hunyuan; Amphion Technology.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e36"></a>

### TEN Framework

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/TEN-framework/ten-framework) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/TEN-framework/ten-framework)

[💻 Repository](https://github.com/TEN-framework/ten-framework) · [![★ 11,219](https://img.shields.io/badge/%E2%98%85%2011%2C219-eab308?style=flat-square)](https://github.com/TEN-framework/ten-framework)

A framework for engineering real-time audiovisual agents and applications.

Scope: The LICENSE includes conditions beyond Apache-2.0, including provisions on endpoint-device hosting; read the official LICENSE before deployment.

Organizations / maintainers: Agora; Contributor community.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e37"></a>

### ⭐ VoxMind

[![ACL 2026](https://img.shields.io/badge/ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.acl-long.459/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2604.15710)

[📄 Paper](https://arxiv.org/abs/2604.15710) · [💻 Repository](https://github.com/MM-Speech/VoxMind) · [![★ 46](https://img.shields.io/badge/%E2%98%85%2046-eab308?style=flat-square)](https://github.com/MM-Speech/VoxMind) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7155019877)

Uses AgentChat data, Think-before-Speak, and dynamic tool retrieval to learn a reasoning–tool-call–feedback loop for spoken agents.

📌 Why read first: Begin with AgentChat formats, training objectives, and tool-loop experiments to connect conversation with task execution.

Scope: Benefits from asynchronous tool management do not establish simultaneous listening/speaking under every condition; inspect the experiments separately.

Organizations / maintainers: Zhejiang University; China University of Petroleum–Beijing at Karamay; Xiamen University.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e38"></a>

### ⭐ F-Actor

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.242/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2601.11329)

[📄 Paper](https://arxiv.org/abs/2601.11329) · [💻 Repository](https://github.com/MaikeZuefle/f-actor) · [![★ 33](https://img.shields.io/badge/%E2%98%85%2033-eab308?style=flat-square)](https://github.com/MaikeZuefle/f-actor) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7124734178)

Controls voice, topic, backchannels, interruptions, and conversation initiation through instructions, using a frozen audio encoder and single-stage training.

📌 Why read first: Learn how interaction behaviors become supervised, controllable instructions alongside speech-generation quality.

Organizations / maintainers: Karlsruhe Institute of Technology; University of Edinburgh; NatWest.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e39"></a>

### ⭐ SOMMELIER

[![ACL Industry Track 2026](https://img.shields.io/badge/ACL%20Industry%20Track%202026-475569?style=flat-square)](https://aclanthology.org/2026.acl-industry.18/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2603.25750)

[📄 Paper](https://arxiv.org/abs/2603.25750) · [💻 Repository](https://github.com/Anonymous-2001-j/Sommelier) · [![★ 0](https://img.shields.io/badge/%E2%98%85%200-eab308?style=flat-square)](https://github.com/Anonymous-2001-j/Sommelier) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7143443580)

Converts real multiparty recordings into temporally aligned two-channel training data through separation, diarization, transcription, and quality filtering.

📌 Why read first: Study how real recordings become full-duplex training data, especially alignment, overlap, and filtering.

Organizations / maintainers: KAIST; NAVER Cloud.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e40"></a>

### CF-Duplex / XA-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2605.10199) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2605.10199)

[📄 Paper](https://arxiv.org/abs/2605.10199) · [🔗 Project](https://light1726.github.io/duplex-demo/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7160904488)

Compares controlled fusion and cross-attention for routing the user audio stream into an actively generating model.

Organizations / maintainers: The Chinese University of Hong Kong; Tsinghua University; SenseTime.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e41"></a>

### ⭐ DuplexGen

[![EMNLP 2026](https://img.shields.io/badge/EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.emnlp-main.2618/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2607.26178)

[📄 Paper](https://arxiv.org/abs/2607.26178) · [💻 Repository](https://github.com/duplexgen/duplexgen-code) · [🔗 Project](https://duplexgen.github.io/) · [![★ 29](https://img.shields.io/badge/%E2%98%85%2029-eab308?style=flat-square)](https://github.com/duplexgen/duplexgen-code) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7171803236)

Calibrates turn-taking predictions with a small amount of human preference data, then synthesizes scenario-specific human–AI dialogue for full-duplex fine-tuning.

📌 Why read first: Connect data construction to target interaction behaviors and trace human preferences through synthesis and fine-tuning.

Organizations / maintainers: University of Illinois Urbana-Champaign; Seoul National University; University of California Berkeley; Georgia Institute of Technology; Columbia University.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e42"></a>

### BayLing-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.14528) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2606.14528)

[📄 Paper](https://arxiv.org/abs/2606.14528) · [💻 Repository](https://github.com/BayLing-Models/BayLing-Duplex) · [![★ 96](https://img.shields.io/badge/%E2%98%85%2096-eab308?style=flat-square)](https://github.com/BayLing-Models/BayLing-Duplex) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7164829614)

Uses a single autoregressive LLM and a small set of state tokens to jointly model listening, speaking, and stopping, with SFT and DPO.

Organizations / maintainers: Institute of Computing Technology, Chinese Academy of Sciences; University of Chinese Academy of Sciences.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e43"></a>

### MultiTalk / MultiTalkBench

[![NeurIPS 2026 · author-reported](https://img.shields.io/badge/NeurIPS%202026%20%C2%B7%20author--reported-475569?style=flat-square)](https://arxiv.org/abs/2609.36903) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.36903)

[📄 Paper](https://arxiv.org/abs/2609.36903) · [🔗 Pretraining data](https://huggingface.co/datasets/MultiTalk/MultiTalkPT) · [🔗 Fine-tuning data](https://huggingface.co/datasets/MultiTalk/MultiTalkFT) · [🔗 Benchmark](https://huggingface.co/datasets/MultiTalk/MultiTalkBench) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214898838)

Extends full-duplex speech modeling to long, multiparty, bilingual conversations, releasing pretraining/fine-tuning data and a benchmark based on real recordings.

Scope: NeurIPS 2026 is reported by the authors on arXiv. Keep MultiTalkBench separate from model training data.

Organizations / maintainers: The Chinese University of Hong Kong; Centre for Perceptual and Interactive Intelligence (InnoHK).

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e44"></a>

### ⭐ Self-Listening / LoopSpeech

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.05592) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.05592)

[📄 Paper](https://arxiv.org/abs/2609.05592) · [💻 Repository](https://github.com/FreedomIntelligence/LoopSpeech) · [![★ 8](https://img.shields.io/badge/%E2%98%85%208-eab308?style=flat-square)](https://github.com/FreedomIntelligence/LoopSpeech) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212059771)

Adds actually played speech to the history, distinguishing intended speech from what the user has heard, to study continuity after interruption.

📌 Why read first: Focus on how playback-grounded history changes subsequent responses and preserves state after interruption.

Organizations / maintainers: Shenzhen Loop Area Institute; The Chinese University of Hong Kong, Shenzhen.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e45"></a>

### D2: Dialogue-to-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.17124) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2610.17124)

[📄 Paper](https://arxiv.org/abs/2610.17124) · [💻 Repository](https://github.com/penguinfish1688/D2-dialogue-to-duplex) · [🔗 Project](https://d2-duplex-demo.github.io/) · [![★ 11](https://img.shields.io/badge/%E2%98%85%2011-eab308?style=flat-square)](https://github.com/penguinfish1688/D2-dialogue-to-duplex) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221777691)

Adapts half-duplex speech backbones to full duplex, examining the quality, latency, and compute trade-offs of audio chunk intervals.

Scope: The repository currently offers a Qwen3-Omni 80 ms checkpoint. Reported acoustic latency excludes some compute and service overhead.

Organizations / maintainers: MIT CSAIL; MIT–IBM Watson AI Lab.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e46"></a>

### TASTE2

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.08956) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.08956)

[📄 Paper](https://arxiv.org/abs/2609.08956) · [💻 Repository](https://github.com/GitYCC/TASTE-SpokenLM-2) · [🔗 Project](https://gitycc.github.io/TASTE2-Homepage/) · [🔗 Voice application](https://github.com/GitYCC/TASTE-Voice-Bot) · [![★ 2](https://img.shields.io/badge/%E2%98%85%202-eab308?style=flat-square)](https://github.com/GitYCC/TASTE-SpokenLM-2) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212080144)

Combines text-aligned speech modeling with deployment design for full-duplex interaction, including paralinguistic signals and real-time operation.

Organizations / maintainers: MediaTek Research; National Taiwan University; NVIDIA AI Technology Center.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e47"></a>

### IRAF

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.06559) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2606.06559)

[📄 Paper](https://arxiv.org/abs/2606.06559) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7163910264)

Estimates target-speaker reliability frame by frame and adaptively fuses audio to improve full-duplex robustness against interfering speakers.

Organizations / maintainers: The Chinese University of Hong Kong; Huawei Leibniz Research Center; Nanyang Technological University.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e48"></a>

### ⭐ MoshiRAG

[![ICML 2026 · author-reported](https://img.shields.io/badge/ICML%202026%20%C2%B7%20author--reported-475569?style=flat-square)](https://arxiv.org/abs/2604.12928) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.12928)

[📄 Paper](https://arxiv.org/abs/2604.12928) · [💻 Repository](https://github.com/kyutai-labs/moshi-rag) · [![★ 195](https://img.shields.io/badge/%E2%98%85%20195-eab308?style=flat-square)](https://github.com/kyutai-labs/moshi-rag) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7154507545)

Triggers retrieval asynchronously and injects knowledge into ongoing full-duplex conversation.

📌 Why read first: Study the interfaces, triggers, and result injection linking continuous speech interaction with slower retrieval.

Scope: ICML 2026 acceptance is reported by the authors on arXiv. Retrieval tasks differ in scope from general tool execution.

Organizations / maintainers: Toyota Technological Institute at Chicago; Kyutai; Gradium.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e49"></a>

### Frontend–Backend Tool Calling

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.19334) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.19334)

[📄 Paper](https://arxiv.org/abs/2609.19334) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213611583)

Separates a real-time speech frontend from a text-based tool backend, connecting streaming transcription, tool execution, and prefill-and-repeat result delivery.

Scope: Currently a preprint; an intention to submit to ICASSP 2027 is not an acceptance.

Organizations / maintainers: NVIDIA.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e50"></a>

### DiffuPlex · Rolling Masked Diffusion

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.12214) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2610.12214)

[📄 Paper](https://arxiv.org/abs/2610.12214) · [🔗 Project](https://diffuplex.github.io/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221088445)

Uses rolling masked diffusion to predict interaction frames, reducing backbone calls while studying interaction quality.

Scope: Distinct from NVIDIA's discrete-diffusion paper; use full titles to disambiguate the shared project name.

Organizations / maintainers: University of Seoul.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e51"></a>

### Diffuplex · Discrete Diffusion

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.17780) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2610.17780)

[📄 Paper](https://arxiv.org/abs/2610.17780) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221757954)

Uses autoregression to decide when to speak and discrete diffusion to generate content in parallel, studying full-duplex generation efficiency.

Scope: The paper announces future code and checkpoint releases; an announcement is not treated as an available release.

Organizations / maintainers: NVIDIA.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e52"></a>

### Voice-Light

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.20995)

[📄 Paper](https://arxiv.org/abs/2609.20995) · [💻 Repository](https://github.com/BertilBraun/Voice-Light) · [![★ 10](https://img.shields.io/badge/%E2%98%85%2010-eab308?style=flat-square)](https://github.com/BertilBraun/Voice-Light) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213934747)

A cascaded system with causal turn-taking, speculative generation, and reversible playback; playback acknowledgments update durable conversation history.

Scope: Online evidence consists of three operator runs totaling 36 turns. Treat it as an engineering case, not a large user study. Institutional affiliation is unverified.

Organizations / maintainers: Bertil Braun.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e53"></a>

### AdaptDuplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.29217) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.29217)

[📄 Paper](https://arxiv.org/abs/2609.29217) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214079271)

Combines adaptive perception windows, non-blocking cognitive consolidation, and external reasoning for dynamic full-duplex interaction and staged post-training.

Scope: This entry links a technical paper and does not assume that weights or a complete training pipeline are available.

Organizations / maintainers: Zuoyebang Education Technology.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e54"></a>

### Realtime-Venus

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.13814) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.13814)

[📄 Paper](https://arxiv.org/abs/2609.13814) · [💻 Repository](https://github.com/inclusionAI/Realtime-Venus) · [![★ 252](https://img.shields.io/badge/%E2%98%85%20252-eab308?style=flat-square)](https://github.com/inclusionAI/Realtime-Venus) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213284145)

A real-time interaction layer delegates background tasks asynchronously and incorporates returned results, connecting multimodal input, trained policies, and runtime design.

Organizations / maintainers: Ant Group; Tsinghua University.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e55"></a>

### NemotronLabs VoiceChat

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.21967) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.21967)

[📄 Paper](https://arxiv.org/abs/2609.21967) · [💻 Repository](https://github.com/NVIDIA-NeMo/Speech/tree/nemotron-labs-voicechat) · [🔗 Model](https://huggingface.co/nvidia/NVIDIA-NemotronLabs-VoiceChat-11B) · [![★ 18,685](https://img.shields.io/badge/%E2%98%85%2018%2C685-eab308?style=flat-square)](https://github.com/NVIDIA-NeMo/Speech/tree/nemotron-labs-voicechat) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213936344)

An open full-duplex speech model using a separate tool channel for action calls and interruptible speech output.

Scope: Code is linked to the nemotron-labs-voicechat branch of NVIDIA-NeMo/Speech. Stars refer to the entire Speech repository.

Organizations / maintainers: NVIDIA.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e56"></a>

### StepAudio 3 Realtime

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.14005) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.14005)

[📄 Paper](https://arxiv.org/abs/2609.14005) · [🔗 Project](https://stepaudiollm.github.io/step-audio-3-realtime/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213371127)

Organizes real-time speech interaction around listening, conversing, thinking, and acting, with Think-While-Speaking and asynchronous tool execution.

Scope: Links the paper and this version's demonstration; the StepAudio 2 repository is not treated as the complete implementation of this release.

Organizations / maintainers: StepFun.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e57"></a>

### Qwen-Audio-3.1-Realtime

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.25176) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.25176)

[📄 Paper](https://arxiv.org/abs/2609.25176) · [💻 Repository](https://github.com/QwenAudio/qwen-audio-agent) · [![★ 3,112](https://img.shields.io/badge/%E2%98%85%203%2C112-eab308?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214103824)

Uses Agent GRPO in executable environments and multimodal policy distillation to study task reliability and interaction post-training.

Scope: qwen-audio-agent is a companion runtime; its availability does not imply release of all model weights or training code.

Organizations / maintainers: Alibaba / Qwen.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e58"></a>

### ⭐ DuplexOmni

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.09186) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2606.09186)

[📄 Paper](https://arxiv.org/abs/2606.09186) · [💻 Repository](https://github.com/MuyeHuang/DuplexOmni) · [![★ 145](https://img.shields.io/badge/%E2%98%85%20145-eab308?style=flat-square)](https://github.com/MuyeHuang/DuplexOmni) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7164028919)

Coordinates real-time interaction with asynchronous reasoning, using a Writer–Director synthesis pipeline for concurrent listening, seeing, thinking, and speaking.

📌 Why read first: Trace the relationship between real-time interaction, asynchronous reasoning, and synthetic data as a reference for end-to-end design.

Organizations / maintainers: Xi’an Jiaotong University; Peking University; Meituan.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="embodied"></a>

## 🤖 Embodied interaction and language feedback

<a id="e13"></a>

### Interactive Language / Language Table

[![IEEE RA-L 2024](https://img.shields.io/badge/IEEE%20RA--L%202024-475569?style=flat-square)](https://doi.org/10.1109/LRA.2023.3295255) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2210.06407)

[📄 Paper](https://arxiv.org/abs/2210.06407) · [💻 Repository](https://github.com/google-research/language-table) · [![★ 367](https://img.shields.io/badge/%E2%98%85%20367-eab308?style=flat-square)](https://github.com/google-research/language-table) [![Cite OA 113](https://img.shields.io/badge/Cite%20OA%20113-0284c7?style=flat-square)](https://openalex.org/W4391759936)

Uses real-time language guidance to steer visuomotor policies, allowing people to adjust a robot's behavior during a task.

Organizations / maintainers: Robotics at Google.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e25"></a>

### ⭐ Hi Robot

[![ICML 2025](https://img.shields.io/badge/ICML%202025-475569?style=flat-square)](https://proceedings.mlr.press/v267/shi25d.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.19417)

[📄 Paper](https://arxiv.org/abs/2502.19417) · [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4416045178) [![Cite S2 319](https://img.shields.io/badge/Cite%20S2%20319-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/69afd10d387423a03617d461c3f47a5f3033cc54)

High-level vision-language reasoning converts complex requests and execution-time feedback into the next task; a lower-level VLA executes actions.

📌 Why read first: Understand the division between high-level language reasoning and low-level action policies.

Scope: Feedback reaches the action policy through high-level planning; this alone does not establish an advantage from raw speech information.

Organizations / maintainers: Physical Intelligence; Stanford University; UC Berkeley.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e26"></a>

### ⭐ Yell At Your Robot / YAY Robot

[![RSS 2024](https://img.shields.io/badge/RSS%202024-475569?style=flat-square)](https://roboticsproceedings.org/rss20/p025.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2403.12910)

[📄 Paper](https://arxiv.org/abs/2403.12910) · [💻 Repository](https://github.com/yay-robot/yay_robot) · [![★ 166](https://img.shields.io/badge/%E2%98%85%20166-eab308?style=flat-square)](https://github.com/yay-robot/yay_robot) [![Cite OA 47](https://img.shields.io/badge/Cite%20OA%2047-0284c7?style=flat-square)](https://openalex.org/W4402354098) [![Cite S2 179](https://img.shields.io/badge/Cite%20S2%20179-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/f213d0cb84b6afca9a4d5722081ba3052e7e89bc)

Uses spoken corrections during long robot tasks for immediate adjustment and subsequent high-level policy training.

📌 Why read first: Understand how execution-time corrections support both current control and later learning.

Scope: Spoken corrections primarily enter control and learning through language representations.

Organizations / maintainers: Stanford University; UC Berkeley.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e24"></a>

### VLAS

[![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2025/hash/804a1a9de5787e3597b4bb64e1a48ec3-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.13508)

[📄 Paper](https://arxiv.org/abs/2502.13508) · [💻 Repository](https://github.com/whichwhichgone/VLAS) · [![★ 50](https://img.shields.io/badge/%E2%98%85%2050-eab308?style=flat-square)](https://github.com/whichwhichgone/VLAS) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4407764312) [![Cite S2 68](https://img.shields.io/badge/Cite%20S2%2068-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/f6075ce4db8dcc359c3ac97b85f2644dc5cadda6)

Conditions visuomotor action on raw speech and retrieves speaker-specific information for personalized manipulation.

Scope: Raw speech and speaker-based personalization are distinct from full-duplex speech/action control.

Organizations / maintainers: Westlake University; Zhejiang University; Xi’an Jiaotong University.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e21"></a>

### ⭐ RoboOmni (OpenMOSS)

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/33610fba262d7b6fed0810b89f55e147-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2510.23763)

[📄 Paper](https://arxiv.org/abs/2510.23763) · [💻 Repository](https://github.com/OpenMOSS/RoboOmni) · [![★ 124](https://img.shields.io/badge/%E2%98%85%20124-eab308?style=flat-square)](https://github.com/OpenMOSS/RoboOmni) [![Cite S2 12](https://img.shields.io/badge/Cite%20S2%2012-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/37cd1e4cbfbfdadc2a898a703ab46bc0e1c83dd3)

Infers intent from dialogue, environmental sound, and vision, then produces manipulation actions after confirmation; studies proactive assistance from implicit contextual instructions.

📌 Why read first: Understand how environmental sounds and implicit intent enter manipulation tasks.

Scope: This entry refers to OpenMOSS's RoboOmni; distinguish it from other papers with the same name.

Organizations / maintainers: Fudan University; Shanghai Innovation Institute; National University of Singapore.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e22"></a>

### ⭐ ELLSA

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/6d8af672c0bca7a4be6f0cd0d229c05c-Abstract-Conference.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.16756)

[📄 Paper](https://arxiv.org/abs/2510.16756) · [💻 Repository](https://github.com/bytedance/SALMONN) · [![★ 1,564](https://img.shields.io/badge/%E2%98%85%201%2C564-eab308?style=flat-square)](https://github.com/bytedance/SALMONN) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415958597) [![Cite S2 7](https://img.shields.io/badge/Cite%20S2%207-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/3af611e47c30a439f8acad312f16cf7837ddbce7)

Processes vision, text, speech, and action in a unified architecture, supporting concurrent speech/action, action interruption, and grounded question answering.

📌 Why read first: Study joint speech/action modeling and experiments on concurrent speaking, acting, and interruption.

Scope: SALMONN is a shared repository. Its stars are not ELLSA-specific; consult official releases for weights and training resources.

Organizations / maintainers: Tsinghua University; ByteDance.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e23"></a>

### VITA-E

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.21817) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.21817)

[📄 Paper](https://arxiv.org/abs/2510.21817) · [💻 Repository](https://github.com/Tencent/VITA) · [![★ 166](https://img.shields.io/badge/%E2%98%85%20166-eab308?style=flat-square)](https://github.com/Tencent/VITA) [![Cite S2 2](https://img.shields.io/badge/Cite%20S2%202-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/62d932e380f9ec7de5d43c17bc933a05887b0007)

Uses parallel active/listening models and control tokens to schedule speech and action, supporting interruption, task switching, and concurrent speech/action.

Organizations / maintainers: Nanjing University; CASIA; Tencent Youtu Lab; Fourier Intelligence.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e11"></a>

### Reachy Mini Conversation App

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)

[💻 Repository](https://github.com/pollen-robotics/reachy_mini_conversation_app) · [![★ 348](https://img.shields.io/badge/%E2%98%85%20348-eab308?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)

Connects real-time speech, camera tools, and robot motion within a conversation application.

Scope: Primarily head/antenna expression and visual tool use, rather than an arm manipulation platform.

Organizations / maintainers: Pollen Robotics / Hugging Face.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e12"></a>

### EMAGE / BEAT2

[![CVPR 2024](https://img.shields.io/badge/CVPR%202024-475569?style=flat-square)](https://pantomatrix.github.io/EMAGE/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2401.00374)

[📄 Paper](https://arxiv.org/abs/2401.00374) · [💻 Repository](https://github.com/haiyangliu0/character-policy) · [![★ 1,312](https://img.shields.io/badge/%E2%98%85%201%2C312-eab308?style=flat-square)](https://github.com/haiyangliu0/character-policy) [![Cite OA 95](https://img.shields.io/badge/Cite%20OA%2095-0284c7?style=flat-square)](https://openalex.org/W4402727140)

Generates coordinated body and facial motion from speech and text, connecting co-speech gesture methods with expressive motion data.

Scope: Targets co-speech gestures and character expression; it does not directly establish physical robot manipulation capability.

Organizations / maintainers: The University of Tokyo; Keio University; Max Planck Institute for Intelligent Systems; JAIST; Tsinghua University.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="robotics"></a>

## 🦾 Actions, data, and deployment

<a id="e19"></a>

### ⭐ LeRobot

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.22818) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2602.22818)

[📄 Paper](https://arxiv.org/abs/2602.22818) · [💻 Repository](https://github.com/huggingface/lerobot) · [![★ 28,653](https://img.shields.io/badge/%E2%98%85%2028%2C653-eab308?style=flat-square)](https://github.com/huggingface/lerobot) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7131860508)

An open toolkit for robot datasets, policy training, hardware control, and evaluation.

📌 Why read first: Connect demonstration collection, data inspection, policy training, and real-robot execution.

Organizations / maintainers: Hugging Face; University of Oxford.

<sub>Count snapshot: 2026-11-02 / 2026-11-03.</sub>

<a id="e32"></a>

### ⭐ ACT / ALOHA

[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://www.roboticsproceedings.org/rss19/p016.pdf) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2304.13705)

[📄 Paper](https://arxiv.org/abs/2304.13705) · [💻 Repository](https://github.com/tonyzhaozh/act) · [![★ 2,318](https://img.shields.io/badge/%E2%98%85%202%2C318-eab308?style=flat-square)](https://github.com/tonyzhaozh/act) [![Cite OA 674](https://img.shields.io/badge/Cite%20OA%20674-0284c7?style=flat-square)](https://openalex.org/W4385430674)

Learns action chunks from teleoperated demonstrations, establishing a visuomotor imitation-learning baseline.

📌 Why read first: Build intuition for imitation learning from observations, demonstrated actions, and action-chunk prediction.

Scope: Standard ACT is not language-conditioned; choosing between goals requires a skill selector or additional goal conditioning.

Organizations / maintainers: Stanford University; Meta; UC Berkeley.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e33"></a>

### Diffusion Policy

[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![IJRR 2024](https://img.shields.io/badge/IJRR%202024-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2303.04137)

[📄 Paper](https://arxiv.org/abs/2303.04137v4) · [💻 Repository](https://github.com/real-stanford/diffusion_policy) · [![★ 4,698](https://img.shields.io/badge/%E2%98%85%204%2C698-eab308?style=flat-square)](https://github.com/real-stanford/diffusion_policy) [![Cite OA 12](https://img.shields.io/badge/Cite%20OA%2012-0284c7?style=flat-square)](https://openalex.org/W4323651335)

Models conditional action distributions through denoising to generate continuous action sequences.

Scope: The linked paper is the RSS 2023 version; IJRR 2024 is an extension. Citation counts refer to the linked database record.

Organizations / maintainers: Columbia University; Toyota Research Institute; MIT.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e34"></a>

### ⭐ SmolVLA

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2506.01844) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2506.01844)

[📄 Paper](https://arxiv.org/abs/2506.01844) · [💻 Repository](https://github.com/huggingface/lerobot) · [![★ 28,653](https://img.shields.io/badge/%E2%98%85%2028%2C653-eab308?style=flat-square)](https://github.com/huggingface/lerobot) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4414898213)

An efficient pretrained VLA reference for adapting language-conditioned actions to robot demonstrations.

📌 Why read first: Follow the official tutorial to adapt a pretrained VLA to a robot dataset.

Scope: Inputs include text instructions, not native speech. Stars refer to all of LeRobot; a small model alone does not ensure real-time whole-system operation.

Organizations / maintainers: Hugging Face; Sorbonne University; valeo.ai; ENS Paris-Saclay.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e20"></a>

### OpenVLA

[![CoRL 2024](https://img.shields.io/badge/CoRL%202024-475569?style=flat-square)](https://proceedings.mlr.press/v270/kim25c.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2406.09246)

[📄 Paper](https://arxiv.org/abs/2406.09246) · [💻 Repository](https://github.com/openvla/openvla) · [![★ 7,250](https://img.shields.io/badge/%E2%98%85%207%2C250-eab308?style=flat-square)](https://github.com/openvla/openvla) [![Cite OA 62](https://img.shields.io/badge/Cite%20OA%2062-0284c7?style=flat-square)](https://openalex.org/W4399695759)

A vision-language-conditioned robot action model, providing a foundation for connecting interaction layers with action policies.

Scope: A vision/language-to-action foundation; native speech and real-time interruption need additional system design.

Organizations / maintainers: Stanford University; UC Berkeley; MIT; Toyota Research Institute; Google DeepMind; Physical Intelligence.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e17"></a>

### llama.cpp ecosystem

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/OpenBMB/llama.cpp-omni) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/ggml-org/llama.cpp/discussions/19759)

[💻 Repository](https://github.com/ggml-org/llama.cpp) · [![★ 133,116](https://img.shields.io/badge/%E2%98%85%20133%2C116-eab308?style=flat-square)](https://github.com/ggml-org/llama.cpp)

A local inference toolchain offering quantization and execution across platforms.

Scope: Complete Omni modes may require a dedicated branch such as OpenBMB/llama.cpp-omni.

Organizations / maintainers: ggml.ai / Hugging Face; llama.cpp contributor community.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e18"></a>

### MNN

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni#deployment-with-mnn) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/alibaba/MNN)

[💻 Repository](https://github.com/alibaba/MNN) · [![★ 16,336](https://img.shields.io/badge/%E2%98%85%2016%2C336-eab308?style=flat-square)](https://github.com/alibaba/MNN)

An inference framework for mobile and edge devices, with an official integration entry point for Qwen2.5-Omni.

Organizations / maintainers: Alibaba.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="evaluation"></a>

## 📏 Evaluation

<a id="e14"></a>

### Daily-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2505.17862) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2505.17862)

[📄 Paper](https://arxiv.org/abs/2505.17862) · [💻 Repository](https://github.com/Lliar-liar/Daily-Omni) · [![★ 53](https://img.shields.io/badge/%E2%98%85%2053-eab308?style=flat-square)](https://github.com/Lliar-liar/Daily-Omni) Citation count —

A benchmark for temporally aligned audiovisual reasoning in everyday video.

Organizations / maintainers: Fudan University.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e15"></a>

### OmniBench (m-a-p)

[![NeurIPS 2025](https://img.shields.io/badge/NeurIPS%202025-475569?style=flat-square)](https://arxiv.org/abs/2409.15272) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2409.15272)

[📄 Paper](https://arxiv.org/abs/2409.15272) · [💻 Repository](https://github.com/multimodal-art-projection/OmniBench) · [![★ 62](https://img.shields.io/badge/%E2%98%85%2062-eab308?style=flat-square)](https://github.com/multimodal-art-projection/OmniBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4403885114) [![Cite S2 111](https://img.shields.io/badge/Cite%20S2%20111-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/bde43a6356341b68a675582cf964fd9725fb40fb)

A benchmark for joint image, audio, and text understanding, accompanied by OmniInstruct.

Organizations / maintainers: M-A-P; University of Manchester; Queen Mary University of London; 01.ai; HKUST; Nanjing University; Dartmouth College.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e16"></a>

### ⭐ Full-Duplex-Bench

[![ASRU 2025](https://img.shields.io/badge/ASRU%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.04721) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2503.04721)

[📄 Paper](https://arxiv.org/abs/2503.04721) · [💻 Repository](https://github.com/DanielLin94144/Full-Duplex-Bench) · [![★ 335](https://img.shields.io/badge/%E2%98%85%20335-eab308?style=flat-square)](https://github.com/DanielLin94144/Full-Duplex-Bench) [![Cite OA 8](https://img.shields.io/badge/Cite%20OA%208-0284c7?style=flat-square)](https://openalex.org/W7148492801)

Evaluates pauses, backchannels, turn transitions, and interruptions; later versions extend to overlap, dynamic multi-turn interaction, and tool use.

📌 Why read first: Translate interruptions, turn transitions, and interaction timing into measurable outcomes.

Organizations / maintainers: National Taiwan University; UC Berkeley; University of Washington; MIT CSAIL.

<sub>Count snapshot: 2026-11-02 / 2026-11-03.</sub>

<a id="e35"></a>

### LIBERO

[![NeurIPS Datasets and Benchmarks 2023](https://img.shields.io/badge/NeurIPS%20Datasets%20and%20Benchmarks%202023-475569?style=flat-square)](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8c3c666820ea055a77726d66fc7d447f-Abstract-Datasets_and_Benchmarks.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2306.03310)

[📄 Paper](https://arxiv.org/abs/2306.03310) · [💻 Repository](https://github.com/Lifelong-Robot-Learning/LIBERO) · [![★ 2,508](https://img.shields.io/badge/%E2%98%85%202%2C508-eab308?style=flat-square)](https://github.com/Lifelong-Robot-Learning/LIBERO) [![Cite OA 136](https://img.shields.io/badge/Cite%20OA%20136-0284c7?style=flat-square)](https://openalex.org/W7133220882)

A simulation benchmark for language-conditioned robot manipulation and lifelong learning.

Scope: Primarily evaluates language-conditioned manipulation, rather than speech interaction or collaboration with real participants.

Organizations / maintainers: UT Austin; Tsinghua University; Sony AI.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e59"></a>

### ⭐ VoiceBench

[![TACL 2026](https://img.shields.io/badge/TACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.tacl-1.18/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2410.17196)

[📄 Paper](https://arxiv.org/abs/2410.17196) · [💻 Repository](https://github.com/MatthewCYM/VoiceBench) · [![★ 407](https://img.shields.io/badge/%E2%98%85%20407-eab308?style=flat-square)](https://github.com/MatthewCYM/VoiceBench) [![Cite OA 12](https://img.shields.io/badge/Cite%20OA%2012-0284c7?style=flat-square)](https://openalex.org/W4404261856)

Evaluates voice-assistant knowledge, instruction following, safety, and response robustness under accents, noise, and other perturbations.

📌 Why read first: Establish a basic voice-assistant reference before comparing interaction and task outcomes separately.

Scope: Primarily evaluates responses to spoken input; it does not replace continuous full-duplex or tool-task evaluation.

Organizations / maintainers: National University of Singapore.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e60"></a>

### VocalBench

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2505.15727) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2505.15727)

[📄 Paper](https://arxiv.org/abs/2505.15727) · [💻 Repository](https://github.com/SJTU-OmniAgent/VocalBench) · [![★ 8](https://img.shields.io/badge/%E2%98%85%208-eab308?style=flat-square)](https://github.com/SJTU-OmniAgent/VocalBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4415329203)

Covers semantic, acoustic, conversational, and robustness dimensions across single-turn and multi-turn speech interaction.

Scope: Check each subset, language, and extension separately. Publication of one subset does not assign that venue to the entire benchmark.

Organizations / maintainers: Shanghai Jiao Tong University; Ant Group.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e61"></a>

### VCB Bench

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.1659/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2510.11098)

[📄 Paper](https://arxiv.org/abs/2510.11098) · [💻 Repository](https://github.com/Tencent/VCB-Bench) · [![★ 5](https://img.shields.io/badge/%E2%98%85%205-eab308?style=flat-square)](https://github.com/Tencent/VCB-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4417101201)

Uses real Chinese speech to evaluate instruction following, knowledge understanding, and robustness to acoustic and content perturbations.

Scope: The core contribution concerns real Chinese speech; report later language extensions separately from the original protocol.

Organizations / maintainers: Wuhan University; Tencent.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e62"></a>

### ⭐ VoiceAgentBench

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.07978) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2510.07978)

[📄 Paper](https://arxiv.org/abs/2510.07978) · [💻 Repository](https://github.com/ola-krutrim/VoiceAgentBench) · [🔗 Data](https://huggingface.co/datasets/krutrim-ai-labs/VoiceAgentBench) · [![★ 6](https://img.shields.io/badge/%E2%98%85%206-eab308?style=flat-square)](https://github.com/ola-krutrim/VoiceAgentBench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415318706)

Connects multilingual speech input to single, parallel, sequential, and multi-turn tool tasks, testing function choice, arguments, and other agent capabilities.

📌 Why read first: Understand speech-conditioned function selection, arguments, and multi-step structure before interpreting real-world task success.

Scope: Focuses on tool structure and arguments; it does not directly establish natural timing of continuous speech output.

Organizations / maintainers: OLA Electric / Krutrim AI.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e63"></a>

### ⭐ τ-Voice

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2603.13686) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2603.13686)

[📄 Paper](https://arxiv.org/abs/2603.13686) · [💻 Repository](https://github.com/sierra-research/tau2-bench) · [![★ 2,382](https://img.shields.io/badge/%E2%98%85%202%2C382-eab308?style=flat-square)](https://github.com/sierra-research/tau2-bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7138316890)

Uses domain policies and environment state to evaluate multi-turn tool use and final task completion by full-duplex voice agents.

📌 Why read first: Judge completion from final environment state and compare text agents with voice agents.

Scope: The tau2-bench repository continues to evolve, including later τ³ development. Pin the paper's version, environment, and user simulator.

Organizations / maintainers: Sierra; Princeton University.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e64"></a>

### ⭐ Full-Duplex-Bench-v3

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.04847) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.04847)

[📄 Paper](https://arxiv.org/abs/2604.04847) · [💻 Repository](https://github.com/DanielLin94144/Full-Duplex-Bench) · [🔗 Project](https://daniellin94144.github.io/FDB-v3-demo/) · [![★ 335](https://img.shields.io/badge/%E2%98%85%20335-eab308?style=flat-square)](https://github.com/DanielLin94144/Full-Duplex-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7151544009)

Combines real spoken hesitations, repetitions, and corrections with multi-step tool use to evaluate task execution during interaction.

📌 Why read first: Test whether spoken corrections and other interaction disturbances cause tool-task errors.

Scope: Shares a repository with v1, v1.5, and v2 but evaluates a different task. The v3 paper is a preprint, not the ASRU 2025 publication of v1.

Organizations / maintainers: National Taiwan University; NVIDIA.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e65"></a>

### ⭐ MTR-DuplexBench

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.263/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2511.10262)

[📄 Paper](https://arxiv.org/abs/2511.10262) · [💻 Repository](https://github.com/ZhangHe0918/MTR-DuplexBench) · [![★ 9](https://img.shields.io/badge/%E2%98%85%209-eab308?style=flat-square)](https://github.com/ZhangHe0918/MTR-DuplexBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4416238789)

Analyzes full-duplex conversations turn by turn, combining interaction dynamics, response quality, instruction following, and safety.

📌 Why read first: Cover cumulative multi-turn problems that short isolated clips can miss.

Organizations / maintainers: Tsinghua University; The Chinese University of Hong Kong; Huawei.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e66"></a>

### HumDial-FDBench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.21406) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.21406)

[📄 Paper](https://arxiv.org/abs/2604.21406) · [💻 Repository](https://github.com/ASLP-lab/HumDial-FDBench) · [![★ 44](https://img.shields.io/badge/%E2%98%85%2044-eab308?style=flat-square)](https://github.com/ASLP-lab/HumDial-FDBench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7155525302)

Uses real two-channel human dialogue to evaluate overlap, interruption, and backchannels, with a HumDial challenge and leaderboard.

Scope: The paper discusses the ICASSP 2026 HumDial challenge. The event name does not establish proceedings publication of this preprint.

Organizations / maintainers: Northwestern Polytechnical University / ASLP Lab; Nanjing University; AISHELL.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e67"></a>

### MP-Bench

[![Findings of EMNLP 2026](https://img.shields.io/badge/Findings%20of%20EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-emnlp.1437/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.13076)

[📄 Paper](https://arxiv.org/abs/2609.13076) · [💻 Repository](https://github.com/atosystem/MP-Bench) · [![★ 1](https://img.shields.io/badge/%E2%98%85%201-eab308?style=flat-square)](https://github.com/atosystem/MP-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212688662)

Evaluates a voice agent as a multiparty conversation participant, including comprehension, turn timing, and response appropriateness.

Organizations / maintainers: The University of Texas at Austin; National Taiwan University; MIT; Carnegie Mellon University; Meta AI.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e68"></a>

### Duplex-MPE

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.31948) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.31948)

[📄 Paper](https://arxiv.org/abs/2609.31948) · [🔗 Project](https://step-out.github.io/Duplex-MPE-Page/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214781414)

Tests participation decisions in multiparty scenes, including explicit address, implicit requests, proactive responses, and appropriate silence.

Organizations / maintainers: Peking University; Renmin University of China; Tsinghua University; National Taiwan University; Xiamen University; Fudan University.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e69"></a>

### Instruct-FD

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2607.20460) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2607.20460)

[📄 Paper](https://arxiv.org/abs/2607.20460) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7170334618)

Tests whether full-duplex systems can follow instructions governing turn-taking, interruption, backchannels, and proactivity.

Organizations / maintainers: Boson AI.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e70"></a>

### DuplexAct-Bench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.39446) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.39446)

[📄 Paper](https://arxiv.org/abs/2609.39446) · [💻 Repository](https://github.com/Alita-xky/DuplexAct-Bench) · [🔗 Project](https://alitaxky.icu/DuplexAct-Bench/) · [![★ 1](https://img.shields.io/badge/%E2%98%85%201-eab308?style=flat-square)](https://github.com/Alita-xky/DuplexAct-Bench) Citation count —

Covers interruption, yielding, resisting interruption, active silence, proactive initiation, and backchannels, evaluating timing and content separately.

Scope: The linked repository primarily contains the project website. Check the project release for complete evaluators and data.

Organizations / maintainers: Beijing Institute for General Artificial Intelligence; Peking University; Shanghai Jiao Tong University.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e71"></a>

### ⭐ EVA-Bench

[![Findings of EMNLP 2026](https://img.shields.io/badge/Findings%20of%20EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-emnlp.2182/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2605.13841)

[📄 Paper](https://arxiv.org/abs/2605.13841) · [💻 Repository](https://github.com/ServiceNow/eva) · [🔗 Project](https://servicenow.github.io/eva/) · [![★ 235](https://img.shields.io/badge/%E2%98%85%20235-eab308?style=flat-square)](https://github.com/ServiceNow/eva) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7161175665)

Uses dynamic bot-to-bot simulation to evaluate complete tasks and interaction experience, separating task/factual fidelity from timing and experience.

📌 Why read first: Learn to evaluate task correctness and experience separately, and inspect the validity of the simulated user.

Organizations / maintainers: ServiceNow AI Research.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e72"></a>

### VAmoS Bench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2607.27453) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2607.27453)

[📄 Paper](https://arxiv.org/abs/2607.27453) · [💻 Repository](https://github.com/veris-ai/riley-agent) · [![★ 18](https://img.shields.io/badge/%E2%98%85%2018-eab308?style=flat-square)](https://github.com/veris-ai/riley-agent) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7172022530)

Simulates voice agents in financial-service scenarios, checking complete dialogues, tool traces, and domain facts.

Scope: Domain-specific to financial services; riley-agent is a reference agent implementation, not necessarily the complete benchmark grader.

Organizations / maintainers: Veris AI.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e73"></a>

### FD-Bench

[![Interspeech 2025](https://img.shields.io/badge/Interspeech%202025-475569?style=flat-square)](https://www.isca-archive.org/interspeech_2025/peng25b_interspeech.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2507.19040)

[📄 Paper](https://arxiv.org/abs/2507.19040) · [💻 Repository](https://github.com/pengyizhou/FD-Bench) · [![★ 27](https://img.shields.io/badge/%E2%98%85%2027-eab308?style=flat-square)](https://github.com/pengyizhou/FD-Bench) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4415433582)

A full-duplex evaluation pipeline with multi-turn interaction, interruptions, and noise, measuring generation quality and latency.

Scope: A different project from DanielLin94144/Full-Duplex-Bench; scores and versions are not interchangeable.

Organizations / maintainers: Nanyang Technological University; Alibaba.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="e74"></a>

### TurnBench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2608.25218) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2608.25218)

[📄 Paper](https://arxiv.org/abs/2608.25218) · [💻 Repository](https://github.com/SesameAILabs/turnbench) · [🔗 Project](https://turnbench.sesame.com/) · [![★ 57](https://img.shields.io/badge/%E2%98%85%2057-eab308?style=flat-square)](https://github.com/SesameAILabs/turnbench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7204453739)

Evaluates end-of-turn and interruption detectors through recall and latency at specified false-positive budgets.

Scope: Primarily a component-level turn-decision benchmark, not a direct test of response content, tool use, or final task completion.

Organizations / maintainers: Sesame AI; Mundo AI; Oto; Carnegie Mellon University; National Taiwan University; Academia Sinica; Brno University of Technology.

<sub>Count snapshot: 2026-11-03.</sub>

<a id="industry"></a>

## 🏭 Industry demonstrations

<a id="e10"></a>

### WITA-Omni

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://www.agibot.com/article/231/detail/122.html) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.agibot.com/article/231/detail/122.html)

[🔗 Official page](https://www.agibot.com/article/231/detail/122.html) · —

AGIBOT's embodied interaction demonstration combines scene understanding, speech, and bodily expression.

Scope: An industry demonstration does not establish that the action model, training data, or complete system is open.

Organizations / maintainers: AGIBOT.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e27"></a>

### Gemini Live API × Robotics demo

[![Technical Demo 2025](https://img.shields.io/badge/Technical%20Demo%202025-475569?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/)

[🔗 Official page](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) · —

An official Google example feeds speech and robot-camera input into the Live API, then connects function calls to robot control interfaces.

Scope: The Live API example and Gemini Robotics models are separate resources. The example does not provide a standardized controlled robot success-rate study.

Organizations / maintainers: Google / Google DeepMind.

<sub>Count snapshot: 2026-11-02.</sub>

<a id="e28"></a>

### Figure Helix 02

[![Technical Demo 2026](https://img.shields.io/badge/Technical%20Demo%202026-475569?style=flat-square)](https://www.figure.ai/news/helix-02) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.figure.ai/news/helix-02)

[🔗 Official page](https://www.figure.ai/news/helix-02) · —

Figure connects language goals with mobile manipulation through S2 semantic planning, S1 visuomotor policies, and S0 whole-body control.

Scope: A company technical demonstration; public videos do not replace reproducible experiments or open training code.

Organizations / maintainers: Figure AI.

<sub>Count snapshot: 2026-11-02.</sub>
