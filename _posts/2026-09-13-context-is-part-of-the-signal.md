---
title: "Context Is Part of the Signal: Two Studies in Computational Pathology and Functional Genomics"
date: 2026-09-13
permalink: /posts/context-is-part-of-the-signal/
tags:
  - computational biology
  - computational pathology
  - functional genomics
  - foundation models
---

Modern biological machine learning increasingly relies on pretrained representations. A pathology foundation model can transform an image into rich embeddings, while a perturbation model can learn recurring transcriptional programs from large single-cell datasets. But representations alone do not always contain enough information to generalize reliably.

Across two ACM BCB 2026 papers, we investigated a shared question: can structured context recover information that an isolated representation misses?

## Tissue context for frozen pathology embeddings

Pathology foundation models are often reused as frozen feature extractors. This is efficient, but a downstream classifier may treat every cell or image region independently—even though cells exist inside organized tissue environments.

In “Patch-Level Tissue Context Improves Learning from Frozen Pathology Foundation Model Embeddings,” we test a lightweight alternative. For each target instance, we aggregate information from cells within the same image patch and combine this contextual representation with the target embedding.

The backbone remains frozen. This makes the method inexpensive and helps isolate the value of tissue context from the effects of foundation-model fine-tuning.

Across Prov-GigaPath, Virchow2, and DINOv2 representations on BRCA-M2C, patch context generally improved or stabilized classification. The gains were not identical across encoders, which is itself informative: the amount of useful context missing from an embedding depends on what the pretrained model has already learned.

[Paper](https://doi.org/10.1145/3807503.3820870) · [Code](https://github.com/Sajib-006/PathContext)

## Biological context for unseen gene perturbations

Perturb-seq can measure transcriptional responses to CRISPR perturbations at single-cell resolution, but experimentally perturbing every gene is impractical. A useful computational model should therefore predict responses for genes that were completely unseen during training.

“Stable-Shift: Predicting Transcriptional Responses of Unseen Gene Perturbations Using Graph Neural Networks with Biological Priors” represents each perturbation through a stable, low-rank transcriptional response program. It then estimates an unseen gene's response using structured biological information: STRING protein interactions, graph topology, baseline expression statistics, and Gene Ontology annotations.

A graph neural network allows information to propagate between biologically related genes. The objective is not simply to reconstruct an observed perturbation, but to generalize to an intervention for which no training response exists.

[Paper](https://doi.org/10.1145/3807503.3820871) · [Code](https://github.com/Sajib-006/PerturbGraph) · [Preprint](https://arxiv.org/abs/2606.24940)

## A shared lesson

These projects operate at different biological scales, but they point toward the same principle.

A frozen representation is not the complete biological state. Tissue organization provides context for pathology embeddings. Interaction networks and functional annotations provide context for unseen gene perturbations.

The appropriate context must also match the prediction problem. Spatial neighborhoods are useful when tissue organization matters; molecular networks are useful when the model must extrapolate between genes.

This suggests a broader direction for biological foundation models: instead of treating pretrained embeddings as complete answers, downstream systems can combine them with structured, domain-specific context. Doing so may improve generalization while keeping the underlying models frozen, interpretable, and computationally practical.

Both projects are open for reuse, evaluation, and extension. I would be particularly interested in collaborations involving cross-center pathology validation, alternative tissue-neighborhood definitions, unseen-perturbation benchmarking, and biologically grounded generalization.
