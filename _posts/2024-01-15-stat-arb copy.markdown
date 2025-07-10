---
layout: post
title:  "stockXarb"
date:   2024-12-15
start_date: 2024-01-01
end_date:   2024-05-01
github: https://github.com/dq2024/clustering_stat_arbitrage
description: Financial time-series clustering for statistical arbitrage
pdf: /assets/files/statXarb.pdf
---

<div class="project-content layout-centered">
  <h4>Embedding‑Driven Clustering for Statistical Arbitrage</h4>

  <p>
    In this project, I sought to uncover latent arbitrage opportunities by clustering over 9,580 NYSE-traded symbols based on custom feature embeddings. After extracting and log scaling key time series features (trade price, volume, moving averages, and cyclically encoded timestamps), I built a neural embedding model with an input embedding layer followed by multiple dense blocks using LeakyReLU activations, dropout, and L2 regularization to ensure robust generalization under memory constraints.
  </p>

  <h4>Machine Learning Techniques</h4>
 <ul style="margin-top: -0.3em; margin-bottom: 1em;">
    <li>Log-scaling and moving-average smoothing of raw price and volume signals</li>
    <li>Cyclical encoding (sine/cosine) of hourly timestamps</li>
    <li>Embedding layer for symbol representation followed by dense networks</li>
    <li>LeakyReLU, dropout layers, and L2 weight regularization to prevent overfitting</li>
    <li>Early stopping and ReduceLROnPlateau learning-rate scheduling in lieu of LSTM layers</li>
    <li>PCA for feature compression and t‑SNE for visual cluster inspection</li>
    <li>Spectral clustering and K‑Means (k=4 via elbow method) evaluated by silhouette and purity scores</li>
  </ul>
  <h4>Results</h4>
  <p>
    After training on 41 days of high frequency data with batch optimization, the embedding driven MLP revealed compact symbol representations that captured market dynamics more effectively than traditional correlation matrices. Applying K‑Means to these embeddings yielded four distinct clusters with a silhouette score of 0.607, while cluster purity against sector labels reached 0.426, demonstrating alignment with known industry groupings and suggesting novel arbitrage groups beyond classical approaches.
  </p>

  <p>
    The end-to-end pipeline, from feature engineering through embedding learning, dimensionality reduction, and unsupervised clustering, provides a scalable framework for statistical arbitrage. Full implementation details and additional quantitative analyses are available in the accompanying paper and GitHub repository.
  </p>
</div>
