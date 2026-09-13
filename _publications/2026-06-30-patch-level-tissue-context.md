---
title: "Patch-Level Tissue Context Improves Learning from Frozen Pathology Foundation Model Embeddings"
collection: publications
category: conferences
permalink: /publication/patch-level-tissue-context/
excerpt: "Lightweight tissue-context fusion for frozen pathology foundation-model embeddings."
date: 2026-06-30
venue: "17th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics (ACM BCB 2026)"
paperurl: "https://doi.org/10.1145/3807503.3820870"
codeurl: "https://github.com/Sajib-006/PathContext"
citation_title: "Patch-Level Tissue Context Improves Learning from Frozen Pathology Foundation Model Embeddings"
citation_authors:
  - "Sajib Acharjee Dip"
  - "Liqing Zhang"
citation_date: "2026/06/30"
citation_conference: "17th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics"
citation_doi: "10.1145/3807503.3820870"
citation_pdf: "https://dl.acm.org/doi/pdf/10.1145/3807503.3820870"
citation: "Dip, Sajib Acharjee, and Liqing Zhang. (2026). &quot;Patch-Level Tissue Context Improves Learning from Frozen Pathology Foundation Model Embeddings.&quot; <i>Proceedings of ACM BCB 2026</i>, Article 72, 6 pages."
---

Pathology foundation models are often reused as frozen feature extractors. This is efficient, but a downstream classifier may treat every cell or image region independently even though cells exist inside organized tissue environments.

This paper evaluates lightweight fusion of local patch-level context with frozen embeddings from Prov-GigaPath, Virchow2, and DINOv2 on BRCA-M2C. Patch context generally improves or stabilizes classification, with gains that vary by encoder, while keeping the foundation-model backbone frozen.

- [Read the paper](https://doi.org/10.1145/3807503.3820870)
- [Code and reproducibility artifacts](https://github.com/Sajib-006/PathContext)

## Citation

```bibtex
@inproceedings{dip2026patch,
  author    = {Dip, Sajib Acharjee and Zhang, Liqing},
  title     = {Patch-Level Tissue Context Improves Learning from Frozen Pathology Foundation Model Embeddings},
  booktitle = {Proceedings of the 17th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics},
  year      = {2026},
  articleno = {72},
  numpages  = {6},
  doi       = {10.1145/3807503.3820870}
}
```
