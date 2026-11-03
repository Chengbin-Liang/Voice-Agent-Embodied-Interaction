# Survey 与总结入口

**中文** | [English](../en/SURVEYS.md)

[返回首页](../../README.md) · [完整索引](CATALOG.md) · [Survey 对照](SURVEYS.md)

按问题选择综述，再到代表论文与代码。各综述的分类、论点和原始条目归其作者；下表仅概括覆盖范围。

[语音、Omni 与 HRI 综述](#comparison) · [LLM 综述与教学参考](#llm-learning)

<a id="comparison"></a>
## 📚 Survey 对照表

| 资源 | 覆盖范围 | 对应阅读阶段 |
|---|---|---|
| ⭐ [WavChat](#s01) | 语音对话模型、表征、训练、流式与交互。 | 02–03 |
| [Recent Advances in Speech Language Models](#s02) | SpeechLM，以及更新后的双工模型、控制组件与评测清单。 | 02–03 |
| [From Turn-Taking to Synchronous Dialogue](#s03) | 全双工模型、同步机制与评价。 | 03 |
| [Speaking While Listening / DuplexSurvey](#s04) | 架构层次、时间关系×用户意图×系统回应，以及对话决策状态。 | 03 |
| [A Survey on Audio–Visual Large Language Models](#s05) | 模态范围、骨干来源、生成目标、数据与应用。 | 02 |
| [Omni-Modal LLMs: Architecture, Training, Evaluation](#s06) | 仓库中的综述稿以 Build → Assess → Apply 组织 Omni 研究。 | 02 |
| ⭐ [MLLM-HRC-Survey](#s07) | 人机协作、空间智能与感知—认知—执行循环。 | 04 |
| [LLM-Based Human-Agent Collaboration and Interaction Systems](#s08) | 反馈类型、粒度、阶段、协作与通信。 | 03–04 |
| ⭐ [How Do We Research HRI in the Age of LLMs?](#s09) | 以人为中心的 HRI 系统、实验设计与评价。 | 04 |
| [Dialogue Management in HRI](#s10) | 传统与现代 HRI 对话管理、情境、多模态及评价。 | 04 |

<a id="s01"></a>

## WavChat

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2411.13577) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2411.13577)

[📄 论文](https://arxiv.org/abs/2411.13577) · [💻 仓库](https://github.com/jishengpeng/WavChat) · [![★ 317](https://img.shields.io/badge/%E2%98%85%20317-eab308?style=flat-square)](https://github.com/jishengpeng/WavChat) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4404649925)

语音对话模型、表征、训练、流式与交互。

📌 优先阅读理由：先建立语音对话模型、训练与交互的整体分类。

<sub>计数快照：2026-11-02。</sub>

<a id="s02"></a>

## Recent Advances in Speech Language Models

[![ACL 2025](https://img.shields.io/badge/ACL%202025-475569?style=flat-square)](https://aclanthology.org/2025.acl-long.682/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2410.03751)

[📄 论文](https://arxiv.org/abs/2410.03751) · [💻 仓库](https://github.com/dreamtheater123/Awesome-SpeechLM-Survey) · [![★ 226](https://img.shields.io/badge/%E2%98%85%20226-eab308?style=flat-square)](https://github.com/dreamtheater123/Awesome-SpeechLM-Survey) [![Cite OA 5](https://img.shields.io/badge/Cite%20OA%205-0284c7?style=flat-square)](https://openalex.org/W4403322156)

SpeechLM，以及更新后的双工模型、控制组件与评测清单。

<sub>计数快照：2026-11-02。</sub>

<a id="s03"></a>

## From Turn-Taking to Synchronous Dialogue

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.14515) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2509.14515)

[📄 论文](https://arxiv.org/abs/2509.14515) · [💻 仓库](https://github.com/elpsykongloo/FD-SLMs) · [![★ 34](https://img.shields.io/badge/%E2%98%85%2034-eab308?style=flat-square)](https://github.com/elpsykongloo/FD-SLMs) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4417081448)

全双工模型、同步机制与评价。

<sub>计数快照：2026-11-02。</sub>

<a id="s04"></a>

## Speaking While Listening / DuplexSurvey

[![EMNLP 2026](https://img.shields.io/badge/EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.emnlp-main.1126/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2606.19453)

[📄 论文](https://arxiv.org/abs/2606.19453) · [💻 仓库](https://github.com/MM-Speech/DuplexSurvey) · [![★ 109](https://img.shields.io/badge/%E2%98%85%20109-eab308?style=flat-square)](https://github.com/MM-Speech/DuplexSurvey) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7165367522)

架构层次、时间关系×用户意图×系统回应，以及对话决策状态。

<sub>计数快照：2026-11-02。</sub>

<a id="s05"></a>

## A Survey on Audio–Visual Large Language Models

[![Knowledge-Based Systems 2026](https://img.shields.io/badge/Knowledge--Based%20Systems%202026-475569?style=flat-square)](https://doi.org/10.1016/j.knosys.2026.116569)

[📄 论文](https://doi.org/10.1016/j.knosys.2026.116569) · [💻 仓库](https://github.com/AiX-Lab-UWO/Audio-Visual-LLMs-Survey) · [![★ 0](https://img.shields.io/badge/%E2%98%85%200-eab308?style=flat-square)](https://github.com/AiX-Lab-UWO/Audio-Visual-LLMs-Survey) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7166807819) [![Cite S2 0](https://img.shields.io/badge/Cite%20S2%200-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/599f04505243db7ceaca5446325182b708a7b1cb)

模态范围、骨干来源、生成目标、数据与应用。

<sub>计数快照：2026-11-02。</sub>

<a id="s06"></a>

## Omni-Modal LLMs: Architecture, Training, Evaluation

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/Abillinaire/omni-model-survey)

[💻 仓库](https://github.com/Abillinaire/omni-model-survey) · [![★ 2](https://img.shields.io/badge/%E2%98%85%202-eab308?style=flat-square)](https://github.com/Abillinaire/omni-model-survey)

仓库中的综述稿以 Build → Assess → Apply 组织 Omni 研究。

<sub>计数快照：2026-11-02。</sub>

<a id="s07"></a>

## MLLM-HRC-Survey

[![RCIM 2026](https://img.shields.io/badge/RCIM%202026-475569?style=flat-square)](https://doi.org/10.1016/j.rcim.2025.103064) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://github.com/WuDuidi/MLLM-HRC-Survey)

[📄 论文](https://doi.org/10.1016/j.rcim.2025.103064) · [💻 仓库](https://github.com/WuDuidi/MLLM-HRC-Survey) · [![★ 8](https://img.shields.io/badge/%E2%98%85%208-eab308?style=flat-square)](https://github.com/WuDuidi/MLLM-HRC-Survey) [![Cite OA 32](https://img.shields.io/badge/Cite%20OA%2032-0284c7?style=flat-square)](https://openalex.org/W4411206891) [![Cite S2 33](https://img.shields.io/badge/Cite%20S2%2033-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/4ddd6e44b7f1f3b349d7ea6756f39175a5b96f0e)

人机协作、空间智能与感知—认知—执行循环。

📌 优先阅读理由：梳理人机协作中感知、认知与执行之间的关系。

<sub>计数快照：2026-11-02。</sub>

<a id="s08"></a>

## LLM-Based Human-Agent Collaboration and Interaction Systems

[![ACL Findings 2026](https://img.shields.io/badge/ACL%20Findings%202026-475569?style=flat-square)](https://arxiv.org/abs/2505.00753) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2505.00753)

[📄 论文](https://arxiv.org/abs/2505.00753) · [💻 仓库](https://github.com/HenryPengZou/Awesome-Human-Agent-Collaboration-Interaction-Systems) · [![★ 242](https://img.shields.io/badge/%E2%98%85%20242-eab308?style=flat-square)](https://github.com/HenryPengZou/Awesome-Human-Agent-Collaboration-Interaction-Systems) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4415164160)

反馈类型、粒度、阶段、协作与通信。

<sub>计数快照：2026-11-02。</sub>

<a id="s09"></a>

## How Do We Research HRI in the Age of LLMs?

[![CHI 2026](https://img.shields.io/badge/CHI%202026-475569?style=flat-square)](https://doi.org/10.1145/3772318.3790920) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2602.15063)

[📄 论文](https://arxiv.org/abs/2602.15063) · [![Cite OA 6](https://img.shields.io/badge/Cite%20OA%206-0284c7?style=flat-square)](https://openalex.org/W7130383196)

以人为中心的 HRI 系统、实验设计与评价。

📌 优先阅读理由：了解真人实验与系统评测分别回答什么问题。

<sub>计数快照：2026-11-02。</sub>

<a id="s10"></a>

## Dialogue Management in HRI

[![ACM THRI 2024](https://img.shields.io/badge/ACM%20THRI%202024-475569?style=flat-square)](https://arxiv.org/abs/2307.10897) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2307.10897)

[📄 论文](https://arxiv.org/abs/2307.10897) · [![Cite OA 34](https://img.shields.io/badge/Cite%20OA%2034-0284c7?style=flat-square)](https://openalex.org/W4392386515)

传统与现代 HRI 对话管理、情境、多模态及评价。

<sub>计数快照：2026-11-02。</sub>

<a id="llm-learning"></a>
## 🎓 LLM 综述与教学参考

以下资源支撑 [LLM 基础](../../docs/zh/01-LLM-Foundations.md)的阅读顺序，与上方 10 个语音、Omni 和 HRI 综述条目分开列出。

| 来源 | 语言 / 定位 | 对阅读路线的作用 |
|---|---|---|
| [A Survey of Large Language Models](https://arxiv.org/abs/2303.18223) · [作者仓库](https://github.com/RUCAIBox/LLMSurvey) | 英文综述 | 提供预训练、适配、使用与能力评测的主题地图，可沿参考文献追溯原始论文。 |
| [《大语言模型》](https://llmbook-zh.github.io/) | 中文教材 | 按需查阅架构、数据、训练、对齐、评测与推理。 |
| [Happy-LLM](https://github.com/datawhalechina/happy-llm) | 中文教学材料 | LLM 入门主线：第 2–7 章；第 8 章按后训练需求查阅。 |
| [HF LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) · [中文版](https://huggingface.co/learn/llm-course/zh-CN/chapter1/1) | 英文课程与中文翻译 | tokenizer、模型使用、微调及动手练习；不同语言版本覆盖不完全一致。 |
| [Stanford CS336](https://cs336.stanford.edu/) | 英文大学课程 | 从实现角度理解语言模型组件、数据、训练与对齐，选做作业作为延伸。 |


Agent 入门：[Hello-Agents](https://github.com/datawhalechina/hello-agents)（中文）与 [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/unit0/introduction)（英文）；推荐阅读范围见 [Agent 基础](../../docs/zh/01-LLM-Foundations.md#agents)。

<a id="embodied-learning"></a>
## 🤖 具身入门指南与教学

| 来源 | 阅读范围 | 对应入口 |
|---|---|---|
| [Lumina 具身智能入门指南](https://lumina-embodied.ai/blog/eai-guide/) | 控制、MPC、RL、模仿学习、VLA、导航、硬件与工具 | [术语速查](../../docs/zh/04-Edge-Embodied-Interaction.md#concepts)与扩展资料 |
| [ScaleLab 具身指南](https://scalelab-sjtu.github.io/embodied_guide.html) | VLA、仿真与数据、全身控制的代表论文和项目 | [动作基座](../../docs/zh/04-Edge-Embodied-Interaction.md#bases)与[扩展阅读](../../docs/zh/04-Edge-Embodied-Interaction.md#research) |
| [MIT Underactuated Robotics](https://underactuated.mit.edu/) | 动力学、控制、轨迹优化与强化学习 | 按需查阅控制与 MPC，补充动作执行的原理 |
| [LeRobot 文档](https://huggingface.co/docs/lerobot/en/il_robots) | 遥操作、数据录制、训练、评测与设备适配 | 从一个示范学习流程开始 |
