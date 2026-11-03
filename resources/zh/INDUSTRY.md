# 工业界实践

**中文** | [English](../en/INDUSTRY.md)

[返回首页](../../README.md) · [完整索引](CATALOG.md) · [Survey 对照](SURVEYS.md)

## 🦾 开放机器人基座与工具

| 项目 | 类型 | 适合阅读与使用的部分 |
|---|---|---|
| ⭐ [openpi / π0 · π0.5](CATALOG.md#e91) | Industry · 权重与训练代码 | 自有机器人数据适配、动作空间与微调。 |
| ⭐ [Isaac GR00T N1.7](CATALOG.md#e92) | Industry · 权重与训练代码 | 新本体配置、数据规范与预训练策略适配。 |
| ⭐ [Unitree SDK2 / MuJoCo](CATALOG.md#e97) · [RL mjlab](CATALOG.md#e98) | Industry · 接口与训练工具 | 通信、状态、仿真、运动策略与部署。 |
| [Qwen-RobotNav](CATALOG.md#e96) | Industry · 技术报告与展示 | 导航系统与 waypoint 接口；当前未开放权重。 |

## 🤖 机器人与具身交互

| 项目 | 主体与类型 | 可参考的能力 | 开放范围与适用边界 |
|---|---|---|---|
| [WITA-Omni](CATALOG.md#e10) | [![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://www.agibot.com/article/231/detail/122.html) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.agibot.com/article/231/detail/122.html) 智元 | 场景感知、语音与身体表达的整体交互体验 | 官方展示；系统训练配方和模型开放情况需依项目发布。 |
| [Reachy Mini Conversation App](CATALOG.md#e11) | [![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app) Pollen Robotics / Hugging Face | 语音、摄像头工具、头部与天线动作 | 可阅读应用代码；适合身体表达，不是机械臂操作。 |
| [Gemini Live API × Robotics](CATALOG.md#e27) | [![Technical Demo 2025](https://img.shields.io/badge/Technical%20Demo%202025-475569?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) Google | 音视频输入经函数调用连接机器人接口 | 官方工程示例；不是 Gemini Robotics 模型开源或通用任务成绩。 |
| [Helix 02](CATALOG.md#e28) | [![Technical Demo 2026](https://img.shields.io/badge/Technical%20Demo%202026-475569?style=flat-square)](https://www.figure.ai/news/helix-02) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.figure.ai/news/helix-02) Figure | 语义规划、视觉运动与全身控制的层次组织 | 技术展示；不能假设可获得同等训练系统。 |
| [Hi Robot](CATALOG.md#e25) | [![ICML 2025](https://img.shields.io/badge/ICML%202025-475569?style=flat-square)](https://proceedings.mlr.press/v267/shi25d.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.19417) 论文署名团队含 Physical Intelligence | 高层语言推理接受反馈，低层策略执行 | 研究论文；适合分析分层接口与反馈实验。 |

语音与端侧基础设施可继续看 [FireRedChat](CATALOG.md#e29)、[Qwen Audio Agent](CATALOG.md#e30)、[MiniCPM-o](CATALOG.md#e01) 与 [MNN](CATALOG.md#e18)。模型、代码、数据及服务 API 的开放范围应分别检查。

## 🎙️ 实时 Voice Agent 技术论文

| 文章 / 项目 | 发表与归属 | 阅读重点与资源 |
|---|---|---|
| [Qwen-Audio-3.1-Realtime](CATALOG.md#e57) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.25176) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.25176) | 在可执行环境中进行 Agent GRPO，结合多模态策略蒸馏，研究任务可靠性与交互行为后训练。<br>[📄 论文](https://arxiv.org/abs/2609.25176) · [💻 仓库](https://github.com/QwenAudio/qwen-audio-agent) |
| [StepAudio 3 Realtime](CATALOG.md#e56) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.14005) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.14005) | 围绕 listen、converse、think、act 组织实时语音交互，结合 Think-While-Speaking 与异步工具执行。<br>[📄 论文](https://arxiv.org/abs/2609.14005) · [🔗 项目](https://stepaudiollm.github.io/step-audio-3-realtime/) |
| [NemotronLabs VoiceChat](CATALOG.md#e55) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.21967) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.21967) | 开放的全双工语音模型，以独立工具通道连接动作调用，并支持可打断语音输出。<br>[📄 论文](https://arxiv.org/abs/2609.21967) · [💻 仓库](https://github.com/NVIDIA-NeMo/Speech/tree/nemotron-labs-voicechat) · [🔗 模型](https://huggingface.co/nvidia/NVIDIA-NemotronLabs-VoiceChat-11B) |
| [AdaptDuplex](CATALOG.md#e53) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.29217) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.29217) | 结合自适应感知窗口、非阻塞认知整合与外部推理，研究动态全双工对话及分阶段后训练。<br>[📄 论文](https://arxiv.org/abs/2609.29217) |
| [Frontend–Backend Tool Calling](CATALOG.md#e49) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.19334) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.19334) | 将实时语音前端与文本工具后端分离，以流式转写、工具执行和 prefill-and-repeat 结果回传连接两者。<br>[📄 论文](https://arxiv.org/abs/2609.19334) |
| [Diffuplex · Discrete Diffusion](CATALOG.md#e51) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.17780) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2610.17780) | 以自回归过程决定何时说话，以离散扩散并行生成内容，研究全双工生成效率。<br>[📄 论文](https://arxiv.org/abs/2610.17780) |

校企合作可对照 [Realtime-Venus](CATALOG.md#e54)、[DuplexOmni](CATALOG.md#e58)、[TASTE2](CATALOG.md#e46)。更多方法见 [Voice Agent](../../docs/zh/03-Voice-Agent.md)，评测见 [Benchmark 导航](../../docs/zh/05-Voice-Agent-Benchmarks.md)。
