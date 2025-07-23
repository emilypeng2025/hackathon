# Hackathon July 2025

# AI-Powered Document Search and Summarization System

# "Power Searchers" Team:
  * Emily
  * Sagi

## Description

AI application for ingesting documents, performing semantic search, and generating summaries of relevant sections.
This tool leverages modern NLP techniques to return contextually accurate and meaningful results from your documents.

---

## Features

1. **Document Ingestion & Text Extraction**
    - Upload PDF, Word, or plain text files via a web interface.

2. **Text Chunking & Cleaning**
    - Splits text into chunks (e.g., 200–500 tokens each).
    - Cleans text (removes unnecessary whitespace, headers, footers).

3. **Semantic Embedding Generation**
    - Uses state-of-the-art models (e.g., all-MiniLM-L6-v2) to represent each chunk as a semantic embedding.

4. **Vector Database Indexing**
    - Stores chunk embeddings in a FAISS index for efficient semantic search.
    - Maintains metadata for accurate result mapping.

5. **Semantic Search Interface**
    - Users can enter queries; the system finds the most semantically relevant chunks across all documents.

6. **AI-Powered Summarization**
    - Summarizes the most relevant text chunks using transformer models.

7. **Result Presentation**
    - Displays both the summary and supporting text context (including document name and location).

---

## Concepts in Use

- **File Upload & Document Ingestion** (Streamlit)
- **Text Extraction** (PyPDF2, python-docx, plain text)
- **Text Splitting & Preprocessing** (nltk)
- **Semantic Embedding Generation** (sentence-transformers)
- **Vector Similarity Search** (FAISS)
- **Query Embedding & Retrieval** (transformer)
- **AI-Based Text Summarization** (transformer models e.g. T5)
- **User Query Interface** (Streamlit web app)

---

## Usage

1. Run the app:  
    TO DO
2. Upload your document(s).
3. Enter your semantic search query.
4. Review summarized results and source context.

---

## Requirements

- Python 3.8+
- See `requirements.txt` for Python dependencies

---

## Video Demo

*A demonstration video will be available here soon!*  
[![Watch the video](https://img.shields.io/badge/YouTube-Video-red)](https://your-demo-link-here)

---




- p.s. - to be considered:

##  vocabulary:

- **Semantic Search:**  
  Search that is based on the *meaning* of text, not just keyword matches. Achieved by comparing text/query embeddings for contextual similarity.

- **Embeddings:**  
  Numerical vector representations of text, where similar meanings produce similar vectors.

- **Chunk:**  
  A small, manageable segment of text (such as a paragraph or a group of sentences) used for precise search and summarization.

- **Metadata:**  
  Supplementary information about each chunk (such as original document name, chunk index, or page number) for traceability and context.

- **Vector Database (FAISS):**  
  A fast and efficient system for storing and searching text embeddings.

---
