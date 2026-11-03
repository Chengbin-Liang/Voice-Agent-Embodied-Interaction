# 04 · Edge and Embodied Interaction

[中文](04-Edge-Embodied-Interaction.md) | **English**

[Home](README.en.md) · [Catalog](CATALOG.en.md) · [Surveys](SURVEYS.en.md)

[Tutorials](#tutorials) · [Action learning](#policies) · [Connecting language and action](#bridges) · [Data and training](#training) · [Deployment and evaluation](#evaluation)

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

<a id="policies"></a>
## 🦾 Action-learning foundations

| Reading | Paper / project | Links and labels | Reading focus |
|---|---|---|---|
| ⭐ Read first | [ACT / ALOHA](CATALOG.en.md#e32) | [📄 Paper](https://arxiv.org/abs/2304.13705) · [💻 Repository](https://github.com/tonyzhaozh/act)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://www.roboticsproceedings.org/rss19/p016.pdf) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2304.13705) | Learn action chunks from demonstrations: a direct starting point for robot imitation learning. |
| ⭐ Read first | [SmolVLA](CATALOG.en.md#e34) | [📄 Paper](https://arxiv.org/abs/2506.01844) · [💻 Repository](https://github.com/huggingface/lerobot)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2506.01844) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2506.01844) | Fine-tune a pretrained vision–language–action model to connect text goals with actions. |
|  | [Diffusion Policy](CATALOG.en.md#e33) | [📄 Paper](https://arxiv.org/abs/2303.04137v4) · [💻 Repository](https://github.com/real-stanford/diffusion_policy)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![IJRR 2024](https://img.shields.io/badge/IJRR%202024-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2303.04137) | Understand continuous, multimodal action distributions and diffusion policies. |
|  | [OpenVLA](CATALOG.en.md#e20) | [📄 Paper](https://arxiv.org/abs/2406.09246) · [💻 Repository](https://github.com/openvla/openvla)<br>[![CoRL 2024](https://img.shields.io/badge/CoRL%202024-475569?style=flat-square)](https://proceedings.mlr.press/v270/kim25c.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2406.09246) | Understand how a VLM is extended to action prediction and the required training data. |
| ⭐ Read first | [LeRobot](CATALOG.en.md#e19) | [📄 Paper](https://arxiv.org/abs/2602.22818) · [💻 Repository](https://github.com/huggingface/lerobot)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.22818) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2602.22818) | A unified entry point for data, policies, hardware adapters, and evaluation. |
|  | [LIBERO](CATALOG.en.md#e35) | [📄 Paper](https://arxiv.org/abs/2306.03310) · [💻 Repository](https://github.com/Lifelong-Robot-Learning/LIBERO)<br>[![NeurIPS Datasets and Benchmarks 2023](https://img.shields.io/badge/NeurIPS%20Datasets%20and%20Benchmarks%202023-475569?style=flat-square)](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8c3c666820ea055a77726d66fc7d447f-Abstract-Datasets_and_Benchmarks.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2306.03310) | Use simulation to understand language-conditioned manipulation and success-rate measurement. |

ACT supports demonstration learning for fixed skills; the standard version is not language-conditioned. SmolVLA and OpenVLA condition on text instructions but still require adaptation to the robot's embodiment, observation format, and action space.

<a id="bridges"></a>
## 🔗 Connecting interaction to action

| Connection | Representative work / venue | Reading focus | Evidence boundary |
|---|---|---|---|
| Language guidance during execution | [Interactive Language / Language Table](CATALOG.en.md#e13) · IEEE RA-L 2024 | How language instructions change an ongoing visuomotor policy | Language feedback does not automatically preserve raw voice characteristics or prosody. |
| High-level reasoning + low-level policy | ⭐ [Hi Robot](CATALOG.en.md#e25) · ICML 2025 | Translating complex instructions and feedback into the next action task | Evaluate high-level planning and action execution separately. |
| Spoken corrections for post-training | ⭐ [Yell At Your Robot / YAY Robot](CATALOG.en.md#e26) · RSS 2024 | Linking corrections to the current task and subsequent policy learning | Separate improvements in high-level decisions from improvements in low-level skills. |
| Raw-speech-conditioned actions | [VLAS](CATALOG.en.md#e24) · ICLR 2025 | Speech, speaker identity, and personalized manipulation | Raw speech inputs and full-duplex control are different capabilities. |
| Environmental sound, dialogue, and vision | ⭐ [RoboOmni (OpenMOSS)](CATALOG.en.md#e21) · ICLR 2026 | Implicit intent, situational awareness, and proactive assistance | Match claimed gains to the paper's tasks, input comparisons, and ablations. |
| Joint speech and action modeling | ⭐ [ELLSA](CATALOG.en.md#e22) · ICLR 2026; [VITA-E](CATALOG.en.md#e23) · arXiv 2025 | Training and scheduling speech, actions, listening, and interruptions | Joint modeling does not guarantee gains on every task. |
| Existing model + robot interface | [Reachy Mini Conversation App](CATALOG.en.md#e11); [Gemini Live API example](CATALOG.en.md#e27) | From voice and camera inputs to tool execution | Distinguish engineering demonstrations from controlled task-success experiments. |

<a id="training"></a>
## 🗂️ Data and post-training

| Layer | Data | Training or implementation objective | References |
|---|---|---|---|
| Action skills | Synchronized images, robot state, executed actions, task labels, and episode boundaries | ACT imitation learning or policy fine-tuning such as SmolVLA | [LeRobot data](https://huggingface.co/docs/lerobot/en/lerobot-dataset-v3), [ACT / ALOHA](CATALOG.en.md#e32), [SmolVLA](CATALOG.en.md#e34) |
| Tasks and feedback | Current scene, dialogue, task state, corrections, and the next valid skill | Task planning and feedback use; supervised fine-tuning of a trainable high-level model | [Hi Robot](CATALOG.en.md#e25), [Yell At Your Robot / YAY Robot](CATALOG.en.md#e26) |
| Real-time interaction | Audio timestamps, turns, interruption events, task versions, and execution feedback | Turn management, invalidating stale results, pausing, and resuming | [FireRedChat](CATALOG.en.md#e29), [Jarvis](CATALOG.en.md#e31) |
| Joint speaking and acting | Aligned visual, speech, text, and action sequences | Joint cross-modal objectives and temporal scheduling | [ELLSA](CATALOG.en.md#e22), [VITA-E](CATALOG.en.md#e23) |

Audio and tool events can be stored alongside standard LeRobot data and aligned by episode and timestamp. Synthetic dialogue can supplement planning examples but cannot supply real robot-action labels by itself. Split training and evaluation by complete episodes, scenes, and objects to avoid leakage from neighboring frames.

A basic implementation sequence is to verify that text commands can invoke fixed skills, collect demonstrations and train an action policy, then connect speech and execution feedback. Add action demonstrations when manipulation fails; train the task layer when task understanding or use of corrections fails. These problems require different data.

<a id="evaluation"></a>
## ⏱️ Edge deployment and evaluation

| Concern | Entry points | What to record |
|---|---|---|
| Model and device compatibility | [MiniCPM-o 4.5](CATALOG.en.md#e01), [MNN](CATALOG.en.md#e18), [llama.cpp ecosystem](CATALOG.en.md#e17) | Actual device, mode, quantization, memory, frame rate, and concurrent audio–video workloads. |
| Policy execution | [LeRobot asynchronous inference](https://huggingface.co/docs/lerobot/en/async) | Inference frequency, control frequency, action-chunk length, buffering, and stale state. |
| Action capability | [LIBERO](CATALOG.en.md#e35), a fixed real-robot task set | Task success, correct target selection, human intervention, and recovery success. |
| Voice interaction | [Full-Duplex-Bench](CATALOG.en.md#e16) | False interruptions, turn transitions, and response latency. |
| Human collaboration | [HRI systematic review](SURVEYS.en.md#s09) | Task completion, interaction burden, participants, and experimental conditions. |

Stopping speech playback, canceling a task request, and the robot physically stopping are three events. Record their trigger and acknowledgment times separately; asynchronous inference does not automatically clear stale action buffers.

State whether computation runs on the robot, a local-network workstation, or in the cloud. Whole-system real-time performance requires measurement with audio, vision, policy inference, and control running together.
