# Differentially Private Covariance Estimation Replication

This repository contains the replication materials for the paper **"Differentially Private Covariance Estimation" (NeurIPS 2019)** by Amin et al. The replication focuses on implementing the proposed differentially private covariance estimation algorithm and reproducing key figures from the accompanying report.

## Repository Contents

- **replication.ipynb**  
  A Jupyter Notebook that implements the replication of the experiments described in the paper. This notebook includes the code for:
  - Estimating the covariance matrix using a combination of the Laplace mechanism (for eigenvalues) and the exponential mechanism (for eigenvectors).
  - Iteratively projecting the covariance matrix to improve the privacy-utility trade-off.
  - Generating the visualizations (figures) that are presented in the report.

- **Figures**  
  Three figures extracted from the report that illustrate:
  - The normalized Frobenius error of the private covariance matrix across different privacy parameters.
  - A comparison between the iterative method and baseline methods (e.g., Laplace and Gaussian mechanisms).
  - Performance evaluations on various datasets under differing privacy regimes.

## Overview

In this work, Amin et al. propose a novel algorithm for estimating a covariance matrix under pure differential privacy. Their approach:
- **Perturbs Eigenvalues:** Uses the Laplace mechanism to add noise to the eigenvalues.
- **Samples Eigenvectors Privately:** Employs the exponential mechanism to select eigenvectors, ensuring they remain orthogonal through iterative projections.
- **Enhances Utility:** Demonstrates improved error bounds, particularly in high-privacy regimes, compared to traditional methods like direct Laplace or Gaussian noise injection.
