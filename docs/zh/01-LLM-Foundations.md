# 01 · LLM 与 Agent 基础

**中文** | [English](../en/01-LLM-Foundations.md)

[返回首页](../../README.md) · [完整索引](../../resources/zh/CATALOG.md) · [Survey 与教学参考](../../resources/zh/SURVEYS.md#llm-learning)

从 LLM 原理直接开始，以 **Happy-LLM → Agent 入门 → ALM / Omni** 为阅读顺序。熟悉的部分可以跳过。

<a id="course"></a>
## 📘 主线：Happy-LLM

⭐ [Happy-LLM：从零开始构建大模型](https://github.com/datawhalechina/happy-llm) · [在线阅读](https://datawhalechina.github.io/happy-llm/)

优先理由：同一套中文教程串起架构、数据、训练和应用，适合建立完整概念，再进入语音与具身论文。

| 主题 | 对应章节 | 阅读要点 |
|---|---|---|
| 模型原理 | [第 2 章](https://github.com/datawhalechina/happy-llm/blob/main/docs/chapter2/%E7%AC%AC%E4%BA%8C%E7%AB%A0%20Transformer%E6%9E%B6%E6%9E%84.md)及第 3–4 章 | 注意力、语言模型架构与生成目标。 |
| 数据与模型构建 | [第 5 章](https://github.com/datawhalechina/happy-llm/blob/main/docs/chapter5/%E7%AC%AC%E4%BA%94%E7%AB%A0%20%E5%8A%A8%E6%89%8B%E6%90%AD%E5%BB%BA%E5%A4%A7%E6%A8%A1%E5%9E%8B.md) | Tokenizer、训练样本、模型组件与预训练。 |
| 模型训练 | [第 6 章](https://github.com/datawhalechina/happy-llm/blob/main/docs/chapter6/%E7%AC%AC%E5%85%AD%E7%AB%A0%20%E5%A4%A7%E6%A8%A1%E5%9E%8B%E8%AE%AD%E7%BB%83%E6%B5%81%E7%A8%8B%E5%AE%9E%E8%B7%B5.md) | 预训练、SFT、LoRA / QLoRA 的目标与流程。 |
| 评测与应用 | [第 7 章](https://github.com/datawhalechina/happy-llm/blob/main/docs/chapter7/%E7%AC%AC%E4%B8%83%E7%AB%A0%20%E5%A4%A7%E6%A8%A1%E5%9E%8B%E5%BA%94%E7%94%A8.md) | 模型评测、RAG 与 Agent 的基本组成。 |

需要研究后训练时，再查阅课程[第 8 章：大模型强化学习](https://github.com/datawhalechina/happy-llm/blob/main/docs/chapter8/%E7%AC%AC%E5%85%AB%E7%AB%A0%20%E5%A4%A7%E6%A8%A1%E5%9E%8B%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0.md)及[相关论文索引](../../resources/zh/CATALOG.md#e75)。

<a id="agents"></a>
## 🛠️ Agent 入门

| 读物 | 类型 / 语言 | 阅读重点与优先理由 |
|---|---|---|
| ⭐ [Hello-Agents](https://github.com/datawhalechina/hello-agents) | 教程 · 中文 | 接续 Happy-LLM；从工具使用、经典 Agent 范式到可运行系统，先建立完整交互循环。 |
| ⭐ [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/unit0/introduction) | 课程 · 英文 | 先读 Unit 1 的基础与 Unit 4 的构建和评测；框架章节按需选择。适合把概念变成一次可检验的任务执行。 |
| ⭐ [Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) | 工程博客 · 英文 · 2024 | 区分预定义工作流与自主 Agent，理解何时需要工具、路由和反馈循环。 |
| [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) | 概念博客 · 英文 · 2023 | 按规划、记忆与工具使用建立结构图；作为概念读物阅读。 |
| [ReAct: Synergizing Reasoning and Acting in Language Models](https://react-lm.github.io/) · [论文](https://arxiv.org/abs/2210.03629) | 经典论文 · 英文 | 理解推理、动作、环境观察如何交替，以及环境反馈如何修正后续行动。 |

读完应能分清：**模型回答、工具调用、环境反馈、任务完成**。进入 [Voice Agent](03-Voice-Agent.md) 时，再加入语音输入输出、轮次与打断；进入 [具身交互](04-Edge-Embodied-Interaction.md) 时，再加入感知、动作执行与任务反馈。

## 🔎 按问题查阅

[LLM Survey 与教学参考](../../resources/zh/SURVEYS.md#llm-learning)提供原论文、教材与进阶课程入口。

下一步：[ALM / Omni 基础 →](02-Omni-Foundations.md)
