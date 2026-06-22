---
layout: single
permalink: /blogs/llm-uncertainty-quantification-survey/
title: "UQ & Confidence Calibration in LLMs: A Survey"
author_profile: true
---

# Uncertainty Quantification and Confidence Calibration in Large Language Models: A Survey

**Xiaoou Liu\*, Tiejin Chen\*, Longchao Da, Chacha Chen, Zhen Lin, Hua Wei**  
*KDD'25 Survey Track*  
[\[Paper\]](https://arxiv.org/abs/2503.15850) [\[Github\]](https://github.com/Xiao0o0o/Awesome-UQ-in-LLMs) [\[Tutorial Page\]](https://xiao0o0o.github.io/2025KDD_tutorial/)

---

## TL;DR

LLMs are increasingly used in high-stakes domains like healthcare, law, and transportation, but they can be confidently wrong. This survey provides a comprehensive overview of **uncertainty quantification (UQ)** and **confidence calibration** methods for LLMs, introducing a novel taxonomy that organizes methods along two key axes: computational efficiency and uncertainty dimensions.

---

## Why Uncertainty Quantification Matters for LLMs

Large Language Models excel in text generation, reasoning, and decision-making. However, their deployment in safety-critical applications requires us to know *when we can trust their outputs*. Uncertainty quantification addresses this by estimating confidence in model outputs, enabling risk mitigation and selective prediction.

The challenges unique to LLMs include:
- **Computational constraints**: Many classical UQ methods are prohibitively expensive for billion-parameter models.
- **Diverse uncertainty sources**: Uncertainty in LLMs can arise from the input, the reasoning process, the model parameters, or the final prediction.
- **Black-box access**: Most frontier models are only available through APIs, ruling out internal-access methods.

---

## Our Taxonomy

We categorize UQ methods along two orthogonal axes:

### Axis 1: Computational Efficiency

- **Single-pass methods**: Extract uncertainty signals from a single forward pass. Fast but potentially less reliable.
- **Sampling-based methods**: Generate multiple outputs and measure consistency. More accurate but computationally expensive.

### Axis 2: Uncertainty Dimensions

- **Input uncertainty**: Ambiguity or noise in the prompt itself.
- **Reasoning uncertainty**: Inconsistencies or errors that accumulate across reasoning steps.
- **Parametric uncertainty**: Arising from model weights and training data limitations.
- **Predictive uncertainty**: The overall uncertainty in the final output.

---

## Key Topics Covered

The survey systematically reviews:

- **Confidence Estimation**: Methods ranging from verbalized confidence to logit-based and sampling-based approaches.
- **Calibration Techniques**: How to align model confidence with actual accuracy, including temperature scaling and LLM-specific approaches.
- **Conformal Prediction**: Distribution-free methods that provide formal coverage guarantees for LLM outputs.
- **Evaluation Metrics**: Expected Calibration Error (ECE), Brier scores, AUROC, and their variants for generative settings.
- **Applications**: UQ in retrieval-augmented generation, multi-agent systems, reasoning chains, and safety-critical deployment.

---

## Open Challenges

We identify several open research directions:

- Developing **efficient UQ methods** that scale to the largest models without sacrificing reliability.
- Building **step-level confidence estimation** for chain-of-thought reasoning (which motivated our ICML'26 follow-up work).
- Creating **standardized benchmarks** for evaluating UQ in diverse LLM tasks beyond MCQA.
- Bridging the gap between **white-box and black-box** UQ methods.

---

## Takeaway

As LLMs move from research demos to real-world deployment, knowing when to trust their outputs becomes critical. This survey provides a structured roadmap for the UQ community, organizing what exists, identifying what's missing, and pointing toward what needs to be built next.
