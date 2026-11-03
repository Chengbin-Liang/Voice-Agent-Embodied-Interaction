# 04 · 端侧与具身交互

**中文** | [English](../en/04-Edge-Embodied-Interaction.md)

[返回首页](../../README.md) · [完整索引](../../resources/zh/CATALOG.md) · [Survey 对照](../../resources/zh/SURVEYS.md)

[入门教程](#tutorials) · [基础概念](#concepts) · [动作学习](#policies) · [工业基座](#bases) · [学术进阶](#research) · [移动与导航](#navigation) · [语言与动作的连接](#bridges) · [数据与训练](#training) · [端侧与评测](#evaluation)

机器人系统通常把交互与动作分层处理：语音交互理解请求，任务层选择目标和技能，动作策略根据图像与机器人状态预测动作，控制器把动作落实到设备。视觉、执行状态和任务结果再返回交互层。联合语音动作模型则尝试让部分环节共享表示与训练目标。

<a id="tutorials"></a>
## 🧰 先读教程

| 阅读 | 官方入口 | 能学到什么 |
|---|---|---|
| ⭐ 优先阅读 | [Lumina 具身指南](https://lumina-embodied.ai/blog/eai-guide/) | 先看模型与控制、模仿学习、强化学习、MPC，建立具身系统的地图。 |
| ⭐ 优先阅读 | [ScaleLab 具身指南](https://scalelab-sjtu.github.io/embodied_guide.html) | 沿 VLA、数据与仿真、全身控制找到原论文及项目。 |
| ⭐ 优先阅读 | [LeRobot 真机模仿学习](https://huggingface.co/docs/lerobot/en/il_robots) | 从遥操作、录制和查看数据，到训练及执行策略的完整顺序。 |
| ⭐ 优先阅读 | [SmolVLA 博客](https://huggingface.co/blog/smolvla) · [训练教程](https://huggingface.co/docs/lerobot/en/smolvla) | 视觉语言动作模型的直觉及预训练模型适配路径。 |
| ⭐ 优先阅读 | [LeRobotDataset v3](https://huggingface.co/docs/lerobot/en/lerobot-dataset-v3) | 视频、状态、动作、episode 与时间信息如何组织。 |
| | [SO-101](https://huggingface.co/docs/lerobot/en/so101) | 低成本机械臂的硬件与操作入口；已有机器人也可接适配接口。 |
| | [ROS 2 Actions](https://docs.ros.org/en/jazzy/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Actions/Understanding-ROS2-Actions.html) | goal、feedback、result 与 cancel 的长任务接口；也可使用设备 SDK 实现这些语义。 |
| | [LeRobot 异步推理](https://huggingface.co/docs/lerobot/en/async) | 分离策略推理与动作执行，理解时延和动作缓冲。 |

<a id="concepts"></a>
## 🧩 任务、策略与控制分别解决什么

| 层次 | 输入 → 输出 | 先读什么 |
|---|---|---|
| 交互与任务规划 | 语音、图像、执行反馈 → 目标、技能、纠正 | [Hi Robot](../../resources/zh/CATALOG.md#e25)、[YAY Robot](../../resources/zh/CATALOG.md#e26) |
| 模仿学习 / VLA | 示范中的图像、状态、指令 → 动作或动作块 | [ACT](../../resources/zh/CATALOG.md#e32)、[SmolVLA](../../resources/zh/CATALOG.md#e34)、[OpenVLA-OFT](../../resources/zh/CATALOG.md#e93) |
| 强化学习 | 环境交互、奖励 → 能完成任务的策略 | [Unitree RL mjlab](../../resources/zh/CATALOG.md#e98)、[SimpleVLA-RL](../../resources/zh/CATALOG.md#e94) |
| MPC | 当前状态、动力学模型、约束 → 规划短时动作并滚动重算 | [Lumina MPC 小节](https://lumina-embodied.ai/blog/eai-guide/#mpc)、[MIT Underactuated Robotics](https://underactuated.mit.edu/) |
| 设备控制 | 目标位置、速度或关节命令 → 电机执行与状态反馈 | [Unitree SDK2](../../resources/zh/CATALOG.md#e97)、[ROS 2 Actions](https://docs.ros.org/en/jazzy/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Actions/Understanding-ROS2-Actions.html) |

学习动作策略并不要求重做所有控制环节。研究语音纠正、任务切换和主动反馈时，可先复用成熟控制器，把可学习部分放在任务层。

<a id="policies"></a>
## 🦾 动作学习基础

| 阅读 | 文章 / 项目 | 入口与标签 | 阅读重点 |
|---|---|---|---|
| ⭐ 优先阅读 | [ACT / ALOHA](../../resources/zh/CATALOG.md#e32) | [📄 论文](https://arxiv.org/abs/2304.13705) · [💻 仓库](https://github.com/tonyzhaozh/act)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://www.roboticsproceedings.org/rss19/p016.pdf) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2304.13705) | 从示范学习动作块；理解机器人模仿学习最直接的起点。 |
| ⭐ 优先阅读 | [SmolVLA](../../resources/zh/CATALOG.md#e34) | [📄 论文](https://arxiv.org/abs/2506.01844) · [💻 仓库](https://github.com/huggingface/lerobot)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2506.01844) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2506.01844) | 在预训练视觉语言动作模型上微调，连接文本目标与动作。 |
|  | [Diffusion Policy](../../resources/zh/CATALOG.md#e33) | [📄 论文](https://arxiv.org/abs/2303.04137v4) · [💻 仓库](https://github.com/real-stanford/diffusion_policy)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![IJRR 2024](https://img.shields.io/badge/IJRR%202024-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2303.04137) | 理解连续、多峰动作分布和扩散策略。 |
|  | [OpenVLA](../../resources/zh/CATALOG.md#e20) | [📄 论文](https://arxiv.org/abs/2406.09246) · [💻 仓库](https://github.com/openvla/openvla)<br>[![CoRL 2024](https://img.shields.io/badge/CoRL%202024-475569?style=flat-square)](https://proceedings.mlr.press/v270/kim25c.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2406.09246) | 理解 VLM 如何扩展为动作预测及其训练数据。 |
| ⭐ 优先阅读 | [LeRobot](../../resources/zh/CATALOG.md#e19) | [📄 论文](https://arxiv.org/abs/2602.22818) · [💻 仓库](https://github.com/huggingface/lerobot)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.22818) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2602.22818) | 数据、策略、硬件适配及评测的统一工具入口。 |
|  | [LIBERO](../../resources/zh/CATALOG.md#e35) | [📄 论文](https://arxiv.org/abs/2306.03310) · [💻 仓库](https://github.com/Lifelong-Robot-Learning/LIBERO)<br>[![NeurIPS Datasets and Benchmarks 2023](https://img.shields.io/badge/NeurIPS%20Datasets%20and%20Benchmarks%202023-475569?style=flat-square)](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8c3c666820ea055a77726d66fc7d447f-Abstract-Datasets_and_Benchmarks.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2306.03310) | 在仿真中先理解语言条件操作任务与成功率统计。 |

ACT 适合固定技能的示范学习；标准版本不以语言为条件。SmolVLA、OpenVLA 提供文本指令条件，仍需适配机器人本体、观测格式和动作空间。

<a id="bases"></a>
## 🏭 可适配的工业基座

| 论文 / 项目 | 发表与来源 | 阅读重点与入口 |
|---|---|---|
| ⭐ [openpi / π0 · π0.5](../../resources/zh/CATALOG.md#e91) | [![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2504.16054) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2504.16054) | 开放 π0、π0-FAST 与 π0.5 的权重、推理和适配代码，连接 VLM、连续动作与多机器人数据。<br>[📄 论文](https://arxiv.org/abs/2504.16054) · [💻 仓库](https://github.com/Physical-Intelligence/openpi) · [🔗 π0 paper](https://arxiv.org/abs/2410.24164) · [🔗 π0.5 blog](https://www.physicalintelligence.company/blog/pi05) |
| ⭐ [Isaac GR00T N1.7](../../resources/zh/CATALOG.md#e92) | [![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T) | 3B 视觉语言动作基座，提供预训练权重、新本体数据适配和微调流程。<br>[💻 仓库](https://github.com/NVIDIA/Isaac-GR00T) · [🔗 N1 background paper](https://arxiv.org/abs/2503.14734) |

| 基座 | 数据与微调入口 | 首次适配重点 |
|---|---|---|
| openpi / π0 · π0.5 | [官方自有数据训练指南](https://github.com/Physical-Intelligence/openpi#fine-tuning-base-models-on-your-own-data) | 图像、状态、动作的映射与归一化；先做单任务适配。LoRA 使用 JAX 路径。 |
| Isaac GR00T N1.7 | [新本体微调](https://github.com/NVIDIA/Isaac-GR00T/blob/main/getting_started/finetune_new_embodiment.md) | 配置本体、相机和动作空间；区分预训练模型与针对特定机器人的检查点。 |
| SmolVLA / LeRobot | [训练教程](https://huggingface.co/docs/lerobot/en/smolvla) | 从录制数据、训练到策略回放，适合先建立完整流程。 |

<a id="research"></a>
## 🎓 从现成基座继续研究

| 论文 / 项目 | 发表与来源 | 阅读重点与入口 |
|---|---|---|
| ⭐ [OpenVLA-OFT](../../resources/zh/CATALOG.md#e93) | [![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://roboticsproceedings.org/rss21/p017.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.19645) | 基于 OpenVLA，比较并行解码、动作块、连续动作和 L1 目标，并用 FiLM 改善语言控制。<br>[📄 论文](https://arxiv.org/abs/2502.19645) · [💻 仓库](https://github.com/moojink/openvla-oft) · [🔗 Project / 项目](https://openvla-oft.github.io/) |
| ⭐ [SimpleVLA-RL](../../resources/zh/CATALOG.md#e94) | [![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/cbfbcb4da14235bd69b134070898ae9d-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2509.09674) | 在 OpenVLA-OFT 等 VLA 上进行强化学习，提供 LIBERO / RoboTwin 的训练、rollout 与评测流程。<br>[📄 论文](https://arxiv.org/abs/2509.09674) · [💻 仓库](https://github.com/PRIME-RL/SimpleVLA-RL) |
| [RDT-1B](../../resources/zh/CATALOG.md#e102) | [![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://github.com/thu-ml/RoboticsDiffusionTransformer) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2410.07864) | 双臂操作的扩散基座，以统一动作表示处理多本体数据，并提供 170M 轻量版本。<br>[📄 论文](https://arxiv.org/abs/2410.07864) · [💻 仓库](https://github.com/thu-ml/RoboticsDiffusionTransformer) |
| ⭐ [RoboTwin 2.0](../../resources/zh/CATALOG.md#e101) | [![ICML 2026](https://img.shields.io/badge/ICML%202026-475569?style=flat-square)](https://github.com/RoboTwin-Platform/RoboTwin) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2506.18088) | 通过自动化仿真数据生成和领域随机化构建双臂操作任务，提供预采集轨迹。<br>[📄 论文](https://arxiv.org/abs/2506.18088) · [💻 仓库](https://github.com/RoboTwin-Platform/RoboTwin) |

| 路线 | 继承什么 | 论文进一步研究什么 | 实践顺序 |
|---|---|---|---|
| OpenVLA → OpenVLA-OFT | 预训练视觉语言动作表示 | 解码、动作表示、动作块与语言条件 | 运行检查点 → 小任务微调 → 对比动作与语言消融。 |
| OpenVLA-OFT → SimpleVLA-RL | SFT 策略与环境 | 用结果奖励改善完成率和分布外泛化 | 先复现 SFT → 验证奖励与环境重置 → 小规模 rollout。 |
| 预训练策略 → 自有操作数据 | RDT / SmolVLA / openpi | 新本体、新物体与新指令的适配 | 检查动作格式 → 固定任务 → 更换物体与指令评测。 |
| RoboTwin 数据 → 策略训练 | 已生成的轨迹与任务 | 数据变化、随机化与泛化 | 先用发布的数据，再做自定义任务生成。 |

<a id="navigation"></a>
## 🐾 移动、导航与全身动作

| 论文 / 项目 | 发表与来源 | 阅读重点与入口 |
|---|---|---|
| ⭐ [NaVILA](../../resources/zh/CATALOG.md#e95) | [![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://navila-bot.github.io/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2412.04453) | 高层 VLA 输出空间语言指令，低层视觉运动策略执行导航，提供 Go2 等平台实验。<br>[📄 论文](https://arxiv.org/abs/2412.04453) · [💻 仓库](https://github.com/AnjieCheng/NaVILA) · [🔗 Locomotion / 运动策略](https://github.com/yang-zj1026/legged-loco) |
| ⭐ [Unitree SDK2 / MuJoCo](../../resources/zh/CATALOG.md#e97) | [![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/unitreerobotics/unitree_sdk2) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/unitreerobotics/unitree_sdk2) | 宇树机器人通信与控制接口，并提供基于 SDK2 的 MuJoCo 仿真入口。<br>[💻 仓库](https://github.com/unitreerobotics/unitree_sdk2) · [🔗 Python SDK](https://github.com/unitreerobotics/unitree_sdk2_python) · [🔗 MuJoCo](https://github.com/unitreerobotics/unitree_mujoco) |
| ⭐ [Unitree RL mjlab](../../resources/zh/CATALOG.md#e98) | [![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab) | 基于 MuJoCo / mjlab 的运动策略训练与部署工具，包含 Go2 等机器人配置。<br>[💻 仓库](https://github.com/unitreerobotics/unitree_rl_mjlab) |
| [ASAP](../../resources/zh/CATALOG.md#e99) | [![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://agile.human2humanoid.com/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.01143) | 用真实机器人数据学习仿真与真实动力学差异，再适配全身动作策略。<br>[📄 论文](https://arxiv.org/abs/2502.01143) · [💻 仓库](https://github.com/LeCAR-Lab/ASAP) |
| [TWIST2](../../resources/zh/CATALOG.md#e100) | [![ICRA 2026](https://img.shields.io/badge/ICRA%202026-475569?style=flat-square)](https://yanjieze.com/projects/TWIST2/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2511.02832) | 全身遥操作与运动跟踪系统，为人形机器人收集复杂接触和双手协作数据。<br>[📄 论文](https://arxiv.org/abs/2511.02832) · [💻 仓库](https://github.com/amazon-far/TWIST2) · [🔗 TWIST / CoRL 2025](https://yanjieze.com/projects/TWIST/) |

导航把目标转成位置、路径或空间指令；运动控制负责稳定执行。机械臂操作则需要目标物体、末端位姿和接触动作，两条路线的数据与评价不同。

- ⭐ [NaVILA](../../resources/zh/CATALOG.md#e95)：先看 VLA 与运动策略的接口、导航数据和闭环反馈，再读低层训练。
- [Unitree RL mjlab](../../resources/zh/CATALOG.md#e98)：用仿真配置学习观测、动作、奖励和 sim-to-real 流程。
- [ASAP](../../resources/zh/CATALOG.md#e99) / [TWIST2](../../resources/zh/CATALOG.md#e100)：深入全身运动迁移、遥操作和示范采集。
- [Qwen-RobotNav](../../resources/zh/CATALOG.md#e96)：工业导航系统报告与部署案例；官方当前没有开放权重。

<a id="bridges"></a>
## 🔗 从交互连接到动作

| 连接方式 | 代表工作 / 发表 | 阅读重点 | 评测时关注 |
|---|---|---|---|
| 执行中的语言指导 | [Interactive Language](../../resources/zh/CATALOG.md#e13) · IEEE RA-L 2024 | 语言指令如何改变正在执行的视觉运动策略 | 语言反馈不自动保留原始音色、韵律等信息。 |
| 高层推理 + 低层策略 | ⭐ [Hi Robot](../../resources/zh/CATALOG.md#e25) · ICML 2025 | 复杂指令与反馈转为下一步动作任务 | 高层规划与动作执行分层评价。 |
| 口头纠正进入后训练 | ⭐ [YAY Robot](../../resources/zh/CATALOG.md#e26) · RSS 2024 | 当前任务纠正与后续策略学习如何衔接 | 区分高层决策改善与低层技能改善。 |
| 原始语音条件动作 | [VLAS](../../resources/zh/CATALOG.md#e24) · ICLR 2025 | 语音、声纹与个性化操作 | 原始语音输入与全双工控制是不同能力。 |
| 环境声音、对话与视觉 | ⭐ [RoboOmni / OpenMOSS](../../resources/zh/CATALOG.md#e21) · ICLR 2026 | 隐式意图、情境感知与主动协助 | 具体增益应对应论文任务、输入对照及消融。 |
| 语音与动作联合建模 | ⭐ [ELLSA](../../resources/zh/CATALOG.md#e22) · ICLR 2026；[VITA-E](../../resources/zh/CATALOG.md#e23) · arXiv 2025 | 说话、动作、监听与中断如何训练和调度 | 同时建模不是所有任务均获益的保证。 |
| 现有模型 + 机器人接口 | [Reachy Mini](../../resources/zh/CATALOG.md#e11)；[Gemini Live API 示例](../../resources/zh/CATALOG.md#e27) | 从语音和摄像头输入到工具执行 | 工程 Demo 与受控的任务成功率实验分别看待。 |

<a id="training"></a>
## 🗂️ 数据与后训练入口

| 层次 | 数据 | 训练或实现目标 | 参考 |
|---|---|---|---|
| 动作技能 | 同步图像、机器人状态、执行动作、任务标签、episode 边界 | ACT 模仿学习，或 SmolVLA 等策略微调 | [LeRobot 数据](https://huggingface.co/docs/lerobot/en/lerobot-dataset-v3)、[ACT](../../resources/zh/CATALOG.md#e32)、[SmolVLA](../../resources/zh/CATALOG.md#e34) |
| 任务与反馈 | 当前场景、对话、任务状态、纠正、下一步合法技能 | 任务规划与反馈利用；可训练的高层模型做监督微调 | [Hi Robot](../../resources/zh/CATALOG.md#e25)、[YAY Robot](../../resources/zh/CATALOG.md#e26) |
| 实时交互 | 音频时间戳、轮次、打断事件、任务版本、执行反馈 | 轮次管理、旧结果作废、暂停与恢复 | [FireRedChat](../../resources/zh/CATALOG.md#e29)、[Jarvis](../../resources/zh/CATALOG.md#e31) |
| 策略 RL | 仿真轨迹、任务结果、奖励、重置状态与终止标记 | 在 SFT 策略上优化环境奖励 | [SimpleVLA-RL](../../resources/zh/CATALOG.md#e94) |
| 联合说做 | 对齐的视觉、语音、文本与动作序列 | 研究跨模态联合目标与时序调度 | [ELLSA](../../resources/zh/CATALOG.md#e22)、[VITA-E](../../resources/zh/CATALOG.md#e23) |

LeRobot 的标准机器人数据之外，音频和工具事件可通过额外文件按 episode 与时间戳对齐。合成对话能补充规划样本，但不能凭空提供真实机器人动作标签。训练与评测应按完整 episode、场景和对象划分，避免相邻帧泄漏。

一个基础实现顺序是：先验证文本命令能调用固定技能，再采集示范训练动作策略，随后接入语音和执行反馈。操作能力不足时补充动作示范；任务理解或纠正利用不足时，再训练可学习的任务层。两类问题需要不同数据。

<a id="evaluation"></a>
## ⏱️ 端侧部署与评测

| 关注点 | 入口 | 记录内容 |
|---|---|---|
| 模型与设备适配 | [MiniCPM-o](../../resources/zh/CATALOG.md#e01)、[MNN](../../resources/zh/CATALOG.md#e18)、[llama.cpp](../../resources/zh/CATALOG.md#e17) | 实际设备、模式、量化、内存、帧率及音视频并发。 |
| 策略执行 | [LeRobot 异步推理](https://huggingface.co/docs/lerobot/en/async) | 推理频率、控制频率、动作块长度、缓冲与状态过期。 |
| 动作能力 | [LIBERO](../../resources/zh/CATALOG.md#e35)、固定真机任务集 | 任务成功率、目标是否正确、人工接管和恢复成功率。 |
| 语音交互 | [Full-Duplex-Bench](../../resources/zh/CATALOG.md#e16) | 误打断、轮次交接、响应时延。 |
| 真人协作 | [HRI 系统综述](../../resources/zh/SURVEYS.md#s09) | 任务完成、交互负担、参与者与实验条件。 |

停止语音播报、取消任务请求和机器人实际停止是三个事件。需要分别记录触发与确认时刻；异步推理本身不会自动清除旧动作缓冲。

端侧也应标清计算发生在机器人本体、局域网工作站还是云端。整机实时性取决于音频、视觉、策略与控制共同运行的测量结果。

## 📚 教程与综述入口

[Lumina 具身指南](https://lumina-embodied.ai/blog/eai-guide/) · [ScaleLab 具身指南](https://scalelab-sjtu.github.io/embodied_guide.html) · [MLLM-HRC](../../resources/zh/SURVEYS.md#s07) · [HRI 系统综述](../../resources/zh/SURVEYS.md#s09)。两份指南提供控制、VLA、数据和仿真等领域的阅读地图；具体方法、代码与实验沿表中原始来源阅读。
