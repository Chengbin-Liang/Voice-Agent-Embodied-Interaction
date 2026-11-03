# 论文与项目索引

[返回首页](README.md) · [完整索引](CATALOG.md) · [Survey 对照](SURVEYS.md)

按技术主题浏览；⭐ 标注适合优先阅读的条目。计数口径见[标签说明](README.md#labels)。

[🎧 Omni 与语音模型](#omni) · [💬 Voice Agent 与交互系统](#voice) · [🤖 具身交互与语言反馈](#embodied) · [🦾 动作、数据与部署](#robotics) · [📏 评测](#evaluation) · [🏭 工业展示](#industry)

<a id="omni"></a>

## 🎧 Omni 与语音模型

<a id="e01"></a>

### ⭐ MiniCPM-o 4.5

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2604.27393) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V)

[📄 论文](https://arxiv.org/abs/2604.27393) · [💻 仓库](https://github.com/OpenBMB/MiniCPM-V) · [![★ 27,047](https://img.shields.io/badge/%E2%98%85%2027%2C047-eab308?style=flat-square)](https://github.com/OpenBMB/MiniCPM-V) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W7159670352)

以共享时间轴组织持续音视频输入与文本、语音输出，并研究主动回应。

📌 优先阅读理由：阅读持续音视频输入、全双工输出及其部署条件。

范围说明：全双工模式的硬件要求以官方部署文档为准；模型内存与完整系统内存应分开记录。

机构 / 维护方：Tsinghua University / THUNLP；ModelBest；OpenBMB。

<sub>计数快照：2026-11-02。</sub>

<a id="e02"></a>

### ⭐ Qwen2.5-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.20215) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni)

[📄 论文](https://arxiv.org/abs/2503.20215) · [💻 仓库](https://github.com/QwenLM/Qwen2.5-Omni) · [![★ 4,092](https://img.shields.io/badge/%E2%98%85%204%2C092-eab308?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni) [![Cite OA 14](https://img.shields.io/badge/Cite%20OA%2014-0284c7?style=flat-square)](https://openalex.org/W4409051416)

音视频、图像和文本输入，联合生成文本与语音；提供 Thinker–Talker 架构参照。

📌 优先阅读理由：建立 Thinker–Talker 架构、数据与分阶段训练的基本参照。

范围说明：流式语音输出不等于原生同时听说；MNN 功能覆盖以对应部署模式为准。

机构 / 维护方：Qwen Team / Alibaba。

<sub>计数快照：2026-11-02。</sub>

<a id="e03"></a>

### Qwen3-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.17765) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni)

[📄 论文](https://arxiv.org/abs/2509.17765) · [💻 仓库](https://github.com/QwenLM/Qwen3-Omni) · [![★ 4,093](https://img.shields.io/badge/%E2%98%85%204%2C093-eab308?style=flat-square)](https://github.com/QwenLM/Qwen3-Omni) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4415255153)

MoE Thinker–Talker 路线，覆盖多模态理解和实时语音生成。

机构 / 维护方：Qwen Team / Alibaba。

<sub>计数快照：2026-11-02。</sub>

<a id="e04"></a>

### InteractiveOmni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.13747) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2510.13747)

[📄 论文](https://arxiv.org/abs/2510.13747) · [💻 仓库](https://github.com/OpenSenseNova/InteractiveOmni) · [![★ 9](https://img.shields.io/badge/%E2%98%85%209-eab308?style=flat-square)](https://github.com/OpenSenseNova/InteractiveOmni) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415277372)

以音视频多轮交互为目标，提供 4B 与 8B 模型及多轮评价。

机构 / 维护方：SenseTime Research。

<sub>计数快照：2026-11-02。</sub>

<a id="e05"></a>

### VITA-1.5

[![NeurIPS 2025](https://img.shields.io/badge/NeurIPS%202025-475569?style=flat-square)](https://arxiv.org/abs/2501.01957) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2501.01957)

[📄 论文](https://arxiv.org/abs/2501.01957) · [💻 仓库](https://github.com/VITA-MLLM/VITA) · [![★ 2,539](https://img.shields.io/badge/%E2%98%85%202%2C539-eab308?style=flat-square)](https://github.com/VITA-MLLM/VITA) [![Cite OA 11](https://img.shields.io/badge/Cite%20OA%2011-0284c7?style=flat-square)](https://openalex.org/W4406093559)

面向实时视觉和语音交互的多模态模型，提供训练与推理流程。

机构 / 维护方：Nanjing University；Xiamen University；CASIA；Tencent Youtu Lab。

<sub>计数快照：2026-11-02。</sub>

<a id="e06"></a>

### Mini-Omni2

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.11190) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2410.11190)

[📄 论文](https://arxiv.org/abs/2410.11190) · [💻 仓库](https://github.com/gpt-omni/mini-omni2) · [![★ 1,936](https://img.shields.io/badge/%E2%98%85%201%2C936-eab308?style=flat-square)](https://github.com/gpt-omni/mini-omni2) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4403576555)

较早开放图像、语音、文本输入与实时语音输出的实验系统。

机构 / 维护方：Tsinghua University；Inspirai。

<sub>计数快照：2026-11-02。</sub>

<a id="e07"></a>

### ⭐ Moshi

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2410.00037) [![Independent Lab](https://img.shields.io/badge/Independent%20Lab-b45309?style=flat-square)](https://arxiv.org/html/2410.00037)

[📄 论文](https://arxiv.org/abs/2410.00037) · [💻 仓库](https://github.com/kyutai-labs/moshi) · [![★ 11,361](https://img.shields.io/badge/%E2%98%85%2011%2C361-eab308?style=flat-square)](https://github.com/kyutai-labs/moshi) [![Cite OA 9](https://img.shields.io/badge/Cite%20OA%209-0284c7?style=flat-square)](https://openalex.org/W4403883071) [![Cite S2 875](https://img.shields.io/badge/Cite%20S2%20875-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/ae4aa7b0c5a327dae63ad20e00b58bcc6176b3b8)

双向语音流与文本协同建模，为连续听说提供开源研究基础。

📌 优先阅读理由：理解双向语音流、文本辅助及低延迟生成。

机构 / 维护方：Kyutai。

<sub>计数快照：2026-11-02。</sub>

<a id="e08"></a>

### Freeze-Omni

[![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2411.00774) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2411.00774)

[📄 论文](https://arxiv.org/abs/2411.00774) · [💻 仓库](https://github.com/VITA-MLLM/Freeze-Omni) · [![★ 403](https://img.shields.io/badge/%E2%98%85%20403-eab308?style=flat-square)](https://github.com/VITA-MLLM/Freeze-Omni) [![Cite OA 4](https://img.shields.io/badge/Cite%20OA%204-0284c7?style=flat-square)](https://openalex.org/W4404390495)

冻结语言模型，结合流式语音编码解码和块级状态预测。

机构 / 维护方：Northwestern Polytechnical University；Nanjing University；Tencent Youtu Lab。

<sub>计数快照：2026-11-02。</sub>

<a id="voice"></a>

## 💬 Voice Agent 与交互系统

<a id="e29"></a>

### ⭐ FireRedChat

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2509.06502) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/abs/2509.06502)

[📄 论文](https://arxiv.org/abs/2509.06502) · [💻 仓库](https://github.com/FireRedTeam/FireRedChat) · [![★ 597](https://img.shields.io/badge/%E2%98%85%20597-eab308?style=flat-square)](https://github.com/FireRedTeam/FireRedChat) [![Cite OA 2](https://img.shields.io/badge/Cite%20OA%202-0284c7?style=flat-square)](https://openalex.org/W4414757003)

全双工语音系统：轮次控制、主说话人打断、对话管理和工具调用。

📌 优先阅读理由：以模块化实现理解打断控制、对话状态和工具调用。

机构 / 维护方：Xiaohongshu / FireRed Team。

<sub>计数快照：2026-11-03。</sub>

<a id="e30"></a>

### Qwen Audio Agent

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent)

[💻 仓库](https://github.com/QwenAudio/qwen-audio-agent) · [![★ 3,111](https://img.shields.io/badge/%E2%98%85%203%2C111-eab308?style=flat-square)](https://github.com/QwenAudio/qwen-audio-agent)

语音前端与后台 Agent 分工，提供异步任务协作和取消机制的工程入口。

机构 / 维护方：Qwen / Alibaba。

<sub>计数快照：2026-11-03。</sub>

<a id="e09"></a>

### DuplexSLA

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2605.20755) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2605.20755)

[📄 论文](https://arxiv.org/abs/2605.20755) · [💻 仓库](https://github.com/hyzhang24/DuplexSLA) · [![★ 147](https://img.shields.io/badge/%E2%98%85%20147-eab308?style=flat-square)](https://github.com/hyzhang24/DuplexSLA) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7161968102)

在共同时间线上输出语音及结构化 action 通道，研究交谈中的规划与工具调用。

范围说明：论文的 action 通道主要对应结构化规划与工具操作，不能直接等同于关节控制。

机构 / 维护方：StepFun；Peking University；Nanyang Technological University；Shanghai Jiao Tong University；University of New South Wales；Imperial College London。

<sub>计数快照：2026-11-02。</sub>

<a id="e31"></a>

### Jarvis

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2610.23804) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2610.23804)

[📄 论文](https://arxiv.org/abs/2610.23804) · [💻 仓库](https://github.com/JensenYX/Jarvis) · [![★ 18](https://img.shields.io/badge/%E2%98%85%2018-eab308?style=flat-square)](https://github.com/JensenYX/Jarvis) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7222979632)

在交互前端和后台任务之间训练协调器，管理任务切换、状态和过期结果。

范围说明：软件 Agent 协调研究，尚不能据此推断真实机器人任务增益。

机构 / 维护方：CUHK Shenzhen；Tencent Hunyuan；Amphion Technology。

<sub>计数快照：2026-11-03。</sub>

<a id="e36"></a>

### TEN Framework

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/TEN-framework/ten-framework) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/TEN-framework/ten-framework)

[💻 仓库](https://github.com/TEN-framework/ten-framework) · [![★ 11,219](https://img.shields.io/badge/%E2%98%85%2011%2C219-eab308?style=flat-square)](https://github.com/TEN-framework/ten-framework)

实时音视频 Agent 框架，提供可组合扩展与多模态应用示例。

范围说明：LICENSE 包含 Apache-2.0 之外的附加使用条件，涉及终端设备托管等；部署前阅读官方 LICENSE。

机构 / 维护方：Agora；Contributor community。

<sub>计数快照：2026-11-03。</sub>

[官方 LICENSE](https://github.com/TEN-framework/ten-framework/blob/main/LICENSE)

<a id="embodied"></a>

## 🤖 具身交互与语言反馈

<a id="e13"></a>

### Interactive Language / Language Table

[![IEEE RA-L 2024](https://img.shields.io/badge/IEEE%20RA--L%202024-475569?style=flat-square)](https://doi.org/10.1109/LRA.2023.3295255) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2210.06407)

[📄 论文](https://arxiv.org/abs/2210.06407) · [💻 仓库](https://github.com/google-research/language-table) · [![★ 367](https://img.shields.io/badge/%E2%98%85%20367-eab308?style=flat-square)](https://github.com/google-research/language-table) [![Cite OA 113](https://img.shields.io/badge/Cite%20OA%20113-0284c7?style=flat-square)](https://openalex.org/W4391759936)

通过实时语言指导视觉运动策略，允许人逐步调整机器人完成目标。

机构 / 维护方：Robotics at Google。

<sub>计数快照：2026-11-02。</sub>

<a id="e25"></a>

### ⭐ Hi Robot

[![ICML 2025](https://img.shields.io/badge/ICML%202025-475569?style=flat-square)](https://proceedings.mlr.press/v267/shi25d.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2502.19417)

[📄 论文](https://arxiv.org/abs/2502.19417) · [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4416045178) [![Cite S2 319](https://img.shields.io/badge/Cite%20S2%20319-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/69afd10d387423a03617d461c3f47a5f3033cc54)

高层视觉语言推理将复杂指令和执行中反馈转为下一步任务，低层 VLA 执行具体动作。

📌 优先阅读理由：理解高层语言推理与低层动作策略的分工。

范围说明：语言反馈经高层规划传给动作策略，不能据此归因为原始语音信息增益。

机构 / 维护方：Physical Intelligence；Stanford University；UC Berkeley。

<sub>计数快照：2026-11-02。</sub>

<a id="e26"></a>

### ⭐ Yell At Your Robot / YAY Robot

[![RSS 2024](https://img.shields.io/badge/RSS%202024-475569?style=flat-square)](https://roboticsproceedings.org/rss20/p025.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2403.12910)

[📄 论文](https://arxiv.org/abs/2403.12910) · [💻 仓库](https://github.com/yay-robot/yay_robot) · [![★ 166](https://img.shields.io/badge/%E2%98%85%20166-eab308?style=flat-square)](https://github.com/yay-robot/yay_robot) [![Cite OA 47](https://img.shields.io/badge/Cite%20OA%2047-0284c7?style=flat-square)](https://openalex.org/W4402354098) [![Cite S2 179](https://img.shields.io/badge/Cite%20S2%20179-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/f213d0cb84b6afca9a4d5722081ba3052e7e89bc)

人在机器人执行长任务时给出口头修正，系统立即利用纠正，并将这些反馈用于后续高层策略训练。

📌 优先阅读理由：理解执行中口头纠正如何用于当前控制与后续学习。

范围说明：口头纠正主要通过语言表示进入控制与学习。

机构 / 维护方：Stanford University；UC Berkeley。

<sub>计数快照：2026-11-02。</sub>

<a id="e24"></a>

### VLAS

[![ICLR 2025](https://img.shields.io/badge/ICLR%202025-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2025/hash/804a1a9de5787e3597b4bb64e1a48ec3-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2502.13508)

[📄 论文](https://arxiv.org/abs/2502.13508) · [💻 仓库](https://github.com/whichwhichgone/VLAS) · [![★ 50](https://img.shields.io/badge/%E2%98%85%2050-eab308?style=flat-square)](https://github.com/whichwhichgone/VLAS) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4407764312) [![Cite S2 68](https://img.shields.io/badge/Cite%20S2%2068-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/f6075ce4db8dcc359c3ac97b85f2644dc5cadda6)

将原始语音接入视觉动作策略，并用声纹检索个体相关信息，执行带有个人偏好的操作。

范围说明：原始语音与声纹个性化操作，不应与全双工说做控制混为同一能力。

机构 / 维护方：Westlake University；Zhejiang University；Xi’an Jiaotong University。

<sub>计数快照：2026-11-02。</sub>

<a id="e21"></a>

### ⭐ RoboOmni (OpenMOSS)

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/33610fba262d7b6fed0810b89f55e147-Abstract-Conference.html) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2510.23763)

[📄 论文](https://arxiv.org/abs/2510.23763) · [💻 仓库](https://github.com/OpenMOSS/RoboOmni) · [![★ 124](https://img.shields.io/badge/%E2%98%85%20124-eab308?style=flat-square)](https://github.com/OpenMOSS/RoboOmni) [![Cite S2 12](https://img.shields.io/badge/Cite%20S2%2012-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/37cd1e4cbfbfdadc2a898a703ab46bc0e1c83dd3)

从对话、环境声音和视觉线索推断意图，经确认后生成操作动作，研究隐式情境指令下的主动协助。

📌 优先阅读理由：了解环境声音与隐式意图如何进入操作任务。

范围说明：此处绑定 OpenMOSS 的 RoboOmni，注意与其他同名论文区分。

机构 / 维护方：Fudan University；Shanghai Innovation Institute；National University of Singapore。

<sub>计数快照：2026-11-02。</sub>

<a id="e22"></a>

### ⭐ ELLSA

[![ICLR 2026](https://img.shields.io/badge/ICLR%202026-475569?style=flat-square)](https://proceedings.iclr.cc/paper_files/paper/2026/hash/6d8af672c0bca7a4be6f0cd0d229c05c-Abstract-Conference.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.16756)

[📄 论文](https://arxiv.org/abs/2510.16756) · [💻 仓库](https://github.com/bytedance/SALMONN) · [![★ 1,564](https://img.shields.io/badge/%E2%98%85%201%2C564-eab308?style=flat-square)](https://github.com/bytedance/SALMONN) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W4415958597) [![Cite S2 7](https://img.shields.io/badge/Cite%20S2%207-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/3af611e47c30a439f8acad312f16cf7837ddbce7)

在统一架构中处理视觉、文本、语音和动作，支持边说边做、动作打断与基于场景的问答。

📌 优先阅读理由：阅读语音与动作共同建模、边说边做及中断实验。

范围说明：SALMONN 是共享仓库；Star 数不等于 ELLSA 子项目独立关注量，具体权重与训练入口见官方发布。

机构 / 维护方：Tsinghua University；ByteDance。

<sub>计数快照：2026-11-02。</sub>

<a id="e23"></a>

### VITA-E

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2510.21817) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2510.21817)

[📄 论文](https://arxiv.org/abs/2510.21817) · [💻 仓库](https://github.com/Tencent/VITA) · [![★ 166](https://img.shields.io/badge/%E2%98%85%20166-eab308?style=flat-square)](https://github.com/Tencent/VITA) [![Cite S2 2](https://img.shields.io/badge/Cite%20S2%202-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/62d932e380f9ec7de5d43c17bc933a05887b0007)

以并行的活动/监听模型和控制 token 调度语音与动作，支持中断、任务切换和边说边做。

机构 / 维护方：Nanjing University；CASIA；Tencent Youtu Lab；Fourier Intelligence。

<sub>计数快照：2026-11-02。</sub>

<a id="e11"></a>

### Reachy Mini Conversation App

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)

[💻 仓库](https://github.com/pollen-robotics/reachy_mini_conversation_app) · [![★ 348](https://img.shields.io/badge/%E2%98%85%20348-eab308?style=flat-square)](https://github.com/pollen-robotics/reachy_mini_conversation_app)

把实时语音、摄像头工具和机器人运动接入同一对话应用。

范围说明：主要是头部、天线等身体表达和视觉工具调用，不是机械臂抓取平台。

机构 / 维护方：Pollen Robotics / Hugging Face。

<sub>计数快照：2026-11-02。</sub>

<a id="e12"></a>

### EMAGE / BEAT2

[![CVPR 2024](https://img.shields.io/badge/CVPR%202024-475569?style=flat-square)](https://pantomatrix.github.io/EMAGE/) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/pdf/2401.00374)

[📄 论文](https://arxiv.org/abs/2401.00374) · [💻 仓库](https://github.com/haiyangliu0/character-policy) · [![★ 1,312](https://img.shields.io/badge/%E2%98%85%201%2C312-eab308?style=flat-square)](https://github.com/haiyangliu0/character-policy) [![Cite OA 95](https://img.shields.io/badge/Cite%20OA%2095-0284c7?style=flat-square)](https://openalex.org/W4402727140)

从语音及文本生成全身与面部协同动作，连接 co-speech gesture 与表达数据。

范围说明：面向共语手势与角色表达；不直接证明真实机器人的操作能力。

机构 / 维护方：The University of Tokyo；Keio University；Max Planck Institute for Intelligent Systems；JAIST；Tsinghua University。

<sub>计数快照：2026-11-02。</sub>

<a id="robotics"></a>

## 🦾 动作、数据与部署

<a id="e19"></a>

### ⭐ LeRobot

[![arXiv 2026](https://img.shields.io/badge/arXiv%202026-475569?style=flat-square)](https://arxiv.org/abs/2602.22818) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2602.22818)

[📄 论文](https://arxiv.org/abs/2602.22818) · [💻 仓库](https://github.com/huggingface/lerobot) · [![★ 28,653](https://img.shields.io/badge/%E2%98%85%2028%2C653-eab308?style=flat-square)](https://github.com/huggingface/lerobot) [![Cite OA 0](https://img.shields.io/badge/Cite%20OA%200-0284c7?style=flat-square)](https://openalex.org/W7131860508)

机器人数据、策略训练、硬件控制与评测的开源工具入口。

📌 优先阅读理由：贯通示范采集、数据查看、策略训练与真机执行。

机构 / 维护方：Hugging Face；University of Oxford。

<sub>计数快照：2026-11-02 / 2026-11-03。</sub>

<a id="e32"></a>

### ⭐ ACT / ALOHA

[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://www.roboticsproceedings.org/rss19/p016.pdf) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2304.13705)

[📄 论文](https://arxiv.org/abs/2304.13705) · [💻 仓库](https://github.com/tonyzhaozh/act) · [![★ 2,318](https://img.shields.io/badge/%E2%98%85%202%2C318-eab308?style=flat-square)](https://github.com/tonyzhaozh/act) [![Cite OA 674](https://img.shields.io/badge/Cite%20OA%20674-0284c7?style=flat-square)](https://openalex.org/W4385430674)

用遥操作示范学习动作块，建立视觉运动模仿学习基线。

📌 优先阅读理由：建立“观测—动作示范—动作块预测”的模仿学习直觉。

范围说明：标准 ACT 不是语言条件模型；多目标选择需技能选择器或另加目标条件。

机构 / 维护方：Stanford University；Meta；UC Berkeley。

<sub>计数快照：2026-11-03。</sub>

<a id="e33"></a>

### Diffusion Policy

[![RSS 2023](https://img.shields.io/badge/RSS%202023-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![IJRR 2024](https://img.shields.io/badge/IJRR%202024-475569?style=flat-square)](https://diffusion-policy.cs.columbia.edu/) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2303.04137)

[📄 论文](https://arxiv.org/abs/2303.04137v4) · [💻 仓库](https://github.com/real-stanford/diffusion_policy) · [![★ 4,698](https://img.shields.io/badge/%E2%98%85%204%2C698-eab308?style=flat-square)](https://github.com/real-stanford/diffusion_policy) [![Cite OA 12](https://img.shields.io/badge/Cite%20OA%2012-0284c7?style=flat-square)](https://openalex.org/W4323651335)

将条件动作分布建模为去噪过程，生成连续动作序列。

范围说明：论文链接为 RSS 2023 版本；IJRR 2024 为扩展版。引文数量绑定所链接的数据库记录。

机构 / 维护方：Columbia University；Toyota Research Institute；MIT。

<sub>计数快照：2026-11-03。</sub>

<a id="e34"></a>

### ⭐ SmolVLA

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2506.01844) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2506.01844)

[📄 论文](https://arxiv.org/abs/2506.01844) · [💻 仓库](https://github.com/huggingface/lerobot) · [![★ 28,653](https://img.shields.io/badge/%E2%98%85%2028%2C653-eab308?style=flat-square)](https://github.com/huggingface/lerobot) [![Cite OA 3](https://img.shields.io/badge/Cite%20OA%203-0284c7?style=flat-square)](https://openalex.org/W4414898213)

450M 视觉语言动作模型，以图像、机器人状态与文本指令为条件生成动作块。

📌 优先阅读理由：沿官方教程把预训练 VLA 适配到自己的机器人数据。

范围说明：输入含文本指令，不是原生语音策略。Star 数为整个 LeRobot 仓库；模型小不自动保证整机实时。

机构 / 维护方：Hugging Face；Sorbonne University；valeo.ai；ENS Paris-Saclay。

<sub>计数快照：2026-11-03。</sub>

<a id="e20"></a>

### OpenVLA

[![CoRL 2024](https://img.shields.io/badge/CoRL%202024-475569?style=flat-square)](https://proceedings.mlr.press/v270/kim25c.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/pdf/2406.09246)

[📄 论文](https://arxiv.org/abs/2406.09246) · [💻 仓库](https://github.com/openvla/openvla) · [![★ 7,250](https://img.shields.io/badge/%E2%98%85%207%2C250-eab308?style=flat-square)](https://github.com/openvla/openvla) [![Cite OA 62](https://img.shields.io/badge/Cite%20OA%2062-0284c7?style=flat-square)](https://openalex.org/W4399695759)

视觉与语言条件下的机器人动作模型，作为交互层连接动作策略的基础参照。

范围说明：视觉、语言到动作的基础；原生语音与实时打断需要额外系统设计。

机构 / 维护方：Stanford University；UC Berkeley；MIT；Toyota Research Institute；Google DeepMind；Physical Intelligence。

<sub>计数快照：2026-11-02。</sub>

<a id="e17"></a>

### llama.cpp ecosystem

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/OpenBMB/llama.cpp-omni) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/ggml-org/llama.cpp/discussions/19759)

[💻 仓库](https://github.com/ggml-org/llama.cpp) · [![★ 133,116](https://img.shields.io/badge/%E2%98%85%20133%2C116-eab308?style=flat-square)](https://github.com/ggml-org/llama.cpp)

本地推理工具链基础，提供量化与多平台运行入口。

范围说明：完整 Omni 模式可能依赖专用分支，例如 OpenBMB/llama.cpp-omni。

机构 / 维护方：ggml.ai / Hugging Face；llama.cpp contributor community。

<sub>计数快照：2026-11-02。</sub>

<a id="e18"></a>

### MNN

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://github.com/QwenLM/Qwen2.5-Omni#deployment-with-mnn) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://github.com/alibaba/MNN)

[💻 仓库](https://github.com/alibaba/MNN) · [![★ 16,336](https://img.shields.io/badge/%E2%98%85%2016%2C336-eab308?style=flat-square)](https://github.com/alibaba/MNN)

面向移动与边缘设备的推理框架；Qwen2.5-Omni 提供官方接入入口。

机构 / 维护方：Alibaba。

<sub>计数快照：2026-11-02。</sub>

<a id="evaluation"></a>

## 📏 评测

<a id="e14"></a>

### Daily-Omni

[![arXiv 2025](https://img.shields.io/badge/arXiv%202025-475569?style=flat-square)](https://arxiv.org/abs/2505.17862) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2505.17862)

[📄 论文](https://arxiv.org/abs/2505.17862) · [💻 仓库](https://github.com/Lliar-liar/Daily-Omni) · [![★ 53](https://img.shields.io/badge/%E2%98%85%2053-eab308?style=flat-square)](https://github.com/Lliar-liar/Daily-Omni) 引文计数 —

日常视频音画联合推理基准，强调跨模态时间对齐。

机构 / 维护方：Fudan University。

<sub>计数快照：2026-11-02。</sub>

<a id="e15"></a>

### OmniBench (m-a-p)

[![NeurIPS 2025](https://img.shields.io/badge/NeurIPS%202025-475569?style=flat-square)](https://arxiv.org/abs/2409.15272) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2409.15272)

[📄 论文](https://arxiv.org/abs/2409.15272) · [💻 仓库](https://github.com/multimodal-art-projection/OmniBench) · [![★ 62](https://img.shields.io/badge/%E2%98%85%2062-eab308?style=flat-square)](https://github.com/multimodal-art-projection/OmniBench) [![Cite OA 1](https://img.shields.io/badge/Cite%20OA%201-0284c7?style=flat-square)](https://openalex.org/W4403885114) [![Cite S2 111](https://img.shields.io/badge/Cite%20S2%20111-0284c7?style=flat-square)](https://www.semanticscholar.org/paper/bde43a6356341b68a675582cf964fd9725fb40fb)

针对图像、音频、文本联合理解的三模态基准，并提供 OmniInstruct。

机构 / 维护方：M-A-P；University of Manchester；Queen Mary University of London；01.ai；HKUST；Nanjing University；Dartmouth College。

<sub>计数快照：2026-11-02。</sub>

<a id="e16"></a>

### ⭐ Full-Duplex-Bench

[![ASRU 2025](https://img.shields.io/badge/ASRU%202025-475569?style=flat-square)](https://arxiv.org/abs/2503.04721) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2503.04721)

[📄 论文](https://arxiv.org/abs/2503.04721) · [💻 仓库](https://github.com/DanielLin94144/Full-Duplex-Bench) · [![★ 336](https://img.shields.io/badge/%E2%98%85%20336-eab308?style=flat-square)](https://github.com/DanielLin94144/Full-Duplex-Bench) [![Cite OA 8](https://img.shields.io/badge/Cite%20OA%208-0284c7?style=flat-square)](https://openalex.org/W7148492801)

覆盖停顿、反馈、轮次交接和打断；后续版本扩展重叠、动态多轮与工具使用。

📌 优先阅读理由：把打断、轮次交接和交互时序转为可测指标。

机构 / 维护方：National Taiwan University；UC Berkeley；University of Washington；MIT CSAIL。

<sub>计数快照：2026-11-02。</sub>

<a id="e35"></a>

### LIBERO

[![NeurIPS Datasets and Benchmarks 2023](https://img.shields.io/badge/NeurIPS%20Datasets%20and%20Benchmarks%202023-475569?style=flat-square)](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8c3c666820ea055a77726d66fc7d447f-Abstract-Datasets_and_Benchmarks.html) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/abs/2306.03310)

[📄 论文](https://arxiv.org/abs/2306.03310) · [💻 仓库](https://github.com/Lifelong-Robot-Learning/LIBERO) · [![★ 2,508](https://img.shields.io/badge/%E2%98%85%202%2C508-eab308?style=flat-square)](https://github.com/Lifelong-Robot-Learning/LIBERO) [![Cite OA 136](https://img.shields.io/badge/Cite%20OA%20136-0284c7?style=flat-square)](https://openalex.org/W7133220882)

语言条件机器人操作基准，考察知识迁移与持续学习。

范围说明：主要评价语言条件操作能力，不直接评价语音交互和真人协作。

机构 / 维护方：UT Austin；Tsinghua University；Sony AI。

<sub>计数快照：2026-11-03。</sub>

<a id="industry"></a>

## 🏭 工业展示

<a id="e10"></a>

### WITA-Omni

[![Project](https://img.shields.io/badge/Project-475569?style=flat-square)](https://www.agibot.com/article/231/detail/122.html) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.agibot.com/article/231/detail/122.html)

[🔗 官方页面](https://www.agibot.com/article/231/detail/122.html) · —

智元的具身交互展示将场景理解、语音和身体表达组合在同一交互过程中。

范围说明：工业展示；不能由演示反推动作模型、训练数据或完整系统已经开放。

机构 / 维护方：AGIBOT / 智元。

<sub>计数快照：2026-11-02。</sub>

<a id="e27"></a>

### Gemini Live API × Robotics demo

[![Technical Demo 2025](https://img.shields.io/badge/Technical%20Demo%202025-475569?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/)

[🔗 官方页面](https://developers.googleblog.com/en/gemini-25-for-robotics-and-embodied-intelligence/) · —

Google 官方展示将语音与机器人摄像头输入交给 Live API，再以函数调用连接机器人控制接口。

范围说明：Live API 工程示例与 Gemini Robotics 模型是不同入口；示例本身不提供统一的机器人成功率对照实验。

机构 / 维护方：Google / Google DeepMind。

<sub>计数快照：2026-11-02。</sub>

<a id="e28"></a>

### Figure Helix 02

[![Technical Demo 2026](https://img.shields.io/badge/Technical%20Demo%202026-475569?style=flat-square)](https://www.figure.ai/news/helix-02) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://www.figure.ai/news/helix-02)

[🔗 官方页面](https://www.figure.ai/news/helix-02) · —

Figure 以 S2 语义规划、S1 视觉运动策略和 S0 全身控制连接语言目标与移动操作。

范围说明：公司技术展示；公开视频不能替代可复现实验和开放训练代码。

机构 / 维护方：Figure AI。

<sub>计数快照：2026-11-02。</sub>
