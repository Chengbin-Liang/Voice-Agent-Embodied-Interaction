# 01 · LLM & Agent Foundations

[中文](../zh/01-LLM-Foundations.md) | **English**

[Home](../../README.en.md) · [Full catalog](../../resources/en/CATALOG.md) · [Surveys & teaching resources](../../resources/en/SURVEYS.md#llm-learning)

Reading sequence: Happy-LLM → agent fundamentals → ALM / Omni.

<a id="course"></a>
## 📘 Core course: Happy-LLM

⭐ [Happy-LLM: building language models from scratch](https://github.com/datawhalechina/happy-llm) · [Read online](https://datawhalechina.github.io/happy-llm/)

Priority rationale: a systematic introduction to architecture, data, training, and applications provides LLM foundations for speech and embodied research. The chapter links below point to the Chinese edition.

| Topic | Chapters | Core concepts |
|---|---|---|
| Model fundamentals | [Chapter 2](https://github.com/datawhalechina/happy-llm/blob/main/docs/chapter2/%E7%AC%AC%E4%BA%8C%E7%AB%A0%20Transformer%E6%9E%B6%E6%9E%84.md) and Chapters 3–4 | Attention, language-model architectures, and generation objectives. |
| Data and model construction | [Chapter 5](https://github.com/datawhalechina/happy-llm/blob/main/docs/chapter5/%E7%AC%AC%E4%BA%94%E7%AB%A0%20%E5%8A%A8%E6%89%8B%E6%90%AD%E5%BB%BA%E5%A4%A7%E6%A8%A1%E5%9E%8B.md) | Tokenization, training examples, model components, and pretraining. |
| Model training | [Chapter 6](https://github.com/datawhalechina/happy-llm/blob/main/docs/chapter6/%E7%AC%AC%E5%85%AD%E7%AB%A0%20%E5%A4%A7%E6%A8%A1%E5%9E%8B%E8%AE%AD%E7%BB%83%E6%B5%81%E7%A8%8B%E5%AE%9E%E8%B7%B5.md) | Objectives and workflows for pretraining, SFT, and LoRA / QLoRA. |
| Evaluation and applications | [Chapter 7](https://github.com/datawhalechina/happy-llm/blob/main/docs/chapter7/%E7%AC%AC%E4%B8%83%E7%AB%A0%20%E5%A4%A7%E6%A8%A1%E5%9E%8B%E5%BA%94%E7%94%A8.md) | Model evaluation, RAG, and agent components. |

For post-training research, consult [Chapter 8: reinforcement learning for LLMs](https://github.com/datawhalechina/happy-llm/blob/main/docs/chapter8/%E7%AC%AC%E5%85%AB%E7%AB%A0%20%E5%A4%A7%E6%A8%A1%E5%9E%8B%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0.md) and the [related paper index](../../resources/en/CATALOG.md#e75) as needed.

<a id="agents"></a>
## 🛠️ Agent fundamentals

| Reading | Format / language | Reading focus |
|---|---|---|
| ⭐ [Hello-Agents](https://github.com/datawhalechina/hello-agents) | Tutorial · Chinese | Continues from Happy-LLM with tools, classic agent patterns, and interaction-loop implementation. |
| [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/unit0/introduction) | Course · English | Suggested sections are Unit 1 fundamentals and Unit 4 construction and evaluation; framework lessons depend on implementation needs. |
| [Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) | Engineering blog · English · 2024 | Distinguish predefined workflows from autonomous agents and understand tools, routing, and feedback loops. |
| [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) | Conceptual blog · English · 2023 | Organize planning, memory, and tool use; read as a conceptual introduction. |
| [ReAct: Synergizing Reasoning and Acting in Language Models](https://react-lm.github.io/) · [Paper](https://arxiv.org/abs/2210.03629) | Classic paper · English | Alternating reasoning, actions, and observations, including the effect of environmental feedback on subsequent actions. |

Core concepts: model responses, tool calls, environmental feedback, and task completion. [Voice agents](03-Voice-Agent.md) add speech input/output, turn-taking, and interruption; [embodied interaction](04-Edge-Embodied-Interaction.md) adds perception, action execution, and task feedback.

## 🔎 Reference shelf

[LLM surveys and teaching resources](../../resources/en/SURVEYS.md#llm-learning) link to original papers, textbooks, and further courses.

Next: [ALM / Omni Foundations →](02-Omni-Foundations.md)
