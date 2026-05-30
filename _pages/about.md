---
layout: about
title: about
permalink: /
subtitle: >
  Computational Biologist · <a href="https://www.bcm.edu/departments/molecular-virology-and-microbiology" target="_blank">Molecular Virology & Microbiology</a> ·
  <a href="https://www.bcm.edu" target="_blank">Baylor College of Medicine</a>

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false
  more_info: >
    <p>Molecular Virology & Microbiology</p>
    <p>Baylor College of Medicine</p>
    <p>Houston, TX</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: true
  scrollable: true
  limit: 5

latest_posts:
  enabled: true
  scrollable: true
  limit: 3
---

I am a computational biologist at **Baylor College of Medicine**, where my work sits at the intersection of statistical machine learning, network biology, and functional genomics.

High-dimensional biological data is noisy, collinear, and humbling. Standard approaches will happily select a feature simply because it lives next to the real driver. My central research question is whether we can teach models what biology already knows — and use that knowledge to find signals that statistics alone would miss.

Practically, this means building regularized regression frameworks that incorporate protein–protein interaction networks, applying them to large-scale cancer dependency screens from [DepMap](https://depmap.org/portal/), and translating the results toward therapeutic hypotheses in precision oncology.

My primary tool is R. My primary motivation is the gap between a statistically significant finding and a biologically meaningful one.

## Research Interests

- **Regularized Regression** — Biologically-informed LASSO, adaptive penalties, and penalty weighting with network priors
- **Functional Genomics** — DepMap CRISPR and RNAi dependency screens, DEMETER2, and Chronos
- **Network Biology** — PPI network integration via STRING DB, co-dependency analysis, and synthetic lethality
- **Precision Oncology** — Biomarker discovery from copy number variation, gene dependency, and drug sensitivity data
- **High-Dimensional Statistics** — Feature selection in p ≫ n regimes, collinearity in omics data, reproducible pipelines
- **Translational Bioinformatics** — Turning computational predictions into testable biological hypotheses
