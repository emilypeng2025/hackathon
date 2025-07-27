# Hackathon July 2025

# AI-Powered Document Search and Summarization System

# "Power Searchers" Team:
  * Emily
  * Sagi

## Description

An AI-powered application for document ingestion, semantic search, and automatic summarization.

Built with modern NLP, deep learning, and vector search technology, this tool enables you to upload documents, search them with natural language queries, and receive accurate, context-rich answers and summaries — all through an easy-to-use web interface.

---

## Features

1.	**Interactive Web Interface (Streamlit)**
	  -	User-friendly web UI for uploading files and entering queries.
	  -	Powered by Streamlit for real-time interaction and visualization.
	  -	Optional: Easily accessible remotely (in Colab/cloud) using pyngrok/ngrok for secure public URLs.

2. **Document Ingestion & Text Extraction**
    - Upload PDF, Word, or plain text files directly in the browser.
    - Extracts raw text from each document using robust parsing libraries.

3. **Text Cleaning & Overlapping Chunking**
    - Splits text into overlapping chunks (configurable, default: 3 sentences per chunk, with optional overlap for better context)
    - Cleans text (removes unnecessary whitespace, headers, footers).

4. **Semantic Embedding Generation**
	  -	Uses advanced transformer-based models (e.g., all-MiniLM-L6-v2 from Sentence Transformers) to convert each chunk into a semantic embedding for powerful context-aware search.

5. **Vector Database Indexing**
	  - Stores embeddings in a Pinecone vector index for lightning-fast, scalable similarity search.
	  - Saves metadata (such as chunk text, document ID) for precise answer retrieval.

6. **Semantic Search Interface**
	 - Users submit natural language questions; the app retrieves the most semantically relevant text chunks from all uploaded documents.

7. **AI-Powered Summarization**
	  - Automatically summarizes top relevant chunks using state-of-the-art transformer models (e.g., T5-small).
	  - Multiple summarization modes: ratio-based, fixed-length, chunkwise.

8. **Result Presentation & Traceability**
	  - Clearly displays the generated answer summary along with supporting context.
	  - Shows which document and chunk each piece of supporting text came from, ensuring transparency.

9. **Secure Public Access with ngrok (Optional)**
	 - For use in environments like Google Colab or on cloud servers with no direct public URL:
	 - Integrates with pyngrok/ngrok to create a secure, temporary public URL for the Streamlit app.
	 - Share your AI app with anyone, anywhere, instantly.
---

## Tech Stack
	•	Python (core language)
	•	Streamlit (interactive web UI)
	•	pyngrok/ngrok (for secure public URLs in notebook/cloud, optional)
	•	PyPDF2, python-docx (for document text extraction)
	•	nltk, re (text cleaning, chunking, sentence splitting)
	•	sentence-transformers (semantic embedding)
	•	transformers (summarization with T5 or similar models)
	•	Pinecone (vector database for semantic search)
	•	rouge-score (for evaluation, if running QA experiments)

⸻

## Typical User Flow
	1.	Launch the App
	•	(Locally or via Colab/cloud with ngrok URL.)
	2.	Upload Documents
	•	Supported: PDF, DOCX, TXT.
	3.	Automatic Processing
	•	Extracts, cleans, and chunks text.
	•	Generates semantic embeddings and indexes them in Pinecone.
	4.	Ask Questions
	•	Enter a question in natural language.
	5.	Get Answers
	•	App retrieves relevant document chunks and summarizes them into a concise, context-aware answer.
	•	Displays supporting text and source information for transparency.
	6.	(Optional) Share your app via ngrok public URL
	•	Share your document search AI securely with others — no deployment required.

⸻



## Requirements

- Python 3.8+
- The following Python packages (install via pip install -r requirements.txt):
# requirements.txt
streamlit
pyngrok
PyPDF2
python-docx
sentence-transformers
transformers
nltk
pinecone
rouge-score
	•	A Pinecone API key (free to create at pinecone.io)
	•	(Optional, for Colab/cloud): An ngrok account and auth token

---

## Video Demo

*A demonstration video will be available here soon!*  
[![Watch the video](https://img.shields.io/badge/YouTube-Video-red)](https://your-demo-link-here)

---




- p.s. - to be considered:

##  voabulary:

- **Semantic Search:**  
  Search that is based on the *meaning* of text, not just keyword matches. Achieved by comparing text/query embeddings for contextual similarity.

- **Embeddings:**  
  Numerical vector representations of text, where semantically similar meanings produce similar vectors in high-dimensional space. Used for efficient comparison and retrieval.

- **Chunk:**  
  A small, manageable segment of text (such as a paragraph or a group of sentences). Chunking makes it possible to perform precise search and summarization.

- **Metadata:**  
  Supplementary information about each chunk (such as the original document name, chunk index, or page number) that helps with traceability, filtering, and providing context in the search results.

- **Vector Database (Pinecone):**  
  A fast and efficient cloud-based system for storing and searching large numbers of embeddings. Allows real-time semantic search across all ingested document chunks.

- **Streamlit:**  
  An open-source Python library for quickly building and deploying interactive web apps, used as the user interface for document upload, search, and result display.

- **pyngrok/ngrok:**  
  Tools that provide secure public URLs for your local web app. Useful for sharing your Streamlit app running on a notebook or a server without direct public access.


---
