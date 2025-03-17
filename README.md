# Rag-Project
RAG-Based Financial Report Analyzer

This project is a Retrieval-Augmented Generation (RAG) system designed to analyze a company's financial reports. It first searches for relevant information within a given financial document (e.g., SEC filings, earnings reports). If the required information is not found, the system queries Llama 2 to generate a relevant response.

Key Features:
✅ Document-Based Search – Extracts insights from the uploaded financial report.
✅ LLM-Based Query Handling – Uses Llama 2 for answers when document data is insufficient.
✅ Efficient Information Retrieval – Combines FAISS for semantic search and LLM for contextual understanding.
