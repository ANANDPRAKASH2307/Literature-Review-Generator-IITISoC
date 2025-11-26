📘 Literature Review Generator — IITISoC

A system that automatically parses academic PDFs and generates structured literature reviews using PDF extraction + NLP + multi-stage LLM summarization.

🚀 Overview

This project solves the IITISoC challenge:

Automatically read research papers and produce accurate literature reviews.

It combines:

PyMuPDF for text blocks + bounding boxes

pdfplumber for tables

Regex heuristics for headings/captions

Chunking with overlap

Groq LLM pipeline (Gemma 2 + Llama 3) for multi-stage summarization

Streamlit + DistilBART (separate app) for fast real-time summaries

🧠 How It Works (Brief)

PDF Parsing
Extract blocks, bounding boxes, tables, captions.

Structure Detection
Identify headings and reconstruct sections.

Cleaning & Chunking
Remove noise; split into 1200-char chunks with overlap.

Hierarchical Summarization

Chunk summaries (Gemma 2)

Merge batches

Final long summary (Llama 3, ~1–1.5 pages)

Outputs

summaries.json

final_summary.txt

Streamlit Demo (Optional)
Fast offline summarizer using DistilBART.

📦 Tech Stack

PyMuPDF

pdfplumber

Regex

NLTK

Groq API (Gemma 2, Llama 3)

Streamlit + DistilBART

🏁 Result

Produces clean, structured, human-like literature reviews from academic PDFs—greatly reducing researchers’ manual reading time.
