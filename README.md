# <img width="45" height="45" alt="8f460c83955297b0c60eb59658dbd296" src="https://github.com/user-attachments/assets/3aaf3670-31d1-4ea6-b0cc-1e627bd498a8" /> AM-VLM: Agentic multimodal LLM-augmented expert system with physics-aware dual-index RAG for metal additive manufacturing

## 📌 Overview
This repository presents **AM-VLM**, an agentic multimodal LLM-augmented expert system for metal additive manufacturing (AM). AM-VLM is built around a physics-aware dual-index retrieval-augmented generation (RAG) architecture that natively unifies two complementary evidence streams: (1) mechanism-level foundations from curated AM literature, and (2) case-based multimodal evidence from in-situ melt pool monitoring. The system supports an end-to-end, evidence-traceable workflow from online anomaly detection → defect typing → root-cause attribution → actionable parameter-level mitigation, and includes a network intelligence agent for controlled web-based knowledge acquisition and incremental index updates to keep the system current.

### Key Highlights

- **Dual-Index Evidence Repositories**
  - **Foundation Literature Index**: built from **75 curated metal AM papers**, covering key themes such as process parameters and optimization, modeling and simulation, melt pool dynamics, defects and quality assurance, as well as review and survey studies.
  - **Multimodal Melt Pool Index**: compiled from **20 datasets** of **paired image–text cases**, enabling retrieval of visually and physically similar melt pool patterns together with their experimental context.
- **Physics-Aware Two-Stage Reranking for Robust RAG**
  - **Stage 1 — Textual reranking (cross-encoder)** to improve semantic alignment and relevance of literature evidence.
  - **Stage 2 — Physics-aware image reranking** using **compact, normalized morphology/intensity descriptors** (e.g., normalized width/length/area scales, compactness, intensity distribution patterns) to reduce multimodal retrieval drift and preserve physics-critical distinctions.
- **Knowledge–Data Co-Driven Quality Diagnosis Pipeline**
  - **Online monitoring**: coaxial videos are converted into morphology proxies, transformed into **CWT scalograms**.
  - **Uncertainty-aware anomaly detection**: a **Bayesian autoencoder-based detector (UQAT-BAE)** produces calibrated anomaly scores with uncertainty awareness.
  - **Anomaly-triggered multimodal RAG reasoning**: abnormal frames trigger retrieval from both indices to generate **defect typing**, **root-cause explanations**, and **parameter-level mitigation suggestions** grounded in traceable evidence.
- **Evaluation and End-to-End Demonstrations**
  - Validated with an **AM 60-question benchmark** for expert-like Q&A.
  - Retrieval/reranking **ablation studies** to quantify evidence fidelity improvements.
  - End-to-end demonstrations on a coaxial-imaging DED platform with **powder-fed 316L** and **wire-fed In718** single-track experiments.
- **Network Intelligence Agent for Continual Updating**
  - Performs controlled browser workflows (e.g., literature retrieval, troubleshooting, procurement support).
  - Supports **incremental index updates** to continually refresh the knowledge base as new evidence emerges.


## 💻 AM-VLM Functionality Demonstration

### *Interactive Expert Q&A*

[![Demo Video](https://i.ytimg.com/vi/M0dYjLlOzZ8/hqdefault.jpg)](https://www.youtube.com/watch?v=M0dYjLlOzZ8)

[![Watch on YouTube](https://img.shields.io/badge/Watch%20Demo-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=M0dYjLlOzZ8)

### *Synergistic knowledge-data driven quality diagnosis*

[![Demo Video](https://i.ytimg.com/vi/YK_MCoWZ4_4/hqdefault.jpg)](https://www.youtube.com/watch?v=YK_MCoWZ4_4)

[![Watch on YouTube](https://img.shields.io/badge/Watch%20Demo-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=YK_MCoWZ4_4)

### *Network agent papersearch*

[![Demo Video](https://i.ytimg.com/vi/aahOaTw1pRU/hqdefault.jpg)](https://www.youtube.com/watch?v=aahOaTw1pRU)

[![Watch on YouTube](https://img.shields.io/badge/Watch%20Demo-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=aahOaTw1pRU)

### *Procurement*

[![Demo Video](https://i.ytimg.com/vi/q5MUEINYZuk/hqdefault.jpg)](https://www.youtube.com/watch?v=q5MUEINYZuk)

[![Watch on YouTube](https://img.shields.io/badge/Watch%20Demo-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=q5MUEINYZuk)

### *Troubleshooting*

[![Demo Video](https://i.ytimg.com/vi/HVD3yHXqevk/hqdefault.jpg)](https://www.youtube.com/watch?v=HVD3yHXqevk)

[![Watch on YouTube](https://img.shields.io/badge/Watch%20Demo-YouTube-red?logo=youtube)](https://www.youtube.com/watch?v=HVD3yHXqevk)
