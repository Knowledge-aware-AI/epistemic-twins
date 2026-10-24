---
layout: default
title: Epistemic twins
---

# Stop benchmarking LLM knowledge.<br>Start mapping it.

## Abstract

Large Language Models (LLMs) are impactful yet opaque artifacts. Subsymbolic by design, they are defined by billions of numeric weights that interact in a largely inscrutable manner. Current analysis paradigms are either black-box benchmarks that test model performance on pre-defined tasks, or mechanistic interpretability approaches that trace back outputs to specific weights. Both analysis methods are limited by the experimenter’s hypothesis space - one must know what to look for to find it. In this article, we argue for a third, radically different analysis paradigm: **Epistemic Twins**. We propose constructing large-scale symbolic approximations of LLMs in human-readable formats. This enables the comprehensive inspection of factual knowledge (or beliefs) inherent in the model without predefining hypotheses, facilitating large-scale auditing towards better understanding and explainability.

From [*Epistemic Twins: Enabling a Symbolic Science of Language Model Knowledge*](https://zenodo.org/records/22661249), Simon Razniewski, Shrestha Ghosh, Luca Giordano, Yujia Hu, Josua Kowalzik, and Tuan-Phong Nguyen. AKBC 2026.

## Epistemic twins we produced

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

| Collection | Twinned model | Methodology | Statistics | Data | File size | Paper |
| --- | --- | --- | --- | --- | --- | --- |
| babylonGPTKB — Ancient Babylon | GPT-4.1-mini | miniGPTKB (GPTKB 1.x) | 2,442 entities; 12,738 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/babylonGPTKB/babylonGPTKB.db) | 876.54 kB | [Findings EACL 2026](https://aclanthology.org/2026.findings-eacl.113/) |
| tbbtGPTKB — The Big Bang Theory | GPT-4.1-mini | miniGPTKB (GPTKB 1.x) | 219 entities; 1,295 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/tbbtGPTKB/tbbtGPTKB.db) | 102.40 kB | [Findings EACL 2026](https://aclanthology.org/2026.findings-eacl.113/) |
| dax40GPTKB — DAX 40 | GPT-4.1-mini | miniGPTKB (GPTKB 1.x) | 362 entities; 2,056 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/dax40GPTKB/dax40GPTKB.db) | 131.07 kB | [Findings EACL 2026](https://aclanthology.org/2026.findings-eacl.113/) |
| Dresden | GPT-5-mini | LLMpedia | 1,000 articles | [Browse collection](https://llmpedia.net/dresden/index.html) | — | [EMNLP 2026](https://arxiv.org/abs/2603.24080) |

The three miniGPTKB releases retain triples that appear in at least 3 of 10 runs. Entity counts refer to nodes of type `instance` in the released SQLite databases.

### Backtranslated exports

English backtranslations of the Babylon language-variation runs, constructed with GPT-4.1-mini using miniGPTKB. These represent the same underlying twins, rather than additional independent twins. See [Foundations of LLM Knowledge Materialization: Termination, Reproducibility, Robustness](https://aclanthology.org/2026.findings-eacl.113/) (Findings of EACL 2026).

| Translation | Statistics | Data | File size |
| --- | --- | --- | --- |
| Arabic → English | 858 entities; 4,919 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/_experiment_runs/lang_variation/backtranslation_EN/babylonGPTKB_AR-EN_20250930_113239.db) | 3.59 MB |
| German → English | 7,857 entities; 87,010 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/_experiment_runs/lang_variation/backtranslation_EN/babylonGPTKB_DE-EN_20250630_100431.db) | 57.61 MB |
| Spanish → English | 2,615 entities; 13,685 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/_experiment_runs/lang_variation/backtranslation_EN/babylonGPTKB_ES-EN_20250616_091934.db) | 7.96 MB |
| French → English | 4,769 entities; 35,418 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/_experiment_runs/lang_variation/backtranslation_EN/babylonGPTKB_FR-EN_20250627_151851.db) | 25.55 MB |
| Italian → English | 11,759 entities; 90,018 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/_experiment_runs/lang_variation/backtranslation_EN/babylonGPTKB_IT-EN_20250628_132420.db) | 58.05 MB |
| Polish → English | 1,093 entities; 5,753 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/_experiment_runs/lang_variation/backtranslation_EN/babylonGPTKB_PO-EN_20250623_102904.db) | 3.55 MB |
| Russian → English | 6,061 entities; 37,434 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/_experiment_runs/lang_variation/backtranslation_EN/babylonGPTKB_RU-EN_20250612_163509.db) | 28.70 MB |
| Swedish → English | 1,546 entities; 11,805 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/_experiment_runs/lang_variation/backtranslation_EN/babylonGPTKB_SV-EN_20250703_095332.db) | 24.43 MB |
| Turkish → English | 412 entities; 1,793 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/_experiment_runs/lang_variation/backtranslation_EN/babylonGPTKB_TR-EN_20250620_104047.db) | 1.40 MB |

*File sizes refer to the linked downloads and use decimal units. “—” means that a download size is not listed. Dataset licenses are specified by the linked projects.*
