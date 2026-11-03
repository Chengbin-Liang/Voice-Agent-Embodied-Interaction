# 论文与项目索引

[返回首页](README.md) · [完整索引](CATALOG.md) · [Survey 对照](SURVEYS.md) · [Benchmark 导航](05-Voice-Agent-Benchmarks.md)

按技术主题浏览；⭐ 标注适合优先阅读的条目。计数口径见[标签说明](README.md#labels)。

[🎧 Omni 与语音模型](#omni) · [💬 Voice Agent 与交互系统](#voice) · [🤖 具身交互与语言反馈](#embodied) · [🦾 动作、数据与部署](#robotics) · [📏 评测](#evaluation) · [🏭 工业展示](#industry)

<a id="omni"></a>

## 🎧 Omni 与语音模型

<a id="e01"></a>

### ⭐ MiniCPM-o 4.5

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.27393) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V)

[📄 论文](https://arxiv.org/abs/2604.27393) · [💻 仓库](https://github.com/OpenBMB/MiniCPM-V) · [![★ 27,047](https://img.shields.io/badge/%E2%98%85%2027%2C047-eab308?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W7159670352)

以共享时间轴组织持续音视频输入与文本、语音输出，并研究主动回应。

📌 优先阅读理由：阅读持续音视频输入、全双工输出及其部署条件。

范围说明：全双工模式的硬件要求以官方部署文档为准；模型内存与完整系统内存应分开记录。

机构 / 维护方：Tsinghua University / THUNLP；ModelBest；OpenBMB。

<sub>计数快照：2026-11-02。</sub>

<a id="e02"></a>

### ⭐ Qwen2.5-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.20215) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni)

[📄 论文](https://arxiv.org/abs/2503.20215) · [💻 仓库](https://github.com/QwenLM/Qwen2.5-Omni) · [![★ 4,092](https://img.shields.io/badge/%E2%98%85%204%2C092-eab308?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni) [![Cite OA 14](https://img.shields.io/badge/Cite%20OA%2014-0284c7?style=flat-square)](https://openalex.org/W4409051416)

音视频、图像和文本输入，联合生成文本与语音；提供 Thinker–Talker 架构参照。

📌 优先阅读理由：建立 Thinker–Talker 架构、数据与分阶段训练的基本参照。

范围说明：流式语音输出不等于原生同时听说；MNN 功能覆盖以对应部署模式为准。

机构 / 维护方：Qwen Team / Alibaba。

<sub>计数快照：2026-11-02。</sub>

<a id="e03"></a>

### Qwen3-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.17765) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni)

[📄 论文](https://arxiv.org/abs/2509.17765) · [💻 仓库](https://github.com/QwenLM/Qwen3-Omni) · [![★ 4,093](https://img.shields.io/badge/%E2%98%85%204%2C093-eab308?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4415255153)

MoE Thinker–Talker 路线，覆盖多模态理解和实时语音生成。

机构 / 维护方：Qwen Team / Alibaba。

<sub>计数快照：2026-11-02。</sub>

<a id="e04"></a>

### InteractiveOmni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.13747) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2510.13747)

[📄 论文](https://arxiv.org/abs/2510.13747) · [💻 仓库](https://github.com/OpenSenseNova/InteractiveOmni) · [![★ 9](https://img.shields.io/badge/%E2%98%85%209-eab308?style=flat-square)](https://github.com/OpenSenseNova/InteractiveOmni) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415277372)

以音视频多轮交互为目标，提供 4B 与 8B 模型及多轮评价。

机构 / 维护方：SenseTime Research。

<sub>计数快照：2026-11-02。</sub>

<a id="e05"></a>

### VITA-1.5

[![NeurIPS 2025](https://img.shields.io/badge/NeurIPS%202025-475569?style=flat-square)](https://arxiv.org/abs/2501.01957) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2501.01957)

[📄 论文](https://arxiv.org/abs/2501.01957) · [💻 仓库](https://github.com/VITA-MLLM/VITA) · [![★ 2,539](https://img.shields.io/badge/%E2%98%85%202%2C539-eab308?style=flat-square)](https://github.com/VITA-MLLM/VITA) [![Cite OA 11](https://img.shields.io/badge/Cite%20OA%2011-0284c7?style=flat-square)](https://openalex.org/W4406093559)

面向实时视觉和语音交互的多模态模型，提供训练与推理流程。

机构 / 维护方：Nanjing University；Xiamen University；CASIA；Tencent Youtu Lab。

<sub>计数快照：2026-11-02。</sub>

<a id="e06"></a>

### Mini-Omni2

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.11190) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2410.11190)

[📄 论文](https://arxiv.org/abs/2410.11190) · [💻 仓库](https://github.com/gpt-omni/mini-omni2) · [![★ 1,936](https://img.shields.io/badge/%E2%98%85%201%2C936-eab308?style=flat-square)](https://github.com/gpt-omni/mini-omni2) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4403576555)

较早开放图像、语音、文本输入与实时语音输出的实验系统。

机构 / 维护方：Tsinghua University；Inspirai。

<sub>计数快照：2026-11-02。</sub>

<a id="e07"></a>

### ⭐ Moshi

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.00037) [![Independent Lab](https://img.shields.io/badge/Independent%20Lab-b45309?style=flat-square)](https://arxiv.org/html/2410.00037)

[📄 论文](https://arxiv.org/abs/2410.00037) · [💻 仓库](https://github.com/kyutai-labs/moshi) · [![★ 11,361](https://img.shields.io/badge/%E2%98%85%2011%2C361-eab308?style=flat-square)](https://github.com/kyutai-labs/moshi) [![Cite OA 9](https://img.shields.io/badge/Cite%20OA%209-0284c7?style=flat-square)](https://openalex.org/W4403883071) [![Cite S2 875](https://img.shields.io/badge/Cite%20S2%20875-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/ae4aa7b0c5a327dae63ad20e00b58bcc6176b3b8)

双向语音流与文本协同建模，为连续听说提供开源研究基础。

📌 优先阅读理由：理解双向语音流、文本辅助及低延迟生成。

机构 / 维护方：Kyutai。

<sub>计数快照：2026-11-02。</sub>

<a id="e08"></a>

### Freeze-Omni

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2411.00774) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2411.00774)

[📄 论文](https://arxiv.org/abs/2411.00774) · [💻 仓库](https://github.com/VITA-MLLM/Freeze-Omni) · [![★ 403](https://img.shields.io/badge/%E2%98%85%20403-eab308?style=flat-square)](https://github.com/VITA-MLLM/Freeze-Omni) [![Cite OA 4](https://img.shields.io/badge/Cite%20OA%204-0284c7?style=flat-square)](https://openalex.org/W4404390495)

冻结语言模型，结合流式语音编码解码和块级状态预测。

机构 / 维护方：Northwestern Polytechnical University；Nanjing University；Tencent Youtu Lab。

<sub>计数快照：2026-11-02。</sub>

<a id="voice"></a>

## 💬 Voice Agent 与交互系统

<a id="e29"></a>

### ⭐ FireRedChat

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.06502) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/abs/2509.06502)

[📄 论文](https://arxiv.org/abs/2509.06502) · [💻 仓库](https://github.com/FireRedTeam/FireRedChat) · [![★ 597](https://img.shields.io/badge/%E2%98%85%20597-eab308?style=flat-square)](https://github.com/FireRedTeam/FireRedChat) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4414757003)

全双工语音系统：轮次控制、主说话人打断、对话管理和工具调用。

📌 优先阅读理由：以模块化实现理解打断控制、对话状态和工具调用。

机构 / 维护方：Xiaohongshu / FireRed Team。

<sub>计数快照：2026-11-03。</sub>

<a id="e30"></a>

### Qwen Audio Agent

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent)

[💻 仓库](https://github.com/QwenAudio/qwen-audio-agent) · [![★ 3,112](https://img.shields.io/badge/%E2%98%85%203%2C112-eab308?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent)

语音前端与后台 Agent 分工，提供异步任务协作和取消机制的工程入口。

机构 / 维护方：Qwen / Alibaba。

<sub>计数快照：2026-11-03。</sub>

<a id="e09"></a>

### DuplexSLA

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2605.20755) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2605.20755)

[📄 论文](https://arxiv.org/abs/2605.20755) · [💻 仓库](https://github.com/hyzhang24/DuplexSLA) · [![★ 147](https://img.shields.io/badge/%E2%98%85%20147-eab308?style=flat-square)](https://github.com/hyzhang24/DuplexSLA) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7161968102)

在共同时间线上输出语音及结构化 action 通道，研究交谈中的规划与工具调用。

范围说明：论文的 action 通道主要对应结构化规划与工具操作，不能直接等同于关节控制。

机构 / 维护方：StepFun；Peking University；Nanyang Technological University；Shanghai Jiao Tong University；University of New South Wales；Imperial College London。

<sub>计数快照：2026-11-02。</sub>

<a id="e31"></a>

### Jarvis

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.23804) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2610.23804)

[📄 论文](https://arxiv.org/abs/2610.23804) · [💻 仓库](https://github.com/JensenYX/Jarvis) · [![★ 18](https://img.shields.io/badge/%E2%98%85%2018-eab308?style=flat-square)](https://github.com/JensenYX/Jarvis) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7222979632)

在交互前端和后台任务之间训练协调器，管理任务切换、状态和过期结果。

范围说明：软件 Agent 协调研究，尚不能据此推断真实机器人任务增益。

机构 / 维护方：CUHK Shenzhen；Tencent Hunyuan；Amphion Technology。

<sub>计数快照：2026-11-03。</sub>

<a id="e36"></a>

### TEN Framework

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/TEN-framework/ten-framework) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/TEN-framework/ten-framework)

[💻 仓库](https://github.com/TEN-framework/ten-framework) · [![★ 11,219](https://img.shields.io/badge/%E2%98%85%2011%2C219-eab308?style=flat-square)](https://github.com/TEN-framework/ten-framework)

实时音视频 Agent 框架，提供可组合扩展与多模态应用示例。

范围说明：LICENSE 包含 Apache-2.0 之外的附加使用条件，涉及终端设备托管等；部署前阅读官方 LICENSE。

机构 / 维护方：Agora；Contributor community。

<sub>计数快照：2026-11-03。</sub>

[官方 LICENSE](https://github.com/TEN-framework/ten-framework/blob/main/LICENSE)

<a id="e37"></a>

### ⭐ VoxMind

[![ACL 2026](https://img.shields.io/badge/ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.acl-long.459/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2604.15710)

[📄 论文](https://arxiv.org/abs/2604.15710) · [💻 仓库](https://github.com/MM-Speech/VoxMind) · [![★ 46](https://img.shields.io/badge/%E2%98%85%2046-eab308?style=flat-square)](https://github.com/MM-Speech/VoxMind) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7155019877)

用 AgentChat 数据、Think-before-Speak 与动态工具检索学习语音 Agent 的推理—调用—反馈闭环。

📌 优先阅读理由：先读 AgentChat 数据格式、训练目标与工具闭环实验，把“能聊天”推进到“能执行任务”。

范围说明：异步工具管理的效果不自动等同于所有条件下的同时听说能力；按论文各项实验分别判断。

机构 / 维护方：Zhejiang University；China University of Petroleum–Beijing at Karamay；Xiamen University。

<sub>计数快照：2026-11-03。</sub>

<a id="e38"></a>

### ⭐ F-Actor

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.242/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2601.11329)

[📄 论文](https://arxiv.org/abs/2601.11329) · [💻 仓库](https://github.com/MaikeZuefle/f-actor) · [![★ 33](https://img.shields.io/badge/%E2%98%85%2033-eab308?style=flat-square)](https://github.com/MaikeZuefle/f-actor) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7124734178)

通过指令控制音色、话题、反馈、打断和主动开场；冻结音频编码器，采用单阶段训练。

📌 优先阅读理由：理解如何把交互行为写成可监督、可控制的指令，而不只改语音生成质量。

机构 / 维护方：Karlsruhe Institute of Technology；University of Edinburgh；NatWest。

<sub>计数快照：2026-11-03。</sub>

<a id="e39"></a>

### ⭐ SOMMELIER

[![ACL Industry Track 2026](https://img.shields.io/badge/ACL%20Industry%20Track%202026-475569?style=flat-square)](https://aclanthology.org/2026.acl-industry.18/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2603.25750)

[📄 论文](https://arxiv.org/abs/2603.25750) · [💻 仓库](https://github.com/Anonymous-2001-j/Sommelier) · [![★ 0](https://img.shields.io/badge/%E2%98%85%200-eab308?style=flat-square)](https://github.com/Anonymous-2001-j/Sommelier) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7143443580)

把真实多人录音转为保留时间关系的双声道训练数据，连接分离、说话人分段、转写和质量筛选。

📌 优先阅读理由：理解真实录音如何转为可训练的全双工数据，重点看时间对齐、重叠和筛选。

机构 / 维护方：KAIST；NAVER Cloud。

<sub>计数快照：2026-11-03。</sub>

<a id="e40"></a>

### CF-Duplex / XA-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2605.10199) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2605.10199)

[📄 论文](https://arxiv.org/abs/2605.10199) · [🔗 项目](https://light1726.github.io/duplex-demo/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7160904488)

对比受控融合与交叉注意力，把用户语音流接入正在生成的模型，分析同时听说的架构选择。

机构 / 维护方：The Chinese University of Hong Kong；Tsinghua University；SenseTime。

<sub>计数快照：2026-11-03。</sub>

<a id="e41"></a>

### ⭐ DuplexGen

[![EMNLP 2026](https://img.shields.io/badge/EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.emnlp-main.2618/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2607.26178)

[📄 论文](https://arxiv.org/abs/2607.26178) · [💻 仓库](https://github.com/duplexgen/duplexgen-code) · [🔗 项目](https://duplexgen.github.io/) · [![★ 29](https://img.shields.io/badge/%E2%98%85%2029-eab308?style=flat-square)](https://github.com/duplexgen/duplexgen-code) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7171803236)

用少量人类偏好校准话轮行为预测，再合成适配不同场景的人机对话，用于全双工模型微调。

📌 优先阅读理由：把数据构造与目标交互行为连起来，阅读人类偏好如何进入合成与微调流程。

机构 / 维护方：University of Illinois Urbana-Champaign；Seoul National University；University of California Berkeley；Georgia Institute of Technology；Columbia University。

<sub>计数快照：2026-11-03。</sub>

<a id="e42"></a>

### BayLing-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.14528) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2606.14528)

[📄 论文](https://arxiv.org/abs/2606.14528) · [💻 仓库](https://github.com/BayLing-Models/BayLing-Duplex) · [![★ 96](https://img.shields.io/badge/%E2%98%85%2096-eab308?style=flat-square)](https://github.com/BayLing-Models/BayLing-Duplex) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7164829614)

以单个自回归 LLM 和少量状态 token 联合建模听、说、停，通过 SFT 与 DPO 学习交互。

机构 / 维护方：Institute of Computing Technology, Chinese Academy of Sciences；University of Chinese Academy of Sciences。

<sub>计数快照：2026-11-03。</sub>

<a id="e43"></a>

### MultiTalk / MultiTalkBench

[![NeurIPS 2026 · 作者标注](https://img.shields.io/badge/NeurIPS%202026%20%C2%B7%20%E4%BD%9C%E8%80%85%E6%A0%87%E6%B3%A8-475569?style=flat-square)](https://arxiv.org/abs/2609.36903) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.36903)

[📄 论文](https://arxiv.org/abs/2609.36903) · [🔗 预训练数据](https://huggingface.co/datasets/MultiTalk/MultiTalkPT) · [🔗 微调数据](https://huggingface.co/datasets/MultiTalk/MultiTalkFT) · [🔗 Benchmark](https://huggingface.co/datasets/MultiTalk/MultiTalkBench) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214898838)

扩展到长时、多方、双语全双工对话；提供预训练、微调数据和来自真实录音的 MultiTalkBench。

范围说明：NeurIPS 2026 依据作者在 arXiv 的标注；MultiTalkBench 与模型训练数据应分别使用。

机构 / 维护方：The Chinese University of Hong Kong；Centre for Perceptual and Interactive Intelligence (InnoHK)。

<sub>计数快照：2026-11-03。</sub>

<a id="e44"></a>

### ⭐ Self-Listening / LoopSpeech

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.05592) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.05592)

[📄 论文](https://arxiv.org/abs/2609.05592) · [💻 仓库](https://github.com/FreedomIntelligence/LoopSpeech) · [![★ 8](https://img.shields.io/badge/%E2%98%85%208-eab308?style=flat-square)](https://github.com/FreedomIntelligence/LoopSpeech) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212059771)

把实际已播放的语音纳入历史，区分“计划说出”与“用户已经听到”，研究打断后的内容连续性。

📌 优先阅读理由：打断后的状态一致性很容易遗漏；重点看已播放历史如何改变后续回答。

机构 / 维护方：Shenzhen Loop Area Institute；The Chinese University of Hong Kong, Shenzhen。

<sub>计数快照：2026-11-03。</sub>

<a id="e45"></a>

### D2: Dialogue-to-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.17124) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2610.17124)

[📄 论文](https://arxiv.org/abs/2610.17124) · [💻 仓库](https://github.com/penguinfish1688/D2-dialogue-to-duplex) · [🔗 项目](https://d2-duplex-demo.github.io/) · [![★ 11](https://img.shields.io/badge/%E2%98%85%2011-eab308?style=flat-square)](https://github.com/penguinfish1688/D2-dialogue-to-duplex) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221777691)

复用半双工语音模型进行全双工适配，分析音频块间隔对质量、时延和计算量的影响。

范围说明：仓库当前提供 Qwen3-Omni 80 ms 配置检查点；论文中的声学时延不包含全部计算与服务开销。

机构 / 维护方：MIT CSAIL；MIT–IBM Watson AI Lab。

<sub>计数快照：2026-11-03。</sub>

<a id="e46"></a>

### TASTE2

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.08956) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.08956)

[📄 论文](https://arxiv.org/abs/2609.08956) · [💻 仓库](https://github.com/GitYCC/TASTE-SpokenLM-2) · [🔗 项目](https://gitycc.github.io/TASTE2-Homepage/) · [🔗 语音应用](https://github.com/GitYCC/TASTE-Voice-Bot) · [![★ 2](https://img.shields.io/badge/%E2%98%85%202-eab308?style=flat-square)](https://github.com/GitYCC/TASTE-SpokenLM-2) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212080144)

以文本对齐的语音建模和部署协同组织全双工交互，补充副语言信号与实时运行的设计。

机构 / 维护方：MediaTek Research；National Taiwan University；NVIDIA AI Technology Center。

<sub>计数快照：2026-11-03。</sub>

<a id="e47"></a>

### IRAF

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.06559) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2606.06559)

[📄 论文](https://arxiv.org/abs/2606.06559) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7163910264)

按帧估计目标说话人可靠性并自适应融合音频，研究干扰说话人条件下的全双工鲁棒性。

机构 / 维护方：The Chinese University of Hong Kong；Huawei Leibniz Research Center；Nanyang Technological University。

<sub>计数快照：2026-11-03。</sub>

<a id="e48"></a>

### ⭐ MoshiRAG

[![ICML 2026 · 作者标注](https://img.shields.io/badge/ICML%202026%20%C2%B7%20%E4%BD%9C%E8%80%85%E6%A0%87%E6%B3%A8-475569?style=flat-square)](https://arxiv.org/abs/2604.12928) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.12928)

[📄 论文](https://arxiv.org/abs/2604.12928) · [💻 仓库](https://github.com/kyutai-labs/moshi-rag) · [![★ 195](https://img.shields.io/badge/%E2%98%85%20195-eab308?style=flat-square)](https://github.com/kyutai-labs/moshi-rag) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7154507545)

在全双工对话中异步触发检索并注入知识，观察检索耗时与持续对话如何协调。

📌 优先阅读理由：学习持续语音交互与耗时检索之间的接口、触发机制及结果注入。

范围说明：ICML 2026 接收状态依据作者在 arXiv 的说明；检索任务范围不同于通用工具执行。

机构 / 维护方：Toyota Technological Institute at Chicago；Kyutai；Gradium。

<sub>计数快照：2026-11-03。</sub>

<a id="e49"></a>

### Frontend–Backend Tool Calling

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.19334) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.19334)

[📄 论文](https://arxiv.org/abs/2609.19334) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213611583)

将实时语音前端与文本工具后端分离，以流式转写、工具执行和 prefill-and-repeat 结果回传连接两者。

范围说明：当前为预印本；计划投稿 ICASSP 2027 不表示已经接收。

机构 / 维护方：NVIDIA。

<sub>计数快照：2026-11-03。</sub>

<a id="e50"></a>

### DiffuPlex · Rolling Masked Diffusion

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.12214) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2610.12214)

[📄 论文](https://arxiv.org/abs/2610.12214) · [🔗 项目](https://diffuplex.github.io/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221088445)

用滚动掩码扩散预测交互帧，在保留交互质量的同时减少主干模型调用。

范围说明：与 NVIDIA 的 Discrete Diffusion 论文为不同工作，项目同名时按完整标题区分。

机构 / 维护方：University of Seoul。

<sub>计数快照：2026-11-03。</sub>

<a id="e51"></a>

### Diffuplex · Discrete Diffusion

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.17780) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2610.17780)

[📄 论文](https://arxiv.org/abs/2610.17780) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221757954)

以自回归过程决定何时说话，以离散扩散并行生成内容，研究全双工生成效率。

范围说明：论文称代码和检查点将发布；当前条目不将预告视为已开放资源。

机构 / 维护方：NVIDIA。

<sub>计数快照：2026-11-03。</sub>

<a id="e52"></a>

### Voice-Light

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.20995)

[📄 论文](https://arxiv.org/abs/2609.20995) · [💻 仓库](https://github.com/BertilBraun/Voice-Light) · [![★ 10](https://img.shields.io/badge/%E2%98%85%2010-eab308?style=flat-square)](https://github.com/BertilBraun/Voice-Light) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213934747)

级联系统中的因果轮次控制、推测生成和可撤销播放；用播放确认更新持久对话历史。

范围说明：论文在线实验为三个操作员运行、共 36 轮；适合作为工程案例，不能据此推断大规模用户效果。作者机构归属未确定。

机构 / 维护方：Bertil Braun。

<sub>计数快照：2026-11-03。</sub>

<a id="e53"></a>

### AdaptDuplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.29217) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.29217)

[📄 论文](https://arxiv.org/abs/2609.29217) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214079271)

结合自适应感知窗口、非阻塞认知整合与外部推理，研究动态全双工对话及分阶段后训练。

范围说明：当前绑定技术论文，未据此假定模型权重或完整训练流程已经开放。

机构 / 维护方：Zuoyebang Education Technology。

<sub>计数快照：2026-11-03。</sub>

<a id="e54"></a>

### Realtime-Venus

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.13814) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.13814)

[📄 论文](https://arxiv.org/abs/2609.13814) · [💻 仓库](https://github.com/inclusionAI/Realtime-Venus) · [![★ 252](https://img.shields.io/badge/%E2%98%85%20252-eab308?style=flat-square)](https://github.com/inclusionAI/Realtime-Venus) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213284145)

实时交互层异步委托后台任务，结果返回后继续对话，连接多模态输入、训练策略与运行时。

机构 / 维护方：Ant Group；Tsinghua University。

<sub>计数快照：2026-11-03。</sub>

<a id="e55"></a>

### NemotronLabs VoiceChat

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.21967) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.21967)

[📄 论文](https://arxiv.org/abs/2609.21967) · [💻 仓库](https://github.com/NVIDIA-NeMo/Speech/tree/nemotron-labs-voicechat) · [🔗 模型](https://huggingface.co/nvidia/NVIDIA-NemotronLabs-VoiceChat-11B) · [![★ 18,685](https://img.shields.io/badge/%E2%98%85%2018%2C685-eab308?style=flat-square)](https://github.com/NVIDIA-NeMo/Speech/tree/nemotron-labs-voicechat) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213936344)

开放的全双工语音模型，以独立工具通道连接动作调用，并支持可打断语音输出。

范围说明：代码入口为 NVIDIA-NeMo/Speech 的 nemotron-labs-voicechat 分支；Star 计整个 Speech 仓库。

机构 / 维护方：NVIDIA。

<sub>计数快照：2026-11-03。</sub>

<a id="e56"></a>

### StepAudio 3 Realtime

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.14005) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.14005)

[📄 论文](https://arxiv.org/abs/2609.14005) · [🔗 项目](https://stepaudiollm.github.io/step-audio-3-realtime/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213371127)

围绕 listen、converse、think、act 组织实时语音交互，结合 Think-While-Speaking 与异步工具执行。

范围说明：提供论文与本版本展示入口；不把 StepAudio 2 仓库当作本版本的完整代码。

机构 / 维护方：StepFun。

<sub>计数快照：2026-11-03。</sub>

<a id="e57"></a>

### Qwen-Audio-3.1-Realtime

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.25176) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.25176)

[📄 论文](https://arxiv.org/abs/2609.25176) · [💻 仓库](https://github.com/QwenAudio/qwen-audio-agent) · [![★ 3,112](https://img.shields.io/badge/%E2%98%85%203%2C112-eab308?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214103824)

在可执行环境中进行 Agent GRPO，结合多模态策略蒸馏，研究任务可靠性与交互行为后训练。

范围说明：qwen-audio-agent 是配套运行时；其开放不等于全部模型权重和训练代码开放。

机构 / 维护方：Alibaba / Qwen。

<sub>计数快照：2026-11-03。</sub>

<a id="e58"></a>

### ⭐ DuplexOmni

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.09186) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2606.09186)

[📄 论文](https://arxiv.org/abs/2606.09186) · [💻 仓库](https://github.com/MuyeHuang/DuplexOmni) · [![★ 145](https://img.shields.io/badge/%E2%98%85%20145-eab308?style=flat-square)](https://github.com/MuyeHuang/DuplexOmni) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7164028919)

实时交互层与异步思考层协同，配合 Writer–Director 数据合成组织边听、边看、边想、边说。

📌 优先阅读理由：阅读实时层、异步思考层与合成数据之间的对应关系，作为端到端系统设计参照。

机构 / 维护方：Xi’an Jiaotong University；Peking University；Meituan。

<sub>计数快照：2026-11-03。</sub>

<a id="embodied"></a>

## 🤖 具身交互与语言反馈

<a id="e13"></a>

### Interactive Language / Language Table

[![IEEE RA-L 2024](https://img.shields.io/badge/IEEE%20RA--L%202024-475569?style=flat-square)](https://doi.org/10.1109/LRA.2023.3295255) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2210.06407)

[📄 论文](https://arxiv.org/abs/2210.06407) · [💻 仓库](https://github.com/google-research/language-table) · [![★ 367](https://img.shields.io/badge/%E2%98%85%20367-eab308?style=flat-square)](https://github.com/google-research/language-table) [![Cite OA 113](https://img.shields.io/badge/Cite%20OA%20113-0284c7?style=flat-square)](https://openalex.org/W4391759936)

通过实时语言指导视觉运动策略，允许人逐步调整机器人完成目标。

机构 / 维护方：Robotics at Google。

<sub>计数快照：2026-11-02。</sub>

<a id="e25"></a>

### ⭐ Hi Robot

[![ICML 2025](https://img.shields.io/badge/ICML%202025-475569?style=flat-square)](https://proceedings.mlr.press/v267/shi25d.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.19417)

[📄 论文](https://arxiv.org/abs/2502.19417) · [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4416045178) [![Cite S2 319](https://img.shields.io/badge/Cite%20S2%20319-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/69afd10d387423a03617d461c3f47a5f3033cc54)

高层视觉语言推理将复杂指令和执行中反馈转为下一步任务，低层 VLA 执行具体动作。

📌 优先阅读理由：理解高层语言推理与低层动作策略的分工。

范围说明：语言反馈经高层规划传给动作策略，不能据此归因为原始语音信息增益。

机构 / 维护方：Physical Intelligence；Stanford University；UC Berkeley。

<sub>计数快照：2026-11-02。</sub>

<a id="e26"></a>

### ⭐ Yell At Your Robot / YAY Robot

[![RSS 2024](https://img.shields.io/badge/RSS%202024-475569?style=flat-square)](https://roboticsproceedings.org/rss20/p025.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2403.12910)

[📄 论文](https://arxiv.org/abs/2403.12910) · [💻 仓库](https://github.com/yay-robot/yay_robot) · [![★ 166](https://img.shields.io/badge/%E2%98%85%20166-eab308?style=flat-square)](https://github.com/yay-robot/yay_robot) [![Cite OA 47](https://img.shields.io/badge/Cite%20OA%2047-0284c7?style=flat-square)](https://openalex.org/W4402354098) [![Cite S2 179](https://img.shields.io/badge/Cite%20S2%20179-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/f213d0cb84b6afca9a4d5722081ba3052e7e89bc)

人在机器人执行长任务时给出口头修正，系统立即利用纠正，并将这些反馈用于后续高层策略训练。

📌 优先阅读理由：理解执行中口头纠正如何用于当前控制与后续学习。

范围说明：口头纠正主要通过语言表示进入控制与学习。

机构 / 维护方：Stanford University；UC Berkeley。

<sub>计数快照：2026-11-02。</sub>

<a id="e24"></a>

### VLAS

[![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2025/hash/804a1a9de5787e3597b4bb64e1a48ec3-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.13508)

[📄 论文](https://arxiv.org/abs/2502.13508) · [💻 仓库](https://github.com/whichwhichgone/VLAS) · [![★ 50](https://img.shields.io/badge/%E2%98%85%2050-eab308?style=flat-square)](https://github.com/whichwhichgone/VLAS) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4407764312) [![Cite S2 68](https://img.shields.io/badge/Cite%20S2%2068-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/f6075ce4db8dcc359c3ac97b85f2644dc5cadda6)

将原始语音接入视觉动作策略，并用声纹检索个体相关信息，执行带有个人偏好的操作。

范围说明：原始语音与声纹个性化操作，不应与全双工说做控制混为同一能力。

机构 / 维护方：Westlake University；Zhejiang University；Xi’an Jiaotong University。

<sub>计数快照：2026-11-02。</sub>

<a id="e21"></a>

### ⭐ RoboOmni (OpenMOSS)

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/33610fba262d7b6fed0810b89f55e147-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2510.23763)

[📄 论文](https://arxiv.org/abs/2510.23763) · [💻 仓库](https://github.com/OpenMOSS/RoboOmni) · [![★ 124](https://img.shields.io/badge/%E2%98%85%20124-eab308?style=flat-square)](https://github.com/OpenMOSS/RoboOmni) [![Cite S2 12](https://img.shields.io/badge/Cite%20S2%2012-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/37cd1e4cbfbfdadc2a898a703ab46bc0e1c83dd3)

从对话、环境声音和视觉线索推断意图，经确认后生成操作动作，研究隐式情境指令下的主动协助。

📌 优先阅读理由：了解环境声音与隐式意图如何进入操作任务。

范围说明：此处绑定 OpenMOSS 的 RoboOmni，注意与其他同名论文区分。

机构 / 维护方：Fudan University；Shanghai Innovation Institute；National University of Singapore。

<sub>计数快照：2026-11-02。</sub>

<a id="e22"></a>

### ⭐ ELLSA

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/6d8af672c0bca7a4be6f0cd0d229c05c-Abstract-Conference.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.16756)

[📄 论文](https://arxiv.org/abs/2510.16756) · [💻 仓库](https://github.com/bytedance/SALMONN) · [![★ 1,564](https://img.shields.io/badge/%E2%98%85%201%2C564-eab308?style=flat-square)](https://github.com/bytedance/SALMONN) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415958597) [![Cite S2 7](https://img.shields.io/badge/Cite%20S2%207-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/3af611e47c30a439f8acad312f16cf7837ddbce7)

在统一架构中处理视觉、文本、语音和动作，支持边说边做、动作打断与基于场景的问答。

📌 优先阅读理由：阅读语音与动作共同建模、边说边做及中断实验。

范围说明：SALMONN 是共享仓库；Star 数不等于 ELLSA 子项目独立关注量，具体权重与训练入口见官方发布。

机构 / 维护方：Tsinghua University；ByteDance。

<sub>计数快照：2026-11-02。</sub>

<a id="e23"></a>

### VITA-E

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.21817) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.21817)

[📄 论文](https://arxiv.org/abs/2510.21817) · [💻 仓库](https://github.com/Tencent/VITA) · [![★ 166](https://img.shields.io/badge/%E2%98%85%20166-eab308?style=flat-square)](https://github.com/Tencent/VITA) [![Cite S2 2](https://img.shields.io/badge/Cite%20S2%202-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/62d932e380f9ec7de5d43c17bc933a05887b0007)

以并行的活动/监听模型和控制 token 调度语音与动作，支持中断、任务切换和边说边做。

机构 / 维护方：Nanjing University；CASIA；Tencent Youtu Lab；Fourier Intelligence。

<sub>计数快照：2026-11-02。</sub>

<a id="e11"></a>

### Reachy Mini Conversation App

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)

[💻 仓库](https://github.com/pollen-robotics/reachy_mini_conversation_app) · [![★ 348](https://img.shields.io/badge/%E2%98%85%20348-eab308?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)

把实时语音、摄像头工具和机器人运动接入同一对话应用。

范围说明：主要是头部、天线等身体表达和视觉工具调用，不是机械臂抓取平台。

机构 / 维护方：Pollen Robotics / Hugging Face。

<sub>计数快照：2026-11-02。</sub>

<a id="e12"></a>

### EMAGE / BEAT2

[![CVPR 2024](https://img.shields.io/badge/CVPR%202024-475569?style=flat-square)](https://pantomatrix.github.io/EMAGE/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2401.00374)

[📄 论文](https://arxiv.org/abs/2401.00374) · [💻 仓库](https://github.com/haiyangliu0/character-policy) · [![★ 1,312](https://img.shields.io/badge/%E2%98%85%201%2C312-eab308?style=flat-square)](https://github.com/haiyangliu0/character-policy) [![Cite OA 95](https://img.shields.io/badge/Cite%20OA%2095-0284c7?style=flat-square)](https://openalex.org/W4402727140)

从语音及文本生成全身与面部协同动作，连接 co-speech gesture 与表达数据。

范围说明：面向共语手势与角色表达；不直接证明真实机器人的操作能力。

机构 / 维护方：The University of Tokyo；Keio University；Max Planck Institute for Intelligent Systems；JAIST；Tsinghua University。

<sub>计数快照：2026-11-02。</sub>

<a id="robotics"></a>

## 🦾 动作、数据与部署

<a id="e19"></a>

### ⭐ LeRobot

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.22818) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2602.22818)

[📄 论文](https://arxiv.org/abs/2602.22818) · [💻 仓库](https://github.com/huggingface/lerobot) · [![★ 28,653](https://img.shields.io/badge/%E2%98%85%2028%2C653-eab308?style=flat-square)](https://github.com/huggingface/lerobot) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7131860508)

机器人数据、策略训练、硬件控制与评测的开源工具入口。

📌 优先阅读理由：贯通示范采集、数据查看、策略训练与真机执行。

机构 / 维护方：Hugging Face；University of Oxford。

<sub>计数快照：2026-11-02 / 2026-11-03。</sub>

<a id="e32"></a>

### ⭐ ACT / ALOHA

[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://www.roboticsproceedings.org/rss19/p016.pdf) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2304.13705)

[📄 论文](https://arxiv.org/abs/2304.13705) · [💻 仓库](https://github.com/tonyzhaozh/act) · [![★ 2,318](https://img.shields.io/badge/%E2%98%85%202%2C318-eab308?style=flat-square)](https://github.com/tonyzhaozh/act) [![Cite OA 674](https://img.shields.io/badge/Cite%20OA%20674-0284c7?style=flat-square)](https://openalex.org/W4385430674)

用遥操作示范学习动作块，建立视觉运动模仿学习基线。

📌 优先阅读理由：建立“观测—动作示范—动作块预测”的模仿学习直觉。

范围说明：标准 ACT 不是语言条件模型；多目标选择需技能选择器或另加目标条件。

机构 / 维护方：Stanford University；Meta；UC Berkeley。

<sub>计数快照：2026-11-03。</sub>

<a id="e33"></a>

### Diffusion Policy

[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2303.04137) [![IJRR 2024](https://img.shields.io/badge/IJRR%202024-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/)

[📄 论文](https://arxiv.org/abs/2303.04137v4) · [💻 仓库](https://github.com/real-stanford/diffusion_policy) · [![★ 4,698](https://img.shields.io/badge/%E2%98%85%204%2C698-eab308?style=flat-square)](https://github.com/real-stanford/diffusion_policy) [![Cite OA 12](https://img.shields.io/badge/Cite%20OA%2012-0284c7?style=flat-square)](https://openalex.org/W4323651335)

将条件动作分布建模为去噪过程，生成连续动作序列。

范围说明：论文链接为 RSS 2023 版本；IJRR 2024 为扩展版。引文数量绑定所链接的数据库记录。

机构 / 维护方：Columbia University；Toyota Research Institute；MIT。

<sub>计数快照：2026-11-03。</sub>

<a id="e34"></a>

### ⭐ SmolVLA

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2506.01844) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2506.01844)

[📄 论文](https://arxiv.org/abs/2506.01844) · [💻 仓库](https://github.com/huggingface/lerobot) · [![★ 28,653](https://img.shields.io/badge/%E2%98%85%2028%2C653-eab308?style=flat-square)](https://github.com/huggingface/lerobot) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4414898213)

450M 视觉语言动作模型，以图像、机器人状态与文本指令为条件生成动作块。

📌 优先阅读理由：沿官方教程把预训练 VLA 适配到自己的机器人数据。

范围说明：输入含文本指令，不是原生语音策略。Star 数为整个 LeRobot 仓库；模型小不自动保证整机实时。

机构 / 维护方：Hugging Face；Sorbonne University；valeo.ai；ENS Paris-Saclay。

<sub>计数快照：2026-11-03。</sub>

<a id="e20"></a>

### OpenVLA

[![CoRL 2024](https://img.shields.io/badge/CoRL%202024-475569?style=flat-square)](https://proceedings.mlr.press/v270/kim25c.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2406.09246)

[📄 论文](https://arxiv.org/abs/2406.09246) · [💻 仓库](https://github.com/openvla/openvla) · [![★ 7,250](https://img.shields.io/badge/%E2%98%85%207%2C250-eab308?style=flat-square)](https://github.com/openvla/openvla) [![Cite OA 62](https://img.shields.io/badge/Cite%20OA%2062-0284c7?style=flat-square)](https://openalex.org/W4399695759)

视觉与语言条件下的机器人动作模型，作为交互层连接动作策略的基础参照。

范围说明：视觉、语言到动作的基础；原生语音与实时打断需要额外系统设计。

机构 / 维护方：Stanford University；UC Berkeley；MIT；Toyota Research Institute；Google DeepMind；Physical Intelligence。

<sub>计数快照：2026-11-02。</sub>

<a id="e17"></a>

### llama.cpp ecosystem

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/OpenBMB/llama.cpp-omni) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/ggml-org/llama.cpp/discussions/19759)

[💻 仓库](https://github.com/ggml-org/llama.cpp) · [![★ 133,116](https://img.shields.io/badge/%E2%98%85%20133%2C116-eab308?style=flat-square)](https://github.com/ggml-org/llama.cpp)

本地推理工具链基础，提供量化与多平台运行入口。

范围说明：完整 Omni 模式可能依赖专用分支，例如 OpenBMB/llama.cpp-omni。

机构 / 维护方：ggml.ai / Hugging Face；llama.cpp contributor community。

<sub>计数快照：2026-11-02。</sub>

<a id="e18"></a>

### MNN

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni#deployment-with-mnn) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/alibaba/MNN)

[💻 仓库](https://github.com/alibaba/MNN) · [![★ 16,336](https://img.shields.io/badge/%E2%98%85%2016%2C336-eab308?style=flat-square)](https://github.com/alibaba/MNN)

面向移动与边缘设备的推理框架；Qwen2.5-Omni 提供官方接入入口。

机构 / 维护方：Alibaba。

<sub>计数快照：2026-11-02。</sub>

<a id="evaluation"></a>

## 📏 评测

<a id="e14"></a>

### Daily-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2505.17862) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2505.17862)

[📄 论文](https://arxiv.org/abs/2505.17862) · [💻 仓库](https://github.com/Lliar-liar/Daily-Omni) · [![★ 53](https://img.shields.io/badge/%E2%98%85%2053-eab308?style=flat-square)](https://github.com/Lliar-liar/Daily-Omni) 引文计数 —

日常视频音画联合推理基准，强调跨模态时间对齐。

机构 / 维护方：Fudan University。

<sub>计数快照：2026-11-02。</sub>

<a id="e15"></a>

### OmniBench (m-a-p)

[![NeurIPS 2025](https://img.shields.io/badge/NeurIPS%202025-475569?style=flat-square)](https://arxiv.org/abs/2409.15272) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2409.15272)

[📄 论文](https://arxiv.org/abs/2409.15272) · [💻 仓库](https://github.com/multimodal-art-projection/OmniBench) · [![★ 62](https://img.shields.io/badge/%E2%98%85%2062-eab308?style=flat-square)](https://github.com/multimodal-art-projection/OmniBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4403885114) [![Cite S2 111](https://img.shields.io/badge/Cite%20S2%20111-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/bde43a6356341b68a675582cf964fd9725fb40fb)

针对图像、音频、文本联合理解的三模态基准，并提供 OmniInstruct。

机构 / 维护方：M-A-P；University of Manchester；Queen Mary University of London；01.ai；HKUST；Nanjing University；Dartmouth College。

<sub>计数快照：2026-11-02。</sub>

<a id="e16"></a>

### ⭐ Full-Duplex-Bench

[![ASRU 2025](https://img.shields.io/badge/ASRU%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.04721) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2503.04721)

[📄 论文](https://arxiv.org/abs/2503.04721) · [💻 仓库](https://github.com/DanielLin94144/Full-Duplex-Bench) · [![★ 335](https://img.shields.io/badge/%E2%98%85%20335-eab308?style=flat-square)](https://github.com/DanielLin94144/Full-Duplex-Bench) [![Cite OA 8](https://img.shields.io/badge/Cite%20OA%208-0284c7?style=flat-square)](https://openalex.org/W7148492801)

覆盖停顿、反馈、轮次交接和打断；后续版本扩展重叠、动态多轮与工具使用。

📌 优先阅读理由：把打断、轮次交接和交互时序转为可测指标。

机构 / 维护方：National Taiwan University；UC Berkeley；University of Washington；MIT CSAIL。

<sub>计数快照：2026-11-02 / 2026-11-03。</sub>

<a id="e35"></a>

### LIBERO

[![NeurIPS Datasets and Benchmarks 2023](https://img.shields.io/badge/NeurIPS%20Datasets%20and%20Benchmarks%202023-475569?style=flat-square)](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8c3c666820ea055a77726d66fc7d447f-Abstract-Datasets_and_Benchmarks.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2306.03310)

[📄 论文](https://arxiv.org/abs/2306.03310) · [💻 仓库](https://github.com/Lifelong-Robot-Learning/LIBERO) · [![★ 2,508](https://img.shields.io/badge/%E2%98%85%202%2C508-eab308?style=flat-square)](https://github.com/Lifelong-Robot-Learning/LIBERO) [![Cite OA 136](https://img.shields.io/badge/Cite%20OA%20136-0284c7?style=flat-square)](https://openalex.org/W7133220882)

语言条件机器人操作基准，考察知识迁移与持续学习。

范围说明：主要评价语言条件操作能力，不直接评价语音交互和真人协作。

机构 / 维护方：UT Austin；Tsinghua University；Sony AI。

<sub>计数快照：2026-11-03。</sub>

<a id="e59"></a>

### ⭐ VoiceBench

[![TACL 2026](https://img.shields.io/badge/TACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.tacl-1.18/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2410.17196)

[📄 论文](https://arxiv.org/abs/2410.17196) · [💻 仓库](https://github.com/MatthewCYM/VoiceBench) · [![★ 407](https://img.shields.io/badge/%E2%98%85%20407-eab308?style=flat-square)](https://github.com/MatthewCYM/VoiceBench) [![Cite OA 12](https://img.shields.io/badge/Cite%20OA%2012-0284c7?style=flat-square)](https://openalex.org/W4404261856)

评价语音助手的知识、指令遵循、安全及口音、噪声等扰动下的回答能力。

📌 优先阅读理由：建立基础语音助手能力参照，再与交互和任务指标分别比较。

范围说明：主要评价语音输入后的回答能力；不能替代连续同时听说或工具任务评测。

机构 / 维护方：National University of Singapore。

<sub>计数快照：2026-11-03。</sub>

<a id="e60"></a>

### VocalBench

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2505.15727) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2505.15727)

[📄 论文](https://arxiv.org/abs/2505.15727) · [💻 仓库](https://github.com/SJTU-OmniAgent/VocalBench) · [![★ 8](https://img.shields.io/badge/%E2%98%85%208-eab308?style=flat-square)](https://github.com/SJTU-OmniAgent/VocalBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4415329203)

覆盖语义、声学、对话与鲁棒性，补充单轮和多轮语音交互能力评测。

范围说明：各子集、语言和后续扩展的发布状态分别核对；子集的会议发表不代表整套 benchmark 同一 venue。

机构 / 维护方：Shanghai Jiao Tong University；Ant Group。

<sub>计数快照：2026-11-03。</sub>

<a id="e61"></a>

### VCB Bench

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.1659/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2510.11098)

[📄 论文](https://arxiv.org/abs/2510.11098) · [💻 仓库](https://github.com/Tencent/VCB-Bench) · [![★ 5](https://img.shields.io/badge/%E2%98%85%205-eab308?style=flat-square)](https://github.com/Tencent/VCB-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4417101201)

以真实中文语音为核心，评价指令遵循、知识理解与声学和内容扰动下的鲁棒性。

范围说明：核心贡献为真实中文语音；后续语言扩展与论文原始协议应分开报告。

机构 / 维护方：Wuhan University；Tencent。

<sub>计数快照：2026-11-03。</sub>

<a id="e62"></a>

### ⭐ VoiceAgentBench

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.07978) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2510.07978)

[📄 论文](https://arxiv.org/abs/2510.07978) · [💻 仓库](https://github.com/ola-krutrim/VoiceAgentBench) · [🔗 数据](https://huggingface.co/datasets/krutrim-ai-labs/VoiceAgentBench) · [![★ 6](https://img.shields.io/badge/%E2%98%85%206-eab308?style=flat-square)](https://github.com/ola-krutrim/VoiceAgentBench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415318706)

将多语言语音输入连接单步、并行、顺序工具调用及多轮场景，检查函数选择和参数等代理能力。

📌 优先阅读理由：先理解语音工具调用的函数、参数和多步结构，再进入真实任务成功率。

范围说明：强调语音条件下的工具调用结构和参数；不能直接代表连续语音输出的时序自然度。

机构 / 维护方：OLA Electric / Krutrim AI。

<sub>计数快照：2026-11-03。</sub>

<a id="e63"></a>

### ⭐ τ-Voice

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2603.13686) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2603.13686)

[📄 论文](https://arxiv.org/abs/2603.13686) · [💻 仓库](https://github.com/sierra-research/tau2-bench) · [![★ 2,382](https://img.shields.io/badge/%E2%98%85%202%2C382-eab308?style=flat-square)](https://github.com/sierra-research/tau2-bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7138316890)

以领域规则和环境状态评价全双工语音 Agent 的多轮工具使用及最终任务完成。

📌 优先阅读理由：从环境终态判断任务是否完成，适合对照文本 Agent 与语音 Agent 的差距。

范围说明：tau2-bench 仓库持续演进并包含后续 τ³ 开发；复现本论文时固定其对应版本、环境和用户模拟器。

机构 / 维护方：Sierra；Princeton University。

<sub>计数快照：2026-11-03。</sub>

<a id="e64"></a>

### ⭐ Full-Duplex-Bench-v3

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.04847) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.04847)

[📄 论文](https://arxiv.org/abs/2604.04847) · [💻 仓库](https://github.com/DanielLin94144/Full-Duplex-Bench) · [🔗 项目](https://daniellin94144.github.io/FDB-v3-demo/) · [![★ 335](https://img.shields.io/badge/%E2%98%85%20335-eab308?style=flat-square)](https://github.com/DanielLin94144/Full-Duplex-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7151544009)

把真人语音中的犹豫、重复、修正等不流利现象与多步工具调用结合，评价交互中的任务执行。

📌 优先阅读理由：把真实口语修正与工具调用放在同一测试中，观察交互干扰是否造成任务错误。

范围说明：与 v1、v1.5、v2 共用仓库但任务不同；v3 论文为预印本，不沿用 v1 的 ASRU 2025 标签。

机构 / 维护方：National Taiwan University；NVIDIA。

<sub>计数快照：2026-11-03。</sub>

<a id="e65"></a>

### ⭐ MTR-DuplexBench

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.263/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2511.10262)

[📄 论文](https://arxiv.org/abs/2511.10262) · [💻 仓库](https://github.com/ZhangHe0918/MTR-DuplexBench) · [![★ 9](https://img.shields.io/badge/%E2%98%85%209-eab308?style=flat-square)](https://github.com/ZhangHe0918/MTR-DuplexBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4416238789)

按轮次分析长一些的全双工对话，联合观察交互动态、回答质量、指令遵循和安全。

📌 优先阅读理由：补上单个片段测试难以覆盖的多轮累积问题。

机构 / 维护方：Tsinghua University；The Chinese University of Hong Kong；Huawei。

<sub>计数快照：2026-11-03。</sub>

<a id="e66"></a>

### HumDial-FDBench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.21406) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.21406)

[📄 论文](https://arxiv.org/abs/2604.21406) · [💻 仓库](https://github.com/ASLP-lab/HumDial-FDBench) · [![★ 44](https://img.shields.io/badge/%E2%98%85%2044-eab308?style=flat-square)](https://github.com/ASLP-lab/HumDial-FDBench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7155525302)

以真实双声道人类对话评测重叠、打断和反馈，并组织 HumDial 全双工挑战与榜单。

范围说明：论文讨论 ICASSP 2026 HumDial 挑战；挑战名称不作为该预印本已收入会议论文集的证据。

机构 / 维护方：Northwestern Polytechnical University / ASLP Lab；Nanjing University；AISHELL。

<sub>计数快照：2026-11-03。</sub>

<a id="e67"></a>

### MP-Bench

[![Findings of EMNLP 2026](https://img.shields.io/badge/Findings%20of%20EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-emnlp.1437/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.13076)

[📄 论文](https://arxiv.org/abs/2609.13076) · [💻 仓库](https://github.com/atosystem/MP-Bench) · [![★ 1](https://img.shields.io/badge/%E2%98%85%201-eab308?style=flat-square)](https://github.com/atosystem/MP-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212688662)

把语音 Agent 作为多人对话的参与者，评价理解、接话时机与回应适切性。

机构 / 维护方：The University of Texas at Austin；National Taiwan University；MIT；Carnegie Mellon University；Meta AI。

<sub>计数快照：2026-11-03。</sub>

<a id="e68"></a>

### Duplex-MPE

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.31948) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.31948)

[📄 论文](https://arxiv.org/abs/2609.31948) · [🔗 项目](https://step-out.github.io/Duplex-MPE-Page/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214781414)

在多人场景中区分被明确点名、隐含求助、主动参与与应保持沉默，测试参与决策。

机构 / 维护方：Peking University；Renmin University of China；Tsinghua University；National Taiwan University；Xiamen University；Fudan University。

<sub>计数快照：2026-11-03。</sub>

<a id="e69"></a>

### Instruct-FD

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2607.20460) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2607.20460)

[📄 论文](https://arxiv.org/abs/2607.20460) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7170334618)

检验全双工系统能否按指令调整接话、打断、反馈及主动性，报告交互指令遵循程度。

机构 / 维护方：Boson AI。

<sub>计数快照：2026-11-03。</sub>

<a id="e70"></a>

### DuplexAct-Bench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.39446) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.39446)

[📄 论文](https://arxiv.org/abs/2609.39446) · [💻 仓库](https://github.com/Alita-xky/DuplexAct-Bench) · [🔗 项目](https://alitaxky.icu/DuplexAct-Bench/) · [![★ 1](https://img.shields.io/badge/%E2%98%85%201-eab308?style=flat-square)](https://github.com/Alita-xky/DuplexAct-Bench) 引文计数 —

覆盖打断、让出话轮、抵抗打断、主动沉默、主动开场、反馈六类行为，分别检查时机与内容。

范围说明：链接仓库主要提供项目页面；完整评测器和数据的可用性以项目发布为准。

机构 / 维护方：Beijing Institute for General Artificial Intelligence；Peking University；Shanghai Jiao Tong University。

<sub>计数快照：2026-11-03。</sub>

<a id="e71"></a>

### ⭐ EVA-Bench

[![Findings of EMNLP 2026](https://img.shields.io/badge/Findings%20of%20EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-emnlp.2182/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2605.13841)

[📄 论文](https://arxiv.org/abs/2605.13841) · [💻 仓库](https://github.com/ServiceNow/eva) · [🔗 项目](https://servicenow.github.io/eva/) · [![★ 235](https://img.shields.io/badge/%E2%98%85%20235-eab308?style=flat-square)](https://github.com/ServiceNow/eva) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7161175665)

以动态 bot-to-bot 对话模拟评价完整任务和交互体验，分别报告任务与事实忠实度、时序与体验。

📌 优先阅读理由：学习将任务正确性与体验分开评估，并检查动态用户模拟器的可信度。

机构 / 维护方：ServiceNow AI Research。

<sub>计数快照：2026-11-03。</sub>

<a id="e72"></a>

### VAmoS Bench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2607.27453) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2607.27453)

[📄 论文](https://arxiv.org/abs/2607.27453) · [💻 仓库](https://github.com/veris-ai/riley-agent) · [![★ 18](https://img.shields.io/badge/%E2%98%85%2018-eab308?style=flat-square)](https://github.com/veris-ai/riley-agent) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7172022530)

在金融服务场景中运行语音代理模拟，通过完整对话、工具轨迹与领域事实检查任务执行。

范围说明：领域为金融服务；riley-agent 是参考代理实现，不能直接视为完整 benchmark 评分器。

机构 / 维护方：Veris AI。

<sub>计数快照：2026-11-03。</sub>

<a id="e73"></a>

### FD-Bench

[![Interspeech 2025](https://img.shields.io/badge/Interspeech%202025-475569?style=flat-square)](https://www.isca-archive.org/interspeech_2025/peng25b_interspeech.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2507.19040)

[📄 论文](https://arxiv.org/abs/2507.19040) · [💻 仓库](https://github.com/pengyizhou/FD-Bench) · [![★ 27](https://img.shields.io/badge/%E2%98%85%2027-eab308?style=flat-square)](https://github.com/pengyizhou/FD-Bench) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4415433582)

以多轮、打断和噪声条件构建全双工评测流程，观察生成质量与延迟。

范围说明：与 DanielLin94144/Full-Duplex-Bench 是不同项目；两者的分数与版本不能混用。

机构 / 维护方：Nanyang Technological University；Alibaba。

<sub>计数快照：2026-11-03。</sub>

<a id="e74"></a>

### TurnBench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2608.25218) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2608.25218)

[📄 论文](https://arxiv.org/abs/2608.25218) · [💻 仓库](https://github.com/SesameAILabs/turnbench) · [🔗 项目](https://turnbench.sesame.com/) · [![★ 57](https://img.shields.io/badge/%E2%98%85%2057-eab308?style=flat-square)](https://github.com/SesameAILabs/turnbench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7204453739)

围绕轮次结束与打断检测，在不同误报预算下比较召回和延迟，评价组件的实时决策。

范围说明：主要评价轮次决策组件；不直接测回复内容、工具调用或最终任务完成。

机构 / 维护方：Sesame AI；Mundo AI；Oto；Carnegie Mellon University；National Taiwan University；Academia Sinica；Brno University of Technology。

<sub>计数快照：2026-11-03。</sub>

<a id="industry"></a>

## 🏭 工业展示

<a id="e10"></a>

### WITA-Omni

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://www.agibot.com/article/231/detail/122.html) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.agibot.com/article/231/detail/122.html)

[🔗 官方页面](https://www.agibot.com/article/231/detail/122.html) · —

智元的具身交互展示将场景理解、语音和身体表达组合在同一交互过程中。

范围说明：工业展示；不能由演示反推动作模型、训练数据或完整系统已经开放。

机构 / 维护方：AGIBOT / 智元。

<sub>计数快照：2026-11-02。</sub>

<a id="e27"></a>

### Gemini Live API × Robotics demo

[![Technical Demo 2025](https://img.shields.io/badge/Technical%20Demo%202025-475569?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/)

[🔗 官方页面](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) · —

Google 官方展示将语音与机器人摄像头输入交给 Live API，再以函数调用连接机器人控制接口。

范围说明：Live API 工程示例与 Gemini Robotics 模型是不同入口；示例本身不提供统一的机器人成功率对照实验。

机构 / 维护方：Google / Google DeepMind。

<sub>计数快照：2026-11-02。</sub>

<a id="e28"></a>

### Figure Helix 02

[![Technical Demo 2026](https://img.shields.io/badge/Technical%20Demo%202026-475569?style=flat-square)](https://www.figure.ai/news/helix-02) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.figure.ai/news/helix-02)

[🔗 官方页面](https://www.figure.ai/news/helix-02) · —

Figure 以 S2 语义规划、S1 视觉运动策略和 S0 全身控制连接语言目标与移动操作。

范围说明：公司技术展示；公开视频不能替代可复现实验和开放训练代码。

机构 / 维护方：Figure AI。

<sub>计数快照：2026-11-02。</sub>
