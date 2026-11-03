# 01 · LLM 基础

**中文** | [English](01-LLM-Foundations.en.md)

[返回首页](README.md) · [完整索引](CATALOG.md) · [Survey 与教学参考](SURVEYS.md#llm-learning)

从 LLM 原理直接开始，面向进入 Omni、Voice Agent 与具身交互研究的本科生及团队成员。已熟悉的主题可直接跳到对应论文或实践入口。

## 🧭 简短阅读路线

| 顺序 / 主题 | 首读资源 | 阅读目标与最小实践 |
|---|---|---|
| 1 · 语言模型与 Transformer | [Happy-LLM](https://github.com/datawhalechina/happy-llm) 第 2–4 章（中文）；[The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)（英文） | 理解 token、Embedding、因果注意力、decoder-only 和下一 token 预测；画出输入到输出的路径。图解原文重心为 encoder–decoder，结合教材补齐现代 LLM。 |
| 2 · 使用与理解生成 | [HF LLM Course 英文](https://huggingface.co/learn/llm-course/chapter1/1) 第 1–3 章；[中文入口](https://huggingface.co/learn/llm-course/zh-CN/chapter1/1) | 跑通一个小模型，检查 tokenizer、聊天模板与生成参数；比较两种采样设置的输出。 |
| 3 · 数据与预训练 | [Happy-LLM](https://github.com/datawhalechina/happy-llm) 第 5 章；[FineWeb 官方博客](https://huggingfacefw-blogpost-fineweb-v1.static.hf.space/index.html) 的过滤与去重部分（英文案例） | 解释训练样本、损失与验证结果的关系；用小样本检查重复和过滤前后的变化。 |
| 4 · 后训练 | [Happy-LLM](https://github.com/datawhalechina/happy-llm) 第 6 章；[HF LLM Course](https://huggingface.co/learn/llm-course/chapter1/1) 第 11 章（英文）；[TRL SFT](https://huggingface.co/docs/trl/en/sft_trainer)（实践文档） | 区分预训练、SFT、LoRA 与偏好优化；在资源允许时做一次小规模 SFT/LoRA，并检查哪些 token 参与损失。 |
| 5 · 强化学习与偏好优化 | [HF LLM Course 第 12 章](https://huggingface.co/learn/llm-course/chapter12/1)；下方 [RL 阅读表](#rl) | 理解 rollout、reward、advantage 和 policy update；区分 RLHF、RLVR 与 PPO、GRPO。 |
| 6 · 评测与推理 | [《大语言模型》](https://llmbook-zh.github.io/)的能力评测与推理相关章节（中文）；[Lighteval](https://huggingface.co/docs/lighteval/)（英文工具文档） | 区分指标、benchmark 与评测框架；固定任务和模板比较基础模型与微调模型，记录质量、首 token 延迟及生成速度。 |

HF 中英文课程的章节覆盖并不完全同步；上表章节编号以对应语言页面为准。中文教程与英文课程是互补阅读入口，不默认互为逐字翻译。资源要求、显存和依赖以所选实践的官方说明为准。

<a id="rl"></a>
## 🎯 强化学习与偏好优化

最小循环：模型生成候选回答 → 奖励函数或环境给分 → 计算优势 → 更新策略 → 在独立任务上评测。SFT 学示范答案；在线 RL 用当前策略产生的新轨迹学习。

| 概念 | 先分清什么 |
|---|---|
| RLHF / RLAIF / RLVR | 区分反馈来自人类偏好、模型判断还是可验证结果。 |
| PPO / GRPO | 优化策略的算法；GRPO 用同一问题的一组回答构造相对优势。 |
| DPO | 从优选 / 劣选回答直接进行偏好优化，通常不运行在线环境采样。 |
| Reward / Benchmark | 训练奖励用于更新策略；独立评测检查泛化、奖励投机和退化。 |

| 论文 / 项目 | 发表与来源 | 阅读重点与入口 |
|---|---|---|
| ⭐ [PPO](CATALOG.md#e75) | [![arXiv 2017](https://img.shields.io/badge/arXiv%202017-475569?style=flat-square)](https://arxiv.org/abs/1707.06347) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/1707.06347) | 通过限制策略更新幅度，在采样轨迹上优化奖励；理解后续 RLHF 的算法基础。<br>[📄 论文](https://arxiv.org/abs/1707.06347) · [💻 仓库](https://github.com/openai/baselines) |
| ⭐ [InstructGPT / RLHF](CATALOG.md#e76) | [![NeurIPS 2022](https://img.shields.io/badge/NeurIPS%202022-475569?style=flat-square)](https://arxiv.org/abs/2203.02155) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2203.02155) | 用示范进行 SFT、用人类排序训练奖励模型，再用 PPO 优化语言模型。<br>[📄 论文](https://arxiv.org/abs/2203.02155) |
| ⭐ [DPO](CATALOG.md#e77) | [![NeurIPS 2023](https://img.shields.io/badge/NeurIPS%202023-475569?style=flat-square)](https://arxiv.org/abs/2305.18290) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2305.18290) | 直接从优选与劣选回答优化相对概率，理解离线偏好优化与在线 RL 的差别。<br>[📄 论文](https://arxiv.org/abs/2305.18290) · [💻 仓库](https://github.com/eric-mitchell/direct-preference-optimization) |
| ⭐ [DeepSeekMath / GRPO](CATALOG.md#e78) | [![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2402.03300) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2402.03300) | 在数学推理中提出 GRPO，以同一问题的多条采样回答构造相对优势。<br>[📄 论文](https://arxiv.org/abs/2402.03300) · [💻 仓库](https://github.com/deepseek-ai/DeepSeek-Math) |
| [DeepSeek-R1](CATALOG.md#e79) | [![Nature 2025](https://img.shields.io/badge/Nature%202025-475569?style=flat-square)](https://www.nature.com/articles/s41586-025-09422-z) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2501.12948) | 研究推理强化学习、冷启动、多阶段后训练与小模型蒸馏。<br>[📄 论文](https://arxiv.org/abs/2501.12948) · [💻 仓库](https://github.com/deepseek-ai/DeepSeek-R1) |

实践入口：[HF GRPO 教学](https://huggingface.co/learn/llm-course/chapter12/1) → [TRL](https://github.com/huggingface/trl)；分布式 rollout 与训练查阅 [verl](https://github.com/verl-project/verl)。先在小模型、短输出和可验证任务上跑通奖励与日志，再扩展任务。

进入语音和具身方向时，先确定优化对象：文本回答、工具选择、语音 token、开口/打断时机，或机器人动作。工具成功、语音可懂度和机器人任务完成需要不同的奖励与评测。

## 🔬 按需深入

| 资源 | 用途 | 推荐阅读范围 |
|---|---|---|
| [Smol Training Playbook](https://huggingfacetb-smol-training-playbook.hf.space/) · 英文 | 数据配比、训练配置、消融与计算成本的工程案例 | 按当前问题查阅数据、架构或训练章节。 |
| [Stanford CS336](https://cs336.stanford.edu/) · 英文课程 | 从组件实现走向完整语言模型训练 | 先看课程概览与 Basics 作业，再按需阅读 Data、Alignment；系统优化作为扩展。 |
| [A Survey of Large Language Models](https://arxiv.org/abs/2303.18223) · 英文综述；[作者仓库](https://github.com/RUCAIBox/LLMSurvey) | 预训练、适配、使用与能力评测的全景索引 | 按主题查询原论文，不要求顺序通读。 |

## 🔗 分类与引用依据

主题参考 [LLM Survey](https://arxiv.org/abs/2303.18223) 的预训练、适配与评测，以及 [CS336](https://cs336.stanford.edu/) 的数据、训练和对齐；入门讲解对应 Happy-LLM 与 HF LLM Course。

进入语音方向前，重点带走四个问题：输入如何变成 token 或表示？模型在什么目标上训练？输出如何流式生成？效果和延迟如何分别测量？

下一步：[ALM / Omni 基础 →](02-Omni-Foundations.md)
