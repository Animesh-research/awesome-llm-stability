
# awesome-llm-stability
This repository investigates the vulnerabilities introduced by Large Language Models (LLMs) in scientific workflows due to prompt sensitivity. It explores how trivial variations in input prompts can drastically alter model outputs, thereby compromising objective truth and scientific reproducibility.# 🚀 Awesome LLM Prompt Robustness

## 📑 Table of Contents
* [🌟 Topic Overview](#-topic-overview)
* [📄 AI-Assisted Research Paper](#-ai-assisted-research-paper)
* [🔍 Citation Integrity Audit](#-citation-integrity-audit)
* [📚 Curated Research Papers](#-curated-research-papers)
  * [Foundational Papers](#foundational-papers)
  * [Mechanics of Prompt Sensitivity](#mechanics-of-prompt-sensitivity)
  * [Optimization and Mitigation Strategies](#optimization-and-mitigation-strategies)
  * [Surveys and Evaluation Metrics](#surveys-and-evaluation-metrics)
* [📊 Datasets](#-datasets)
* [🛠️ Tools and Libraries](#️-tools-and-libraries)
* [💻 GitHub Implementations](#-github-implementations)
* [🎓 Tutorials and Learning Resources](#-tutorials-and-learning-resources)
* [📜 License](#-license)

---

## 🌟 Topic Overview
Large Language Models (LLMs) have fundamentally disrupted traditional research methodologies, accelerating tasks such as literature synthesis, data analysis, and qualitative coding[cite: 1]. However, the integration of these models introduces a critical vulnerability: **acute prompt sensitivity**[cite: 1]. This repository explores the structural instability of LLMs, where minor lexical changes, syntactic formatting variations, or shifts in the order of in-context examples produce significantly divergent outputs[cite: 1].

In scientific research, this brittleness threatens the foundational principles of reproducibility and objective truth[cite: 1]. When research conclusions rely on LLM-assisted interpretation, the fragility of the input prompt directly translates to the fragility of the final empirical claims, creating a hidden variance dictated by subjective linguistic choices rather than empirical reality[cite: 1].

This curated collection investigates the underlying mechanics of prompt sensitivity, including majority label bias, recency bias, and semantic drift in long-context windows[cite: 1]. It highlights current programmatic and architectural interventions designed to mitigate these flaws, such as prompt ensembling, self-consistency frameworks, automatic prompt optimization, and contextual calibration techniques[cite: 1]. Ultimately, this repository aims to provide researchers and engineers with the resources necessary to understand LLM vulnerabilities, establish rigorous reporting standards, and build epistemological frameworks that ensure the reliability of AI-assisted scientific inquiry[cite: 1].

---

## 📄 AI-Assisted Research Paper
**Prompt Sensitivity and its Effects on the Stability of LLM-Generated Research Conclusions: An Analytical Review**
This paper examines the phenomenon of prompt sensitivity in Large Language Models and evaluates its cascading effects on the validity and reproducibility of scientific research conclusions[cite: 1]. It analyzes in-context learning biases and current mitigation strategies to highlight the fundamental challenges of relying on uncalibrated LLMs[cite: 1].
* 🔗 [**View the Paper Here**](paper/AI_Assisted_Research_Paper.pdf)[cite: 2]

---

## 🔍 Citation Integrity Audit
All references and empirical claims generated in the baseline AI research paper were systematically audited for authenticity, metadata accuracy, and claim-citation support using Google Scholar, arXiv, and publisher databases[cite: 2].
* 🔗 [**View the Audit Here**](citation-audit/Citation_Integrity_Audit.pdf)[cite: 2]

---

## 📚 Curated Research Papers

### Foundational Papers
**1. Language Models are Few-Shot Learners**
Authors: Brown, T., et al. | Year: 2020 | Venue: NeurIPS
🔗 [arXiv:2005.14165](https://arxiv.org/abs/2005.14165)
> *Relevance:* Introduced the paradigm of in-context learning, foundational to understanding how LLMs process instructions without weight updates.

**2. Calibrate Before Use: Improving Few-Shot Performance of Language Models**
Authors: Zhao, Z., et al. | Year: 2021 | Venue: ICML
🔗 [arXiv:2102.09690](https://arxiv.org/abs/2102.09690)
> *Relevance:* Demonstrates major biases (recency, majority label) in prompt design and proposes contextual calibration to mitigate instability.

**3. Fantastically Ordered Prompts and Where to Find Them: Overcoming Few-Shot Prompt Order Sensitivity**
Authors: Lu, Y., et al. | Year: 2022 | Venue: ACL
🔗 [arXiv:2104.08786](https://arxiv.org/abs/2104.08786)
> *Relevance:* Reveals that permuting the order of few-shot examples can cause LLM accuracy to swing from state-of-the-art to random guessing.

**4. Chain-of-Thought Prompting Elicits Reasoning in Large Language Models**
Authors: Wei, J., et al. | Year: 2022 | Venue: NeurIPS
🔗 [arXiv:2201.11903](https://arxiv.org/abs/2201.11903)
> *Relevance:* A foundational paper demonstrating how intermediate reasoning steps in prompts stabilize outputs on complex logical tasks.

**5. Large Language Models are Zero-Shot Reasoners**
Authors: Kojima, T., et al. | Year: 2022 | Venue: NeurIPS
🔗 [arXiv:2205.11916](https://arxiv.org/abs/2205.11916)
> *Relevance:* Highlights how a simple prompt addition ("Let's think step by step") drastically alters and improves reasoning capabilities.

### Mechanics of Prompt Sensitivity
**6. Quantifying language models' sensitivity to spurious features in prompt design**
Authors: Sclar, M., et al. | Year: 2023 | Venue: arXiv
🔗 [arXiv:2310.11324](https://arxiv.org/abs/2310.11324)
> *Relevance:* Quantifies how trivial formatting choices (e.g., commas vs. brackets) severely destabilize model reasoning and arithmetic.

**7. Evaluating and Explaining Prompt Sensitivity of LLMs Using Game-Theoretic Interaction**
Authors: Wang, Z., et al. | Year: 2025 | Venue: ICLR
🔗 [OpenReview: 6fHZR6uxNa](https://openreview.net/forum?id=6fHZR6uxNa)
> *Relevance:* Introduces a novel fine-grained metric to measure prompt sensitivity through the lens of interaction patterns between input variables.

**8. Flaw or Artifact? Rethinking Prompt Sensitivity in Evaluating LLMs**
Authors: Anonymous | Year: 2025 | Venue: arXiv
🔗 [arXiv:2509.01790](https://arxiv.org/abs/2509.01790)
> *Relevance:* Investigates whether prompt sensitivity is a fundamental flaw of transformers or an artifact of poor evaluation setups.

**9. Let Me Speak Freely? A Study on the Impact of Format Restrictions on Performance of LLMs**
Authors: Zheng, C., et al. | Year: 2024 | Venue: arXiv
🔗 [arXiv:2408.02442](https://arxiv.org/abs/2408.02442)
> *Relevance:* Examines how constraining prompt outputs to highly structured formats (like strict JSON) degrades the underlying reasoning stability.

**10. How is ChatGPT's behavior changing over time?**
Authors: Chen, L., et al. | Year: 2023 | Venue: arXiv
🔗 [arXiv:2307.09009](https://arxiv.org/abs/2307.09009)
> *Relevance:* Shows that proprietary API models suffer from longitudinal instability, where the same prompt yields different conclusions across model updates.

### Optimization and Mitigation Strategies
**11. DSPy: Compiling Declarative Language Model Calls into Self-Improving Pipelines**
Authors: Khattab, O., et al. | Year: 2023 | Venue: arXiv
🔗 [arXiv:2310.03714](https://arxiv.org/abs/2310.03714)
> *Relevance:* Introduces a framework that shifts prompt engineering from manual tweaking to systematic algorithmic optimization.

**12. TextGrad: Automatic "Differentiation" via Text**
Authors: Zheng, L., et al. | Year: 2024 | Venue: arXiv
🔗 [arXiv:2406.07496](https://arxiv.org/abs/2406.07496)
> *Relevance:* Treats LLM pipelines as computation graphs, using textual feedback to optimize prompts programmatically.

**13. Large Language Models Are Human-Level Prompt Engineers (APE)**
Authors: Zhou, Y., et al. | Year: 2022 | Venue: ICLR
🔗 [arXiv:2211.01910](https://arxiv.org/abs/2211.01910)
> *Relevance:* Proposes Automatic Prompt Engineer (APE), utilizing LLMs to automatically generate, score, and select robust instructions.

**14. Self-Consistency Improves Chain of Thought Reasoning in Language Models**
Authors: Wang, X., et al. | Year: 2022 | Venue: ICLR
🔗 [arXiv:2203.11171](https://arxiv.org/abs/2203.11171)
> *Relevance:* Demonstrates how sampling multiple diverse prompt completions and aggregating them via majority vote drastically stabilizes outputs.

**15. Prompt Optimisation with Random Sampling**
Authors: Lu, Y., et al. | Year: 2023 | Venue: arXiv
🔗 [arXiv:2311.09569](https://arxiv.org/abs/2311.09569)
> *Relevance:* Provides a lightweight, tuning-free method to systematically search for prompt configurations that maximize stability.

### Surveys and Evaluation Metrics
**16. Holistic Evaluation of Language Models (HELM)**
Authors: Liang, P., et al. | Year: 2022 | Venue: Annals of NYAS
🔗 [arXiv:2211.09110](https://arxiv.org/abs/2211.09110)
> *Relevance:* A massive benchmark study revealing that robustness to prompt perturbations is consistently a weak point across modern LLMs.

**17. The Prompt Report: A Systematic Survey of Prompting Techniques**
Authors: Schulhoff, S., et al. | Year: 2024 | Venue: arXiv
🔗 [arXiv:2406.06608](https://arxiv.org/abs/2406.06608)
> *Relevance:* The most comprehensive recent survey cataloging 58 different prompting techniques and analyzing their impact on model reliability.

**18. PromptBench: Towards Evaluating the Robustness of Large Language Models on Adversarial Prompts**
Authors: Zhu, K., et al. | Year: 2023 | Venue: arXiv
🔗 [arXiv:2306.04528](https://arxiv.org/abs/2306.04528)
> *Relevance:* Introduces a benchmarking framework specifically designed to stress-test LLM prompt sensitivity against character and semantic perturbations.

**19. Pre-train, Prompt, and Predict: A Systematic Survey of Prompting Methods in Natural Language Processing**
Authors: Liu, P., et al. | Year: 2023 | Venue: ACM Computing Surveys
🔗 [DOI: 10.1145/3560815](https://doi.org/10.1145/3560815)
> *Relevance:* A fundamental overview of how prompting structurally replaces traditional fine-tuning and the reliability trade-offs involved.

**20. Scaling LLM Test-Time Compute Optimally can be More Effective than Scaling Model Parameters**
Authors: Snell, C., et al. | Year: 2024 | Venue: arXiv
🔗 [arXiv:2408.03314](https://arxiv.org/abs/2408.03314)
> *Relevance:* Explores how utilizing dynamic prompt adjustments (like revision and search) during inference improves output stability over base generation.

---

## 📊 Datasets
**1. PromptBench Dataset** 
🔗 [GitHub Repository](https://github.com/microsoft/promptbench)
> *Description:* A dataset containing varied adversarial prompts specifically designed to test the sensitivity and robustness of LLMs to lexical and semantic changes[cite: 2].

**2. BIG-bench Hard (BBH)** 
🔗 [GitHub Repository](https://github.com/suzgunmirza/BIG-bench-hard)
> *Description:* A subset of 23 highly challenging tasks used to evaluate the stability of chain-of-thought prompting and model reasoning under different instruction variations[cite: 2].

**3. MMLU (Massive Multitask Language Understanding)** 
🔗 [HuggingFace Dataset](https://huggingface.co/datasets/cais/mmlu)
> *Description:* The standard benchmark often used alongside prompt optimization frameworks to evaluate how effectively a modified prompt maintains zero-shot accuracy across 57 subjects[cite: 2].

---

## 🛠️ Tools and Libraries
**1. DSPy** 
🔗 [Official Documentation](https://dspy-docs.vercel.app/)
> *Purpose:* A framework that algorithmically optimizes prompt structures and weights, moving away from manual, fragile prompt engineering[cite: 2].

**2. PromptBench Library** 
🔗 [Project Link](https://www.emergentmind.com/topics/promptbench)
> *Purpose:* A modular LLM evaluation toolkit for analyzing prompt performance, adversarial attacks, and prompt sensitivity metrics[cite: 2].

**3. LangChain** 
🔗 [Official Documentation](https://python.langchain.com/)
> *Purpose:* Provides extensive utilities for prompt templating, few-shot example selection, and dynamic prompt routing to build stable LLM pipelines[cite: 2].

**4. TextGrad** 
🔗 [Project Link](https://textgrad.com/)
> *Purpose:* An optimization tool that uses text-based feedback to automatically refine and stabilize prompt instructions over multiple iterations[cite: 2].

**5. Promptim (LangChain Labs)** 
🔗 [GitHub Page](https://github.com/langchain-ai/promptim)
> *Purpose:* An experimental library designed for automated prompt optimization loops to improve task consistency[cite: 2].

---

## 💻 GitHub Implementations
**1. DSPy Repository** 
🔗 [Link](https://github.com/stanfordnlp/dspy)
> *Relevance:* The core implementation of the DSPy framework by Stanford NLP, crucial for compiling declarative prompts into robust pipelines[cite: 2].

**2. Awesome Prompt Optimization** 
🔗 [Link](https://github.com/malteos/awesome-prompt-optimization)
> *Relevance:* A highly relevant sister-repository curating scripts and implementations specifically focused on automated prompt generation[cite: 2].

**3. TextGrad Codebase** 
🔗 [Link](https://github.com/zou-group/textgrad)
> *Relevance:* Implements text-based backpropagation, allowing researchers to run prompt stability experiments out of the box[cite: 2].

**4. PromptBench** 
🔗 [Link](https://github.com/microsoft/promptbench)
> *Relevance:* Microsoft's implementation for testing the robustness of LLMs against prompt perturbations; highly relevant for reproducing sensitivity metrics[cite: 2].

**5. AutoPrompt** 
🔗 [Link](https://github.com/ucinlp/autoprompt)
> *Relevance:* An implementation of gradient-guided prompt search that automatically discovers the most stable trigger tokens for specific tasks[cite: 2].

---

## 🎓 Tutorials and Learning Resources
**1. OpenAI Prompt Engineering Guide** 
🔗 [Guide Link](https://platform.openai.com/docs/guides/prompt-engineering)
> *Purpose:* The authoritative baseline tutorial on structuring prompts to minimize hallucination and maximize deterministic outputs[cite: 2].

**2. Anthropic Interactive Prompt Tutorial** 
🔗 [Tutorial Link](https://github.com/anthropics/anthropic-cookbook)
> *Purpose:* Provides hands-on Jupyter notebooks demonstrating how slight structural changes impact Claude's behavior[cite: 2].

**3. Prompt Engineering for ChatGPT (Vanderbilt University)** 
🔗 [Coursera Link](https://www.coursera.org/learn/prompt-engineering)
> *Purpose:* A foundational academic course covering in-context learning biases and the mechanics of prompt design[cite: 2].

**4. DSPy Introductory Tutorial** 
🔗 [Notebook Link](https://github.com/stanfordnlp/dspy/blob/main/intro.ipynb)
> *Purpose:* A step-by-step practical guide teaching researchers how to replace manual prompt tuning with metric-driven optimization[cite: 2].

**5. IBM Prompt Engineering Guide** 
🔗 [Guide Link](https://www.ibm.com/topics/prompt-engineering)
> *Purpose:* A comprehensive resource detailing best practices for enterprise-level prompt stability and reliability testing[cite: 2].

---

## 📜 License
Distributed under the MIT License.
