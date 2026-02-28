# 🎓 Academic Research Assistant

> An AI-powered research ecosystem designed to streamline the complete academic research lifecycle — from paper discovery and gap analysis to writing assistance and intelligent summarization.

![License](https://img.shields.io/badge/License-MIT-green.svg)
![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Framework](https://img.shields.io/badge/Framework-Streamlit-red.svg)
![AI](https://img.shields.io/badge/AI-Gemini_Pro-orange.svg)

---

## 🚀 Overview

Academic Research Assistant is a comprehensive AI-driven platform that empowers researchers by automating critical stages of the research workflow:

- 🔍 Smart Paper Discovery  
- 🕳️ Research Gap Identification  
- ✍️ AI-Assisted Academic Writing  
- 📄 Paper Summarization  
- 💬 RAG-based Q&A on PDFs  

The system integrates modern NLP models, transformer architectures, vector databases, and LLM-powered analysis to deliver contextual and intelligent research support.

---

## 🧠 Key Features

### 🔍 Smart Reference Finder

- Semantic Search using **SciBERT embeddings**
- Aggregates results from:
  - arXiv  
  - Semantic Scholar  
  - CrossRef  
- Custom **Impact Score Calculation** based on:
  - Citation count  
  - Recency  
  - Venue prestige  

---

### 🕳️ Research Gap Analyzer

- 2D Research Landscape Visualization using PCA-reduced embeddings  
- Outlier detection for identifying potential research gaps  
- Emerging trend detection using **KeyBERT**

---

### ✍️ AI Writing Assistant

- Section-wise academic guidance (Abstract, Introduction, Methodology, etc.)
- Powered by **Gemini Pro API**
- Real-time feedback on:
  - Academic tone  
  - Clarity  
  - Structural consistency  
- Export structured paper in JSON format  

---

### 📄 Paper Summarizer

- Section-level summarization  
- Transformer-based abstractive summarization using **BART-Large-CNN**  
- Summary quality evaluation using **ROUGE metrics**

---

### 💬 Q&A Assistant (RAG Architecture)

- Upload any research PDF and ask contextual questions  
- Uses:
  - FAISS vector store  
  - LangChain  
  - Gemini API  
- OCR support with **Tesseract** for scanned PDFs  

---

## 🛠️ Technical Architecture

```mermaid
graph TD
    User((User)) --> Streamlit[Streamlit UI]
    Streamlit --> RefFinder[Reference Finder]
    Streamlit --> GapFinder[Gap Analyzer]
    Streamlit --> Writing[Writing Assistant]
    Streamlit --> QA[Q&A Assistant]
    Streamlit --> Summarizer[Paper Summarizer]

    RefFinder --> SciBERT[SciBERT Embeddings]
    RefFinder --> APIs[arXiv/Semantic Scholar/CrossRef]

    GapFinder --> KeyBERT[KeyBERT Extraction]
    GapFinder --> PCA[PCA Reduction]

    Writing --> Gemini[Gemini Pro API]

    QA --> FAISS[FAISS Vector Store]
    QA --> LangChain[LangChain Orchestration]

    Summarizer --> BART[BART-Large-CNN]