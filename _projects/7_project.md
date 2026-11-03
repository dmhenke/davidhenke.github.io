---
layout: page
title: Drug2DiseaseDiscovery
description: Single-cell foundation-model embeddings and signature reversal to nominate candidate therapeutics for lupus
img: assets/img/drug2disease-discovery.svg
importance: 7
category: fun
github: https://github.com/dmhenke/Drug2DiseaseDiscovery
redirect: https://dmhenke.github.io/Drug2DiseaseDiscovery/
---

Drug2DiseaseDiscovery is a computational drug-repurposing workflow that links disease-specific cellular transcriptional states to compounds predicted to reverse them. Single-cell profiles from systemic lupus erythematosus (SLE) are embedded with the Universal Cell Embeddings (UCE) foundation model, and cell-type-resolved disease signatures are matched against perturbational compound signatures. Current reports are diagnostic and exploratory, not results for publication.

## Features

- UCE 33-layer model test run on the Perez 2022 SLE cohort (20 cases vs. 20 controls)
- Interferon-signature "answer-key" check to confirm known lupus biology is recovered
- Measured throughput and resource estimates to plan a full-cohort run
- Exploratory drug-reversal lookup: SLE monocyte signatures against LINCS L1000 compound signatures
- Null calibration against random signatures, with results in a filterable table
