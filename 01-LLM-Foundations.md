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
| 5 · 评测与推理 | [《大语言模型》](https://llmbook-zh.github.io/)的能力评测与推理相关章节（中文）；[Lighteval](https://huggingface.co/docs/lighteval/)（英文工具文档） | 区分指标、benchmark 与评测框架；固定任务和模板比较基础模型与微调模型，记录质量、首 token 延迟及生成速度。 |

HF 中英文课程的章节覆盖并不完全同步；上表章节编号以对应语言页面为准。中文教程与英文课程是互补阅读入口，不默认互为逐字翻译。资源要求、显存和依赖以所选实践的官方说明为准。

## 🔬 按需深入

| 资源 | 用途 | 推荐阅读范围 |
|---|---|---|
| [Smol Training Playbook](https://huggingfacetb-smol-training-playbook.hf.space/) · 英文 | 数据配比、训练配置、消融与计算成本的工程案例 | 按当前问题查阅数据、架构或训练章节。 |
| [Stanford CS336](https://cs336.stanford.edu/) · 英文课程 | 从组件实现走向完整语言模型训练 | 先看课程概览与 Basics 作业，再按需阅读 Data、Alignment；系统优化作为扩展。 |
| [A Survey of Large Language Models](https://arxiv.org/abs/2303.18223) · 英文综述；[作者仓库](https://github.com/RUCAIBox/LLMSurvey) | 预训练、适配、使用与能力评测的全景索引 | 按主题查询原论文，不要求顺序通读。 |

## 🔗 分类与引用依据

本页采用适合入门的阅读顺序，并以数据、架构、训练、后训练、评测与推理作为主题索引。框架参考上列 LLM Survey 与 CS336 的覆盖范围；教学入口参考 Happy-LLM 和 HF LLM Course。本页的排列与最小实践是阅读建议，不代表原课程或综述使用完全相同的分类。各资源保留作者或官方页面链接。

进入语音方向前，重点带走四个问题：输入如何变成 token 或表示？模型在什么目标上训练？输出如何流式生成？效果和延迟如何分别测量？

下一步：[Omni 基础 →](02-Omni-Foundations.md)
