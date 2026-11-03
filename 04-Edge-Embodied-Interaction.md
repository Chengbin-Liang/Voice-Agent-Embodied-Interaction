# 04 · 端侧与具身交互

[返回首页](README.md) · [完整索引](CATALOG.md) · [Survey 对照](SURVEYS.md)

[入门教程](#tutorials) · [动作学习](#policies) · [语言与动作的连接](#bridges) · [数据与训练](#training) · [端侧与评测](#evaluation)

机器人系统通常把交互与动作分层处理：语音交互理解请求，任务层选择目标和技能，动作策略根据图像与机器人状态预测动作，控制器把动作落实到设备。视觉、执行状态和任务结果再返回交互层。联合语音动作模型则尝试让部分环节共享表示与训练目标。

<a id="tutorials"></a>
## 🧰 先读教程

| 阅读 | 官方入口 | 能学到什么 |
|---|---|---|
| ⭐ 优先阅读 | [LeRobot 真机模仿学习](https://huggingface.co/docs/lerobot/en/il_robots) | 从遥操作、录制和查看数据，到训练及执行策略的完整顺序。 |
| ⭐ 优先阅读 | [SmolVLA 博客](https://huggingface.co/blog/smolvla) · [训练教程](https://huggingface.co/docs/lerobot/en/smolvla) | 视觉语言动作模型的直觉及预训练模型适配路径。 |
| ⭐ 优先阅读 | [LeRobotDataset v3](https://huggingface.co/docs/lerobot/en/lerobot-dataset-v3) | 视频、状态、动作、episode 与时间信息如何组织。 |
| | [SO-101](https://huggingface.co/docs/lerobot/en/so101) | 低成本机械臂的硬件与操作入口；已有机器人也可接适配接口。 |
| | [ROS 2 Actions](https://docs.ros.org/en/jazzy/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Actions/Understanding-ROS2-Actions.html) | goal、feedback、result 与 cancel 的长任务接口；也可使用设备 SDK 实现这些语义。 |
| | [LeRobot 异步推理](https://huggingface.co/docs/lerobot/en/async) | 分离策略推理与动作执行，理解时延和动作缓冲。 |

<a id="policies"></a>
## 🦾 动作学习基础

| 阅读 | 文章 / 项目 | 入口与标签 | 阅读重点 |
|---|---|---|---|
| ⭐ 优先阅读 | [ACT / ALOHA](CATALOG.md#e32) | [📄 论文](https://arxiv.org/abs/2304.13705) · [💻 仓库](https://github.com/tonyzhaozh/act)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://www.roboticsproceedings.org/rss19/p016.pdf) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2304.13705) | 从示范学习动作块；理解机器人模仿学习最直接的起点。 |
| ⭐ 优先阅读 | [SmolVLA](CATALOG.md#e34) | [📄 论文](https://arxiv.org/abs/2506.01844) · [💻 仓库](https://github.com/huggingface/lerobot)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2506.01844) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2506.01844) | 在预训练视觉语言动作模型上微调，连接文本目标与动作。 |
|  | [Diffusion Policy](CATALOG.md#e33) | [📄 论文](https://arxiv.org/abs/2303.04137v4) · [💻 仓库](https://github.com/real-stanford/diffusion_policy)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![IJRR 2024](https://img.shields.io/badge/IJRR%202024-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2303.04137) | 理解连续、多峰动作分布和扩散策略。 |
|  | [OpenVLA](CATALOG.md#e20) | [📄 论文](https://arxiv.org/abs/2406.09246) · [💻 仓库](https://github.com/openvla/openvla)<br>[![CoRL 2024](https://img.shields.io/badge/CoRL%202024-475569?style=flat-square)](https://proceedings.mlr.press/v270/kim25c.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2406.09246) | 理解 VLM 如何扩展为动作预测及其训练数据。 |
| ⭐ 优先阅读 | [LeRobot](CATALOG.md#e19) | [📄 论文](https://arxiv.org/abs/2602.22818) · [💻 仓库](https://github.com/huggingface/lerobot)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.22818) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2602.22818) | 数据、策略、硬件适配及评测的统一工具入口。 |
|  | [LIBERO](CATALOG.md#e35) | [📄 论文](https://arxiv.org/abs/2306.03310) · [💻 仓库](https://github.com/Lifelong-Robot-Learning/LIBERO)<br>[![NeurIPS Datasets and Benchmarks 2023](https://img.shields.io/badge/NeurIPS%20Datasets%20and%20Benchmarks%202023-475569?style=flat-square)](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8c3c666820ea055a77726d66fc7d447f-Abstract-Datasets_and_Benchmarks.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2306.03310) | 在仿真中先理解语言条件操作任务与成功率统计。 |

ACT 适合固定技能的示范学习；标准版本不以语言为条件。SmolVLA、OpenVLA 提供文本指令条件，仍需适配机器人本体、观测格式和动作空间。

<a id="bridges"></a>
## 🔗 从交互连接到动作

| 连接方式 | 代表工作 / 发表 | 阅读重点 | 证据边界 |
|---|---|---|---|
| 执行中的语言指导 | [Interactive Language](CATALOG.md#e13) · IEEE RA-L 2024 | 语言指令如何改变正在执行的视觉运动策略 | 语言反馈不自动保留原始音色、韵律等信息。 |
| 高层推理 + 低层策略 | ⭐ [Hi Robot](CATALOG.md#e25) · ICML 2025 | 复杂指令与反馈转为下一步动作任务 | 高层规划与动作执行分层评价。 |
| 口头纠正进入后训练 | ⭐ [YAY Robot](CATALOG.md#e26) · RSS 2024 | 当前任务纠正与后续策略学习如何衔接 | 区分高层决策改善与低层技能改善。 |
| 原始语音条件动作 | [VLAS](CATALOG.md#e24) · ICLR 2025 | 语音、声纹与个性化操作 | 原始语音输入与全双工控制是不同能力。 |
| 环境声音、对话与视觉 | ⭐ [RoboOmni / OpenMOSS](CATALOG.md#e21) · ICLR 2026 | 隐式意图、情境感知与主动协助 | 具体增益应对应论文任务、输入对照及消融。 |
| 语音与动作联合建模 | ⭐ [ELLSA](CATALOG.md#e22) · ICLR 2026；[VITA-E](CATALOG.md#e23) · arXiv 2025 | 说话、动作、监听与中断如何训练和调度 | 同时建模不是所有任务均获益的保证。 |
| 现有模型 + 机器人接口 | [Reachy Mini](CATALOG.md#e11)；[Gemini Live API 示例](CATALOG.md#e27) | 从语音和摄像头输入到工具执行 | 工程 Demo 与受控的任务成功率实验分别看待。 |

<a id="training"></a>
## 🗂️ 数据与后训练入口

| 层次 | 数据 | 训练或实现目标 | 参考 |
|---|---|---|---|
| 动作技能 | 同步图像、机器人状态、执行动作、任务标签、episode 边界 | ACT 模仿学习，或 SmolVLA 等策略微调 | [LeRobot 数据](https://huggingface.co/docs/lerobot/en/lerobot-dataset-v3)、[ACT](CATALOG.md#e32)、[SmolVLA](CATALOG.md#e34) |
| 任务与反馈 | 当前场景、对话、任务状态、纠正、下一步合法技能 | 任务规划与反馈利用；可训练的高层模型做监督微调 | [Hi Robot](CATALOG.md#e25)、[YAY Robot](CATALOG.md#e26) |
| 实时交互 | 音频时间戳、轮次、打断事件、任务版本、执行反馈 | 轮次管理、旧结果作废、暂停与恢复 | [FireRedChat](CATALOG.md#e29)、[Jarvis](CATALOG.md#e31) |
| 联合说做 | 对齐的视觉、语音、文本与动作序列 | 研究跨模态联合目标与时序调度 | [ELLSA](CATALOG.md#e22)、[VITA-E](CATALOG.md#e23) |

LeRobot 的标准机器人数据之外，音频和工具事件可通过额外文件按 episode 与时间戳对齐。合成对话能补充规划样本，但不能凭空提供真实机器人动作标签。训练与评测应按完整 episode、场景和对象划分，避免相邻帧泄漏。

一个基础实现顺序是：先验证文本命令能调用固定技能，再采集示范训练动作策略，随后接入语音和执行反馈。操作能力不足时补充动作示范；任务理解或纠正利用不足时，再训练可学习的任务层。两类问题需要不同数据。

<a id="evaluation"></a>
## ⏱️ 端侧部署与评测

| 关注点 | 入口 | 记录内容 |
|---|---|---|
| 模型与设备适配 | [MiniCPM-o](CATALOG.md#e01)、[MNN](CATALOG.md#e18)、[llama.cpp](CATALOG.md#e17) | 实际设备、模式、量化、内存、帧率及音视频并发。 |
| 策略执行 | [LeRobot 异步推理](https://huggingface.co/docs/lerobot/en/async) | 推理频率、控制频率、动作块长度、缓冲与状态过期。 |
| 动作能力 | [LIBERO](CATALOG.md#e35)、固定真机任务集 | 任务成功率、目标是否正确、人工接管和恢复成功率。 |
| 语音交互 | [Full-Duplex-Bench](CATALOG.md#e16) | 误打断、轮次交接、响应时延。 |
| 真人协作 | [HRI 系统综述](SURVEYS.md#s09) | 任务完成、交互负担、参与者与实验条件。 |

停止语音播报、取消任务请求和机器人实际停止是三个事件。需要分别记录触发与确认时刻；异步推理本身不会自动清除旧动作缓冲。

端侧也应标清计算发生在机器人本体、局域网工作站还是云端。整机实时性取决于音频、视觉、策略与控制共同运行的测量结果。
