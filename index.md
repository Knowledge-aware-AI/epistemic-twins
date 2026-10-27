---
layout: default
title: Epistemic twins
---

# Stop benchmarking LLM knowledge.<br>Start mapping it.

Epistemic twins turn blackbox LLMs into symbolic, inspectable resources. Explore the twins we have constructed.

<details class="abstract" markdown="1">
<summary>Read the abstract <span class="paper-link">· <a href="https://aclanthology.org/2026.akbc-1.1/">Read the paper ↗</a></span></summary>

Large Language Models (LLMs) are opaque artifacts. Subsymbolic by design, they are defined by billions of numeric weights that interact in a largely inscrutable manner. Current analysis paradigms are either black-box benchmarks that test model performance on pre-defined tasks, or mechanistic interpretability approaches that trace back outputs to specific weights. Both analysis methods are limited by the experimenter’s hypothesis space - one must know what to look for to find it. We propose **Epistemic Twins**, large-scale symbolic approximations of LLMs in human-readable formats. This enables the comprehensive inspection of factual knowledge (or beliefs) inherent in the model without predefining hypotheses, facilitating large-scale auditing towards better understanding and explainability.

From [*Epistemic Twins: Enabling a Symbolic Science of Language Model Knowledge*](https://aclanthology.org/2026.akbc-1.1), Simon Razniewski, Shrestha Ghosh, Luca Giordano, Yujia Hu, Josua Kowalzik, and Tuan-Phong Nguyen. AKBC 2026.

</details>

### Open-domain epistemic twins

| Twinned model | Methodology | Statistics | Data | File size | Paper |
| --- | --- | --- | --- | --- | --- |
| GPT-4o-mini | GPTKB 1.0 | 2.9M entities; 101M triples, $3,500 API cost | [Download TTL](https://huggingface.co/datasets/Knowledge-aware-AI/GPTKB_v1/resolve/main/gptkb_v1.1.1.ttl) | 4.72 GB | [ACL 2025](https://arxiv.org/abs/2411.04920) |
| GPT-4.1 | GPTKB 1.5 | 6.1M entities; 100M triples, $14,000 API cost | [Download TTL](https://huggingface.co/datasets/Knowledge-aware-AI/GPTKB_v1.5/resolve/main/gptkb_v1.5.3.ttl) | 6.70 GB | [AAAI 2026](https://arxiv.org/abs/2507.05740) |
| GPT-5.1 | GPTKB 2.0 | 2.3 M entities; 38.5 M triples, $7,000 API cost | [Download NT.gz](https://huggingface.co/datasets/Knowledge-aware-AI/GPTKB_v2/resolve/main/gptkb_v2.0.1_rdf.nt.gz) | 425.45 MB | [AACL 2026](https://arxiv.org/abs/2608.03729) |
| GPT-5-mini | LLMpedia | 1 M articles, $3,000 API cost | [Download JSONL](https://huggingface.co/datasets/Knowledge-aware-AI/LLMpedia/resolve/main/gpt-5-mini/articles.jsonl) | 7.09 GB | [EMNLP 2026](https://arxiv.org/abs/2603.24080) |
| DeepSeek-V3.2 | LLMpedia | 120 K articles | [Browse collection](https://llmpedia.net/deepseek/index.html) | — | [EMNLP 2026](https://arxiv.org/abs/2603.24080) |
| Llama-3.3-70B | LLMpedia | 120 K articles | [Browse collection](https://llmpedia.net/llama/index.html) | — | [EMNLP 2026](https://arxiv.org/abs/2603.24080) |

### Domain-specific epistemic twins

| Domain | Twinned model | Methodology | Statistics | Data | File size | Paper |
| --- | --- | --- | --- | --- | --- | --- |
| Ancient Babylon | GPT-4.1-mini | miniGPTKB (GPTKB 1.x) | 2,442 entities; 12,738 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/babylonGPTKB/babylonGPTKB.db) | 876.54 kB | [Findings EACL 2026](https://aclanthology.org/2026.findings-eacl.113/) |
| The Big Bang Theory | GPT-4.1-mini | miniGPTKB (GPTKB 1.x) | 219 entities; 1,295 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/tbbtGPTKB/tbbtGPTKB.db) | 102.40 kB | [Findings EACL 2026](https://aclanthology.org/2026.findings-eacl.113/) |
| DAX 40 | GPT-4.1-mini | miniGPTKB (GPTKB 1.x) | 362 entities; 2,056 triples | [Download SQLite](https://github.com/Knowledge-aware-AI/miniGPTKB/raw/refs/heads/main/KBs/dax40GPTKB/dax40GPTKB.db) | 131.07 kB | [Findings EACL 2026](https://aclanthology.org/2026.findings-eacl.113/) |
| Dresden | GPT-5-mini | LLMpedia | 1,000 articles | [Browse collection](https://llmpedia.net/dresden/index.html) | — | [EMNLP 2026](https://arxiv.org/abs/2603.24080) |

## FAQ

### What is this good for?

LLMs are a prime example of latent knowledge representation, i.e., there is no obvious way to read them as a human by looking at their parameters. Benchmarks only sample them by what the experimenters choose to ask. With epistemic twins, we aim to extract the entirety of their factual knowledge, for human inspection and auditing.

### LLM answers are sensitive to minor reformulations in prompts. Do your twins really capture what the models believe in (precision)?

Fair objection. Our twins are a simplification of what LLMs really are, and “all models are wrong, but some are useful”. Defining LLM knowledge is an [active research field](https://arxiv.org/abs/2405.21030). Depending on the protocol, we find that LLMs strongly believe in 76–90% of statements in our twins.

### LLM answers are sensitive to minor reformulations in prompts. Do your twins really capture all that the models believe in (recall)?

For monetary reasons, none of our open-domain twins has exhausted the LLM's internal knowledge graph yet. All were ad-hoc terminated. The domain-specific twins, in turn, represent complete graph exploration. Still, we can't rule out further beliefs.

### But don't LLMs know more than facts?

Indeed, LLMs know about language, commonsense properties and rules, capabilities (how to rhyme, or construct recipes), and more. These types of knowledge are out of scope so far.

### This sounds cool, how can I get started?

Download our twins and play with them. Or, [get the code](https://github.com/Knowledge-aware-AI/) and construct your own twins.

### Can you construct a twin for me?

That might be possible. Please [email us](mailto:kaai@tu-dresden.de) your desired model and topical focus, and we will get back to you.
