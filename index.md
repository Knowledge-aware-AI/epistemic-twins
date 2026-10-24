---
layout: default
title: Epistemic twins
---

# Stop benchmarking LLM knowledge.<br>Start mapping it.

Epistemic twins turn parametric LLMs into symbolic, inspectable resources. Explore the twins we have constructed.

<details class="abstract" markdown="1">
<summary>Read the abstract <span class="paper-link">· <a href="https://zenodo.org/records/22661249">Read the paper ↗</a></span></summary>

Large Language Models (LLMs) are opaque artifacts. Subsymbolic by design, they are defined by billions of numeric weights that interact in a largely inscrutable manner. Current analysis paradigms are either black-box benchmarks that test model performance on pre-defined tasks, or mechanistic interpretability approaches that trace back outputs to specific weights. Both analysis methods are limited by the experimenter’s hypothesis space - one must know what to look for to find it. We propose **Epistemic Twins**, large-scale symbolic approximations of LLMs in human-readable formats. This enables the comprehensive inspection of factual knowledge (or beliefs) inherent in the model without predefining hypotheses, facilitating large-scale auditing towards better understanding and explainability.

From [*Epistemic Twins: Enabling a Symbolic Science of Language Model Knowledge*](https://zenodo.org/records/22661249), Simon Razniewski, Shrestha Ghosh, Luca Giordano, Yujia Hu, Josua Kowalzik, and Tuan-Phong Nguyen. AKBC 2026.

</details>

### Open-domain epistemic twins

| Twinned model | Methodology | Statistics | Data | File size | Paper |
| --- | --- | --- | --- | --- | --- |
| GPT-4o-mini | GPTKB 1.0 | 2.9M entities; 101M triples | [Download TTL](https://huggingface.co/datasets/Knowledge-aware-AI/GPTKB_v1/resolve/main/gptkb_v1.1.1.ttl) | 4.72 GB | [ACL 2025](https://arxiv.org/abs/2411.04920) |
| GPT-4.1 | GPTKB 1.5 | 6.1M entities; 100M triples | [Download TTL](https://huggingface.co/datasets/Knowledge-aware-AI/GPTKB_v1.5/resolve/main/gptkb_v1.5.3.ttl) | 6.70 GB | [AAAI 2026](https://arxiv.org/abs/2507.05740) |
| GPT-5.1 | GPTKB 2.0 | 2.3 M entities; 38.5 M triples | [Download NT.gz](https://huggingface.co/datasets/Knowledge-aware-AI/GPTKB_v2/resolve/main/gptkb_v2.0.1_rdf.nt.gz) | 425.45 MB | [AACL 2026](https://arxiv.org/abs/2608.03729) |
| GPT-5-mini | LLMpedia | 1 M articles | [Download JSONL](https://huggingface.co/datasets/Knowledge-aware-AI/LLMpedia/resolve/main/gpt-5-mini/articles.jsonl) | 7.09 GB | [EMNLP 2026](https://arxiv.org/abs/2603.24080) |
| DeepSeek-V3.2 | LLMpedia | 120 K articles | [Browse collection](https://llmpedia.net/deepseek/index.html) | — | [EMNLP 2026](https://arxiv.org/abs/2603.24080) |
| Llama-3.3-70B | LLMpedia | 120 K articles | [Browse collection](https://llmpedia.net/llama/index.html) | — | [EMNLP 2026](https://arxiv.org/abs/2603.24080) |

### Domain-specific epistemic twins

| Domain | Twinned model | Methodology | Statistics | Data | File size | Paper |
| --- | --- | --- | --- | --- | --- | --- |
| Ancient Babylon | GPT-4.1-mini | miniGPTKB (GPTKB 1.x) | 2,442 entities; 12,738 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/babylonGPTKB/babylonGPTKB.db) | 876.54 kB | [Findings EACL 2026](https://aclanthology.org/2026.findings-eacl.113/) |
| The Big Bang Theory | GPT-4.1-mini | miniGPTKB (GPTKB 1.x) | 219 entities; 1,295 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/tbbtGPTKB/tbbtGPTKB.db) | 102.40 kB | [Findings EACL 2026](https://aclanthology.org/2026.findings-eacl.113/) |
| DAX 40 | GPT-4.1-mini | miniGPTKB (GPTKB 1.x) | 362 entities; 2,056 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/dax40GPTKB/dax40GPTKB.db) | 131.07 kB | [Findings EACL 2026](https://aclanthology.org/2026.findings-eacl.113/) |
| Dresden | GPT-5-mini | LLMpedia | 1,000 articles | [Browse collection](https://llmpedia.net/dresden/index.html) | — | [EMNLP 2026](https://arxiv.org/abs/2603.24080) |
