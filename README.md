# Rag-Project
RAG-Based Financial Report Analyzer

This project is a Retrieval-Augmented Generation (RAG) system designed to analyze a company's financial reports. It first searches for relevant information within a given financial document (e.g., SEC filings, earnings reports). If the required information is not found, the system queries Llama 2 to generate a relevant response.

Key Features:
✅ Document-Based Search – Extracts insights from the uploaded financial report.
✅ LLM-Based Query Handling – Uses Llama 2 for answers when document data is insufficient.
✅ Efficient Information Retrieval – Combines FAISS for semantic search and LLM for contextual understanding.

Implementation Process of RAG-Based Financial Report Analyzer
Step-by-Step Process:
1️⃣ Load & Preprocess Financial Report

Convert PDF into text using PyMuPDF (fitz).
Split text into chunks for efficient retrieval.
2️⃣ Generate Text Embeddings

Use SentenceTransformer (all-MiniLM-L6-v2) to convert text chunks into embeddings.
3️⃣ Create FAISS Index for Retrieval

Store embeddings in FAISS for fast similarity-based search.
4️⃣ User Query Handling

Convert user question into an embedding.
Search FAISS for the most relevant document chunks.
5️⃣ Determine Response Source

If relevant document chunks exist, return the extracted text.
If no relevant document found, query Llama 2 for a generated response.
6️⃣ Generate & Display Response

If document is used: Return retrieved content.
If Llama 2 is used: Generate LLM-based response
