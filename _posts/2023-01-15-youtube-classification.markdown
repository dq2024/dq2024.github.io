---
layout: post
title:  "Channel Atlas"
date:   2024-12-15
start_date: 2023-01-01
end_date:   2023-05-01
github: https://github.com/dq2024/NLP-Cluster-Categorization
description: YouTube channel clustering system
---

<div class="project-content layout-centered-yt">
<div class="project-image">
    <img src="/assets/img/yt-cluster.png" alt="VENT App Screenshot">
  </div>
  <h4>Unsupervised YouTube Channel Classification System</h4>
  
  
  <p>
    Channel Atlas is an unsupervised NLP framework I developed to automatically categorize and explore thematic relationships across YouTube channels. The project began by scraping and collecting transcript corpora from over 250 diverse YouTube channels using BeautifulSoup, then preprocessing them with NLTK for tokenization, stop-word removal, and normalization.
  </p>

  <p>
    To capture each channel’s distinctive content signature, I used KeyBERT to extract the top-n most relevant keywords from every channel transcript, producing concise semantic profiles. These keywords were then embedded with word2vec to generate high-dimensional feature vectors that encode subtle semantic similarities between topics. I implemented a weighted cosine similarity metric that measures the overlap in these keyword embeddings, providing a flexible way to quantify thematic affinity between channels.
  </p>

  <p>
    With these pairwise similarities, I constructed a channel similarity graph in NetworkX, where edges represent semantic closeness. Applying the Clauset–Newman–Moore modularity optimization algorithm allowed me to detect tightly knit communities—groups of channels that consistently cover related topics without any prior labels or supervision. I then visualized these clusters and their interconnections using Gephi to qualitatively assess topic coherence and uncover hidden content ecosystems on YouTube.
  </p>

  <p>
    For quantitative evaluation, I explored how different keyword counts and similarity thresholds impacted clustering granularity, calculating precision, recall, and F-scores to assess performance. This analysis revealed important trade-offs between capturing broad thematic groups and isolating more niche channel communities. You can explore the full codebase on GitHub and read more about the methodology and results in the accompanying research paper.
  </p>
</div>

