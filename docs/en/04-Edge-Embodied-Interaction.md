# 04 · Edge and Embodied Interaction

[中文](../zh/04-Edge-Embodied-Interaction.md) | **English**

[Home](../../README.en.md) · [Catalog](../../resources/en/CATALOG.md) · [Surveys](../../resources/en/SURVEYS.md)

[Tutorials](#tutorials) · [Core concepts](#concepts) · [Action learning](#policies) · [Industry bases](#bases) · [Academic follow-ups](#research) · [Navigation](#navigation) · [Connecting language and action](#bridges) · [Data and training](#training) · [Deployment and evaluation](#evaluation)

Robot systems commonly separate interaction and action into layers: voice interaction interprets the request; a task layer selects goals and skills; an action policy predicts actions from images and robot state; and a controller executes them on the device. Visual observations, execution state, and task outcomes return to the interaction layer. Joint speech–action models explore sharing representations and training objectives across some of these stages.

<a id="tutorials"></a>
## 🧰 Start with tutorials

| Reading | Official resource | What to learn |
|---|---|---|
| ⭐ Read first | [LeRobot real-robot imitation learning](https://huggingface.co/docs/lerobot/en/il_robots) | The complete sequence from teleoperation, recording, and inspecting data to training and running a policy. |
| ⭐ Read first | [SmolVLA blog](https://huggingface.co/blog/smolvla) · [Training tutorial](https://huggingface.co/docs/lerobot/en/smolvla) | Intuition for vision–language–action models and adapting a pretrained model. |
| ⭐ Read first | [LeRobotDataset v3](https://huggingface.co/docs/lerobot/en/lerobot-dataset-v3) | How videos, states, actions, episodes, and timestamps are organized. |
| | [SO-101](https://huggingface.co/docs/lerobot/en/so101) | Hardware and operation for a low-cost arm; existing robots can also use an adapter interface. |
| | [ROS 2 Actions](https://docs.ros.org/en/jazzy/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Actions/Understanding-ROS2-Actions.html) | Long-running task interfaces with goals, feedback, results, and cancellation. A device SDK can implement the same semantics. |
| | [LeRobot asynchronous inference](https://huggingface.co/docs/lerobot/en/async) | Separate policy inference from action execution; understand latency and action buffers. |

<a id="concepts"></a>
## 🧩 Tasks, policies, and control

Start with the Chinese [Lumina embodied AI guide](https://lumina-embodied.ai/blog/eai-guide/) and [ScaleLab guide](https://scalelab-sjtu.github.io/embodied_guide.html): they map control, imitation learning, RL, VLAs, data, and simulation to original resources.

| Layer | Input → output | First readings |
|---|---|---|
| Interaction and task planning | Speech, images, execution feedback → goals, skills, corrections | [Hi Robot](../../resources/en/CATALOG.md#e25), [YAY Robot](../../resources/en/CATALOG.md#e26) |
| Imitation learning / VLA | Demonstration images, states, instructions → actions or action chunks | [ACT](../../resources/en/CATALOG.md#e32), [SmolVLA](../../resources/en/CATALOG.md#e34), [OpenVLA-OFT](../../resources/en/CATALOG.md#e93) |
| Reinforcement learning | Environment interaction and rewards → a task policy | [Unitree RL mjlab](../../resources/en/CATALOG.md#e98), [SimpleVLA-RL](../../resources/en/CATALOG.md#e94) |
| MPC | State, dynamics, constraints → short-horizon actions, repeatedly replanned | [Lumina MPC section](https://lumina-embodied.ai/blog/eai-guide/#mpc), [MIT Underactuated Robotics](https://underactuated.mit.edu/) |
| Device control | Position, velocity, or joint commands → actuation and state feedback | [Unitree SDK2](../../resources/en/CATALOG.md#e97), [ROS 2 Actions](https://docs.ros.org/en/jazzy/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Actions/Understanding-ROS2-Actions.html) |

Learning a policy need not replace every control loop. For speech corrections, task switching, and proactive feedback, start with an established controller and place the trainable component at the task layer.

<a id="policies"></a>
## 🦾 Action-learning foundations

| Reading | Paper / project | Links and labels | Reading focus |
|---|---|---|---|
| ⭐ Read first | [ACT / ALOHA](../../resources/en/CATALOG.md#e32) | [📄 Paper](https://arxiv.org/abs/2304.13705) · [💻 Repository](https://github.com/tonyzhaozh/act)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://www.roboticsproceedings.org/rss19/p016.pdf) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2304.13705) | Learn action chunks from demonstrations: a direct starting point for robot imitation learning. |
| ⭐ Read first | [SmolVLA](../../resources/en/CATALOG.md#e34) | [📄 Paper](https://arxiv.org/abs/2506.01844) · [💻 Repository](https://github.com/huggingface/lerobot)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2506.01844) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2506.01844) | Fine-tune a pretrained vision–language–action model to connect text goals with actions. |
|  | [Diffusion Policy](../../resources/en/CATALOG.md#e33) | [📄 Paper](https://arxiv.org/abs/2303.04137v4) · [💻 Repository](https://github.com/real-stanford/diffusion_policy)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![IJRR 2024](https://img.shields.io/badge/IJRR%202024-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2303.04137) | Understand continuous, multimodal action distributions and diffusion policies. |
|  | [OpenVLA](../../resources/en/CATALOG.md#e20) | [📄 Paper](https://arxiv.org/abs/2406.09246) · [💻 Repository](https://github.com/openvla/openvla)<br>[![CoRL 2024](https://img.shields.io/badge/CoRL%202024-475569?style=flat-square)](https://proceedings.mlr.press/v270/kim25c.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2406.09246) | Understand how a VLM is extended to action prediction and the required training data. |
| ⭐ Read first | [LeRobot](../../resources/en/CATALOG.md#e19) | [📄 Paper](https://arxiv.org/abs/2602.22818) · [💻 Repository](https://github.com/huggingface/lerobot)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.22818) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2602.22818) | A unified entry point for data, policies, hardware adapters, and evaluation. |
|  | [LIBERO](../../resources/en/CATALOG.md#e35) | [📄 Paper](https://arxiv.org/abs/2306.03310) · [💻 Repository](https://github.com/Lifelong-Robot-Learning/LIBERO)<br>[![NeurIPS Datasets and Benchmarks 2023](https://img.shields.io/badge/NeurIPS%20Datasets%20and%20Benchmarks%202023-475569?style=flat-square)](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8c3c666820ea055a77726d66fc7d447f-Abstract-Datasets_and_Benchmarks.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2306.03310) | Use simulation to understand language-conditioned manipulation and success-rate measurement. |

ACT supports demonstration learning for fixed skills; the standard version is not language-conditioned. SmolVLA and OpenVLA condition on text instructions but still require adaptation to the robot's embodiment, observation format, and action space.

<a id="bases"></a>
## 🏭 Adaptable industry bases

| Paper / project | Publication and affiliation | Reading focus and resources |
|---|---|---|
| ⭐ [openpi / π0 · π0.5](../../resources/en/CATALOG.md#e91) | [![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2504.16054) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2504.16054) | Releases π0, π0-FAST, and π0.5 weights, inference, and adaptation code, connecting VLMs to continuous actions and multi-robot data.<br>[📄 Paper](https://arxiv.org/abs/2504.16054) · [💻 Repository](https://github.com/Physical-Intelligence/openpi) · [🔗 π0 paper](https://arxiv.org/abs/2410.24164) · [🔗 π0.5 blog](https://www.physicalintelligence.company/blog/pi05) |
| ⭐ [Isaac GR00T N1.7](../../resources/en/CATALOG.md#e92) | [![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T) | A 3B vision-language-action base with pretrained weights, new-embodiment data adaptation, and fine-tuning workflows.<br>[💻 Repository](https://github.com/NVIDIA/Isaac-GR00T) · [🔗 N1 background paper](https://arxiv.org/abs/2503.14734) |

| Base | Data and fine-tuning resources | First adaptation focus |
|---|---|---|
| openpi / π0 · π0.5 | [Official custom-data guide](https://github.com/Physical-Intelligence/openpi#fine-tuning-base-models-on-your-own-data) | Image/state/action mappings and normalization; start with one task. LoRA uses the JAX path. |
| Isaac GR00T N1.7 | [New-embodiment fine-tuning](https://github.com/NVIDIA/Isaac-GR00T/blob/main/getting_started/finetune_new_embodiment.md) | Embodiment, camera, and action-space configuration; distinguish base weights from robot-specific checkpoints. |
| SmolVLA / LeRobot | [Training tutorial](https://huggingface.co/docs/lerobot/en/smolvla) | Establish the full recording, training, and policy-playback workflow. |

<a id="research"></a>
## 🎓 Research on existing bases

| Paper / project | Publication and affiliation | Reading focus and resources |
|---|---|---|
| ⭐ [OpenVLA-OFT](../../resources/en/CATALOG.md#e93) | [![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://roboticsproceedings.org/rss21/p017.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.19645) | Builds on OpenVLA with parallel decoding, action chunks, continuous actions, L1 training, and FiLM for language control.<br>[📄 Paper](https://arxiv.org/abs/2502.19645) · [💻 Repository](https://github.com/moojink/openvla-oft) · [🔗 Project](https://openvla-oft.github.io/) |
| ⭐ [SimpleVLA-RL](../../resources/en/CATALOG.md#e94) | [![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/cbfbcb4da14235bd69b134070898ae9d-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2509.09674) | Applies RL to VLAs including OpenVLA-OFT, with training, rollout, and evaluation workflows for LIBERO and RoboTwin.<br>[📄 Paper](https://arxiv.org/abs/2509.09674) · [💻 Repository](https://github.com/PRIME-RL/SimpleVLA-RL) |
| [RDT-1B](../../resources/en/CATALOG.md#e102) | [![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://github.com/thu-ml/RoboticsDiffusionTransformer) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2410.07864) | A diffusion base for bimanual manipulation with a unified action representation and a lighter 170M variant.<br>[📄 Paper](https://arxiv.org/abs/2410.07864) · [💻 Repository](https://github.com/thu-ml/RoboticsDiffusionTransformer) |
| ⭐ [RoboTwin 2.0](../../resources/en/CATALOG.md#e101) | [![ICML 2026](https://img.shields.io/badge/ICML%202026-475569?style=flat-square)](https://github.com/RoboTwin-Platform/RoboTwin) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2506.18088) | Builds bimanual tasks through automated simulation data generation and domain randomization, with pre-collected trajectories.<br>[📄 Paper](https://arxiv.org/abs/2506.18088) · [💻 Repository](https://github.com/RoboTwin-Platform/RoboTwin) |

| Route | Inherited components | Research question | Practical sequence |
|---|---|---|---|
| OpenVLA → OpenVLA-OFT | Pretrained vision-language-action representations | Decoding, action representations, chunking, and language conditioning | Run a checkpoint → fine-tune a small task → ablate action/language design choices. |
| OpenVLA-OFT → SimpleVLA-RL | SFT policy and environment | Outcome rewards for completion and out-of-distribution generalization | Reproduce SFT → validate rewards and resets → small-scale rollouts. |
| Pretrained policies → custom manipulation data | RDT / SmolVLA / openpi | New embodiments, objects, and instructions | Validate action format → fix tasks → evaluate changed objects and instructions. |
| RoboTwin data → policy training | Released trajectories and tasks | Data variation, randomization, and generalization | Use released data before generating custom tasks. |

<a id="navigation"></a>
## 🐾 Mobility, navigation, and whole-body actions

| Paper / project | Publication and affiliation | Reading focus and resources |
|---|---|---|
| ⭐ [NaVILA](../../resources/en/CATALOG.md#e95) | [![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://navila-bot.github.io/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2412.04453) | A high-level VLA emits spatial-language commands for a low-level visual locomotion policy, with experiments on Go2 and other platforms.<br>[📄 Paper](https://arxiv.org/abs/2412.04453) · [💻 Repository](https://github.com/AnjieCheng/NaVILA) · [🔗 Locomotion](https://github.com/yang-zj1026/legged-loco) |
| ⭐ [Unitree SDK2 / MuJoCo](../../resources/en/CATALOG.md#e97) | [![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/unitreerobotics/unitree_sdk2) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/unitreerobotics/unitree_sdk2) | Unitree communication/control interfaces and a MuJoCo simulation entry point based on SDK2.<br>[💻 Repository](https://github.com/unitreerobotics/unitree_sdk2) · [🔗 Python SDK](https://github.com/unitreerobotics/unitree_sdk2_python) · [🔗 MuJoCo](https://github.com/unitreerobotics/unitree_mujoco) |
| ⭐ [Unitree RL mjlab](../../resources/en/CATALOG.md#e98) | [![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab) | MuJoCo/mjlab locomotion-policy training and deployment tools, including Go2 configurations.<br>[💻 Repository](https://github.com/unitreerobotics/unitree_rl_mjlab) |
| [ASAP](../../resources/en/CATALOG.md#e99) | [![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://agile.human2humanoid.com/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.01143) | Learns discrepancies between simulated and real dynamics from robot data to adapt whole-body motion policies.<br>[📄 Paper](https://arxiv.org/abs/2502.01143) · [💻 Repository](https://github.com/LeCAR-Lab/ASAP) |
| [TWIST2](../../resources/en/CATALOG.md#e100) | [![ICRA 2026](https://img.shields.io/badge/ICRA%202026-475569?style=flat-square)](https://yanjieze.com/projects/TWIST2/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2511.02832) | Whole-body teleoperation and motion tracking for collecting humanoid data with contact and bimanual coordination.<br>[📄 Paper](https://arxiv.org/abs/2511.02832) · [💻 Repository](https://github.com/amazon-far/TWIST2) · [🔗 TWIST](https://yanjieze.com/projects/TWIST/) |

Navigation turns goals into positions, paths, or spatial instructions; locomotion control executes them stably. Manipulation instead requires target objects, end-effector poses, and contact actions, with different data and evaluations.

- ⭐ [NaVILA](../../resources/en/CATALOG.md#e95): read the VLA/locomotion interface, navigation data, and feedback loop before low-level training.
- [Unitree RL mjlab](../../resources/en/CATALOG.md#e98): use simulation configurations to study observations, actions, rewards, and sim-to-real deployment.
- [ASAP](../../resources/en/CATALOG.md#e99) / [TWIST2](../../resources/en/CATALOG.md#e100): advance to whole-body transfer, teleoperation, and demonstration collection.
- [Qwen-RobotNav](../../resources/en/CATALOG.md#e96): an industry navigation-system report and deployment case; weights are currently unavailable.

<a id="bridges"></a>
## 🔗 Connecting interaction to action

| Connection | Representative work / venue | Reading focus | Evaluation focus |
|---|---|---|---|
| Language guidance during execution | [Interactive Language / Language Table](../../resources/en/CATALOG.md#e13) · IEEE RA-L 2024 | How language instructions change an ongoing visuomotor policy | Language feedback does not automatically preserve raw voice characteristics or prosody. |
| High-level reasoning + low-level policy | ⭐ [Hi Robot](../../resources/en/CATALOG.md#e25) · ICML 2025 | Translating complex instructions and feedback into the next action task | Evaluate high-level planning and action execution separately. |
| Spoken corrections for post-training | ⭐ [Yell At Your Robot / YAY Robot](../../resources/en/CATALOG.md#e26) · RSS 2024 | Linking corrections to the current task and subsequent policy learning | Separate improvements in high-level decisions from improvements in low-level skills. |
| Raw-speech-conditioned actions | [VLAS](../../resources/en/CATALOG.md#e24) · ICLR 2025 | Speech, speaker identity, and personalized manipulation | Raw speech inputs and full-duplex control are different capabilities. |
| Environmental sound, dialogue, and vision | ⭐ [RoboOmni (OpenMOSS)](../../resources/en/CATALOG.md#e21) · ICLR 2026 | Implicit intent, situational awareness, and proactive assistance | Match claimed gains to the paper's tasks, input comparisons, and ablations. |
| Joint speech and action modeling | ⭐ [ELLSA](../../resources/en/CATALOG.md#e22) · ICLR 2026; [VITA-E](../../resources/en/CATALOG.md#e23) · arXiv 2025 | Training and scheduling speech, actions, listening, and interruptions | Joint modeling does not guarantee gains on every task. |
| Existing model + robot interface | [Reachy Mini Conversation App](../../resources/en/CATALOG.md#e11); [Gemini Live API example](../../resources/en/CATALOG.md#e27) | From voice and camera inputs to tool execution | Distinguish engineering demonstrations from controlled task-success experiments. |

<a id="training"></a>
## 🗂️ Data and post-training

| Layer | Data | Training or implementation objective | References |
|---|---|---|---|
| Action skills | Synchronized images, robot state, executed actions, task labels, and episode boundaries | ACT imitation learning or policy fine-tuning such as SmolVLA | [LeRobot data](https://huggingface.co/docs/lerobot/en/lerobot-dataset-v3), [ACT / ALOHA](../../resources/en/CATALOG.md#e32), [SmolVLA](../../resources/en/CATALOG.md#e34) |
| Tasks and feedback | Current scene, dialogue, task state, corrections, and the next valid skill | Task planning and feedback use; supervised fine-tuning of a trainable high-level model | [Hi Robot](../../resources/en/CATALOG.md#e25), [Yell At Your Robot / YAY Robot](../../resources/en/CATALOG.md#e26) |
| Real-time interaction | Audio timestamps, turns, interruption events, task versions, and execution feedback | Turn management, invalidating stale results, pausing, and resuming | [FireRedChat](../../resources/en/CATALOG.md#e29), [Jarvis](../../resources/en/CATALOG.md#e31) |
| Joint speaking and acting | Aligned visual, speech, text, and action sequences | Joint cross-modal objectives and temporal scheduling | [ELLSA](../../resources/en/CATALOG.md#e22), [VITA-E](../../resources/en/CATALOG.md#e23) |
| Policy RL | Simulation trajectories, outcomes, rewards, reset states, termination flags | Optimize environment rewards from an SFT policy | [SimpleVLA-RL](../../resources/en/CATALOG.md#e94) |

Audio and tool events can be stored alongside standard LeRobot data and aligned by episode and timestamp. Synthetic dialogue can supplement planning examples but cannot supply real robot-action labels by itself. Split training and evaluation by complete episodes, scenes, and objects to avoid leakage from neighboring frames.

A basic implementation sequence is to verify that text commands can invoke fixed skills, collect demonstrations and train an action policy, then connect speech and execution feedback. Add action demonstrations when manipulation fails; train the task layer when task understanding or use of corrections fails. These problems require different data.

<a id="evaluation"></a>
## ⏱️ Edge deployment and evaluation

| Concern | Entry points | What to record |
|---|---|---|
| Model and device compatibility | [MiniCPM-o 4.5](../../resources/en/CATALOG.md#e01), [MNN](../../resources/en/CATALOG.md#e18), [llama.cpp ecosystem](../../resources/en/CATALOG.md#e17) | Actual device, mode, quantization, memory, frame rate, and concurrent audio–video workloads. |
| Policy execution | [LeRobot asynchronous inference](https://huggingface.co/docs/lerobot/en/async) | Inference frequency, control frequency, action-chunk length, buffering, and stale state. |
| Action capability | [LIBERO](../../resources/en/CATALOG.md#e35), a fixed real-robot task set | Task success, correct target selection, human intervention, and recovery success. |
| Voice interaction | [Full-Duplex-Bench](../../resources/en/CATALOG.md#e16) | False interruptions, turn transitions, and response latency. |
| Human collaboration | [HRI systematic review](../../resources/en/SURVEYS.md#s09) | Task completion, interaction burden, participants, and experimental conditions. |

Stopping speech playback, canceling a task request, and the robot physically stopping are three events. Record their trigger and acknowledgment times separately; asynchronous inference does not automatically clear stale action buffers.

State whether computation runs on the robot, a local-network workstation, or in the cloud. Whole-system real-time performance requires measurement with audio, vision, policy inference, and control running together.

## 📚 Guides and surveys

[Lumina embodied AI guide](https://lumina-embodied.ai/blog/eai-guide/) · [ScaleLab guide](https://scalelab-sjtu.github.io/embodied_guide.html) · [MLLM-HRC](../../resources/en/SURVEYS.md#s07) · [HRI systematic review](../../resources/en/SURVEYS.md#s09). The two guides provide maps of control, VLAs, data, and simulation; follow the original papers and repositories in the tables for methods and experiments.
