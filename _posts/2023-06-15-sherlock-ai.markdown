---
layout: post
title:  "Sherlock AI"
date:   2024-12-15
start_date: 2023-06-01
end_date:   2023-07-01
description: Intelligent Coding Chatbot
---

<div class="project-content">

  <h4>Intelligent Chatbot for Large Codebases</h4>
  
  <p>
  During my internship at Zoom Video Communications as a Software Engineering Intern I had the opportunity to participate in the company's annual AI Hackathon.  
  During the two-week stint, I implemented an internal chatbot aimed at accelerating developer onboarding across Zoom’s sprawling codebase.
</p>

<p>
  To achieve this, I built a retrieval-augmented generation (RAG) pipeline that begins by parsing and chunking source files using LangChain, then indexes those chunks in a Pinecone vector database.  This setup delivers low-latency, high-relevance semantic search over millions of lines of code.  User questions are sent via a Flask-based REST API to Anthropic’s language models, which generate context-aware answers by combining retrieved code snippets with LLM inference.
</p>

<p>
  The final product is a seamless developer assistant that can answer deep technical questions—everything from “How does our authentication middleware work?” to “Where are database migrations defined?”—in real time.  During the Hackathon demo, the chatbot answered queries with over 90% accuracy, slashing initial ramp-up time for new engineers from days to mere hours.
</p>

</div>

