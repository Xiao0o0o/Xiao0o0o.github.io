---
layout: prism
title: "Curriculum Vitae"
permalink: /cv/
redirect_from:
  - /resume
---

{% assign cv_pdf = "/files/Xiaoou_Liu_CV.pdf" %}
{% assign has_pdf = site.static_files | where: "path", cv_pdf | size %}
<div class="cv-actions">
  {% if has_pdf > 0 %}<a class="btn btn-primary" href="{{ site.baseurl }}{{ cv_pdf }}" target="_blank" rel="noopener">Download PDF</a>{% endif %}
  <a class="btn btn-outline" href="mailto:{{ site.author.email }}">{{ site.author.email }}</a>
</div>

## Education

<div class="cv-entry"><span class="cv-entry-title">Ph.D. in Computer Science, Arizona State University</span><span class="cv-entry-date">Sep 2024 – Now</span></div>

<div class="cv-entry"><span class="cv-entry-title">M.Sc. in Computer Science, University of British Columbia</span><span class="cv-entry-date">Sep 2021 – May 2024</span></div>

<div class="cv-entry"><span class="cv-entry-title">B.Eng. in Computer Science, Beijing Jiaotong University</span><span class="cv-entry-date">Sep 2017 – Jul 2021</span></div>

## Research Interests

- **Uncertainty Quantification in LLMs**: Developing methods to quantify uncertainty and confidence in LLM outputs and using these estimates to enhance reasoning performance, efficiency, and reliability.
- **Learning and Adaptation in LLM Agents**: Developing LLM agents that continually learn from interaction, acquire and refine reusable skills, and optimize multi-agent coordination for reliable real-world applications.

## Industry Experience

<div class="cv-entry"><span class="cv-entry-title">TikTok, Research Scientist Intern</span><span class="cv-entry-date">May 2026 – Aug 2026</span></div>

- Built an AI agent that analyzes user reports to identify why content was flagged, turning noisy, large-scale, real-world feedback into reliable, actionable signals with over 90% precision.

## Research Projects

<div class="cv-entry"><span class="cv-entry-title">Reliable LLM Reasoning: Uncertainty, Confidence, and Diversity</span><span class="cv-entry-date">Aug 2024 – Present</span></div>

- **Step-Wise Confidence Attribution:** Proposed a black-box framework based on the Information Bottleneck principle that assigns confidence scores to individual reasoning steps by identifying consensus structures across correct solutions, improving self-correction success rates by up to 13.5% over answer-level feedback.
- **Diverse Reasoning Paths for RLVR:** Studied how reasoning diversity in SFT affects downstream RL and proposed EquivAug, a symbolic-equivalence augmentation method that generates diverse, provably correct reasoning paths, achieving top post-SFT diversity and post-GRPO accuracy on GSM8K and FOLIO.
- **Input Ambiguity Detection:** Developed a perturbation-based framework that detects whether an input admits multiple plausible interpretations before answer generation, using response variations under controlled perturbations to distinguish inherent ambiguity from unreliable model behavior.
- **Survey and Taxonomy:** Authored a comprehensive survey introducing a taxonomy of UQ for LLMs based on computational efficiency and four sources of uncertainty: input, reasoning, parameters, and prediction.

<div class="cv-entry"><span class="cv-entry-title">Adaptive and Reliable LLM Agents</span><span class="cv-entry-date">Dec 2025 – Present</span></div>

- **Robustness Benchmark for Mobile Agents:** Introduced *AndroidReality*, an AndroidWorld-based benchmark testing mobile-agent robustness to state, transition, and action perturbations, and developed a training-free recovery method that improves performance in both perturbed and clean settings.
- **Self-Improving Multi-Agent LLM Systems:** Developed LangMARL and MASkills, two frameworks that let multi-agent LLM systems improve through interaction. LangMARL introduces agent-level language credit assignment and natural-language policy optimization; MASkills extends this to skill-level credit assignment and the continual evolution of reusable skill libraries.

## Honors and Awards

- SDM Doctoral Student Forum Travel Award
- IROS 2026 IEEE RAS Travel Support
- Best Artifact Award, ICCPS 2025
- ASU Fulton Fellow Scholarship
- UBC Graduate Research Scholarship (awarded twice)
- UBC Graduate Dean's Entrance Scholarship

## Teaching

{% for t in site.data.teaching %}
<div class="cv-entry"><span class="cv-entry-title">{{ t.role }}, {{ t.course }}</span><span class="cv-entry-date">{{ t.term }}</span></div>
<p class="cv-entry-sub">{{ t.school }}</p>
{% endfor %}

## Service

- **Tutorials:** "Uncertainty Quantification and Confidence Calibration in LLMs" at [ICDM 2025](https://darl-genai.github.io/ICDM-UQ-LLM-Tutorial/) and [KDD 2025]({{ site.baseurl }}/2025KDD_tutorial/)
- **Peer Reviewer:** ACL 2025 Demo, PAKDD 2026, NeurIPS 2026 Datasets & Benchmarks, ACL 2026, EMNLP 2026
