# 📚 Curated Research Papers

## Foundational Papers
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

---

## Mechanics of Prompt Sensitivity
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

---

## Optimization and Mitigation Strategies
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

---

## Surveys and Evaluation Metrics
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
