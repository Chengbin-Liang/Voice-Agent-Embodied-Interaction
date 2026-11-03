# 04 · 端侧与具身交互

**中文** | [English](../en/04-Edge-Embodied-Interaction.md)

[返回首页](../../README.md) · [完整索引](../../resources/zh/CATALOG.md)

[动作基座](#bases) → [语言反馈](#bridges) → [音频与语音交互](#audio) → [工业系统](#systems) · [数据与训练](#training) · [评测与部署](#evaluation) · [扩展阅读](#research) · [综述与教程](#tutorials)

以 π0 为动作模型的阅读起点，π0.5 作为泛化训练的补充；随后考察语言反馈、音频输入与实时交互如何影响动作执行。

<a id="bases"></a>
## 🦾 1 · 动作基座

| 类别 | 代表工作 | 核心问题 |
|---|---|---|
| 操作 VLA | [π0](https://arxiv.org/abs/2410.24164) · [π0.5](https://arxiv.org/abs/2504.16054) | 图像、指令与机器人状态如何转化为操作动作？ |
| 移动导航 | [NaVILA](../../resources/zh/CATALOG.md#e95) | 语言目标如何转化为空间指令并由运动策略执行？ |
| 全身运动 | [ASAP](../../resources/zh/CATALOG.md#e99) · [TWIST2](../../resources/zh/CATALOG.md#e100) | 人体运动、遥操作与机器人全身控制如何对应？ |

### 操作 VLA：π0 与 π0.5

| 论文与官方资源 | 方法特点 | 阅读重点 |
|---|---|---|
| ⭐ [π0: A Vision-Language-Action Flow Model for General Robot Control](https://arxiv.org/abs/2410.24164)<br>[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://roboticsproceedings.org/rss21/p010.html) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.physicalintelligence.company/blog/pi0)<br>[博客](https://www.physicalintelligence.company/blog/pi0) · [openpi 代码](https://github.com/Physical-Intelligence/openpi) | 预训练 VLM 与动作专家结合，通过 flow matching 预测连续动作块。 | 优先理由：同一模型包含视觉语言输入、动作表示与示范训练，可作为理解操作 VLA 的具体实例。重点为架构图、输入输出及训练目标。 |
| [π0.5: a Vision-Language-Action Model with Open-World Generalization](https://arxiv.org/abs/2504.16054)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2504.16054) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.physicalintelligence.company/blog/pi05)<br>[博客](https://www.physicalintelligence.company/blog/pi05) · [openpi 代码](https://github.com/Physical-Intelligence/openpi) | 在 π0 基础上联合训练多机器人、语义子任务与网络视觉语言数据。 | 补充阅读：数据来源如何对应不同目标，以及新环境下的指令遵循与操作成功率。 |

以“将杯子放入托盘”为例，动作模型接收相机图像、任务指令和机器人状态，预测一段连续动作；执行系统将动作转换为设备命令，并持续提供新观测。交互模块可以进一步修改目标、补充约束或反馈执行结果。

其他操作基座与适配方法：[OpenVLA](../../resources/zh/CATALOG.md#e20) · [SmolVLA](../../resources/zh/CATALOG.md#e34) · [Isaac GR00T N1.7](../../resources/zh/CATALOG.md#e92)。具体实现与训练入口见[扩展阅读](#research)。

<a id="bridges"></a>
## 💬 2 · 语言反馈与任务调整

| 工作 / 发表与归属 | 交互如何进入动作系统 | 阅读重点 |
|---|---|---|
| ⭐ [Hi Robot](../../resources/zh/CATALOG.md#e25)<br>[![ICML 2025](https://img.shields.io/badge/ICML%202025-475569?style=flat-square)](https://proceedings.mlr.press/v267/shi25d.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.19417)<br>[📄 论文](https://arxiv.org/abs/2502.19417) · [🔗 项目](https://www.pi.website/research/hirobot) | 高层 VLM 根据指令、场景与执行反馈生成子任务，由低层 VLA 执行。 | 优先理由：明确展示任务规划与动作策略的接口。重点为反馈后的子任务更新，以及高低层各自的训练数据。 |
| [Yell At Your Robot / YAY Robot](../../resources/zh/CATALOG.md#e26)<br>[![RSS 2024](https://img.shields.io/badge/RSS%202024-475569?style=flat-square)](https://roboticsproceedings.org/rss20/p025.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2403.12910)<br>[📄 论文](https://arxiv.org/abs/2403.12910) · [💻 代码](https://github.com/yay-robot/yay_robot) | 执行中接收口头纠正，并将纠正数据用于后续高层策略训练。 | 当前任务调整、纠正数据记录与后训练之间的关系。 |
| [Interactive Language / Language Table](../../resources/zh/CATALOG.md#e13)<br>[![IEEE RA-L 2024](https://img.shields.io/badge/IEEE%20RA--L%202024-475569?style=flat-square)](https://doi.org/10.1109/LRA.2023.3295255) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2210.06407)<br>[📄 论文](https://arxiv.org/abs/2210.06407) · [💻 代码](https://github.com/google-research/language-table) | 持续语言指导直接改变视觉运动策略的目标。 | 语言标注与机器人轨迹的对应方式，以及执行中修改指令的实验。 |

这组工作的主要反馈载体是语言表示。原始声音中的说话人身份、韵律和环境音，对应下一组工作的研究问题。

<a id="audio"></a>
## 🎧 3 · 音频输入与语音—动作交互

| 工作 / 发表与归属 | 相比语言条件动作增加的部分 | 阅读重点 |
|---|---|---|
| ⭐ [VLAS](../../resources/zh/CATALOG.md#e24)<br>[![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2025/hash/804a1a9de5787e3597b4bb64e1a48ec3-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.13508)<br>[📄 论文](https://arxiv.org/abs/2502.13508) · [💻 代码](https://github.com/whichwhichgone/VLAS) | 语音编码器接入视觉动作模型，结合声纹检索支持个性化操作。 | 优先理由：提供较直接的“视觉动作模型 + 语音输入”实例。重点为编码器对齐、语音指令训练与个性化任务对照。 |
| [RoboOmni (OpenMOSS)](../../resources/zh/CATALOG.md#e21)<br>[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/33610fba262d7b6fed0810b89f55e147-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2510.23763)<br>[📄 论文](https://arxiv.org/abs/2510.23763) · [💻 代码](https://github.com/OpenMOSS/RoboOmni) | 将语音、环境声音、视觉与动作表示结合，研究情境意图和主动协助。 | OmniAction 的情境构造，以及文本、转写和音频条件下的动作结果对照。 |
| ⭐ [ELLSA](../../resources/zh/CATALOG.md#e22)<br>[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/6d8af672c0bca7a4be6f0cd0d229c05c-Abstract-Conference.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.16756)<br>[📄 论文](https://arxiv.org/abs/2510.16756) · [💻 代码](https://github.com/bytedance/SALMONN/tree/ELLSA) | 语音专家与动作专家联合建模，处理同时说做、动作打断和场景问答。 | 优先理由：将实时语音与动作执行纳入同一训练框架。重点为 SA-MoE、分阶段适配与打断实验。 |
| [VITA-E](../../resources/zh/CATALOG.md#e23)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.21817) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.21817)<br>[📄 论文](https://arxiv.org/abs/2510.21817) · [💻 代码](https://github.com/Tencent/VITA/tree/VITA-E) | 通过活动/监听模型与控制 token 调度语音和动作。 | 并发交互、任务切换、控制状态与动作恢复。 |

比较这些工作时，关注新增信息或时序机制带来的任务变化：操作成功率、纠正后的恢复、个性化目标选择，以及执行中的响应时延。模型输入包含音频与实际使用声音信息，是需要通过对照实验区分的两个问题。

<a id="systems"></a>
## 🏭 4 · 工业系统与工程实现

| 系统 / 来源 | 交互与动作接口 | 资源范围 |
|---|---|---|
| [Reachy Mini Conversation App](../../resources/zh/CATALOG.md#e11)<br>[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)<br>[💻 代码](https://github.com/pollen-robotics/reachy_mini_conversation_app) | 语音和摄像头工具连接头部、天线等动作。 | 开放应用代码；适合分析交互状态与工具执行。 |
| [Gemini Live API × Robotics demo](../../resources/zh/CATALOG.md#e27)<br>[![Technical Demo 2025](https://img.shields.io/badge/Technical%20Demo%202025-475569?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/)<br>[🔗 项目](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) | 音视频输入通过函数调用连接机器人接口。 | 官方工程示例；关注函数参数、执行反馈与异常处理。 |
| [WITA-Omni](../../resources/zh/CATALOG.md#e10)<br>[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://www.agibot.com/article/231/detail/122.html) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.agibot.com/article/231/detail/122.html)<br>[🔗 项目](https://www.agibot.com/article/231/detail/122.html) | 场景感知、语音与身体表达相结合。 | 官方展示；关注交互形式与反馈设计。 |
| [Figure Helix 02](../../resources/zh/CATALOG.md#e28)<br>[![Technical Demo 2026](https://img.shields.io/badge/Technical%20Demo%202026-475569?style=flat-square)](https://www.figure.ai/news/helix-02) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.figure.ai/news/helix-02)<br>[🔗 项目](https://www.figure.ai/news/helix-02) | 语义规划、视觉运动与全身控制分层协同。 | 技术说明与展示；关注高低层接口。 |

<a id="training"></a>
## 🗂️ 5 · 数据与模型适配

| 训练对象 | 样本内容 | 参考入口 |
|---|---|---|
| 动作策略 | 同步图像、状态、动作、任务标签与 episode 边界 | [openpi 自有数据微调](https://github.com/Physical-Intelligence/openpi#fine-tuning-base-models-on-your-own-data) · [LeRobotDataset v3](https://huggingface.co/docs/lerobot/en/lerobot-dataset-v3) |
| 高层任务与纠正 | 场景、任务状态、用户反馈、下一子任务或技能 | [Hi Robot](../../resources/zh/CATALOG.md#e25) · [Yell At Your Robot / YAY Robot](../../resources/zh/CATALOG.md#e26) |
| 语音条件动作 | 音频、视觉观测、语言内容或身份条件、动作示范 | [VLAS](../../resources/zh/CATALOG.md#e24) · [RoboOmni (OpenMOSS)](../../resources/zh/CATALOG.md#e21) |
| 实时交互 | 音视频时间戳、说话/监听状态、动作片段、打断与恢复记录 | [ELLSA](../../resources/zh/CATALOG.md#e22) · [VITA-E](../../resources/zh/CATALOG.md#e23) |
| 仿真数据 | 任务配置、随机化场景与示范轨迹 | [RoboTwin 2.0](../../resources/zh/CATALOG.md#e101) |

音频与工具事件可通过 episode 标识和时间戳关联机器人数据。合成对话可补充语言与规划样本；动作监督需来自示范、仿真或其他有依据的动作数据。训练与评测按 episode、场景和对象划分，以控制相邻帧泄漏。

模型适配可按组件验证：已有动作策略执行文本指令 → 交互模块生成任务请求 → 执行状态返回交互模块。动作技能与语言反馈分别对应动作示范、纠正记录等训练数据。

<a id="evaluation"></a>
## 📊 6 · Benchmarks、端侧部署与系统评测

| 评测对象 | 数据集 / 入口 | 主要指标或对照 |
|---|---|---|
| 语言条件操作 | [LIBERO](../../resources/zh/CATALOG.md#e35) · [RoboTwin 2.0](../../resources/zh/CATALOG.md#e101) | 任务成功率、长任务完成、场景与对象泛化 |
| 语音及情境信息的作用 | [VLAS](../../resources/zh/CATALOG.md#e24) · [RoboOmni (OpenMOSS)](../../resources/zh/CATALOG.md#e21) 的配套任务 | 文本 / 转写 / 原始音频条件，身份与环境声音消融 |
| 交互对动作的影响 | [ELLSA](../../resources/zh/CATALOG.md#e22) · [VITA-E](../../resources/zh/CATALOG.md#e23) 的交互实验 | 说做并发、动作打断、任务切换与恢复成功率 |
| 语言纠正与后训练 | [Hi Robot](../../resources/zh/CATALOG.md#e25) · [Yell At Your Robot / YAY Robot](../../resources/zh/CATALOG.md#e26) | 反馈前后、不同反馈表示与训练设置的任务表现 |
| 语音交互组件 | [Voice Agent Benchmarks](05-Voice-Agent-Benchmarks.md) | 语音内容、轮次、工具调用与交互时延 |

系统报告需区分模型推理、音频播放、动作下发与机器人执行时延；停止播报、取消请求和设备实际停止分别记录。异步执行还涉及动作缓冲的更新与清除。部署位置可标注为机器人本体、局域网工作站或云端。

接口与部署：[ROS 2 Actions](https://docs.ros.org/en/jazzy/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Actions/Understanding-ROS2-Actions.html) · [LeRobot 异步推理](https://huggingface.co/docs/lerobot/en/async) · [Unitree SDK2 / MuJoCo](../../resources/zh/CATALOG.md#e97) · [llama.cpp ecosystem](../../resources/zh/CATALOG.md#e17) · [MNN](../../resources/zh/CATALOG.md#e18)。

<a id="research"></a>
## 📚 7 · 扩展阅读

<a id="policies"></a>
### 操作模型与后训练

| 工作 | 主题 | 阅读重点 |
|---|---|---|
| [ACT / ALOHA](../../resources/zh/CATALOG.md#e32)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://www.roboticsproceedings.org/rss19/p016.pdf) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2304.13705)<br>[📄 论文](https://arxiv.org/abs/2304.13705) · [💻 代码](https://github.com/tonyzhaozh/act) | 示范学习 | 观测条件动作块预测与时序集成。 |
| [Diffusion Policy](../../resources/zh/CATALOG.md#e33)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2303.04137)<br>[📄 论文](https://arxiv.org/abs/2303.04137v4) · [💻 代码](https://github.com/real-stanford/diffusion_policy) | 扩散策略 | 连续、多峰动作分布与视觉条件生成。 |
| [OpenVLA](../../resources/zh/CATALOG.md#e20)<br>[![CoRL 2024](https://img.shields.io/badge/CoRL%202024-475569?style=flat-square)](https://proceedings.mlr.press/v270/kim25c.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2406.09246)<br>[📄 论文](https://arxiv.org/abs/2406.09246) · [💻 代码](https://github.com/openvla/openvla) | 通用操作 VLA | 预训练视觉语言表示与离散动作预测。 |
| [SmolVLA](../../resources/zh/CATALOG.md#e34)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2506.01844) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2506.01844)<br>[📄 论文](https://arxiv.org/abs/2506.01844) · [💻 代码](https://github.com/huggingface/lerobot) | 轻量 VLA | 文本条件动作与机器人数据适配。 |
| [Isaac GR00T N1.7](../../resources/zh/CATALOG.md#e92)<br>[![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T)<br>[💻 代码](https://github.com/NVIDIA/Isaac-GR00T) | 工业 VLA | 本体配置、动作空间与检查点适配。 |
| [OpenVLA-OFT](../../resources/zh/CATALOG.md#e93)<br>[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://roboticsproceedings.org/rss21/p017.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.19645)<br>[📄 论文](https://arxiv.org/abs/2502.19645) · [💻 代码](https://github.com/moojink/openvla-oft) | OpenVLA 高效适配 | 并行解码、动作块、连续动作与 FiLM。 |
| [SimpleVLA-RL](../../resources/zh/CATALOG.md#e94)<br>[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/cbfbcb4da14235bd69b134070898ae9d-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2509.09674)<br>[📄 论文](https://arxiv.org/abs/2509.09674) · [💻 代码](https://github.com/PRIME-RL/SimpleVLA-RL) | VLA 强化学习 | SFT 策略、环境奖励与在线 rollout。 |
| [RDT-1B](../../resources/zh/CATALOG.md#e102)<br>[![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://github.com/thu-ml/RoboticsDiffusionTransformer) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2410.07864)<br>[📄 论文](https://arxiv.org/abs/2410.07864) · [💻 代码](https://github.com/thu-ml/RoboticsDiffusionTransformer) | 双臂扩散基座 | 多本体动作表示与双臂示范训练。 |

适配教程：[SmolVLA](https://huggingface.co/docs/lerobot/en/smolvla) · [GR00T 新本体微调](https://github.com/NVIDIA/Isaac-GR00T/blob/main/getting_started/finetune_new_embodiment.md)。

<a id="navigation"></a>
### 移动与全身运动

| 工作 | 阅读重点 |
|---|---|
| [NaVILA](../../resources/zh/CATALOG.md#e95)<br>[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://navila-bot.github.io/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2412.04453)<br>[📄 论文](https://arxiv.org/abs/2412.04453) · [💻 代码](https://github.com/AnjieCheng/NaVILA) | 高层空间语言指令与低层视觉运动策略的接口。 |
| [Qwen-RobotNav](../../resources/zh/CATALOG.md#e96)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.18112) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2606.18112)<br>[📄 论文](https://arxiv.org/abs/2606.18112) · [💻 代码](https://github.com/QwenLM/Qwen-RobotNav) | 导航系统与 waypoint 接口，作为工业部署案例。 |
| [ASAP](../../resources/zh/CATALOG.md#e99)<br>[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://agile.human2humanoid.com/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.01143)<br>[📄 论文](https://arxiv.org/abs/2502.01143) · [💻 代码](https://github.com/LeCAR-Lab/ASAP) | 仿真与真实动力学差异，以及运动策略适配。 |
| [TWIST2](../../resources/zh/CATALOG.md#e100)<br>[![ICRA 2026](https://img.shields.io/badge/ICRA%202026-475569?style=flat-square)](https://yanjieze.com/projects/TWIST2/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2511.02832)<br>[📄 论文](https://arxiv.org/abs/2511.02832) · [💻 代码](https://github.com/amazon-far/TWIST2) | 全身遥操作、运动跟踪与示范采集。 |
| [Unitree RL mjlab](../../resources/zh/CATALOG.md#e98)<br>[![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab)<br>[💻 代码](https://github.com/unitreerobotics/unitree_rl_mjlab) | 机器人配置、奖励、仿真回放与运动策略部署。 |

运动策略与仿真：[legged-loco](https://github.com/yang-zj1026/legged-loco) · [Unitree MuJoCo](https://github.com/unitreerobotics/unitree_mujoco) · [Python SDK](https://github.com/unitreerobotics/unitree_sdk2_python)。

<a id="tutorials"></a>
## 🗺️ 8 · 综述与工具教程

| 资源 | 查阅范围 |
|---|---|
| [ScaleLab 具身指南](https://scalelab-sjtu.github.io/embodied_guide.html) | 操作基座、仿真平台与全身运动的代表论文 |
| [Lumina 具身指南](https://lumina-embodied.ai/blog/eai-guide/) | 控制、MPC、模仿学习、强化学习与硬件 |
| [MLLM-HRC](../../resources/zh/SURVEYS.md#s07) · [HRI 系统综述](../../resources/zh/SURVEYS.md#s09) | 人机协作框架与实验设计 |
| [LeRobot](../../resources/zh/CATALOG.md#e19) · [模仿学习教程](https://huggingface.co/docs/lerobot/en/il_robots) · [SO-101](https://huggingface.co/docs/lerobot/en/so101) | 数据录制、训练、设备适配与执行 |
| [MIT Underactuated Robotics](https://underactuated.mit.edu/) | 动力学、控制与轨迹优化 |

<a id="concepts"></a>
<details>
<summary>术语速查：任务、策略与控制</summary>

| 层次 | 输入 → 输出 |
|---|---|
| 任务规划 | 用户请求、场景与执行反馈 → 子任务、技能或约束 |
| 动作策略 | 图像、状态与任务条件 → 动作或动作块 |
| 强化学习 | 环境轨迹与奖励 → 更新后的策略 |
| MPC | 状态、动力学模型与约束 → 滚动优化的短时控制序列 |
| 设备控制 | 位置、速度或关节目标 → 电机执行与状态反馈 |

</details>
