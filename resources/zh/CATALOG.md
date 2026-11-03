# 论文与项目索引

**中文** | [English](../en/CATALOG.md)

[返回首页](../../README.md) · [Survey](SURVEYS.md) · [Benchmarks](../../docs/zh/05-Voice-Agent-Benchmarks.md)

⭐ 优先阅读条目附具体理由。计数口径见[标签说明](../../README.md#labels)。

[🧠 LLM 后训练与强化学习](#llm) · [🎧 ALM / Omni 与语音模型](#omni) · [💬 Voice Agent 与交互系统](#voice) · [🤖 具身交互与语言反馈](#embodied) · [🦾 动作、数据与部署](#robotics) · [📏 评测](#evaluation) · [🏭 工业展示](#industry)

<a id="llm"></a>

## 🧠 LLM 后训练与强化学习

<a id="e75"></a>

### ⭐ PPO

[![arXiv 2017](https://img.shields.io/badge/arXiv%202017-475569?style=flat-square)](https://arxiv.org/abs/1707.06347) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/1707.06347)

[📄 论文](https://arxiv.org/abs/1707.06347) · [💻 仓库](https://github.com/openai/baselines) · [![★ 16,775](https://img.shields.io/badge/%E2%98%85%2016%2C775-eab308?style=flat-square)](https://github.com/openai/baselines) [![Cite OA 10,618](https://img.shields.io/badge/Cite%20OA%2010%2C618-0284c7?style=flat-square)](https://openalex.org/W2736601468)

通过限制策略更新幅度，在采样轨迹上优化奖励；理解后续 RLHF 的算法基础。

📌 优先阅读理由：介绍策略、奖励、优势估计与 clipped objective，作为语言模型 PPO 的算法背景。

机构 / 维护方：OpenAI

<sub>计数快照：2026-11-03</sub>

<a id="e76"></a>

### ⭐ InstructGPT / RLHF

[![NeurIPS 2022](https://img.shields.io/badge/NeurIPS%202022-475569?style=flat-square)](https://arxiv.org/abs/2203.02155) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2203.02155)

[📄 论文](https://arxiv.org/abs/2203.02155) · [![Cite OA 4,208](https://img.shields.io/badge/Cite%20OA%204%2C208-0284c7?style=flat-square)](https://openalex.org/W4226278401)

用示范进行 SFT、用人类排序训练奖励模型，再用 PPO 优化语言模型。

📌 优先阅读理由：建立 SFT → 偏好数据 → 奖励模型 → RL 的完整参照。

机构 / 维护方：OpenAI

<sub>计数快照：2026-11-03</sub>

<a id="e77"></a>

### ⭐ DPO

[![NeurIPS 2023](https://img.shields.io/badge/NeurIPS%202023-475569?style=flat-square)](https://arxiv.org/abs/2305.18290) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2305.18290)

[📄 论文](https://arxiv.org/abs/2305.18290) · [💻 仓库](https://github.com/eric-mitchell/direct-preference-optimization) · [![★ 2,922](https://img.shields.io/badge/%E2%98%85%202%2C922-eab308?style=flat-square)](https://github.com/eric-mitchell/direct-preference-optimization) Cite —

直接从优选与劣选回答优化相对概率，理解离线偏好优化与在线 RL 的差别。

📌 优先阅读理由：理解同一份偏好数据如何用于不同的后训练方法。

DPO 本身不需要在线环境 rollout。

机构 / 维护方：Stanford University

<sub>计数快照：2026-11-03</sub>

<a id="e78"></a>

### ⭐ DeepSeekMath / GRPO

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2402.03300) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2402.03300)

[📄 论文](https://arxiv.org/abs/2402.03300) · [💻 仓库](https://github.com/deepseek-ai/DeepSeek-Math) · [![★ 3,478](https://img.shields.io/badge/%E2%98%85%203%2C478-eab308?style=flat-square)](https://github.com/deepseek-ai/DeepSeek-Math) [![Cite OA 101](https://img.shields.io/badge/Cite%20OA%20101-0284c7?style=flat-square)](https://openalex.org/W4391631327)

在数学推理中提出 GRPO，以同一问题的多条采样回答构造相对优势。

📌 优先阅读理由：阅读组内奖励、优势估计和 KL 约束，连接可验证奖励实践。

机构 / 维护方：DeepSeek-AI; Tsinghua University; Peking University

<sub>计数快照：2026-11-03</sub>

<a id="e79"></a>

### DeepSeek-R1

[![Nature 2025](https://img.shields.io/badge/Nature%202025-475569?style=flat-square)](https://www.nature.com/articles/s41586-025-09422-z) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2501.12948)

[📄 论文](https://arxiv.org/abs/2501.12948) · [💻 仓库](https://github.com/deepseek-ai/DeepSeek-R1) · [![★ 91,995](https://img.shields.io/badge/%E2%98%85%2091%2C995-eab308?style=flat-square)](https://github.com/deepseek-ai/DeepSeek-R1) [![Cite OA 1,701](https://img.shields.io/badge/Cite%20OA%201%2C701-0284c7?style=flat-square)](https://openalex.org/W4414281281)

研究推理强化学习、冷启动、多阶段后训练与小模型蒸馏。

可从蒸馏模型开展适配；仓库的权重发布与完整原始 RL 训练配方是不同资源。

机构 / 维护方：DeepSeek-AI

<sub>计数快照：2026-11-03</sub>

<a id="omni"></a>

## 🎧 ALM / Omni 与语音模型

<a id="e01"></a>

### ⭐ MiniCPM-o 4.5

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.27393) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V)

[📄 论文](https://arxiv.org/abs/2604.27393) · [💻 仓库](https://github.com/OpenBMB/MiniCPM-V) · [![★ 27,047](https://img.shields.io/badge/%E2%98%85%2027%2C047-eab308?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W7159670352)

以共享时间轴组织持续音视频输入与文本、语音输出，并研究主动回应。

📌 优先阅读理由：阅读持续音视频输入、全双工输出及其部署条件。

全双工模式的硬件要求以官方部署文档为准；模型内存与完整系统内存应分开记录。

机构 / 维护方：Tsinghua University / THUNLP; ModelBest; OpenBMB

<sub>计数快照：2026-11-02</sub>

<a id="e02"></a>

### ⭐ Qwen2.5-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.20215) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni)

[📄 论文](https://arxiv.org/abs/2503.20215) · [💻 仓库](https://github.com/QwenLM/Qwen2.5-Omni) · [![★ 4,092](https://img.shields.io/badge/%E2%98%85%204%2C092-eab308?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni) [![Cite OA 14](https://img.shields.io/badge/Cite%20OA%2014-0284c7?style=flat-square)](https://openalex.org/W4409051416)

音视频、图像和文本输入，联合生成文本与语音；提供 Thinker–Talker 架构参照。

📌 优先阅读理由：建立 Thinker–Talker 架构、数据与分阶段训练的基本参照。

流式语音输出与原生全双工交互分别评估；MNN 支持范围取决于部署模式。

机构 / 维护方：Qwen Team / Alibaba

<sub>计数快照：2026-11-02</sub>

<a id="e03"></a>

### Qwen3-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.17765) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni)

[📄 论文](https://arxiv.org/abs/2509.17765) · [💻 仓库](https://github.com/QwenLM/Qwen3-Omni) · [![★ 4,093](https://img.shields.io/badge/%E2%98%85%204%2C093-eab308?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4415255153)

MoE Thinker–Talker 路线，覆盖多模态理解和实时语音生成。

机构 / 维护方：Qwen Team / Alibaba

<sub>计数快照：2026-11-02</sub>

<a id="e04"></a>

### InteractiveOmni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.13747) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2510.13747)

[📄 论文](https://arxiv.org/abs/2510.13747) · [💻 仓库](https://github.com/OpenSenseNova/InteractiveOmni) · [![★ 9](https://img.shields.io/badge/%E2%98%85%209-eab308?style=flat-square)](https://github.com/OpenSenseNova/InteractiveOmni) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415277372)

以音视频多轮交互为目标，提供 4B 与 8B 模型及多轮评价。

机构 / 维护方：SenseTime Research

<sub>计数快照：2026-11-02</sub>

<a id="e05"></a>

### VITA-1.5

[![NeurIPS 2025](https://img.shields.io/badge/NeurIPS%202025-475569?style=flat-square)](https://arxiv.org/abs/2501.01957) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2501.01957)

[📄 论文](https://arxiv.org/abs/2501.01957) · [💻 仓库](https://github.com/VITA-MLLM/VITA) · [![★ 2,539](https://img.shields.io/badge/%E2%98%85%202%2C539-eab308?style=flat-square)](https://github.com/VITA-MLLM/VITA) [![Cite OA 11](https://img.shields.io/badge/Cite%20OA%2011-0284c7?style=flat-square)](https://openalex.org/W4406093559)

面向实时视觉和语音交互的多模态模型，提供训练与推理流程。

机构 / 维护方：Nanjing University; Xiamen University; CASIA; Tencent Youtu Lab

<sub>计数快照：2026-11-02</sub>

<a id="e06"></a>

### Mini-Omni2

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.11190) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2410.11190)

[📄 论文](https://arxiv.org/abs/2410.11190) · [💻 仓库](https://github.com/gpt-omni/mini-omni2) · [![★ 1,936](https://img.shields.io/badge/%E2%98%85%201%2C936-eab308?style=flat-square)](https://github.com/gpt-omni/mini-omni2) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4403576555)

较早开放图像、语音、文本输入与实时语音输出的实验系统。

机构 / 维护方：Tsinghua University; Inspirai

<sub>计数快照：2026-11-02</sub>

<a id="e07"></a>

### ⭐ Moshi

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.00037) [![Independent Lab](https://img.shields.io/badge/Independent%20Lab-b45309?style=flat-square)](https://arxiv.org/html/2410.00037)

[📄 论文](https://arxiv.org/abs/2410.00037) · [💻 仓库](https://github.com/kyutai-labs/moshi) · [![★ 11,361](https://img.shields.io/badge/%E2%98%85%2011%2C361-eab308?style=flat-square)](https://github.com/kyutai-labs/moshi) [![Cite OA 9](https://img.shields.io/badge/Cite%20OA%209-0284c7?style=flat-square)](https://openalex.org/W4403883071) [![Cite S2 875](https://img.shields.io/badge/Cite%20S2%20875-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/ae4aa7b0c5a327dae63ad20e00b58bcc6176b3b8)

双向语音流与文本协同建模，为连续听说提供开源研究基础。

📌 优先阅读理由：理解双向语音流、文本辅助及低延迟生成。

机构 / 维护方：Kyutai

<sub>计数快照：2026-11-02</sub>

<a id="e08"></a>

### Freeze-Omni

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2411.00774) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2411.00774)

[📄 论文](https://arxiv.org/abs/2411.00774) · [💻 仓库](https://github.com/VITA-MLLM/Freeze-Omni) · [![★ 403](https://img.shields.io/badge/%E2%98%85%20403-eab308?style=flat-square)](https://github.com/VITA-MLLM/Freeze-Omni) [![Cite OA 4](https://img.shields.io/badge/Cite%20OA%204-0284c7?style=flat-square)](https://openalex.org/W4404390495)

冻结语言模型，结合流式语音编码解码和块级状态预测。

机构 / 维护方：Northwestern Polytechnical University; Nanjing University; Tencent Youtu Lab

<sub>计数快照：2026-11-02</sub>

<a id="e80"></a>

### ⭐ Qwen2-Audio

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2407.10759) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2407.10759)

[📄 论文](https://arxiv.org/abs/2407.10759) · [💻 仓库](https://github.com/QwenLM/Qwen2-Audio) · [![★ 2,101](https://img.shields.io/badge/%E2%98%85%202%2C101-eab308?style=flat-square)](https://github.com/QwenLM/Qwen2-Audio) [![Cite OA 8](https://img.shields.io/badge/Cite%20OA%208-0284c7?style=flat-square)](https://openalex.org/W4400717319)

7B 音频语言模型，以音频理解和文本回答为主，覆盖语音、声音与音乐。

📌 优先阅读理由：从音频编码器接入 LLM 入门，建立音频理解基线。

机构 / 维护方：Alibaba / Qwen Team

<sub>计数快照：2026-11-03</sub>

<a id="e81"></a>

### GLM-4-Voice

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2412.02612) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2412.02612)

[📄 论文](https://arxiv.org/abs/2412.02612) · [💻 仓库](https://github.com/zai-org/GLM-4-Voice) · [![★ 3,243](https://img.shields.io/badge/%E2%98%85%203%2C243-eab308?style=flat-square)](https://github.com/zai-org/GLM-4-Voice) [![Cite OA 4](https://img.shields.io/badge/Cite%20OA%204-0284c7?style=flat-square)](https://openalex.org/W4405057125)

9B 语音对话模型，结合离散语音 token、语音文本交错建模与流式解码。

机构 / 维护方：Tsinghua University; Zhipu.AI

<sub>计数快照：2026-11-03</sub>

<a id="e82"></a>

### ⭐ Audio Flamingo 3

[![NeurIPS Spotlight 2025](https://img.shields.io/badge/NeurIPS%20Spotlight%202025-475569?style=flat-square)](https://openreview.net/forum?id=FjByDpDVIO) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2507.08128)

[📄 论文](https://arxiv.org/abs/2507.08128) · [💻 仓库](https://github.com/NVIDIA/audio-flamingo) · [🔗 Training / 训练](https://github.com/NVIDIA/audio-flamingo/tree/audio_flamingo_3) · [![★ 1,219](https://img.shields.io/badge/%E2%98%85%201%2C219-eab308?style=flat-square)](https://github.com/NVIDIA/audio-flamingo) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W6929354950)

7B 音频语言模型，研究语音、声音、音乐理解与音频推理，提供训练、数据和推理入口。

📌 优先阅读理由：结合公开训练分支阅读数据构造与分阶段训练。

模型与数据许可需分别查看；权重采用非商业研究许可。

机构 / 维护方：NVIDIA; University of Maryland

<sub>计数快照：2026-11-03</sub>

<a id="e83"></a>

### Audio Flamingo Next

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.10905) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2604.10905)

[📄 论文](https://arxiv.org/abs/2604.10905) · [🔗 Weights / 权重](https://huggingface.co/nvidia/audio-flamingo-next-hf) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7154207876)

扩展长音频、时间定位、说话人归属和多说话人推理。

已发布的 HF 检查点为音频/文本输入、文本输出；流式语音输出不包含在该检查点中。

机构 / 维护方：NVIDIA; University of Maryland

<sub>计数快照：2026-11-03</sub>

<a id="e84"></a>

### ⭐ MiMo-Audio

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2512.23808) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2512.23808)

[📄 论文](https://arxiv.org/abs/2512.23808) · [💻 仓库](https://github.com/XiaomiMiMo/MiMo-Audio) · [🔗 Training / 训练](https://github.com/XiaomiMiMo/MiMo-Audio-Training) · [![★ 1,088](https://img.shields.io/badge/%E2%98%85%201%2C088-eab308?style=flat-square)](https://github.com/XiaomiMiMo/MiMo-Audio) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W7117988839)

7B 语音基座与指令模型；官方微调工具支持识别、合成、音频理解和口语对话。

📌 优先阅读理由：直接阅读任务数据格式与 SFT 脚本，适合作为现有语音基座适配入口。

机构 / 维护方：Xiaomi MiMo

<sub>计数快照：2026-11-03</sub>

<a id="e85"></a>

### Step-Audio 2

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2507.16632) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2507.16632)

[📄 论文](https://arxiv.org/abs/2507.16632) · [💻 仓库](https://github.com/stepfun-ai/Step-Audio2) · [![★ 1,526](https://img.shields.io/badge/%E2%98%85%201%2C526-eab308?style=flat-square)](https://github.com/stepfun-ai/Step-Audio2) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4415202956)

面向多模态语音交互、音频推理与工具使用；提供 Mini 系列检查点和推理实现。

机构 / 维护方：StepFun

<sub>计数快照：2026-11-03</sub>

<a id="e86"></a>

### ⭐ SALMONN

[![ICLR 2024](https://img.shields.io/badge/ICLR%202024-475569?style=flat-square)](https://github.com/bytedance/SALMONN/tree/salmonn) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2310.13289)

[📄 论文](https://arxiv.org/abs/2310.13289) · [💻 仓库](https://github.com/bytedance/SALMONN) · [🔗 Training / 训练](https://github.com/bytedance/SALMONN/tree/salmonn) · [![★ 1,564](https://img.shields.io/badge/%E2%98%85%201%2C564-eab308?style=flat-square)](https://github.com/bytedance/SALMONN) [![Cite OA 67](https://img.shields.io/badge/Cite%20OA%2067-0284c7?style=flat-square)](https://openalex.org/W4387891768)

融合语音与通用音频编码器，通过适配器与 LLM 连接语音、声音和音乐任务。

📌 优先阅读理由：理解双编码器、适配器与多任务训练如何补足纯 ASR 信息。

机构 / 维护方：Tsinghua University; ByteDance

<sub>计数快照：2026-11-03</sub>

<a id="e87"></a>

### ⭐ SpeechGPT

[![EMNLP Findings 2023](https://img.shields.io/badge/EMNLP%20Findings%202023-475569?style=flat-square)](https://aclanthology.org/2023.findings-emnlp.1055/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2305.11000)

[📄 论文](https://arxiv.org/abs/2305.11000) · [💻 仓库](https://github.com/0nutation/SpeechGPT) · [![★ 1,401](https://img.shields.io/badge/%E2%98%85%201%2C401-eab308?style=flat-square)](https://github.com/0nutation/SpeechGPT) [![Cite OA 189](https://img.shields.io/badge/Cite%20OA%20189-0284c7?style=flat-square)](https://openalex.org/W4389524500)

利用离散语音单元与 SpeechInstruct，将文本 LLM 扩展到语音输入输出。

📌 优先阅读理由：按模态适配、跨模态指令与 chain-of-modality 阶段组织数据和训练。

机构 / 维护方：Fudan University

<sub>计数快照：2026-11-03</sub>

<a id="e88"></a>

### ⭐ BLSP

[![arXiv 2023](https://img.shields.io/badge/arXiv%202023-475569?style=flat-square)](https://arxiv.org/abs/2309.00916) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2309.00916)

[📄 论文](https://arxiv.org/abs/2309.00916) · [💻 仓库](https://github.com/cwang621/blsp) · [![★ 59](https://img.shields.io/badge/%E2%98%85%2059-eab308?style=flat-square)](https://github.com/cwang621/blsp) [![Cite OA 9](https://img.shields.io/badge/Cite%20OA%209-0284c7?style=flat-square)](https://openalex.org/W4386552581)

通过语音和转写的续写行为对齐，训练冻结语音编码器与 LLM 之间的轻量适配器。

📌 优先阅读理由：目标和可训练模块清晰，适合理解低成本的语音接入方式。

机构 / 维护方：CASIA; UCAS; Alibaba DAMO Academy

<sub>计数快照：2026-11-03</sub>

<a id="e89"></a>

### ⭐ LLaMA-Omni2

[![ACL 2025](https://img.shields.io/badge/ACL%202025-475569?style=flat-square)](https://aclanthology.org/2025.acl-long.912/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2505.02625)

[📄 论文](https://arxiv.org/abs/2505.02625) · [💻 仓库](https://github.com/ictnlp/LLaMA-Omni2) · [![★ 281](https://img.shields.io/badge/%E2%98%85%20281-eab308?style=flat-square)](https://github.com/ictnlp/LLaMA-Omni2) [![Cite OA 11](https://img.shields.io/badge/Cite%20OA%2011-0284c7?style=flat-square)](https://openalex.org/W4412944968)

在 Qwen2.5 上构建双语语音对话与流式语音生成，公开多种模型规模与推理代码。

📌 优先阅读理由：提供 0.5B–3B 版本，用于分析语音指令数据、对齐和流式输出。

代码与模型使用不同许可；模型限研究用途。

机构 / 维护方：Institute of Computing Technology, CAS; UCAS

<sub>计数快照：2026-11-03</sub>

<a id="e90"></a>

### PersonaPlex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.06053) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2602.06053)

[📄 论文](https://arxiv.org/abs/2602.06053) · [💻 仓库](https://github.com/NVIDIA/personaplex) · [![★ 12,018](https://img.shields.io/badge/%E2%98%85%2012%2C018-eab308?style=flat-square)](https://github.com/NVIDIA/personaplex) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W7128377012)

基于 Moshi 的 7B 全双工对话模型，通过声音与文本提示控制说话人和角色。

官方仓库提供权重与推理入口；训练实践可结合 DuplexGen 阅读。

机构 / 维护方：NVIDIA

<sub>计数快照：2026-11-03</sub>

<a id="voice"></a>

## 💬 Voice Agent 与交互系统

<a id="e29"></a>

### ⭐ FireRedChat

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.06502) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/abs/2509.06502)

[📄 论文](https://arxiv.org/abs/2509.06502) · [💻 仓库](https://github.com/FireRedTeam/FireRedChat) · [![★ 597](https://img.shields.io/badge/%E2%98%85%20597-eab308?style=flat-square)](https://github.com/FireRedTeam/FireRedChat) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4414757003)

全双工语音系统：轮次控制、主说话人打断、对话管理和工具调用。

📌 优先阅读理由：以模块化实现理解打断控制、对话状态和工具调用。

机构 / 维护方：Xiaohongshu / FireRed Team

<sub>计数快照：2026-11-03</sub>

<a id="e30"></a>

### Qwen Audio Agent

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent)

[💻 仓库](https://github.com/QwenAudio/qwen-audio-agent) · [![★ 3,112](https://img.shields.io/badge/%E2%98%85%203%2C112-eab308?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent)

语音前端与后台 Agent 分工，提供异步任务协作和取消机制的工程入口。

机构 / 维护方：Qwen / Alibaba

<sub>计数快照：2026-11-03</sub>

<a id="e09"></a>

### DuplexSLA

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2605.20755) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2605.20755)

[📄 论文](https://arxiv.org/abs/2605.20755) · [💻 仓库](https://github.com/hyzhang24/DuplexSLA) · [![★ 147](https://img.shields.io/badge/%E2%98%85%20147-eab308?style=flat-square)](https://github.com/hyzhang24/DuplexSLA) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7161968102)

在共同时间线上输出语音及结构化 action 通道，研究交谈中的规划与工具调用。

action 通道用于结构化规划与工具操作；关节控制由下游执行系统实现。

机构 / 维护方：StepFun; Peking University; Nanyang Technological University; Shanghai Jiao Tong University; University of New South Wales; Imperial College London

<sub>计数快照：2026-11-02</sub>

<a id="e31"></a>

### Jarvis

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.23804) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2610.23804)

[📄 论文](https://arxiv.org/abs/2610.23804) · [💻 仓库](https://github.com/JensenYX/Jarvis) · [![★ 18](https://img.shields.io/badge/%E2%98%85%2018-eab308?style=flat-square)](https://github.com/JensenYX/Jarvis) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7222979632)

在交互前端和后台任务之间训练协调器，管理任务切换、状态和过期结果。

研究对象为软件 Agent 协调；真实机器人任务增益需独立验证。

机构 / 维护方：CUHK Shenzhen; Tencent Hunyuan; Amphion Technology

<sub>计数快照：2026-11-03</sub>

<a id="e36"></a>

### TEN Framework

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/TEN-framework/ten-framework) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/TEN-framework/ten-framework)

[💻 仓库](https://github.com/TEN-framework/ten-framework) · [![★ 11,219](https://img.shields.io/badge/%E2%98%85%2011%2C219-eab308?style=flat-square)](https://github.com/TEN-framework/ten-framework)

实时音视频 Agent 框架，提供可组合扩展与多模态应用示例。

LICENSE 包含 Apache-2.0 之外的附加使用条件，涉及终端设备托管等；部署前阅读官方 LICENSE。

机构 / 维护方：Agora; Contributor community

<sub>计数快照：2026-11-03</sub>

<a id="e37"></a>

### ⭐ VoxMind

[![ACL 2026](https://img.shields.io/badge/ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.acl-long.459/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2604.15710)

[📄 论文](https://arxiv.org/abs/2604.15710) · [💻 仓库](https://github.com/MM-Speech/VoxMind) · [![★ 46](https://img.shields.io/badge/%E2%98%85%2046-eab308?style=flat-square)](https://github.com/MM-Speech/VoxMind) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7155019877)

用 AgentChat 数据、Think-before-Speak 与动态工具检索学习语音 Agent 的推理—调用—反馈闭环。

📌 优先阅读理由：AgentChat 数据格式、训练目标与工具实验共同展示语音交互如何参与任务执行。

异步工具管理与同时听说能力对应不同实验，结果按各自任务与交互条件解释。

机构 / 维护方：Zhejiang University; China University of Petroleum–Beijing at Karamay; Xiamen University

<sub>计数快照：2026-11-03</sub>

<a id="e38"></a>

### ⭐ F-Actor

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.242/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2601.11329)

[📄 论文](https://arxiv.org/abs/2601.11329) · [💻 仓库](https://github.com/MaikeZuefle/f-actor) · [![★ 33](https://img.shields.io/badge/%E2%98%85%2033-eab308?style=flat-square)](https://github.com/MaikeZuefle/f-actor) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7124734178)

通过指令控制音色、话题、反馈、打断和主动开场；冻结音频编码器，采用单阶段训练。

📌 优先阅读理由：将打断、反馈等交互行为表示为可监督、可控制的指令。

机构 / 维护方：Karlsruhe Institute of Technology; University of Edinburgh; NatWest

<sub>计数快照：2026-11-03</sub>

<a id="e39"></a>

### ⭐ SOMMELIER

[![ACL Industry Track 2026](https://img.shields.io/badge/ACL%20Industry%20Track%202026-475569?style=flat-square)](https://aclanthology.org/2026.acl-industry.18/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2603.25750)

[📄 论文](https://arxiv.org/abs/2603.25750) · [💻 仓库](https://github.com/Anonymous-2001-j/Sommelier) · [![★ 0](https://img.shields.io/badge/%E2%98%85%200-eab308?style=flat-square)](https://github.com/Anonymous-2001-j/Sommelier) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7143443580)

把真实多人录音转为保留时间关系的双声道训练数据，连接分离、说话人分段、转写和质量筛选。

📌 优先阅读理由：展示真实录音转化为全双工训练数据时的时间对齐、重叠处理与筛选。

机构 / 维护方：KAIST; NAVER Cloud

<sub>计数快照：2026-11-03</sub>

<a id="e40"></a>

### CF-Duplex / XA-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2605.10199) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2605.10199)

[📄 论文](https://arxiv.org/abs/2605.10199) · [🔗 项目](https://light1726.github.io/duplex-demo/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7160904488)

对比受控融合与交叉注意力，把用户语音流接入正在生成的模型，分析同时听说的架构选择。

机构 / 维护方：The Chinese University of Hong Kong; Tsinghua University; SenseTime

<sub>计数快照：2026-11-03</sub>

<a id="e41"></a>

### ⭐ DuplexGen

[![EMNLP 2026](https://img.shields.io/badge/EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.emnlp-main.2618/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2607.26178)

[📄 论文](https://arxiv.org/abs/2607.26178) · [💻 仓库](https://github.com/duplexgen/duplexgen-code) · [🔗 项目](https://duplexgen.github.io/) · [![★ 29](https://img.shields.io/badge/%E2%98%85%2029-eab308?style=flat-square)](https://github.com/duplexgen/duplexgen-code) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7171803236)

用少量人类偏好校准话轮行为预测，再合成适配不同场景的人机对话，用于全双工模型微调。

📌 优先阅读理由：说明目标交互行为与数据构造的关系，以及人类偏好在合成和微调中的作用。

机构 / 维护方：University of Illinois Urbana-Champaign; Seoul National University; University of California Berkeley; Georgia Institute of Technology; Columbia University

<sub>计数快照：2026-11-03</sub>

<a id="e42"></a>

### BayLing-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.14528) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2606.14528)

[📄 论文](https://arxiv.org/abs/2606.14528) · [💻 仓库](https://github.com/BayLing-Models/BayLing-Duplex) · [![★ 96](https://img.shields.io/badge/%E2%98%85%2096-eab308?style=flat-square)](https://github.com/BayLing-Models/BayLing-Duplex) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7164829614)

以单个自回归 LLM 和少量状态 token 联合建模听、说、停，通过 SFT 与 DPO 学习交互。

机构 / 维护方：Institute of Computing Technology, Chinese Academy of Sciences; University of Chinese Academy of Sciences

<sub>计数快照：2026-11-03</sub>

<a id="e43"></a>

### MultiTalk / MultiTalkBench

[![NeurIPS 2026 · 作者标注](https://img.shields.io/badge/NeurIPS%202026%20%C2%B7%20%E4%BD%9C%E8%80%85%E6%A0%87%E6%B3%A8-475569?style=flat-square)](https://arxiv.org/abs/2609.36903) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.36903)

[📄 论文](https://arxiv.org/abs/2609.36903) · [🔗 预训练数据](https://huggingface.co/datasets/MultiTalk/MultiTalkPT) · [🔗 微调数据](https://huggingface.co/datasets/MultiTalk/MultiTalkFT) · [🔗 Benchmark](https://huggingface.co/datasets/MultiTalk/MultiTalkBench) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214898838)

扩展到长时、多方、双语全双工对话；提供预训练、微调数据和来自真实录音的 MultiTalkBench。

NeurIPS 2026 依据作者在 arXiv 的标注；MultiTalkBench 与模型训练数据应分别使用。

机构 / 维护方：The Chinese University of Hong Kong; Centre for Perceptual and Interactive Intelligence (InnoHK)

<sub>计数快照：2026-11-03</sub>

<a id="e44"></a>

### ⭐ Self-Listening / LoopSpeech

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.05592) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.05592)

[📄 论文](https://arxiv.org/abs/2609.05592) · [💻 仓库](https://github.com/FreedomIntelligence/LoopSpeech) · [![★ 8](https://img.shields.io/badge/%E2%98%85%208-eab308?style=flat-square)](https://github.com/FreedomIntelligence/LoopSpeech) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212059771)

把实际已播放的语音纳入历史，区分“计划说出”与“用户已经听到”，研究打断后的内容连续性。

📌 优先阅读理由：以已播放历史为条件，分析打断后的对话状态与后续响应。

机构 / 维护方：Shenzhen Loop Area Institute; The Chinese University of Hong Kong, Shenzhen

<sub>计数快照：2026-11-03</sub>

<a id="e45"></a>

### D2: Dialogue-to-Duplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.17124) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2610.17124)

[📄 论文](https://arxiv.org/abs/2610.17124) · [💻 仓库](https://github.com/penguinfish1688/D2-dialogue-to-duplex) · [🔗 项目](https://d2-duplex-demo.github.io/) · [![★ 11](https://img.shields.io/badge/%E2%98%85%2011-eab308?style=flat-square)](https://github.com/penguinfish1688/D2-dialogue-to-duplex) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221777691)

复用半双工语音模型进行全双工适配，分析音频块间隔对质量、时延和计算量的影响。

仓库当前提供 Qwen3-Omni 80 ms 配置检查点；论文中的声学时延不包含全部计算与服务开销。

机构 / 维护方：MIT CSAIL; MIT–IBM Watson AI Lab

<sub>计数快照：2026-11-03</sub>

<a id="e46"></a>

### TASTE2

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.08956) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.08956)

[📄 论文](https://arxiv.org/abs/2609.08956) · [💻 仓库](https://github.com/GitYCC/TASTE-SpokenLM-2) · [🔗 项目](https://gitycc.github.io/TASTE2-Homepage/) · [🔗 语音应用](https://github.com/GitYCC/TASTE-Voice-Bot) · [![★ 2](https://img.shields.io/badge/%E2%98%85%202-eab308?style=flat-square)](https://github.com/GitYCC/TASTE-SpokenLM-2) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212080144)

以文本对齐的语音建模和部署协同组织全双工交互，补充副语言信号与实时运行的设计。

机构 / 维护方：MediaTek Research; National Taiwan University; NVIDIA AI Technology Center

<sub>计数快照：2026-11-03</sub>

<a id="e47"></a>

### IRAF

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.06559) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2606.06559)

[📄 论文](https://arxiv.org/abs/2606.06559) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7163910264)

按帧估计目标说话人可靠性并自适应融合音频，研究干扰说话人条件下的全双工鲁棒性。

机构 / 维护方：The Chinese University of Hong Kong; Huawei Leibniz Research Center; Nanyang Technological University

<sub>计数快照：2026-11-03</sub>

<a id="e48"></a>

### ⭐ MoshiRAG

[![ICML 2026 · 作者标注](https://img.shields.io/badge/ICML%202026%20%C2%B7%20%E4%BD%9C%E8%80%85%E6%A0%87%E6%B3%A8-475569?style=flat-square)](https://arxiv.org/abs/2604.12928) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.12928)

[📄 论文](https://arxiv.org/abs/2604.12928) · [💻 仓库](https://github.com/kyutai-labs/moshi-rag) · [![★ 195](https://img.shields.io/badge/%E2%98%85%20195-eab308?style=flat-square)](https://github.com/kyutai-labs/moshi-rag) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7154507545)

在全双工对话中异步触发检索并注入知识，观察检索耗时与持续对话如何协调。

📌 优先阅读理由：学习持续语音交互与耗时检索之间的接口、触发机制及结果注入。

ICML 2026 接收状态依据作者在 arXiv 的说明；检索任务范围不同于通用工具执行。

机构 / 维护方：Toyota Technological Institute at Chicago; Kyutai; Gradium

<sub>计数快照：2026-11-03</sub>

<a id="e49"></a>

### Frontend–Backend Tool Calling

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.19334) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.19334)

[📄 论文](https://arxiv.org/abs/2609.19334) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213611583)

将实时语音前端与文本工具后端分离，以流式转写、工具执行和 prefill-and-repeat 结果回传连接两者。

当前发表状态为预印本；作者列出的 ICASSP 2027 为投稿计划。

机构 / 维护方：NVIDIA

<sub>计数快照：2026-11-03</sub>

<a id="e50"></a>

### DiffuPlex · Rolling Masked Diffusion

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.12214) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2610.12214)

[📄 论文](https://arxiv.org/abs/2610.12214) · [🔗 项目](https://diffuplex.github.io/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221088445)

用滚动掩码扩散预测交互帧，在保留交互质量的同时减少主干模型调用。

与 NVIDIA 的 Discrete Diffusion 论文为不同工作，项目同名时按完整标题区分。

机构 / 维护方：University of Seoul

<sub>计数快照：2026-11-03</sub>

<a id="e51"></a>

### Diffuplex · Discrete Diffusion

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.17780) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2610.17780)

[📄 论文](https://arxiv.org/abs/2610.17780) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7221757954)

以自回归过程决定何时说话，以离散扩散并行生成内容，研究全双工生成效率。

论文预告代码与检查点发布；本条目尚未核实可下载版本。

机构 / 维护方：NVIDIA

<sub>计数快照：2026-11-03</sub>

<a id="e52"></a>

### Voice-Light

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.20995)

[📄 论文](https://arxiv.org/abs/2609.20995) · [💻 仓库](https://github.com/BertilBraun/Voice-Light) · [![★ 10](https://img.shields.io/badge/%E2%98%85%2010-eab308?style=flat-square)](https://github.com/BertilBraun/Voice-Light) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213934747)

级联系统中的因果轮次控制、推测生成和可撤销播放；用播放确认更新持久对话历史。

在线实验包含三个操作员运行、共 36 轮，可作为工程案例；更大规模用户效果需进一步评测。作者机构归属待核实。

机构 / 维护方：Bertil Braun

<sub>计数快照：2026-11-03</sub>

<a id="e53"></a>

### AdaptDuplex

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.29217) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.29217)

[📄 论文](https://arxiv.org/abs/2609.29217) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214079271)

结合自适应感知窗口、非阻塞认知整合与外部推理，研究动态全双工对话及分阶段后训练。

已核实资源为技术论文；模型权重和完整训练流程的开放状态待核实。

机构 / 维护方：Zuoyebang Education Technology

<sub>计数快照：2026-11-03</sub>

<a id="e54"></a>

### Realtime-Venus

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.13814) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.13814)

[📄 论文](https://arxiv.org/abs/2609.13814) · [💻 仓库](https://github.com/inclusionAI/Realtime-Venus) · [![★ 252](https://img.shields.io/badge/%E2%98%85%20252-eab308?style=flat-square)](https://github.com/inclusionAI/Realtime-Venus) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213284145)

实时交互层异步委托后台任务，结果返回后继续对话，连接多模态输入、训练策略与运行时。

机构 / 维护方：Ant Group; Tsinghua University

<sub>计数快照：2026-11-03</sub>

<a id="e55"></a>

### NemotronLabs VoiceChat

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.21967) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.21967)

[📄 论文](https://arxiv.org/abs/2609.21967) · [💻 仓库](https://github.com/NVIDIA-NeMo/Speech/tree/nemotron-labs-voicechat) · [🔗 模型](https://huggingface.co/nvidia/NVIDIA-NemotronLabs-VoiceChat-11B) · [![★ 18,685](https://img.shields.io/badge/%E2%98%85%2018%2C685-eab308?style=flat-square)](https://github.com/NVIDIA-NeMo/Speech/tree/nemotron-labs-voicechat) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213936344)

开放的全双工语音模型，以独立工具通道连接动作调用，并支持可打断语音输出。

代码入口为 NVIDIA-NeMo/Speech 的 nemotron-labs-voicechat 分支；Star 计整个 Speech 仓库。

机构 / 维护方：NVIDIA

<sub>计数快照：2026-11-03</sub>

<a id="e56"></a>

### StepAudio 3 Realtime

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.14005) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.14005)

[📄 论文](https://arxiv.org/abs/2609.14005) · [🔗 项目](https://stepaudiollm.github.io/step-audio-3-realtime/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7213371127)

围绕 listen、converse、think、act 组织实时语音交互，结合 Think-While-Speaking 与异步工具执行。

已列出本版本论文与展示；完整代码的开放状态按本版本单独核实。

机构 / 维护方：StepFun

<sub>计数快照：2026-11-03</sub>

<a id="e57"></a>

### Qwen-Audio-3.1-Realtime

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.25176) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.25176)

[📄 论文](https://arxiv.org/abs/2609.25176) · [💻 仓库](https://github.com/QwenAudio/qwen-audio-agent) · [![★ 3,112](https://img.shields.io/badge/%E2%98%85%203%2C112-eab308?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214103824)

在可执行环境中进行 Agent GRPO，结合多模态策略蒸馏，研究任务可靠性与交互行为后训练。

qwen-audio-agent 提供配套运行时；模型权重和训练代码的开放范围分别记录。

机构 / 维护方：Alibaba / Qwen

<sub>计数快照：2026-11-03</sub>

<a id="e58"></a>

### ⭐ DuplexOmni

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.09186) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2606.09186)

[📄 论文](https://arxiv.org/abs/2606.09186) · [💻 仓库](https://github.com/MuyeHuang/DuplexOmni) · [![★ 145](https://img.shields.io/badge/%E2%98%85%20145-eab308?style=flat-square)](https://github.com/MuyeHuang/DuplexOmni) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7164028919)

实时交互层与异步思考层协同，配合 Writer–Director 数据合成组织边听、边看、边想、边说。

📌 优先阅读理由：阅读实时层、异步思考层与合成数据之间的对应关系，作为端到端系统设计参照。

机构 / 维护方：Xi’an Jiaotong University; Peking University; Meituan

<sub>计数快照：2026-11-03</sub>

<a id="embodied"></a>

## 🤖 具身交互与语言反馈

<a id="e13"></a>

### Interactive Language / Language Table

[![IEEE RA-L 2024](https://img.shields.io/badge/IEEE%20RA--L%202024-475569?style=flat-square)](https://doi.org/10.1109/LRA.2023.3295255) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2210.06407)

[📄 论文](https://arxiv.org/abs/2210.06407) · [💻 仓库](https://github.com/google-research/language-table) · [![★ 367](https://img.shields.io/badge/%E2%98%85%20367-eab308?style=flat-square)](https://github.com/google-research/language-table) [![Cite OA 113](https://img.shields.io/badge/Cite%20OA%20113-0284c7?style=flat-square)](https://openalex.org/W4391759936)

通过实时语言指导视觉运动策略，允许人逐步调整机器人完成目标。

机构 / 维护方：Robotics at Google

<sub>计数快照：2026-11-02</sub>

<a id="e25"></a>

### ⭐ Hi Robot

[![ICML 2025](https://img.shields.io/badge/ICML%202025-475569?style=flat-square)](https://proceedings.mlr.press/v267/shi25d.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.19417)

[📄 论文](https://arxiv.org/abs/2502.19417) · [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4416045178) [![Cite S2 319](https://img.shields.io/badge/Cite%20S2%20319-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/69afd10d387423a03617d461c3f47a5f3033cc54)

高层视觉语言推理将复杂指令和执行中反馈转为下一步任务，低层 VLA 执行具体动作。

📌 优先阅读理由：以高层语言推理配合低层动作策略为例，说明执行反馈如何改变任务分解。

语言反馈通过高层规划传递至动作策略；原始语音特征的贡献需单独消融。

机构 / 维护方：Physical Intelligence; Stanford University; UC Berkeley

<sub>计数快照：2026-11-02</sub>

<a id="e26"></a>

### Yell At Your Robot / YAY Robot

[![RSS 2024](https://img.shields.io/badge/RSS%202024-475569?style=flat-square)](https://roboticsproceedings.org/rss20/p025.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2403.12910)

[📄 论文](https://arxiv.org/abs/2403.12910) · [💻 仓库](https://github.com/yay-robot/yay_robot) · [![★ 166](https://img.shields.io/badge/%E2%98%85%20166-eab308?style=flat-square)](https://github.com/yay-robot/yay_robot) [![Cite OA 47](https://img.shields.io/badge/Cite%20OA%2047-0284c7?style=flat-square)](https://openalex.org/W4402354098) [![Cite S2 179](https://img.shields.io/badge/Cite%20S2%20179-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/f213d0cb84b6afca9a4d5722081ba3052e7e89bc)

人在机器人执行长任务时给出口头修正，系统立即利用纠正，并将这些反馈用于后续高层策略训练。

阅读重点：理解执行中口头纠正如何用于当前控制与后续学习。

口头纠正主要通过语言表示进入控制与学习。

机构 / 维护方：Stanford University; UC Berkeley

<sub>计数快照：2026-11-02</sub>

<a id="e24"></a>

### ⭐ VLAS

[![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2025/hash/804a1a9de5787e3597b4bb64e1a48ec3-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.13508)

[📄 论文](https://arxiv.org/abs/2502.13508) · [💻 仓库](https://github.com/whichwhichgone/VLAS) · [![★ 50](https://img.shields.io/badge/%E2%98%85%2050-eab308?style=flat-square)](https://github.com/whichwhichgone/VLAS) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4407764312) [![Cite S2 68](https://img.shields.io/badge/Cite%20S2%2068-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/f6075ce4db8dcc359c3ac97b85f2644dc5cadda6)

将原始语音接入视觉动作策略，并用声纹检索个体相关信息，执行带有个人偏好的操作。

📌 优先阅读理由：以视觉动作模型接入语音编码器为例，分析语音指令适配与声纹条件操作。

评测重点为语音指令与声纹个性化操作；全双工说做交互需单独评价。

机构 / 维护方：Westlake University; Zhejiang University; Xi’an Jiaotong University

<sub>计数快照：2026-11-02</sub>

<a id="e21"></a>

### RoboOmni (OpenMOSS)

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/33610fba262d7b6fed0810b89f55e147-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2510.23763)

[📄 论文](https://arxiv.org/abs/2510.23763) · [💻 仓库](https://github.com/OpenMOSS/RoboOmni) · [![★ 124](https://img.shields.io/badge/%E2%98%85%20124-eab308?style=flat-square)](https://github.com/OpenMOSS/RoboOmni) [![Cite S2 12](https://img.shields.io/badge/Cite%20S2%2012-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/37cd1e4cbfbfdadc2a898a703ab46bc0e1c83dd3)

从对话、环境声音和视觉线索推断意图，经确认后生成操作动作，研究隐式情境指令下的主动协助。

阅读重点：了解环境声音与隐式意图如何进入操作任务。

本条目对应 OpenMOSS 团队的 RoboOmni。

机构 / 维护方：Fudan University; Shanghai Innovation Institute; National University of Singapore

<sub>计数快照：2026-11-02</sub>

<a id="e22"></a>

### ⭐ ELLSA

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/6d8af672c0bca7a4be6f0cd0d229c05c-Abstract-Conference.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.16756)

[📄 论文](https://arxiv.org/abs/2510.16756) · [💻 仓库](https://github.com/bytedance/SALMONN) · [![★ 1,564](https://img.shields.io/badge/%E2%98%85%201%2C564-eab308?style=flat-square)](https://github.com/bytedance/SALMONN) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415958597) [![Cite S2 7](https://img.shields.io/badge/Cite%20S2%207-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/3af611e47c30a439f8acad312f16cf7837ddbce7)

在统一架构中处理视觉、文本、语音和动作，支持边说边做、动作打断与基于场景的问答。

📌 优先阅读理由：以语音与动作专家的联合训练为例，分析同时说做、动作打断及分阶段适配。

Star 数对应整个 SALMONN 仓库；ELLSA 的权重与训练资源见其专用分支和模型页面。

机构 / 维护方：Tsinghua University; ByteDance

<sub>计数快照：2026-11-02</sub>

<a id="e23"></a>

### VITA-E

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.21817) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.21817)

[📄 论文](https://arxiv.org/abs/2510.21817) · [💻 仓库](https://github.com/Tencent/VITA) · [![★ 166](https://img.shields.io/badge/%E2%98%85%20166-eab308?style=flat-square)](https://github.com/Tencent/VITA) [![Cite S2 2](https://img.shields.io/badge/Cite%20S2%202-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/62d932e380f9ec7de5d43c17bc933a05887b0007)

以并行的活动/监听模型和控制 token 调度语音与动作，支持中断、任务切换和边说边做。

机构 / 维护方：Nanjing University; CASIA; Tencent Youtu Lab; Fourier Intelligence

<sub>计数快照：2026-11-02</sub>

<a id="e95"></a>

### NaVILA

[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://navila-bot.github.io/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2412.04453)

[📄 论文](https://arxiv.org/abs/2412.04453) · [💻 仓库](https://github.com/AnjieCheng/NaVILA) · [🔗 Locomotion / 运动策略](https://github.com/yang-zj1026/legged-loco) · [![★ 731](https://img.shields.io/badge/%E2%98%85%20731-eab308?style=flat-square)](https://github.com/AnjieCheng/NaVILA) [![Cite OA 55](https://img.shields.io/badge/Cite%20OA%2055-0284c7?style=flat-square)](https://openalex.org/W4414050442)

高层 VLA 输出空间语言指令，低层视觉运动策略执行导航，提供 Go2 等平台实验。

阅读重点：说明语言导航目标、高低层策略接口与执行反馈之间的关系。

机构 / 维护方：UC San Diego; University of Southern California; NVIDIA

<sub>计数快照：2026-11-03</sub>

<a id="e11"></a>

### Reachy Mini Conversation App

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)

[💻 仓库](https://github.com/pollen-robotics/reachy_mini_conversation_app) · [![★ 348](https://img.shields.io/badge/%E2%98%85%20348-eab308?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)

把实时语音、摄像头工具和机器人运动接入同一对话应用。

主要覆盖头部、天线等身体表达与视觉工具调用。

机构 / 维护方：Pollen Robotics / Hugging Face

<sub>计数快照：2026-11-02</sub>

<a id="e12"></a>

### EMAGE / BEAT2

[![CVPR 2024](https://img.shields.io/badge/CVPR%202024-475569?style=flat-square)](https://pantomatrix.github.io/EMAGE/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2401.00374)

[📄 论文](https://arxiv.org/abs/2401.00374) · [💻 仓库](https://github.com/haiyangliu0/character-policy) · [![★ 1,312](https://img.shields.io/badge/%E2%98%85%201%2C312-eab308?style=flat-square)](https://github.com/haiyangliu0/character-policy) [![Cite OA 95](https://img.shields.io/badge/Cite%20OA%2095-0284c7?style=flat-square)](https://openalex.org/W4402727140)

从语音及文本生成全身与面部协同动作，连接 co-speech gesture 与表达数据。

研究范围为共语手势与角色表达；真实机器人操作需独立评测。

机构 / 维护方：The University of Tokyo; Keio University; Max Planck Institute for Intelligent Systems; JAIST; Tsinghua University

<sub>计数快照：2026-11-02</sub>

<a id="robotics"></a>

## 🦾 动作、数据与部署

<a id="e19"></a>

### LeRobot

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.22818) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2602.22818)

[📄 论文](https://arxiv.org/abs/2602.22818) · [💻 仓库](https://github.com/huggingface/lerobot) · [![★ 28,653](https://img.shields.io/badge/%E2%98%85%2028%2C653-eab308?style=flat-square)](https://github.com/huggingface/lerobot) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7131860508)

机器人数据、策略训练、硬件控制与评测的开源工具入口。

阅读重点：覆盖示范采集、数据检查、策略训练与真机执行的完整流程。

机构 / 维护方：Hugging Face; University of Oxford

<sub>计数快照：2026-11-02 / 2026-11-03</sub>

<a id="e32"></a>

### ACT / ALOHA

[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://www.roboticsproceedings.org/rss19/p016.pdf) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2304.13705)

[📄 论文](https://arxiv.org/abs/2304.13705) · [💻 仓库](https://github.com/tonyzhaozh/act) · [![★ 2,318](https://img.shields.io/badge/%E2%98%85%202%2C318-eab308?style=flat-square)](https://github.com/tonyzhaozh/act) [![Cite OA 674](https://img.shields.io/badge/Cite%20OA%20674-0284c7?style=flat-square)](https://openalex.org/W4385430674)

用遥操作示范学习动作块，建立视觉运动模仿学习基线。

阅读重点：通过观测、动作示范与动作块预测介绍模仿学习。

标准 ACT 采用观测条件动作预测；多目标任务可通过技能选择器或额外目标条件扩展。

机构 / 维护方：Stanford University; Meta; UC Berkeley

<sub>计数快照：2026-11-03</sub>

<a id="e33"></a>

### Diffusion Policy

[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![IJRR 2024](https://img.shields.io/badge/IJRR%202024-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2303.04137)

[📄 论文](https://arxiv.org/abs/2303.04137v4) · [💻 仓库](https://github.com/real-stanford/diffusion_policy) · [![★ 4,698](https://img.shields.io/badge/%E2%98%85%204%2C698-eab308?style=flat-square)](https://github.com/real-stanford/diffusion_policy) [![Cite OA 12](https://img.shields.io/badge/Cite%20OA%2012-0284c7?style=flat-square)](https://openalex.org/W4323651335)

将条件动作分布建模为去噪过程，生成连续动作序列。

论文链接为 RSS 2023 版本；IJRR 2024 为扩展版。引文数量绑定所链接的数据库记录。

机构 / 维护方：Columbia University; Toyota Research Institute; MIT

<sub>计数快照：2026-11-03</sub>

<a id="e34"></a>

### SmolVLA

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2506.01844) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2506.01844)

[📄 论文](https://arxiv.org/abs/2506.01844) · [💻 仓库](https://github.com/huggingface/lerobot) · [![★ 28,653](https://img.shields.io/badge/%E2%98%85%2028%2C653-eab308?style=flat-square)](https://github.com/huggingface/lerobot) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4414898213)

450M 视觉语言动作模型，以图像、机器人状态与文本指令为条件生成动作块。

阅读重点：提供预训练 VLA 适配机器人数据的官方教程与实现。

策略以文本指令为条件。Star 数对应整个 LeRobot 仓库；整机实时性需结合感知与控制链路测量。

机构 / 维护方：Hugging Face; Sorbonne University; valeo.ai; ENS Paris-Saclay

<sub>计数快照：2026-11-03</sub>

<a id="e20"></a>

### OpenVLA

[![CoRL 2024](https://img.shields.io/badge/CoRL%202024-475569?style=flat-square)](https://proceedings.mlr.press/v270/kim25c.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2406.09246)

[📄 论文](https://arxiv.org/abs/2406.09246) · [💻 仓库](https://github.com/openvla/openvla) · [![★ 7,250](https://img.shields.io/badge/%E2%98%85%207%2C250-eab308?style=flat-square)](https://github.com/openvla/openvla) [![Cite OA 62](https://img.shields.io/badge/Cite%20OA%2062-0284c7?style=flat-square)](https://openalex.org/W4399695759)

视觉与语言条件下的机器人动作模型，作为交互层连接动作策略的基础参照。

视觉、语言到动作的基础；原生语音与实时打断需要额外系统设计。

机构 / 维护方：Stanford University; UC Berkeley; MIT; Toyota Research Institute; Google DeepMind; Physical Intelligence

<sub>计数快照：2026-11-02</sub>

<a id="e91"></a>

### ⭐ openpi / π0 · π0.5

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2504.16054) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2504.16054)

[📄 论文](https://arxiv.org/abs/2504.16054) · [💻 仓库](https://github.com/Physical-Intelligence/openpi) · [🔗 π0 paper](https://arxiv.org/abs/2410.24164) · [🔗 π0.5 blog](https://www.physicalintelligence.company/blog/pi05) · [![★ 14,510](https://img.shields.io/badge/%E2%98%85%2014%2C510-eab308?style=flat-square)](https://github.com/Physical-Intelligence/openpi) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4414674749)

开放 π0、π0-FAST 与 π0.5 的权重、推理和适配代码，连接 VLM、连续动作与多机器人数据。

📌 优先阅读理由：π0 介绍 VLM 与动作专家的连接；π0.5 补充多来源联合训练与新环境泛化。

本条目的引文计数对应 π0.5，Star 数对应 openpi 仓库。π0 原论文见附加链接；LoRA 使用 JAX 实现，PyTorch 路径的功能范围见官方文档。

机构 / 维护方：Physical Intelligence

<sub>计数快照：2026-11-03</sub>

<a id="e92"></a>

### Isaac GR00T N1.7

[![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T)

[💻 仓库](https://github.com/NVIDIA/Isaac-GR00T) · [🔗 N1 background paper](https://arxiv.org/abs/2503.14734) · [![★ 8,308](https://img.shields.io/badge/%E2%98%85%208%2C308-eab308?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T)

3B 视觉语言动作基座，提供预训练权重、新本体数据适配和微调流程。

阅读重点：阅读本体配置、动作空间与自有数据微调，比较工业基座的适配成本。

仓库当前版本为 N1.7；背景论文描述早期 N1，训练配置和结果需按版本读取。

机构 / 维护方：NVIDIA

<sub>计数快照：2026-11-03</sub>

<a id="e93"></a>

### OpenVLA-OFT

[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://roboticsproceedings.org/rss21/p017.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.19645)

[📄 论文](https://arxiv.org/abs/2502.19645) · [💻 仓库](https://github.com/moojink/openvla-oft) · [🔗 Project / 项目](https://openvla-oft.github.io/) · [![★ 1,440](https://img.shields.io/badge/%E2%98%85%201%2C440-eab308?style=flat-square)](https://github.com/moojink/openvla-oft) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W6948104436)

基于 OpenVLA，比较并行解码、动作块、连续动作和 L1 目标，并用 FiLM 改善语言控制。

阅读重点：基座明确、训练开放、算力说明具体；适合研究基座上的适配方法。

机构 / 维护方：Stanford University

<sub>计数快照：2026-11-03</sub>

<a id="e94"></a>

### SimpleVLA-RL

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/cbfbcb4da14235bd69b134070898ae9d-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2509.09674)

[📄 论文](https://arxiv.org/abs/2509.09674) · [💻 仓库](https://github.com/PRIME-RL/SimpleVLA-RL) · [![★ 1,903](https://img.shields.io/badge/%E2%98%85%201%2C903-eab308?style=flat-square)](https://github.com/PRIME-RL/SimpleVLA-RL) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W7081569152)

在 OpenVLA-OFT 等 VLA 上进行强化学习，提供 LIBERO / RoboTwin 的训练、rollout 与评测流程。

阅读重点：作为 SFT 之后的进阶阅读，分析环境奖励、rollout 成本与泛化评测。

机构 / 维护方：Tsinghua University; Shanghai AI Lab; Shanghai Jiao Tong University; Peking University; University of Hong Kong

<sub>计数快照：2026-11-03</sub>

<a id="e97"></a>

### Unitree SDK2 / MuJoCo

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/unitreerobotics/unitree_sdk2) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/unitreerobotics/unitree_sdk2)

[💻 仓库](https://github.com/unitreerobotics/unitree_sdk2) · [🔗 Python SDK](https://github.com/unitreerobotics/unitree_sdk2_python) · [🔗 MuJoCo](https://github.com/unitreerobotics/unitree_mujoco) · [![★ 1,431](https://img.shields.io/badge/%E2%98%85%201%2C431-eab308?style=flat-square)](https://github.com/unitreerobotics/unitree_sdk2)

宇树机器人通信与控制接口，并提供基于 SDK2 的 MuJoCo 仿真入口。

阅读重点：提供状态、命令与设备接口，支持任务层连接可执行技能。

unitree_mujoco 主要对接底层控制；具体机器人与固件的接口支持需单独核实。

机构 / 维护方：Unitree Robotics

<sub>计数快照：2026-11-03</sub>

<a id="e98"></a>

### Unitree RL mjlab

[![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab)

[💻 仓库](https://github.com/unitreerobotics/unitree_rl_mjlab) · [![★ 719](https://img.shields.io/badge/%E2%98%85%20719-eab308?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab)

基于 MuJoCo / mjlab 的运动策略训练与部署工具，包含 Go2 等机器人配置。

阅读重点：用官方配置理解训练、仿真回放与实机部署之间的关系。

机构 / 维护方：Unitree Robotics

<sub>计数快照：2026-11-03</sub>

<a id="e99"></a>

### ASAP

[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://agile.human2humanoid.com/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.01143)

[📄 论文](https://arxiv.org/abs/2502.01143) · [💻 仓库](https://github.com/LeCAR-Lab/ASAP) · [![★ 2,138](https://img.shields.io/badge/%E2%98%85%202%2C138-eab308?style=flat-square)](https://github.com/LeCAR-Lab/ASAP) [![Cite OA 58](https://img.shields.io/badge/Cite%20OA%2058-0284c7?style=flat-square)](https://openalex.org/W4414051111)

用真实机器人数据学习仿真与真实动力学差异，再适配全身动作策略。

机构 / 维护方：Carnegie Mellon University; NVIDIA

<sub>计数快照：2026-11-03</sub>

<a id="e100"></a>

### TWIST2

[![ICRA 2026](https://img.shields.io/badge/ICRA%202026-475569?style=flat-square)](https://yanjieze.com/projects/TWIST2/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2511.02832)

[📄 论文](https://arxiv.org/abs/2511.02832) · [💻 仓库](https://github.com/amazon-far/TWIST2) · [🔗 TWIST / CoRL 2025](https://yanjieze.com/projects/TWIST/) · [![★ 894](https://img.shields.io/badge/%E2%98%85%20894-eab308?style=flat-square)](https://github.com/amazon-far/TWIST2) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7103984447)

全身遥操作与运动跟踪系统，为人形机器人收集复杂接触和双手协作数据。

已发布控制器、训练及遥操作入口；高层视觉运动策略代码需查看独立发布状态。

机构 / 维护方：Amazon FAR; Stanford University; University of Southern California; UC Berkeley; Carnegie Mellon University

<sub>计数快照：2026-11-03</sub>

<a id="e101"></a>

### RoboTwin 2.0

[![ICML 2026](https://img.shields.io/badge/ICML%202026-475569?style=flat-square)](https://github.com/RoboTwin-Platform/RoboTwin) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2506.18088)

[📄 论文](https://arxiv.org/abs/2506.18088) · [💻 仓库](https://github.com/RoboTwin-Platform/RoboTwin) · [![★ 3,032](https://img.shields.io/badge/%E2%98%85%203%2C032-eab308?style=flat-square)](https://github.com/RoboTwin-Platform/RoboTwin) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W6929480010)

通过自动化仿真数据生成和领域随机化构建双臂操作任务，提供预采集轨迹。

阅读重点：提供策略训练与评测数据，并支持任务生成和领域随机化。

机构 / 维护方：Shanghai AI Lab; Shenzhen University; Nanjing University; SJTU; HKU; TeleAI; D-Robotics

<sub>计数快照：2026-11-03</sub>

<a id="e102"></a>

### RDT-1B

[![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://github.com/thu-ml/RoboticsDiffusionTransformer) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2410.07864)

[📄 论文](https://arxiv.org/abs/2410.07864) · [💻 仓库](https://github.com/thu-ml/RoboticsDiffusionTransformer) · [![★ 1,816](https://img.shields.io/badge/%E2%98%85%201%2C816-eab308?style=flat-square)](https://github.com/thu-ml/RoboticsDiffusionTransformer) [![Cite OA 5](https://img.shields.io/badge/Cite%20OA%205-0284c7?style=flat-square)](https://openalex.org/W4403364995)

双臂操作的扩散基座，以统一动作表示处理多本体数据，并提供 170M 轻量版本。

机构 / 维护方：Tsinghua University

<sub>计数快照：2026-11-03</sub>

<a id="e17"></a>

### llama.cpp ecosystem

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/OpenBMB/llama.cpp-omni) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/ggml-org/llama.cpp/discussions/19759)

[💻 仓库](https://github.com/ggml-org/llama.cpp) · [![★ 133,116](https://img.shields.io/badge/%E2%98%85%20133%2C116-eab308?style=flat-square)](https://github.com/ggml-org/llama.cpp)

本地推理工具链基础，提供量化与多平台运行入口。

完整 Omni 模式可能依赖专用分支，例如 OpenBMB/llama.cpp-omni。

机构 / 维护方：ggml.ai / Hugging Face; llama.cpp contributor community

<sub>计数快照：2026-11-02</sub>

<a id="e18"></a>

### MNN

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni#deployment-with-mnn) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/alibaba/MNN)

[💻 仓库](https://github.com/alibaba/MNN) · [![★ 16,336](https://img.shields.io/badge/%E2%98%85%2016%2C336-eab308?style=flat-square)](https://github.com/alibaba/MNN)

面向移动与边缘设备的推理框架；Qwen2.5-Omni 提供官方接入入口。

机构 / 维护方：Alibaba

<sub>计数快照：2026-11-02</sub>

<a id="evaluation"></a>

## 📏 评测

<a id="e14"></a>

### Daily-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2505.17862) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2505.17862)

[📄 论文](https://arxiv.org/abs/2505.17862) · [💻 仓库](https://github.com/Lliar-liar/Daily-Omni) · [![★ 53](https://img.shields.io/badge/%E2%98%85%2053-eab308?style=flat-square)](https://github.com/Lliar-liar/Daily-Omni) Cite —

日常视频音画联合推理基准，强调跨模态时间对齐。

机构 / 维护方：Fudan University

<sub>计数快照：2026-11-02</sub>

<a id="e15"></a>

### OmniBench (m-a-p)

[![NeurIPS 2025](https://img.shields.io/badge/NeurIPS%202025-475569?style=flat-square)](https://arxiv.org/abs/2409.15272) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2409.15272)

[📄 论文](https://arxiv.org/abs/2409.15272) · [💻 仓库](https://github.com/multimodal-art-projection/OmniBench) · [![★ 62](https://img.shields.io/badge/%E2%98%85%2062-eab308?style=flat-square)](https://github.com/multimodal-art-projection/OmniBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4403885114) [![Cite S2 111](https://img.shields.io/badge/Cite%20S2%20111-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/bde43a6356341b68a675582cf964fd9725fb40fb)

针对图像、音频、文本联合理解的三模态基准，并提供 OmniInstruct。

机构 / 维护方：M-A-P; University of Manchester; Queen Mary University of London; 01.ai; HKUST; Nanjing University; Dartmouth College

<sub>计数快照：2026-11-02</sub>

<a id="e16"></a>

### ⭐ Full-Duplex-Bench

[![ASRU 2025](https://img.shields.io/badge/ASRU%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.04721) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2503.04721)

[📄 论文](https://arxiv.org/abs/2503.04721) · [💻 仓库](https://github.com/DanielLin94144/Full-Duplex-Bench) · [![★ 335](https://img.shields.io/badge/%E2%98%85%20335-eab308?style=flat-square)](https://github.com/DanielLin94144/Full-Duplex-Bench) [![Cite OA 8](https://img.shields.io/badge/Cite%20OA%208-0284c7?style=flat-square)](https://openalex.org/W7148492801)

覆盖停顿、反馈、轮次交接和打断；后续版本扩展重叠、动态多轮与工具使用。

📌 优先阅读理由：把打断、轮次交接和交互时序转为可测指标。

机构 / 维护方：National Taiwan University; UC Berkeley; University of Washington; MIT CSAIL

<sub>计数快照：2026-11-02 / 2026-11-03</sub>

<a id="e35"></a>

### LIBERO

[![NeurIPS Datasets and Benchmarks 2023](https://img.shields.io/badge/NeurIPS%20Datasets%20and%20Benchmarks%202023-475569?style=flat-square)](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8c3c666820ea055a77726d66fc7d447f-Abstract-Datasets_and_Benchmarks.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2306.03310)

[📄 论文](https://arxiv.org/abs/2306.03310) · [💻 仓库](https://github.com/Lifelong-Robot-Learning/LIBERO) · [![★ 2,508](https://img.shields.io/badge/%E2%98%85%202%2C508-eab308?style=flat-square)](https://github.com/Lifelong-Robot-Learning/LIBERO) [![Cite OA 136](https://img.shields.io/badge/Cite%20OA%20136-0284c7?style=flat-square)](https://openalex.org/W7133220882)

语言条件机器人操作基准，考察知识迁移与持续学习。

评测范围为语言条件操作；语音交互和真人协作需补充专项评测。

机构 / 维护方：UT Austin; Tsinghua University; Sony AI

<sub>计数快照：2026-11-03</sub>

<a id="e59"></a>

### ⭐ VoiceBench

[![TACL 2026](https://img.shields.io/badge/TACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.tacl-1.18/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2410.17196)

[📄 论文](https://arxiv.org/abs/2410.17196) · [💻 仓库](https://github.com/MatthewCYM/VoiceBench) · [![★ 407](https://img.shields.io/badge/%E2%98%85%20407-eab308?style=flat-square)](https://github.com/MatthewCYM/VoiceBench) [![Cite OA 12](https://img.shields.io/badge/Cite%20OA%2012-0284c7?style=flat-square)](https://openalex.org/W4404261856)

评价语音助手的知识、指令遵循、安全及口音、噪声等扰动下的回答能力。

📌 优先阅读理由：建立基础语音助手能力参照，再与交互和任务指标分别比较。

主要评价语音输入后的回答能力；连续全双工交互与工具任务需使用对应评测。

机构 / 维护方：National University of Singapore

<sub>计数快照：2026-11-03</sub>

<a id="e60"></a>

### VocalBench

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2505.15727) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2505.15727)

[📄 论文](https://arxiv.org/abs/2505.15727) · [💻 仓库](https://github.com/SJTU-OmniAgent/VocalBench) · [![★ 8](https://img.shields.io/badge/%E2%98%85%208-eab308?style=flat-square)](https://github.com/SJTU-OmniAgent/VocalBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4415329203)

覆盖语义、声学、对话与鲁棒性，补充单轮和多轮语音交互能力评测。

各子集、语言和扩展版本分别记录发布状态与发表位置。

机构 / 维护方：Shanghai Jiao Tong University; Ant Group

<sub>计数快照：2026-11-03</sub>

<a id="e61"></a>

### VCB Bench

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.1659/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2510.11098)

[📄 论文](https://arxiv.org/abs/2510.11098) · [💻 仓库](https://github.com/Tencent/VCB-Bench) · [![★ 5](https://img.shields.io/badge/%E2%98%85%205-eab308?style=flat-square)](https://github.com/Tencent/VCB-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4417101201)

以真实中文语音为核心，评价指令遵循、知识理解与声学和内容扰动下的鲁棒性。

核心贡献为真实中文语音；后续语言扩展与论文原始协议应分开报告。

机构 / 维护方：Wuhan University; Tencent

<sub>计数快照：2026-11-03</sub>

<a id="e62"></a>

### ⭐ VoiceAgentBench

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.07978) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2510.07978)

[📄 论文](https://arxiv.org/abs/2510.07978) · [💻 仓库](https://github.com/ola-krutrim/VoiceAgentBench) · [🔗 数据](https://huggingface.co/datasets/krutrim-ai-labs/VoiceAgentBench) · [![★ 6](https://img.shields.io/badge/%E2%98%85%206-eab308?style=flat-square)](https://github.com/ola-krutrim/VoiceAgentBench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415318706)

将多语言语音输入连接单步、并行、顺序工具调用及多轮场景，检查函数选择和参数等代理能力。

📌 优先阅读理由：明确语音工具调用的函数、参数和多步结构，为任务级评测提供基础。

评测重点为语音条件下的工具结构和参数；连续语音输出的时序自然度属于独立指标。

机构 / 维护方：OLA Electric / Krutrim AI

<sub>计数快照：2026-11-03</sub>

<a id="e63"></a>

### ⭐ τ-Voice

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2603.13686) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2603.13686)

[📄 论文](https://arxiv.org/abs/2603.13686) · [💻 仓库](https://github.com/sierra-research/tau2-bench) · [![★ 2,382](https://img.shields.io/badge/%E2%98%85%202%2C382-eab308?style=flat-square)](https://github.com/sierra-research/tau2-bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7138316890)

以领域规则和环境状态评价全双工语音 Agent 的多轮工具使用及最终任务完成。

📌 优先阅读理由：从环境终态判断任务是否完成，适合对照文本 Agent 与语音 Agent 的差距。

tau2-bench 仓库持续演进并包含后续 τ³ 开发；复现本论文时固定其对应版本、环境和用户模拟器。

机构 / 维护方：Sierra; Princeton University

<sub>计数快照：2026-11-03</sub>

<a id="e64"></a>

### ⭐ Full-Duplex-Bench-v3

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.04847) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.04847)

[📄 论文](https://arxiv.org/abs/2604.04847) · [💻 仓库](https://github.com/DanielLin94144/Full-Duplex-Bench) · [🔗 项目](https://daniellin94144.github.io/FDB-v3-demo/) · [![★ 335](https://img.shields.io/badge/%E2%98%85%20335-eab308?style=flat-square)](https://github.com/DanielLin94144/Full-Duplex-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7151544009)

把真人语音中的犹豫、重复、修正等不流利现象与多步工具调用结合，评价交互中的任务执行。

📌 优先阅读理由：把真实口语修正与工具调用放在同一测试中，观察交互干扰是否造成任务错误。

与 v1、v1.5、v2 共用仓库，评测任务不同；v3 为预印本，v1 发表于 ASRU 2025。

机构 / 维护方：National Taiwan University; NVIDIA

<sub>计数快照：2026-11-03</sub>

<a id="e65"></a>

### ⭐ MTR-DuplexBench

[![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.263/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2511.10262)

[📄 论文](https://arxiv.org/abs/2511.10262) · [💻 仓库](https://github.com/ZhangHe0918/MTR-DuplexBench) · [![★ 9](https://img.shields.io/badge/%E2%98%85%209-eab308?style=flat-square)](https://github.com/ZhangHe0918/MTR-DuplexBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4416238789)

按轮次分析长一些的全双工对话，联合观察交互动态、回答质量、指令遵循和安全。

📌 优先阅读理由：覆盖多轮交互中的误差累积与上下文依赖。

机构 / 维护方：Tsinghua University; The Chinese University of Hong Kong; Huawei

<sub>计数快照：2026-11-03</sub>

<a id="e66"></a>

### HumDial-FDBench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.21406) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.21406)

[📄 论文](https://arxiv.org/abs/2604.21406) · [💻 仓库](https://github.com/ASLP-lab/HumDial-FDBench) · [![★ 44](https://img.shields.io/badge/%E2%98%85%2044-eab308?style=flat-square)](https://github.com/ASLP-lab/HumDial-FDBench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7155525302)

以真实双声道人类对话评测重叠、打断和反馈，并组织 HumDial 全双工挑战与榜单。

论文讨论 ICASSP 2026 HumDial 挑战；本条目的发表状态仍按预印本记录。

机构 / 维护方：Northwestern Polytechnical University / ASLP Lab; Nanjing University; AISHELL

<sub>计数快照：2026-11-03</sub>

<a id="e67"></a>

### MP-Bench

[![Findings of EMNLP 2026](https://img.shields.io/badge/Findings%20of%20EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-emnlp.1437/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.13076)

[📄 论文](https://arxiv.org/abs/2609.13076) · [💻 仓库](https://github.com/atosystem/MP-Bench) · [![★ 1](https://img.shields.io/badge/%E2%98%85%201-eab308?style=flat-square)](https://github.com/atosystem/MP-Bench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7212688662)

把语音 Agent 作为多人对话的参与者，评价理解、接话时机与回应适切性。

机构 / 维护方：The University of Texas at Austin; National Taiwan University; MIT; Carnegie Mellon University; Meta AI

<sub>计数快照：2026-11-03</sub>

<a id="e68"></a>

### Duplex-MPE

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.31948) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.31948)

[📄 论文](https://arxiv.org/abs/2609.31948) · [🔗 项目](https://step-out.github.io/Duplex-MPE-Page/) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7214781414)

在多人场景中区分被明确点名、隐含求助、主动参与与应保持沉默，测试参与决策。

机构 / 维护方：Peking University; Renmin University of China; Tsinghua University; National Taiwan University; Xiamen University; Fudan University

<sub>计数快照：2026-11-03</sub>

<a id="e69"></a>

### Instruct-FD

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2607.20460) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2607.20460)

[📄 论文](https://arxiv.org/abs/2607.20460) · [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7170334618)

检验全双工系统能否按指令调整接话、打断、反馈及主动性，报告交互指令遵循程度。

机构 / 维护方：Boson AI

<sub>计数快照：2026-11-03</sub>

<a id="e70"></a>

### DuplexAct-Bench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.39446) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.39446)

[📄 论文](https://arxiv.org/abs/2609.39446) · [💻 仓库](https://github.com/Alita-xky/DuplexAct-Bench) · [🔗 项目](https://alitaxky.icu/DuplexAct-Bench/) · [![★ 1](https://img.shields.io/badge/%E2%98%85%201-eab308?style=flat-square)](https://github.com/Alita-xky/DuplexAct-Bench) Cite —

覆盖打断、让出话轮、抵抗打断、主动沉默、主动开场、反馈六类行为，分别检查时机与内容。

链接仓库主要提供项目页面；完整评测器和数据的可用性以项目发布为准。

机构 / 维护方：Beijing Institute for General Artificial Intelligence; Peking University; Shanghai Jiao Tong University

<sub>计数快照：2026-11-03</sub>

<a id="e71"></a>

### ⭐ EVA-Bench

[![Findings of EMNLP 2026](https://img.shields.io/badge/Findings%20of%20EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-emnlp.2182/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2605.13841)

[📄 论文](https://arxiv.org/abs/2605.13841) · [💻 仓库](https://github.com/ServiceNow/eva) · [🔗 项目](https://servicenow.github.io/eva/) · [![★ 235](https://img.shields.io/badge/%E2%98%85%20235-eab308?style=flat-square)](https://github.com/ServiceNow/eva) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7161175665)

以动态 bot-to-bot 对话模拟评价完整任务和交互体验，分别报告任务与事实忠实度、时序与体验。

📌 优先阅读理由：学习将任务正确性与体验分开评估，并检查动态用户模拟器的可信度。

机构 / 维护方：ServiceNow AI Research

<sub>计数快照：2026-11-03</sub>

<a id="e72"></a>

### VAmoS Bench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2607.27453) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2607.27453)

[📄 论文](https://arxiv.org/abs/2607.27453) · [💻 仓库](https://github.com/veris-ai/riley-agent) · [![★ 18](https://img.shields.io/badge/%E2%98%85%2018-eab308?style=flat-square)](https://github.com/veris-ai/riley-agent) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7172022530)

在金融服务场景中运行语音代理模拟，通过完整对话、工具轨迹与领域事实检查任务执行。

评测领域为金融服务；riley-agent 提供参考代理实现，完整评分器的可用性需单独核实。

机构 / 维护方：Veris AI

<sub>计数快照：2026-11-03</sub>

<a id="e73"></a>

### FD-Bench

[![Interspeech 2025](https://img.shields.io/badge/Interspeech%202025-475569?style=flat-square)](https://www.isca-archive.org/interspeech_2025/peng25b_interspeech.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2507.19040)

[📄 论文](https://arxiv.org/abs/2507.19040) · [💻 仓库](https://github.com/pengyizhou/FD-Bench) · [![★ 27](https://img.shields.io/badge/%E2%98%85%2027-eab308?style=flat-square)](https://github.com/pengyizhou/FD-Bench) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4415433582)

以多轮、打断和噪声条件构建全双工评测流程，观察生成质量与延迟。

与 DanielLin94144/Full-Duplex-Bench 为独立项目，分别使用各自版本与评分协议。

机构 / 维护方：Nanyang Technological University; Alibaba

<sub>计数快照：2026-11-03</sub>

<a id="e74"></a>

### TurnBench

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2608.25218) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2608.25218)

[📄 论文](https://arxiv.org/abs/2608.25218) · [💻 仓库](https://github.com/SesameAILabs/turnbench) · [🔗 项目](https://turnbench.sesame.com/) · [![★ 57](https://img.shields.io/badge/%E2%98%85%2057-eab308?style=flat-square)](https://github.com/SesameAILabs/turnbench) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7204453739)

围绕轮次结束与打断检测，在不同误报预算下比较召回和延迟，评价组件的实时决策。

评测重点为轮次决策组件；回复内容、工具调用和最终任务完成需补充系统级评测。

机构 / 维护方：Sesame AI; Mundo AI; Oto; Carnegie Mellon University; National Taiwan University; Academia Sinica; Brno University of Technology

<sub>计数快照：2026-11-03</sub>

<a id="industry"></a>

## 🏭 工业展示

<a id="e10"></a>

### WITA-Omni

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://www.agibot.com/article/231/detail/122.html) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.agibot.com/article/231/detail/122.html)

[🔗 官网](https://www.agibot.com/article/231/detail/122.html) · —

智元的具身交互展示将场景理解、语音和身体表达组合在同一交互过程中。

公开材料以系统展示为主；动作模型、训练数据与完整系统的开放状态以官方发布为准。

机构 / 维护方：AGIBOT / 智元

<a id="e27"></a>

### Gemini Live API × Robotics demo

[![Technical Demo 2025](https://img.shields.io/badge/Technical%20Demo%202025-475569?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/)

[🔗 官网](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) · —

Google 官方展示将语音与机器人摄像头输入交给 Live API，再以函数调用连接机器人控制接口。

提供 Live API 连接机器人接口的工程示例；Gemini Robotics 模型发布与机器人成功率实验属于独立资源。

机构 / 维护方：Google / Google DeepMind

<a id="e28"></a>

### Figure Helix 02

[![Technical Demo 2026](https://img.shields.io/badge/Technical%20Demo%202026-475569?style=flat-square)](https://www.figure.ai/news/helix-02) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.figure.ai/news/helix-02)

[🔗 官网](https://www.figure.ai/news/helix-02) · —

Figure 以 S2 语义规划、S1 视觉运动策略和 S0 全身控制连接语言目标与移动操作。

公开材料为系统技术展示，适合参考分层设计；训练代码与可复现实验的可用性以官方发布为准。

机构 / 维护方：Figure AI

<a id="e96"></a>

### Qwen-RobotNav

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.18112) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2606.18112)

[📄 论文](https://arxiv.org/abs/2606.18112) · [💻 仓库](https://github.com/QwenLM/Qwen-RobotNav) · [![★ 198](https://img.shields.io/badge/%E2%98%85%20198-eab308?style=flat-square)](https://github.com/QwenLM/Qwen-RobotNav) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7165037828)

Qwen3-VL 导航系统报告，研究任务模式、上下文与 waypoint 接口，并展示 Go2 部署。

官方仓库说明暂无权重发布计划；公开内容适合系统设计与部署参考。

机构 / 维护方：Alibaba / Qwen Team

<sub>计数快照：2026-11-03</sub>
