---
title: "Stable-Shift: Predicting Transcriptional Responses of Unseen Gene Perturbations Using Graph Neural Networks with Biological Priors"
collection: publications
category: conferences
permalink: /publication/stable-shift/
excerpt: "Graph-based prediction of transcriptional responses for genes never perturbed during training."
date: 2026-06-30
venue: "17th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics (ACM BCB 2026)"
paperurl: "https://doi.org/10.1145/3807503.3820871"
codeurl: "https://github.com/Sajib-006/PerturbGraph"
citation_title: "Stable-Shift: Predicting Transcriptional Responses of Unseen Gene Perturbations Using Graph Neural Networks with Biological Priors"
citation_authors:
  - "Sajib Acharjee Dip"
  - "Liqing Zhang"
citation_date: "2026/06/30"
citation_conference: "17th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics"
citation_doi: "10.1145/3807503.3820871"
citation_pdf: "https://dl.acm.org/doi/pdf/10.1145/3807503.3820871"
citation: "Dip, Sajib Acharjee, and Liqing Zhang. (2026). &quot;Stable-Shift: Predicting Transcriptional Responses of Unseen Gene Perturbations Using Graph Neural Networks with Biological Priors.&quot; <i>Proceedings of ACM BCB 2026</i>, Article 101, 6 pages."
---

Predicting transcriptional responses to genetic perturbations could reduce the experimental burden of functional genomics, but extrapolation to genes never perturbed during training remains difficult.

Stable-Shift aggregates single-cell measurements into perturbation-level expression shifts, fits a low-rank response basis using training perturbations only, and predicts an unseen gene's coordinates in that basis from biological context. The context combines STRING interactions, network structure, control-cell expression statistics, and Gene Ontology annotations; graph convolution integrates these inputs.

On the supplied K562 Perturb-seq benchmark, Stable-Shift obtained 0.592 cosine similarity, compared with 0.569 for GEARS, together with higher Spearman correlation and top-gene precision among the evaluated methods. Its mean cosine similarity over five unseen-gene splits was 0.589 ± 0.008. The same ordering was observed in the supplied graph-aware, residualized, gene-space, and Norman-dataset comparisons.

These results support further study of biologically structured latent-response prediction, while the lower gene-space accuracy and sensitivity to sparse graph neighborhoods limit the scope of the present conclusions.

- [Read the ACM paper](https://doi.org/10.1145/3807503.3820871)
- [Code](https://github.com/Sajib-006/PerturbGraph)

## Citation

```bibtex
@inproceedings{dip2026stableshift,
  author    = {Dip, Sajib Acharjee and Zhang, Liqing},
  title     = {Stable-Shift: Predicting Transcriptional Responses of Unseen Gene Perturbations Using Graph Neural Networks with Biological Priors},
  booktitle = {Proceedings of the 17th ACM International Conference on Bioinformatics, Computational Biology and Health Informatics},
  year      = {2026},
  articleno = {101},
  numpages  = {6},
  doi       = {10.1145/3807503.3820871}
}
```
