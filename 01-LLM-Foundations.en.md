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
| 5 · Evaluation and inference | Evaluation and inference sections of the Chinese [LLM textbook](https://llmbook-zh.github.io/); [Lighteval](https://huggingface.co/docs/lighteval/) (English tooling documentation) | Distinguish metrics, benchmarks, and evaluation frameworks. Compare base and fine-tuned models with fixed tasks and templates; record quality, time to first token, and generation speed. |

The Chinese and English HF course editions do not have identical coverage. Check chapter numbering in the linked language. Chinese tutorials and English courses are complementary resources, not necessarily translations of one another. Follow each exercise's official requirements for dependencies and hardware.

## 🔬 Further reading as needed

| Resource | Purpose | Suggested scope |
|---|---|---|
| [Smol Training Playbook](https://huggingfacetb-smol-training-playbook.hf.space/) · English | Engineering case studies in data mixtures, training configurations, ablations, and compute cost | Select data, architecture, or training sections for the problem at hand. |
| [Stanford CS336](https://cs336.stanford.edu/) · English course | From component implementation to a complete language-model training pipeline | Begin with the overview and Basics assignment; consult Data and Alignment as needed. Systems optimization is an extension. |
| [A Survey of Large Language Models](https://arxiv.org/abs/2303.18223) · English survey; [author repository](https://github.com/RUCAIBox/LLMSurvey) | A map of pretraining, adaptation, utilization, and capability evaluation | Use it to locate original papers by topic rather than reading it linearly. |

## 🔗 Organization and attribution

This page uses an introductory reading sequence, with data, architecture, training, post-training, evaluation, and inference as topic indexes. Coverage is informed by the LLM Survey and CS336; teaching resources include Happy-LLM and the HF LLM Course. The ordering and small exercises are reading recommendations, not a claim that the source courses or surveys use this exact taxonomy. Links point to the authors or official resources.

Before moving into speech, keep four questions in view: how is input represented, what objective trains the model, how is output streamed, and how are quality and latency measured separately?

Next: [Omni Foundations →](02-Omni-Foundations.en.md)
