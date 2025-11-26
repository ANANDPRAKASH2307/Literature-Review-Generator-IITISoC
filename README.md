# 📘 Literature Review Generator — IITISoC

A system that automatically **parses academic PDFs** and generates **structured literature reviews** using PDF extraction, NLP, and multi-stage LLM summarization.

---

## 🚀 Overview

This project solves the IITISoC challenge:

> **Automatically read research papers and produce accurate literature reviews.**

It combines multiple components:

- **PyMuPDF** — text blocks + bounding boxes  
- **pdfplumber** — table extraction  
- **Regex heuristics** — headings, subsections, captions  
- **Chunking with overlap** — to preserve context  
- **Groq LLM pipeline** (Gemma 2 → Llama 3)  
- **Streamlit + DistilBART** — fast offline summarizer (separate lightweight app)

---

## 🧠 How It Works (Brief)

### **1. PDF Parsing**
Extract:
- text blocks  
- bounding boxes  
- tables  
- figure captions

### **2. Structure Detection**
Regex + layout used to detect:
- headings  
- subsections  
- section boundaries  

### **3. Cleaning & Chunking**
- remove page numbers, noise  
- split into ~1200-char chunks  
- add 200-char overlap

### **4. Hierarchical Summarization**
- chunk summaries → **Gemma 2**  
- merge summaries in batches  
- final literature review (~1–1.5 pages) → **Llama 3 (70B)**

### **5. Outputs**
- `summaries.json`  
- `final_summary.txt`

### **6. Streamlit Demo (Optional)**
Fast offline summarizer using **DistilBART**.

---

## 📦 Tech Stack

- PyMuPDF  
- pdfplumber  
- Regex  
- NLTK  
- Groq API (Gemma 2, Llama 3)  
- Streamlit  
- DistilBART  

---

## 🏁 Result

Generates **clean, structured, human-like literature reviews** from academic PDFs — reducing hours of manual reading to just minutes.

---
