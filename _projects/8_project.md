---
layout: page
title: BioPrimeLASSO
description: Network-informed LASSO that encodes protein–protein interactions into the penalty to find biologically relevant biomarkers
img: assets/img/bioprimelasso.svg
importance: 0
category: fun
github: https://github.com/dmhenke/BioPrimeLASSO
---

BioPrimeLASSO is an R package that extends LASSO regression so that biological knowledge shapes the regularization. Features that interact with the gene of interest in the STRING DB protein–protein interaction network are penalized less, so among a group of collinear candidates the model prefers the one biology already supports.

The method is described in _[Bio-primed machine learning to enhance discovery of relevant biomarkers](https://www.nature.com/articles/s41698-025-00825-9)_ (_npj Precision Oncology_, 2025).

{% include figure.liquid loading="eager" path="assets/img/bioprimelasso-overview.png" class="img-fluid rounded z-depth-1" alt="BioPrimeLASSO overview: protein–protein interaction confidence is integrated into LASSO regularization, then lambda and phi are optimized before the model is fit and its coefficients interpreted" %}

<div class="caption">
  Method overview. (A) Interaction confidence from the PPI network is integrated into the LASSO penalty for a target dependency and an omic profile. (B) λ and Φ are optimized in turn before the final model is fit.
</div>

## Result

Applied to 453 cancer targets across 1,048 DepMap cell lines, BioPrimeLASSO recovered **GAB2** as a biomarker of **EGFR** dependency, a signal that conventional feature selection missed.

## Install

```r
install.packages("devtools")
devtools::install_github("dmhenke/BioPrimeLASSO")
```

## Usage

```r
# PPI-derived penalty scores for the gene of interest
scores <- get_scores(gene = "EGFR", network = ppi)

# Bio-primed LASSO: omic features (X) against dependency scores (y)
results <- bplasso(scale(X), y, scores, n_folds = 10, phi_range = seq(0, 1, length = 30))
```

The [README](https://github.com/dmhenke/BioPrimeLASSO#r-package-walkthrough) has a full walkthrough with toy EGFR data, and the code behind the paper's figures is in [Reproducibility](https://github.com/dmhenke/BioPrimeLASSO/tree/main/Reproducibility).
