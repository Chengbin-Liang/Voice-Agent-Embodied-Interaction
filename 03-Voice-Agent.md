# 03 · Voice Agent

[返回首页](README.md) · [完整索引](CATALOG.md) · [Survey 对照](SURVEYS.md) · [📏 Benchmark 导航](05-Voice-Agent-Benchmarks.md)

从语音对话能力进入交互策略、工具调用和任务完成。基础模型见 [Omni 基础](02-Omni-Foundations.md)；本页按可研究的问题组织论文，学术与校企合作工作优先展开。覆盖至 **2026-11-03**，包含 2026 年 10 月新预印本。

[🧭 选读路径](#route) · [🎓 学术与合作研究](#academic) · [🏭 工业研究](#industry) · [🛠️ 工程实现](#engineering) · [📏 评测](05-Voice-Agent-Benchmarks.md)

<a id="route"></a>
## 🧭 按问题选读

⭐ 表示建议先读，完整条目保留具体理由、机构、资源开放边界及 Star / Cite。无标记条目不作等级排名。

| 研究问题 | 首读入口 | 继续对照 |
|---|---|---|
| 语音模型怎样学会调用工具并利用结果？ | [VoxMind](CATALOG.md#e37) | [MoshiRAG](CATALOG.md#e48) · [Realtime-Venus](CATALOG.md#e54) · [Jarvis](CATALOG.md#e31) |
| 怎样控制打断、反馈、主动开场？ | [F-Actor](CATALOG.md#e38) | [BayLing-Duplex](CATALOG.md#e42) · [CF-Duplex / XA-Duplex](CATALOG.md#e40) |
| 训练数据从哪里来，如何保留时间关系？ | [SOMMELIER](CATALOG.md#e39) → [DuplexGen](CATALOG.md#e41) | [DuplexOmni](CATALOG.md#e58) · [MultiTalk / MultiTalkBench](CATALOG.md#e43) |
| 打断后记住什么，长对话如何继续？ | [Self-Listening / LoopSpeech](CATALOG.md#e44) | [MultiTalk / MultiTalkBench](CATALOG.md#e43) · [Jarvis](CATALOG.md#e31) |
| 如何复用现有模型并降低实时成本？ | [D2: Dialogue-to-Duplex](CATALOG.md#e45) | [TASTE2](CATALOG.md#e46) · [DiffuPlex · Rolling Masked Diffusion](CATALOG.md#e50) |
| 如何判断更会交互，也更能完成任务？ | [Full-Duplex-Bench-v3](CATALOG.md#e64) → [τ-Voice](CATALOG.md#e63) | [按能力选择 benchmark](05-Voice-Agent-Benchmarks.md#selection) |

<a id="academic"></a>
## 🎓 学术与校企合作研究

### 🧰 工具调用、检索与异步任务

| 文章 / 项目 | 发表与归属 | 阅读重点与资源 |
|---|---|---|
| ⭐ [VoxMind](CATALOG.md#e37) | [![ACL 2026](https://img.shields.io/badge/ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.acl-long.459/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2604.15710) | 用 AgentChat 数据、Think-before-Speak 与动态工具检索学习语音 Agent 的推理—调用—反馈闭环。<br>[📄 论文](https://arxiv.org/abs/2604.15710) · [💻 仓库](https://github.com/MM-Speech/VoxMind) |
| ⭐ [MoshiRAG](CATALOG.md#e48) | [![ICML 2026 · 作者标注](https://img.shields.io/badge/ICML%202026%20%C2%B7%20%E4%BD%9C%E8%80%85%E6%A0%87%E6%B3%A8-475569?style=flat-square)](https://arxiv.org/abs/2604.12928) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2604.12928) | 在全双工对话中异步触发检索并注入知识，观察检索耗时与持续对话如何协调。<br>[📄 论文](https://arxiv.org/abs/2604.12928) · [💻 仓库](https://github.com/kyutai-labs/moshi-rag) |
| ⭐ [DuplexOmni](CATALOG.md#e58) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.09186) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2606.09186) | 实时交互层与异步思考层协同，配合 Writer–Director 数据合成组织边听、边看、边想、边说。<br>[📄 论文](https://arxiv.org/abs/2606.09186) · [💻 仓库](https://github.com/MuyeHuang/DuplexOmni) |
| [Realtime-Venus](CATALOG.md#e54) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.13814) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.13814) | 实时交互层异步委托后台任务，结果返回后继续对话，连接多模态输入、训练策略与运行时。<br>[📄 论文](https://arxiv.org/abs/2609.13814) · [💻 仓库](https://github.com/inclusionAI/Realtime-Venus) |
| [DuplexSLA](CATALOG.md#e09) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2605.20755) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2605.20755) | 在共同时间线上输出语音及结构化 action 通道，研究交谈中的规划与工具调用。<br>[📄 论文](https://arxiv.org/abs/2605.20755) · [💻 仓库](https://github.com/hyzhang24/DuplexSLA) |
| [Jarvis](CATALOG.md#e31) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.23804) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2610.23804) | 在交互前端和后台任务之间训练协调器，管理任务切换、状态和过期结果。<br>[📄 论文](https://arxiv.org/abs/2610.23804) · [💻 仓库](https://github.com/JensenYX/Jarvis) |

### 🗣️ 交互策略、记忆与鲁棒性

| 文章 / 项目 | 发表与归属 | 阅读重点与资源 |
|---|---|---|
| ⭐ [F-Actor](CATALOG.md#e38) | [![Findings of ACL 2026](https://img.shields.io/badge/Findings%20of%20ACL%202026-475569?style=flat-square)](https://aclanthology.org/2026.findings-acl.242/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2601.11329) | 通过指令控制音色、话题、反馈、打断和主动开场；冻结音频编码器，采用单阶段训练。<br>[📄 论文](https://arxiv.org/abs/2601.11329) · [💻 仓库](https://github.com/MaikeZuefle/f-actor) |
| [BayLing-Duplex](CATALOG.md#e42) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.14528) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2606.14528) | 以单个自回归 LLM 和少量状态 token 联合建模听、说、停，通过 SFT 与 DPO 学习交互。<br>[📄 论文](https://arxiv.org/abs/2606.14528) · [💻 仓库](https://github.com/BayLing-Models/BayLing-Duplex) |
| [CF-Duplex / XA-Duplex](CATALOG.md#e40) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2605.10199) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2605.10199) | 对比受控融合与交叉注意力，把用户语音流接入正在生成的模型，分析同时听说的架构选择。<br>[📄 论文](https://arxiv.org/abs/2605.10199) · [🔗 项目](https://light1726.github.io/duplex-demo/) |
| ⭐ [Self-Listening / LoopSpeech](CATALOG.md#e44) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.05592) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.05592) | 把实际已播放的语音纳入历史，区分“计划说出”与“用户已经听到”，研究打断后的内容连续性。<br>[📄 论文](https://arxiv.org/abs/2609.05592) · [💻 仓库](https://github.com/FreedomIntelligence/LoopSpeech) |
| [IRAF](CATALOG.md#e47) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2606.06559) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2606.06559) | 按帧估计目标说话人可靠性并自适应融合音频，研究干扰说话人条件下的全双工鲁棒性。<br>[📄 论文](https://arxiv.org/abs/2606.06559) |

### 🧪 数据生产、长对话与高效建模

| 文章 / 项目 | 发表与归属 | 阅读重点与资源 |
|---|---|---|
| ⭐ [SOMMELIER](CATALOG.md#e39) | [![ACL Industry Track 2026](https://img.shields.io/badge/ACL%20Industry%20Track%202026-475569?style=flat-square)](https://aclanthology.org/2026.acl-industry.18/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2603.25750) | 把真实多人录音转为保留时间关系的双声道训练数据，连接分离、说话人分段、转写和质量筛选。<br>[📄 论文](https://arxiv.org/abs/2603.25750) · [💻 仓库](https://github.com/Anonymous-2001-j/Sommelier) |
| ⭐ [DuplexGen](CATALOG.md#e41) | [![EMNLP 2026](https://img.shields.io/badge/EMNLP%202026-475569?style=flat-square)](https://aclanthology.org/2026.emnlp-main.2618/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2607.26178) | 用少量人类偏好校准话轮行为预测，再合成适配不同场景的人机对话，用于全双工模型微调。<br>[📄 论文](https://arxiv.org/abs/2607.26178) · [💻 仓库](https://github.com/duplexgen/duplexgen-code) · [🔗 项目](https://duplexgen.github.io/) |
| [MultiTalk / MultiTalkBench](CATALOG.md#e43) | [![NeurIPS 2026 · 作者标注](https://img.shields.io/badge/NeurIPS%202026%20%C2%B7%20%E4%BD%9C%E8%80%85%E6%A0%87%E6%B3%A8-475569?style=flat-square)](https://arxiv.org/abs/2609.36903) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2609.36903) | 扩展到长时、多方、双语全双工对话；提供预训练、微调数据和来自真实录音的 MultiTalkBench。<br>[📄 论文](https://arxiv.org/abs/2609.36903) · [🔗 预训练数据](https://huggingface.co/datasets/MultiTalk/MultiTalkPT) · [🔗 微调数据](https://huggingface.co/datasets/MultiTalk/MultiTalkFT) · [🔗 Benchmark](https://huggingface.co/datasets/MultiTalk/MultiTalkBench) |
| [D2: Dialogue-to-Duplex](CATALOG.md#e45) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.17124) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2610.17124) | 复用半双工语音模型进行全双工适配，分析音频块间隔对质量、时延和计算量的影响。<br>[📄 论文](https://arxiv.org/abs/2610.17124) · [💻 仓库](https://github.com/penguinfish1688/D2-dialogue-to-duplex) · [🔗 项目](https://d2-duplex-demo.github.io/) |
| [TASTE2](CATALOG.md#e46) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.08956) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2609.08956) | 以文本对齐的语音建模和部署协同组织全双工交互，补充副语言信号与实时运行的设计。<br>[📄 论文](https://arxiv.org/abs/2609.08956) · [💻 仓库](https://github.com/GitYCC/TASTE-SpokenLM-2) · [🔗 项目](https://gitycc.github.io/TASTE2-Homepage/) · [🔗 语音应用](https://github.com/GitYCC/TASTE-Voice-Bot) |
| [DiffuPlex · Rolling Masked Diffusion](CATALOG.md#e50) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.12214) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2610.12214) | 用滚动掩码扩散预测交互帧，在保留交互质量的同时减少主干模型调用。<br>[📄 论文](https://arxiv.org/abs/2610.12214) · [🔗 项目](https://diffuplex.github.io/) |

<a id="industry"></a>
## 🏭 工业研究与技术报告

论文、权重、训练代码与运行时的开放范围分别记录；校企共同署名的 Realtime-Venus、DuplexOmni 等列于上方并保留联合标签。

| 文章 / 项目 | 发表与归属 | 阅读重点与资源 |
|---|---|---|
| [Qwen-Audio-3.1-Realtime](CATALOG.md#e57) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.25176) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.25176) | 在可执行环境中进行 Agent GRPO，结合多模态策略蒸馏，研究任务可靠性与交互行为后训练。<br>[📄 论文](https://arxiv.org/abs/2609.25176) · [💻 仓库](https://github.com/QwenAudio/qwen-audio-agent) |
| [StepAudio 3 Realtime](CATALOG.md#e56) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.14005) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.14005) | 围绕 listen、converse、think、act 组织实时语音交互，结合 Think-While-Speaking 与异步工具执行。<br>[📄 论文](https://arxiv.org/abs/2609.14005) · [🔗 项目](https://stepaudiollm.github.io/step-audio-3-realtime/) |
| [NemotronLabs VoiceChat](CATALOG.md#e55) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.21967) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.21967) | 开放的全双工语音模型，以独立工具通道连接动作调用，并支持可打断语音输出。<br>[📄 论文](https://arxiv.org/abs/2609.21967) · [💻 仓库](https://github.com/NVIDIA-NeMo/Speech/tree/nemotron-labs-voicechat) · [🔗 模型](https://huggingface.co/nvidia/NVIDIA-NemotronLabs-VoiceChat-11B) |
| [AdaptDuplex](CATALOG.md#e53) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.29217) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.29217) | 结合自适应感知窗口、非阻塞认知整合与外部推理，研究动态全双工对话及分阶段后训练。<br>[📄 论文](https://arxiv.org/abs/2609.29217) |
| [Frontend–Backend Tool Calling](CATALOG.md#e49) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.19334) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2609.19334) | 将实时语音前端与文本工具后端分离，以流式转写、工具执行和 prefill-and-repeat 结果回传连接两者。<br>[📄 论文](https://arxiv.org/abs/2609.19334) |
| [Diffuplex · Discrete Diffusion](CATALOG.md#e51) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.17780) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/pdf/2610.17780) | 以自回归过程决定何时说话，以离散扩散并行生成内容，研究全双工生成效率。<br>[📄 论文](https://arxiv.org/abs/2610.17780) |
| ⭐ [FireRedChat](CATALOG.md#e29) | [![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.06502) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/abs/2509.06502) | 全双工语音系统：轮次控制、主说话人打断、对话管理和工具调用。<br>[📄 论文](https://arxiv.org/abs/2509.06502) · [💻 仓库](https://github.com/FireRedTeam/FireRedChat) |

<a id="engineering"></a>
## 🛠️ 工程实现与补充案例

| 文章 / 项目 | 发表与归属 | 阅读重点与资源 |
|---|---|---|
| [Qwen Audio Agent](CATALOG.md#e30) | [![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent) | 语音前端与后台 Agent 分工，提供异步任务协作和取消机制的工程入口。<br>[💻 仓库](https://github.com/QwenAudio/qwen-audio-agent) |
| [TEN Framework](CATALOG.md#e36) | [![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/TEN-framework/ten-framework) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/TEN-framework/ten-framework) | 实时音视频 Agent 框架，提供可组合扩展与多模态应用示例。<br>[💻 仓库](https://github.com/TEN-framework/ten-framework) |
| [Voice-Light](CATALOG.md#e52) | [![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2609.20995) | 级联系统中的因果轮次控制、推测生成和可撤销播放；用播放确认更新持久对话历史。<br>[📄 论文](https://arxiv.org/abs/2609.20995) · [💻 仓库](https://github.com/BertilBraun/Voice-Light) |

Voice-Light 的作者机构归属尚未确定，暂不添加 Academic / Industry 标签；其有限规模在线实验见[条目边界](CATALOG.md#e52)。

## 📏 从模型结果走向系统结果

[Benchmark 专页](05-Voice-Agent-Benchmarks.md)区分基础回答、轮次决策、多轮与多人、交互指令、工具与任务完成。工具调用成功、用户听到正确内容和环境任务完成是不同事件，需要分别评价。

综述入口：[WavChat](SURVEYS.md#s01) · [SpeechLM Survey](SURVEYS.md#s02) · [Full-duplex Survey](SURVEYS.md#s03) · [DuplexSurvey](SURVEYS.md#s04)。不同综述的层级编号服务于各自分类，使用时保留原定义。

语音工具调用产生任务请求；连接机器人还需可执行技能或动作策略、状态反馈和取消处理。

下一步：[端侧与具身交互 →](04-Edge-Embodied-Interaction.md)
