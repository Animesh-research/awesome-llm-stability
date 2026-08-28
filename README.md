
# awesome-llm-stability

A curated collection of research papers, datasets, tools, implementations, and learning resources exploring how prompt sensitivity, lexical variations, and syntactic formatting impact the structural stability and reproducibility of Large Language Models (LLMs).

---

## 📑 Table of Contents
* [🌟 Overview](#-overview)
* [📄 AI-Assisted Research Paper](#-ai-assisted-research-paper)
* [🔍 Citation Integrity Audit](#-citation-integrity-audit)
* [📚 Curated Research Papers](#-curated-research-papers)
* [📊 Datasets](#-datasets)
* [🛠️ Tools and Libraries](#️-tools-and-libraries)
* [💻 GitHub Implementations ](#-github-implementations)
* [📜 License](#-license)


## 🌟 Overview

Large Language Models (LLMs) are increasingly integrated into scientific research workflows to automate literature synthesis, qualitative coding, and data extraction. However, these models exhibit a critical vulnerability: **acute prompt sensitivity**. Minor changes in phrasing, formatting, or example order can drastically alter generated outputs, introducing three major failure modes:

* **In-Context Bias:** High susceptibility to majority label bias, recency bias, and formatting conventions during few-shot prompting.
* **Output Variance:** Inability to maintain identical conclusions across minor synonym swaps or syntax permutations.
* **Epistemic Instability:** Translating subjective linguistic choices in input prompts into fragile, non-reproducible scientific claims.

This repository aggregates research, benchmarks, and programmatic frameworks designed to measure, analyze, and mitigate prompt brittleness in LLMs.

---

## 📄 AI-Assisted Research Paper

* **Title:** *Prompt Sensitivity and its Effects on the Stability of LLM-Generated Research Conclusions: An Analytical Review*
* **Access Paper:** [View Paper PDF](paper/AI_Assisted_Research_Paper.pdf)
* **Summary:** The paper analyzes the mechanics of prompt sensitivity, quantifies performance swings caused by trivial prompt permutations, and evaluates mitigation frameworks such as self-consistency, contextual calibration, and automatic prompt optimization. It was preserved exactly as generated to evaluate real-world AI reasoning stability.

---

## 🔍 Citation Integrity Audit

* **Audit Overview:** Evaluated a systematic sample of references and empirical claims generated in the baseline AI research paper using Google Scholar, arXiv, and publisher databases.
* **Key Finding:** Achieved an Authenticity Score of **96.0/100**, with primary issues involving minor metadata discrepancies (e.g., publication year or volume number mismatches on genuine papers) rather than fake citations.
* **Access Audit Report:** [View Citation Audit PDF](citation-audit/Citation_Integrity_Audit.pdf)

---

## 📚 Curated Research Papers

### Mechanics of Prompt Sensitivity

* **Calibrate Before Use: Improving Few-Shot Performance of Language Models**
  * *Zhao et al., 2021, ICML* | [arXiv:2102.09690](https://arxiv.org/abs/2102.09690)
  * Demonstrates severe recency and majority-label biases in few-shot prompting and proposes contextual calibration.
* **Fantastically Ordered Prompts and Where to Find Them: Overcoming Few-Shot Prompt Order Sensitivity**
  * *Lu et al., 2022, ACL* | [arXiv:2104.08786](https://arxiv.org/abs/2104.08786)
  * Reveals that permuting few-shot example order causes accuracy to fluctuate between state-of-the-art and random guessing.

### Optimization & Mitigation Strategies

* **DSPy: Compiling Declarative Language Model Calls into Self-Improving Pipelines**
  * *Khattab et al., 2023, arXiv* | [arXiv:2310.03714](https://arxiv.org/abs/2310.03714)
  * Replaces manual prompt engineering with algorithmic compilation and automatic instruction optimization.
* **TextGrad: Automatic "Differentiation" via Text**
  * *Zheng et al., 2024, arXiv* | [arXiv:2406.07496](https://arxiv.org/abs/2406.07496)
  * Treats LLM workflows as computation graphs, backpropagating textual feedback to refine system prompts programmatically.

### Evaluation Metrics & Benchmarks

* **PromptBench: Towards Evaluating the Robustness of Large Language Models on Adversarial Prompts**
  * *Zhu et al., 2023, arXiv* | [arXiv:2306.04528](https://arxiv.org/abs/2306.04528)
  * Establishes a unified evaluation framework to stress-test LLM robustness against character, word, and semantic perturbations.

> 🔗 *View the full collection of 20 verified papers in [`references/references.md`](references/references.md)*.

---

## 📊 Datasets

* **PromptBench Dataset** | [Repository](https://github.com/microsoft/promptbench)
  * A dataset containing adversarial prompt perturbations designed to evaluate model sensitivity across core NLP tasks.
* **BIG-bench Hard (BBH)** | [Repository](https://github.com/suzgunmirza/BIG-bench-hard)
  * A collection of 23 complex reasoning tasks used to stress-test prompt brittleness and chain-of-thought stability.
* **MMLU (Massive Multitask Language Understanding)** | [HuggingFace](https://huggingface.co/datasets/cais/mmlu)
  * Standard benchmark used alongside automatic prompt optimizers to test zero-shot prompt robustness across 57 subjects.

> 🔗 *View all dataset details in [`datasets/datasets.md`](datasets/datasets.md)*.

---

## 🛠️ Tools and Libraries

* **DSPy** | Framework that compiles declarative prompts into robust, self-improving pipelines.
* **PromptBench Library** | Modular evaluation toolkit for generating adversarial attacks and calculating prompt sensitivity metrics.
* **LangChain** | Production framework offering prompt templates, example selectors, and fallback execution chains.
* **TextGrad** | Gradient-like textual optimization engine that iteratively updates instructions based on output feedback.
* **Promptim** | Experimental library from LangChain Labs designed for automated prompt optimization loops.

> 🔗 *View all tool documentation in [`tools/tools.md`](tools/tools.md)*.

---

## 💻 GitHub Implementations

* **DSPy Codebase** | Official Stanford NLP implementation for automatic prompt compilation and optimization.
* **Awesome Prompt Optimization** | Curated collection of open-source scripts and research code for automated prompt tuning.
* **TextGrad Engine** | Codebase implementing textual backpropagation to optimize prompt nodes in complex pipelines.
* **PromptBench Framework** | Microsoft implementation for executing adversarial stress tests on modern LLMs.
* **AutoPrompt Implementation** | Gradient-guided search codebase for discovering robust prompt triggers.

> 🔗 *View all repository links in [`implementations/github-repositories.md`](implementations/github-repositories.md)*.

---

## 🎓 Tutorials & Learning Resources

* **OpenAI Prompt Engineering Guide** | Official guide detailing strategies to minimize output variance and hallucination.
* **Anthropic Interactive Prompt Tutorial** | Hands-on Jupyter notebooks demonstrating prompt structuring for Claude models.
* **Prompt Engineering for ChatGPT (Vanderbilt University)** | Coursera course covering in-context learning mechanics and prompt design.
* **DSPy Introductory Tutorial** | Step-by-step interactive guide on replacing hand-crafted prompts with metric-driven optimization.
* **IBM Enterprise Prompt Engineering Guide** | Architectural overview of robust prompt deployment and testing strategies.

> 🔗 *View all learning links in [`implementations/github-repositories.md`](implementations/github-repositories.md)*.

---

## 📜 License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for more information.
