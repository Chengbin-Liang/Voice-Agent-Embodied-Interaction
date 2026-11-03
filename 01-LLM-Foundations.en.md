# 01 · LLM Foundations

[中文](01-LLM-Foundations.md) | **English**

[Home](README.en.md) · [Catalog](CATALOG.en.md) · [Surveys and teaching references](SURVEYS.en.md#llm-learning)

Start directly with LLM principles. This reading route is for undergraduates and team members moving toward Omni models, voice agents, and embodied interaction. Skip familiar topics and go directly to the relevant paper or implementation.

## 🧭 A short reading route

| Order / topic | Start here | Learning goal and small exercise |
|---|---|---|
| 1 · Language models and Transformers | [Happy-LLM](https://github.com/datawhalechina/happy-llm), Chapters 2–4 (Chinese); [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) (English) | Understand tokens, embeddings, causal attention, decoder-only models, and next-token prediction; sketch the input-to-output path. The illustrated article focuses on the original encoder–decoder architecture, so supplement it with modern LLM material. |
| 2 · Using models and understanding generation | [HF LLM Course](https://huggingface.co/learn/llm-course/chapter1/1), Chapters 1–3 (English); [Chinese edition](https://huggingface.co/learn/llm-course/zh-CN/chapter1/1) | Run a small model, inspect its tokenizer, chat template, and generation settings, then compare outputs under two sampling configurations. |
| 3 · Data and pretraining | [Happy-LLM](https://github.com/datawhalechina/happy-llm), Chapter 5; filtering and deduplication sections of the [FineWeb report](https://huggingfacefw-blogpost-fineweb-v1.static.hf.space/index.html) (English case study) | Explain the relationship between training examples, loss, and validation results; inspect duplicates and filtering effects on a small sample. |
| 4 · Post-training | [Happy-LLM](https://github.com/datawhalechina/happy-llm), Chapter 6; [HF LLM Course](https://huggingface.co/learn/llm-course/chapter1/1), Chapter 11 (English); [TRL SFT](https://huggingface.co/docs/trl/en/sft_trainer) (implementation documentation) | Distinguish pretraining, SFT, LoRA, and preference optimization. If resources permit, run a small SFT/LoRA experiment and check which tokens contribute to the loss. |
| 5 · RL and preference optimization | [HF LLM Course, Chapter 12](https://huggingface.co/learn/llm-course/chapter12/1); [RL readings below](#rl) | Understand rollouts, rewards, advantages, and policy updates; distinguish feedback sources from algorithms. |
| 6 · Evaluation and inference | Evaluation and inference sections of the Chinese [LLM textbook](https://llmbook-zh.github.io/); [Lighteval](https://huggingface.co/docs/lighteval/) (English tooling documentation) | Distinguish metrics, benchmarks, and evaluation frameworks. Compare base and fine-tuned models with fixed tasks and templates; record quality, time to first token, and generation speed. |

The Chinese and English HF course editions do not have identical coverage. Check chapter numbering in the linked language. Chinese tutorials and English courses are complementary resources, not necessarily translations of one another. Follow each exercise's official requirements for dependencies and hardware.

<a id="rl"></a>
## 🎯 Reinforcement learning and preference optimization

Minimal loop: sample responses → score them with a reward function or environment → estimate advantages → update the policy → evaluate on held-out tasks. SFT learns from demonstrations; online RL learns from newly sampled trajectories.

| Concept | Key distinction |
|---|---|
| RLHF / RLAIF / RLVR | Feedback from human preferences, model judgments, or verifiable outcomes. |
| PPO / GRPO | Policy optimization algorithms; GRPO derives relative advantages within a group of responses to the same prompt. |
| DPO | Direct preference optimization from preferred/rejected pairs, typically without online environment sampling. |
| Reward / benchmark | Training rewards drive updates; independent evaluation checks generalization, reward exploitation, and regressions. |

| Paper / project | Publication and affiliation | Reading focus and resources |
|---|---|---|
| ⭐ [PPO](CATALOG.en.md#e75) | [![arXiv 2017](https://img.shields.io/badge/arXiv%202017-475569?style=flat-square)](https://arxiv.org/abs/1707.06347) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/1707.06347) | Optimizes rewards on sampled trajectories while constraining policy updates; a foundation for subsequent RLHF methods.<br>[📄 Paper](https://arxiv.org/abs/1707.06347) · [💻 Repository](https://github.com/openai/baselines) |
| ⭐ [InstructGPT / RLHF](CATALOG.en.md#e76) | [![NeurIPS 2022](https://img.shields.io/badge/NeurIPS%202022-475569?style=flat-square)](https://arxiv.org/abs/2203.02155) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2203.02155) | Combines supervised demonstrations, a reward model trained on human rankings, and PPO optimization.<br>[📄 Paper](https://arxiv.org/abs/2203.02155) |
| ⭐ [DPO](CATALOG.en.md#e77) | [![NeurIPS 2023](https://img.shields.io/badge/NeurIPS%202023-475569?style=flat-square)](https://arxiv.org/abs/2305.18290) [![Academic](https://img.shields.io/badge/Academic-2563eb?style=flat-square)](https://arxiv.org/html/2305.18290) | Optimizes relative response probabilities from preference pairs, providing an offline alternative to online RL.<br>[📄 Paper](https://arxiv.org/abs/2305.18290) · [💻 Repository](https://github.com/eric-mitchell/direct-preference-optimization) |
| ⭐ [DeepSeekMath / GRPO](CATALOG.en.md#e78) | [![arXiv 2024](https://img.shields.io/badge/arXiv%202024-475569?style=flat-square)](https://arxiv.org/abs/2402.03300) [![Academic + Industry](https://img.shields.io/badge/Academic%20%2B%20Industry-7c3aed?style=flat-square)](https://arxiv.org/html/2402.03300) | Introduces GRPO for mathematical reasoning, deriving relative advantages from groups of sampled answers.<br>[📄 Paper](https://arxiv.org/abs/2402.03300) · [💻 Repository](https://github.com/deepseek-ai/DeepSeek-Math) |
| [DeepSeek-R1](CATALOG.en.md#e79) | [![Nature 2025](https://img.shields.io/badge/Nature%202025-475569?style=flat-square)](https://www.nature.com/articles/s41586-025-09422-z) [![Industry](https://img.shields.io/badge/Industry-0f766e?style=flat-square)](https://arxiv.org/html/2501.12948) | Studies reasoning RL, cold starts, multistage post-training, and distillation into smaller models.<br>[📄 Paper](https://arxiv.org/abs/2501.12948) · [💻 Repository](https://github.com/deepseek-ai/DeepSeek-R1) |

Practice: [HF GRPO lessons](https://huggingface.co/learn/llm-course/chapter12/1) → [TRL](https://github.com/huggingface/trl). For distributed rollouts and training, see [verl](https://github.com/verl-project/verl). Start with small models, short outputs, and verifiable tasks to validate rewards and logging.

For speech and robotics, identify the optimization target first: text answers, tool selection, speech tokens, speaking/interruption timing, or robot actions. Tool success, speech intelligibility, and physical task completion need different rewards and evaluations.

## 🔬 Further reading as needed

| Resource | Purpose | Suggested scope |
|---|---|---|
| [Smol Training Playbook](https://huggingfacetb-smol-training-playbook.hf.space/) · English | Engineering case studies in data mixtures, training configurations, ablations, and compute cost | Select data, architecture, or training sections for the problem at hand. |
| [Stanford CS336](https://cs336.stanford.edu/) · English course | From component implementation to a complete language-model training pipeline | Begin with the overview and Basics assignment; consult Data and Alignment as needed. Systems optimization is an extension. |
| [A Survey of Large Language Models](https://arxiv.org/abs/2303.18223) · English survey; [author repository](https://github.com/RUCAIBox/LLMSurvey) | A map of pretraining, adaptation, utilization, and capability evaluation | Use it to locate original papers by topic rather than reading it linearly. |

## 🔗 Organization and attribution

Topics draw on the [LLM Survey](https://arxiv.org/abs/2303.18223) and [CS336](https://cs336.stanford.edu/); introductory explanations come from Happy-LLM and the HF LLM Course.

Before moving into speech, keep four questions in view: how is input represented, what objective trains the model, how is output streamed, and how are quality and latency measured separately?

Next: [ALM / Omni Foundations →](02-Omni-Foundations.en.md)
