---
layout: post
title:  "Venture AI"
date:   2024-12-15
start_date:   2024-10-01
end_date:   2025-01-01
github: https://github.com/dq2024/VentureAI
description: AI-driven travel itinerary planner
pdf: /assets/files/venture_ai.pdf
---

<div class="project-content layout-centered">
  <h4>Venture AI: AI-Powered Travel Planner</h4>

  <p>
    Venture AI automates the entire travel planning process, generating personalized, day by day itineraries based on user preferences and real time data. We synthesized a structured dataset of 2,000 itinerary prompt–response pairs via model distillation and fine-tuned open-source large language models (Falcon, LLaMA, Mistral, FLAN-T5) using parameter efficient LoRA adapters. By integrating a FAISS vector store over live point of interest APIs, the system retrieves up to date POI details in a Retrieval-Augmented Generation (RAG) pipeline to ground the LLM in factual travel information.
  </p>

  <h4>Machine Learning Techniques</h4>
  <ul style="margin-top: -0.3em; margin-bottom: 1em;">
    <li>Model distillation to create a 2,000-entry synthetic dataset of structured prompt–response pairings from Wikivoyage data and 4o‑mini outputs.</li>
    <li>PEFT fine-tuning (LoRA) of open-source LLMs, employing 8‑bit quantization and FP16 mixed‑precision to reduce compute.</li>
    <li>Vector datastore construction using FAISS (and optional Chroma) to index real‑time POI embeddings for low-latency semantic retrieval.</li>
    <li>RAG integration that prepends retrieved POI context to user prompts, enhancing the model’s factual accuracy and reducing hallucination.</li>
    <li>Distributed training via PyTorch DDP on multiple GPUs and hyperparameter sweeps in Weights & Biases for reproducible optimization.</li>
  </ul>

  <h4>Results</h4>
  <p>
    Our RAG‑aware, LoRA‑fine‑tuned models outperformed base LLMs on various benchmarks such as BLEU, Self-BLEU, and perplexity. We noticed an average of 38% lower perplexity and a 2.3x higher BLEU score after fine tuning. Qualitative ablation studies confirmed that itineraries respect budget, timing, and preference constraints while adapting seamlessly to real‑time updates. 

  </p>

  <p>
    This end to end pipeline, from synthetic data generation through PEFT fine‑tuning, vector retrieval, and benchmark evaluation, provides a scalable foundation for next‑generation AI travel planners. Next steps for this project would be to evaluate against the TravelPlanner and RAGAs benchmarks. Full implementation details and quantitative findings are available in the paper and on GitHub.
  </p>

  
</div>
