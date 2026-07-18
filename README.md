# 🚀 Dual-Stage RAG for E-Commerce Customer Service

> Master Thesis Project  
> National Yunlin University of Science and Technology  
> Graduate Institute of Artificial Intelligence  
> Author: Quan-Fu Chen

---

## 📖 Overview

This project proposes a **Dual-Stage Retrieval-Augmented Generation (RAG)** framework for Chinese E-commerce Customer Service.

The system addresses the limitations of traditional keyword retrieval and single-stage semantic retrieval by combining:

- BM25 Sparse Retrieval
- BGE-M3 Dense Retrieval
- Reciprocal Rank Fusion (RRF)
- BGE-Reranker-v2-m3
- Qwen2.5 Large Language Model

The framework improves retrieval accuracy, response reliability, and reduces hallucination in customer service scenarios.

---

## 🏆 Thesis Contribution

### Contribution 1

A Dual-Stage Retrieval Architecture combining sparse and dense retrieval methods for Chinese E-commerce customer service.

### Contribution 2

A complete RAG evaluation framework including:

- Hit@5
- MRR
- NDCG@5
- Coverage
- Hallucination Rate
- Latency Analysis

### Contribution 3

A practical AI customer service system deployable on CPU-only environments.

---

# 🏗 System Architecture

```text
User Query
     │
     ▼
┌─────────────────┐
│ BM25 Retrieval  │
└─────────────────┘
     │
     ▼
┌─────────────────┐
│ BGE-M3 Dense    │
│ Retrieval       │
└─────────────────┘
     │
     ▼
┌─────────────────┐
│ RRF Fusion      │
└─────────────────┘
     │
     ▼
┌─────────────────┐
│ BGE-Reranker    │
└─────────────────┘
     │
     ▼
┌─────────────────┐
│ Qwen2.5 LLM     │
└─────────────────┘
     │
     ▼
Generated Answer
```

---

# 🔄 RAG Pipeline

```text
Customer Question
        │
        ▼
BM25 Sparse Retrieval
        │
        ▼
BGE-M3 Dense Retrieval
        │
        ▼
Reciprocal Rank Fusion
        │
        ▼
BGE-Reranker-v2-m3
        │
        ▼
Qwen2.5 Generation
        │
        ▼
Final Answer
```

---

# 📊 Experimental Results

Dataset:

- 115 Evaluation Questions
- Chinese E-commerce FAQ Knowledge Base

| Metric | Result |
|----------|----------|
| Hit@5 | 1.0000 |
| MRR | 0.9401 |
| NDCG@5 | 0.9125 |
| Coverage | 1.0000 |
| Average Latency | 188.66 ms |
| P95 Latency | 217.64 ms |

---

# 🧪 Technology Stack

## Backend

- Python
- Flask
- Streamlit

## Retrieval

- BM25
- BGE-M3
- RRF

## Re-ranking

- BGE-Reranker-v2-m3

## Generation

- Qwen2.5

## Vector Search

- FAISS

## Data Processing

- Pandas
- NumPy
- Jieba

---

# 📂 Project Structure

```text
3fm/
│
├── knowledge_base/
├── rag/
│   ├── retrieval/
│   ├── reranker/
│   ├── generator/
│   └── utils/
│
├── routes/
├── static/
├── templates/
├── web/
│
├── app.py
├── app_streamlit_thesis.py
└── README.md
```

---

# 💡 Features

- Dual-Stage Retrieval
- Chinese Semantic Search
- Hybrid Retrieval
- Re-ranking Optimization
- Hallucination Reduction
- Evaluation Dashboard
- Streamlit Monitoring Interface

---

# 🖥 Demo

## Customer Service Query

```text
Q:
如何申請退貨？

A:
您可於訂單完成後七日內申請退貨，
系統將引導您完成退貨流程...
```

---

# 📈 Research Keywords

- Retrieval-Augmented Generation (RAG)
- Large Language Models (LLM)
- Information Retrieval
- BM25
- BGE-M3
- Reranker
- Qwen2.5
- E-Commerce AI
- Customer Service Automation

---

# 👨‍💻 Author

**Quan-Fu Chen**

AI Application Engineer  
Generative AI Developer  
RAG System Developer

GitHub:
https://github.com/quanfu2026

---

# 📜 License

MIT License
