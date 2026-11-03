# 04 · Edge & Embodied Interaction

[中文](../zh/04-Edge-Embodied-Interaction.md) | **English**

[Home](../../README.en.md) · [Full catalog](../../resources/en/CATALOG.md)

[Action foundations](#bases) → [Language feedback](#bridges) → [Audio and speech interaction](#audio) → [Industry systems](#systems) · [Data and training](#training) · [Evaluation and deployment](#evaluation) · [Further reading](#research) · [Surveys and tutorials](#tutorials)

Start with π0 as a concrete action model, with π0.5 as a companion on generalization training. Then examine how language feedback, audio inputs, and real-time interaction affect action execution.

<a id="bases"></a>
## 🦾 1 · Action foundations

| Category | Representative work | Core question |
|---|---|---|
| Manipulation VLAs | [π0](https://arxiv.org/abs/2410.24164) · [π0.5](https://arxiv.org/abs/2504.16054) | How do images, instructions, and robot state become manipulation actions? |
| Mobile navigation | [NaVILA](../../resources/en/CATALOG.md#e95) | How do language goals become spatial commands executed by a locomotion policy? |
| Whole-body motion | [ASAP](../../resources/en/CATALOG.md#e99) · [TWIST2](../../resources/en/CATALOG.md#e100) | How are human motion and teleoperation mapped to whole-body robot control? |

### Manipulation VLAs: π0 and π0.5

| Paper and official resources | Method | Reading focus |
|---|---|---|
| ⭐ [π0: A Vision-Language-Action Flow Model for General Robot Control](https://arxiv.org/abs/2410.24164)<br>[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://roboticsproceedings.org/rss21/p010.html) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.physicalintelligence.company/blog/pi0)<br>[Blog](https://www.physicalintelligence.company/blog/pi0) · [openpi code](https://github.com/Physical-Intelligence/openpi) | Combines a pretrained VLM and an action expert, predicting continuous action chunks through flow matching. | Priority reason: a concrete manipulation VLA connects vision/language inputs, action representations, and demonstration training. Focus on the architecture, inputs/outputs, and objective. |
| [π0.5: a Vision-Language-Action Model with Open-World Generalization](https://arxiv.org/abs/2504.16054)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2504.16054) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.physicalintelligence.company/blog/pi05)<br>[Blog](https://www.physicalintelligence.company/blog/pi05) · [openpi code](https://github.com/Physical-Intelligence/openpi) | Extends π0 with co-training on multiple robots, semantic subtasks, and web vision/language data. | Companion reading: how data sources correspond to training objectives, instruction following, and manipulation success in new environments. |

For an instruction such as “place the cup in the tray,” the action model receives camera images, the instruction, and robot state, then predicts a continuous action sequence. The execution system converts actions into device commands and provides new observations. An interaction module can revise goals, add constraints, or report execution outcomes.

Other manipulation foundations and adaptation methods: [OpenVLA](../../resources/en/CATALOG.md#e20) · [SmolVLA](../../resources/en/CATALOG.md#e34) · [Isaac GR00T N1.7](../../resources/en/CATALOG.md#e92). Implementations and training resources appear under [further reading](#research).

<a id="bridges"></a>
## 💬 2 · Language feedback and task revision

| Work / venue and affiliation | How interaction enters the action system | Reading focus |
|---|---|---|
| ⭐ [Hi Robot](../../resources/en/CATALOG.md#e25)<br>[![ICML 2025](https://img.shields.io/badge/ICML%202025-475569?style=flat-square)](https://proceedings.mlr.press/v267/shi25d.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.19417)<br>[📄 Paper](https://arxiv.org/abs/2502.19417) · [🔗 Project](https://www.pi.website/research/hirobot) | A high-level VLM uses instructions, the scene, and execution feedback to generate subtasks for a low-level VLA. | Priority reason: makes the planning–policy interface explicit. Focus on subtask updates after feedback and training data for each level. |
| [Yell At Your Robot / YAY Robot](../../resources/en/CATALOG.md#e26)<br>[![RSS 2024](https://img.shields.io/badge/RSS%202024-475569?style=flat-square)](https://roboticsproceedings.org/rss20/p025.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2403.12910)<br>[📄 Paper](https://arxiv.org/abs/2403.12910) · [💻 Code](https://github.com/yay-robot/yay_robot) | Accepts spoken corrections during execution and uses correction data for subsequent high-level policy training. | The relationship between immediate task revision, correction records, and post-training. |
| [Interactive Language / Language Table](../../resources/en/CATALOG.md#e13)<br>[![IEEE RA-L 2024](https://img.shields.io/badge/IEEE%20RA--L%202024-475569?style=flat-square)](https://doi.org/10.1109/LRA.2023.3295255) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2210.06407)<br>[📄 Paper](https://arxiv.org/abs/2210.06407) · [💻 Code](https://github.com/google-research/language-table) | Continuous language guidance changes the goal of a visuomotor policy. | Alignment between language annotations and robot trajectories, and experiments with instruction changes during execution. |

Language representations carry the main feedback in this group. Speaker identity, prosody, and environmental sound are additional inputs studied in the next group.

<a id="audio"></a>
## 🎧 3 · Audio inputs and speech–action interaction

| Work / venue and affiliation | Addition to language-conditioned action | Reading focus |
|---|---|---|
| ⭐ [VLAS](../../resources/en/CATALOG.md#e24)<br>[![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2025/hash/804a1a9de5787e3597b4bb64e1a48ec3-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.13508)<br>[📄 Paper](https://arxiv.org/abs/2502.13508) · [💻 Code](https://github.com/whichwhichgone/VLAS) | Adds a speech encoder to a visuomotor model and speaker retrieval for personalized manipulation. | Priority reason: a direct example of adding speech input to action prediction. Focus on encoder alignment, speech-instruction training, and personalized-task comparisons. |
| [RoboOmni (OpenMOSS)](../../resources/en/CATALOG.md#e21)<br>[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/33610fba262d7b6fed0810b89f55e147-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2510.23763)<br>[📄 Paper](https://arxiv.org/abs/2510.23763) · [💻 Code](https://github.com/OpenMOSS/RoboOmni) | Combines speech, environmental audio, vision, and actions to study contextual intent and proactive assistance. | OmniAction context construction and action outcomes under text, transcript, and audio conditions. |
| ⭐ [ELLSA](../../resources/en/CATALOG.md#e22)<br>[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/6d8af672c0bca7a4be6f0cd0d229c05c-Abstract-Conference.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.16756)<br>[📄 Paper](https://arxiv.org/abs/2510.16756) · [💻 Code](https://github.com/bytedance/SALMONN/tree/ELLSA) | Jointly models speech and action experts for concurrent speaking/acting, action interruption, and contextual questions. | Priority reason: brings real-time speech and action execution into one training framework. Focus on SA-MoE, staged adaptation, and interruption experiments. |
| [VITA-E](../../resources/en/CATALOG.md#e23)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.21817) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.21817)<br>[📄 Paper](https://arxiv.org/abs/2510.21817) · [💻 Code](https://github.com/Tencent/VITA/tree/VITA-E) | Uses active/listening models and control tokens to schedule speech and actions. | Concurrent interaction, task switching, control state, and action recovery. |

Comparisons concern task changes due to added information or timing mechanisms: manipulation success, recovery after corrections, personalized goal selection, and response latency during execution. Controlled comparisons distinguish the presence of an audio input from effective use of its information.

<a id="systems"></a>
## 🏭 4 · Industry systems and engineering implementations

| System / source | Interaction–action interface | Resource scope |
|---|---|---|
| [Reachy Mini Conversation App](../../resources/en/CATALOG.md#e11)<br>[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)<br>[💻 Code](https://github.com/pollen-robotics/reachy_mini_conversation_app) | Speech and camera tools connect to head and antenna movements. | Open application code for studying interaction state and tool execution. |
| [Gemini Live API × Robotics demo](../../resources/en/CATALOG.md#e27)<br>[![Technical Demo 2025](https://img.shields.io/badge/Technical%20Demo%202025-475569?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/)<br>[🔗 Project](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) | Audiovisual inputs connect to robot interfaces through function calls. | Official engineering example covering arguments, execution feedback, and error handling. |
| [WITA-Omni](../../resources/en/CATALOG.md#e10)<br>[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://www.agibot.com/article/231/detail/122.html) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.agibot.com/article/231/detail/122.html)<br>[🔗 Project](https://www.agibot.com/article/231/detail/122.html) | Combines scene perception, speech, and bodily expression. | Official demonstration of interaction and feedback design. |
| [Figure Helix 02](../../resources/en/CATALOG.md#e28)<br>[![Technical Demo 2026](https://img.shields.io/badge/Technical%20Demo%202026-475569?style=flat-square)](https://www.figure.ai/news/helix-02) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.figure.ai/news/helix-02)<br>[🔗 Project](https://www.figure.ai/news/helix-02) | Hierarchical semantic planning, visuomotor policies, and whole-body control. | Technical description and demonstration of high/low-level interfaces. |

<a id="training"></a>
## 🗂️ 5 · Data and model adaptation

| Training target | Sample contents | References |
|---|---|---|
| Action policy | Synchronized images, state, actions, task labels, and episode boundaries | [openpi custom-data fine-tuning](https://github.com/Physical-Intelligence/openpi#fine-tuning-base-models-on-your-own-data) · [LeRobotDataset v3](https://huggingface.co/docs/lerobot/en/lerobot-dataset-v3) |
| High-level tasks and corrections | Scene, task state, user feedback, and next subtask or skill | [Hi Robot](../../resources/en/CATALOG.md#e25) · [Yell At Your Robot / YAY Robot](../../resources/en/CATALOG.md#e26) |
| Speech-conditioned action | Audio, visual observations, language or identity conditions, and action demonstrations | [VLAS](../../resources/en/CATALOG.md#e24) · [RoboOmni (OpenMOSS)](../../resources/en/CATALOG.md#e21) |
| Real-time interaction | Audiovisual timestamps, speaking/listening states, action segments, interruptions, and recovery records | [ELLSA](../../resources/en/CATALOG.md#e22) · [VITA-E](../../resources/en/CATALOG.md#e23) |
| Simulation data | Task configurations, randomized scenes, and demonstration trajectories | [RoboTwin 2.0](../../resources/en/CATALOG.md#e101) |

Audio and tool events can be associated with robot data through episode identifiers and timestamps. Synthetic dialogue can supplement language and planning samples; action supervision requires demonstrations, simulation, or other grounded action data. Episode, scene, and object splits control leakage between adjacent frames.

Component validation can follow this sequence: an existing policy executes text instructions → an interaction module generates task requests → execution status returns to the interaction module. Action skills and language feedback use different supervision, such as action demonstrations and correction records.

<a id="evaluation"></a>
## 📊 6 · Benchmarks, edge deployment, and system evaluation

| Evaluation target | Dataset / resource | Metrics or comparisons |
|---|---|---|
| Language-conditioned manipulation | [LIBERO](../../resources/en/CATALOG.md#e35) · [RoboTwin 2.0](../../resources/en/CATALOG.md#e101) | Success rate, long-horizon completion, and scene/object generalization |
| Contributions of speech and context | Companion tasks from [VLAS](../../resources/en/CATALOG.md#e24) · [RoboOmni (OpenMOSS)](../../resources/en/CATALOG.md#e21) | Text/transcript/raw-audio conditions; identity and environmental-sound ablations |
| Effects of interaction on actions | Interaction experiments from [ELLSA](../../resources/en/CATALOG.md#e22) · [VITA-E](../../resources/en/CATALOG.md#e23) | Concurrent speaking/acting, action interruption, task switching, and recovery success |
| Language corrections and post-training | [Hi Robot](../../resources/en/CATALOG.md#e25) · [Yell At Your Robot / YAY Robot](../../resources/en/CATALOG.md#e26) | Task outcomes across feedback representations and training settings |
| Speech interaction components | [Voice Agent Benchmarks](05-Voice-Agent-Benchmarks.md) | Response content, turns, tool use, and interaction latency |

System reports distinguish model inference, audio playback, action dispatch, and robot execution latency. Stopping playback, cancelling a request, and physically stopping the robot have separate timestamps. Asynchronous execution also requires action-buffer updates and cancellation handling. Deployment locations can be identified as onboard, local workstation, or cloud.

Interfaces and deployment: [ROS 2 Actions](https://docs.ros.org/en/jazzy/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Actions/Understanding-ROS2-Actions.html) · [LeRobot asynchronous inference](https://huggingface.co/docs/lerobot/en/async) · [Unitree SDK2 / MuJoCo](../../resources/en/CATALOG.md#e97) · [llama.cpp ecosystem](../../resources/en/CATALOG.md#e17) · [MNN](../../resources/en/CATALOG.md#e18).

<a id="research"></a>
## 📚 7 · Further reading

<a id="policies"></a>
### Manipulation models and post-training

| Work | Topic | Reading focus |
|---|---|---|
| [ACT / ALOHA](../../resources/en/CATALOG.md#e32)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://www.roboticsproceedings.org/rss19/p016.pdf) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2304.13705)<br>[📄 Paper](https://arxiv.org/abs/2304.13705) · [💻 Code](https://github.com/tonyzhaozh/act) | Learning from demonstrations | Observation-conditioned action chunks and temporal ensembling. |
| [Diffusion Policy](../../resources/en/CATALOG.md#e33)<br>[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2303.04137)<br>[📄 Paper](https://arxiv.org/abs/2303.04137v4) · [💻 Code](https://github.com/real-stanford/diffusion_policy) | Diffusion policies | Continuous multimodal action distributions and visual conditioning. |
| [OpenVLA](../../resources/en/CATALOG.md#e20)<br>[![CoRL 2024](https://img.shields.io/badge/CoRL%202024-475569?style=flat-square)](https://proceedings.mlr.press/v270/kim25c.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2406.09246)<br>[📄 Paper](https://arxiv.org/abs/2406.09246) · [💻 Code](https://github.com/openvla/openvla) | General manipulation VLA | Pretrained vision/language representations and discrete action prediction. |
| [SmolVLA](../../resources/en/CATALOG.md#e34)<br>[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2506.01844) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2506.01844)<br>[📄 Paper](https://arxiv.org/abs/2506.01844) · [💻 Code](https://github.com/huggingface/lerobot) | Lightweight VLA | Text-conditioned actions and robot-data adaptation. |
| [Isaac GR00T N1.7](../../resources/en/CATALOG.md#e92)<br>[![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/NVIDIA/Isaac-GR00T)<br>[💻 Code](https://github.com/NVIDIA/Isaac-GR00T) | Industrial VLA | Embodiment configuration, action spaces, and checkpoint adaptation. |
| [OpenVLA-OFT](../../resources/en/CATALOG.md#e93)<br>[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://roboticsproceedings.org/rss21/p017.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.19645)<br>[📄 Paper](https://arxiv.org/abs/2502.19645) · [💻 Code](https://github.com/moojink/openvla-oft) | Efficient OpenVLA adaptation | Parallel decoding, action chunks, continuous actions, and FiLM. |
| [SimpleVLA-RL](../../resources/en/CATALOG.md#e94)<br>[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/cbfbcb4da14235bd69b134070898ae9d-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2509.09674)<br>[📄 Paper](https://arxiv.org/abs/2509.09674) · [💻 Code](https://github.com/PRIME-RL/SimpleVLA-RL) | VLA reinforcement learning | SFT policies, environment rewards, and online rollouts. |
| [RDT-1B](../../resources/en/CATALOG.md#e102)<br>[![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://github.com/thu-ml/RoboticsDiffusionTransformer) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2410.07864)<br>[📄 Paper](https://arxiv.org/abs/2410.07864) · [💻 Code](https://github.com/thu-ml/RoboticsDiffusionTransformer) | Bimanual diffusion foundation | Cross-embodiment action representations and bimanual demonstrations. |

Adaptation tutorials: [SmolVLA](https://huggingface.co/docs/lerobot/en/smolvla) · [GR00T new-embodiment fine-tuning](https://github.com/NVIDIA/Isaac-GR00T/blob/main/getting_started/finetune_new_embodiment.md).

<a id="navigation"></a>
### Navigation and whole-body motion

| Work | Reading focus |
|---|---|
| [NaVILA](../../resources/en/CATALOG.md#e95)<br>[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://navila-bot.github.io/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2412.04453)<br>[📄 Paper](https://arxiv.org/abs/2412.04453) · [💻 Code](https://github.com/AnjieCheng/NaVILA) | Interface between high-level spatial language and low-level visuomotor policies. |
| [Qwen-RobotNav](../../resources/en/CATALOG.md#e96)<br>[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.18112) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2606.18112)<br>[📄 Paper](https://arxiv.org/abs/2606.18112) · [💻 Code](https://github.com/QwenLM/Qwen-RobotNav) | Navigation system and waypoint interfaces as an industrial deployment case. |
| [ASAP](../../resources/en/CATALOG.md#e99)<br>[![RSS 2025](https://img.shields.io/badge/RSS%202025-475569?style=flat-square)](https://agile.human2humanoid.com/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.01143)<br>[📄 Paper](https://arxiv.org/abs/2502.01143) · [💻 Code](https://github.com/LeCAR-Lab/ASAP) | Simulation–real dynamics differences and motion-policy adaptation. |
| [TWIST2](../../resources/en/CATALOG.md#e100)<br>[![ICRA 2026](https://img.shields.io/badge/ICRA%202026-475569?style=flat-square)](https://yanjieze.com/projects/TWIST2/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2511.02832)<br>[📄 Paper](https://arxiv.org/abs/2511.02832) · [💻 Code](https://github.com/amazon-far/TWIST2) | Whole-body teleoperation, motion tracking, and demonstration collection. |
| [Unitree RL mjlab](../../resources/en/CATALOG.md#e98)<br>[![Project 2026](https://img.shields.io/badge/Project%202026-475569?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/unitreerobotics/unitree_rl_mjlab)<br>[💻 Code](https://github.com/unitreerobotics/unitree_rl_mjlab) | Robot configurations, rewards, simulation playback, and locomotion deployment. |

Locomotion and simulation: [legged-loco](https://github.com/yang-zj1026/legged-loco) · [Unitree MuJoCo](https://github.com/unitreerobotics/unitree_mujoco) · [Python SDK](https://github.com/unitreerobotics/unitree_sdk2_python).

<a id="tutorials"></a>
## 🗺️ 8 · Surveys and tool tutorials

| Resource | Reference scope |
|---|---|
| [ScaleLab embodied guide](https://scalelab-sjtu.github.io/embodied_guide.html) | Representative manipulation foundations, simulation platforms, and whole-body motion papers |
| [Lumina embodied guide](https://lumina-embodied.ai/blog/eai-guide/) | Control, MPC, imitation learning, reinforcement learning, and hardware |
| [MLLM-HRC](../../resources/en/SURVEYS.md#s07) · [HRI systems survey](../../resources/en/SURVEYS.md#s09) | Human–robot collaboration frameworks and study design |
| [LeRobot](../../resources/en/CATALOG.md#e19) · [Imitation-learning tutorial](https://huggingface.co/docs/lerobot/en/il_robots) · [SO-101](https://huggingface.co/docs/lerobot/en/so101) | Data recording, training, device adaptation, and execution |
| [MIT Underactuated Robotics](https://underactuated.mit.edu/) | Dynamics, control, and trajectory optimization |

<a id="concepts"></a>
<details>
<summary>Terminology: tasks, policies, and control</summary>

| Layer | Input → output |
|---|---|
| Task planning | Requests, scene, and execution feedback → subtasks, skills, or constraints |
| Action policy | Images, state, and task conditions → actions or action chunks |
| Reinforcement learning | Environment trajectories and rewards → updated policy |
| MPC | State, dynamics model, and constraints → receding-horizon control sequence |
| Device control | Position, velocity, or joint targets → motor execution and state feedback |

</details>
