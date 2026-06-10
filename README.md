# RAG-Based Conversational Bot over NLP Research Papers

A Retrieval-Augmented Generation (RAG) application that ingests 5 foundational
NLP research papers, builds a semantic vector database, and powers a
conversational bot with memory of the last 4 interactions.

---

## Google Colab Notebook

**[Click here to open the project notebook](https://colab.research.google.com/drive/1dOvrgIBQC2A4O_dRPk4o-1kBD6ikuXqh?usp=sharing)**

---

## Final Report

The final project report PDF is available in this repository.

---

## Papers Used

| Paper | Authors | Year |
|-------|---------|------|
| Attention Is All You Need | Vaswani et al. | 2017 |
| BERT | Devlin et al. | 2018 |
| GPT-3 | Brown et al. | 2020 |
| RoBERTa | Liu et al. | 2019 |
| T5 | Raffel et al. | 2019 |

---

## System Architecture

PDFs → Text Extraction → Cleaning → Chunking (1,335 chunks)
→ Embeddings → FAISS Vector DB
→ Retrieval + Memory (last 4 turns)
→ flan-t5 LLM → Answer → Evaluation

---

## Tech Stack

| Component | Tool |
|-----------|------|
| PDF Extraction | pypdf |
| Text Chunking | langchain-text-splitters |
| Embeddings | sentence-transformers (all-MiniLM-L6-v2) |
| Vector Database | FAISS |
| Language Model | google/flan-t5-base (Hugging Face) |
| Evaluation | Cosine Similarity + Keyword Overlap |

---

## Project Files

| File | Description |
|------|-------------|
| **[RAG_Project.ipynb](https://colab.research.google.com/drive/1dOvrgIBQC2A4O_dRPk4o-1kBD6ikuXqh?usp=sharing)** | Main project notebook (all 5 phases) |
| **[RAG_Project_Report.pdf](https://github.com/SaurabhChaudhary046/rag-conversational-bot/blob/main/report/RAG_Project_Report.pdf)** | Final project report |
| **[requirements.txt](https://github.com/SaurabhChaudhary046/rag-conversational-bot/blob/main/requirements.txt)** | All Python dependencies |
| **[SETUP.md](https://github.com/SaurabhChaudhary046/rag-conversational-bot/blob/main/SETUP.md)** | Detailed setup instructions |

---

## Evaluation Results

| Metric | Average Score |
|--------|--------------|
| Answer Relevance | 0.216 |
| Faithfulness | 0.450 |

---

## How to Run

See [SETUP.md](SETUP.md) for full instructions.

Quickest way: Open the Colab link above and run all
cells from top to bottom.

---

## Author

| Field | Details |
|-------|---------|
| Name | SAURABH CHAUDHARY |
