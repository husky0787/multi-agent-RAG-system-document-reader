# Document-Based QA System

This repository contains a Document-Based Question-Answering (QA) System designed to process and query uploaded documents (PDF, DOCX, TXT, MD) using advanced retrieval-augmented generation (RAG) techniques. Built with Python, the system leverages large language models (LLMs) and hybrid search to provide accurate, context-grounded responses.

## Features
- **Document Processing**: Converts uploaded documents to Markdown using Docling and splits them into chunks based on headers for efficient retrieval.
- **Hybrid Retrieval**: Combines BM25 (keyword-based) and SentenceTransformer embeddings (all-MiniLM-L6-v2) with Chroma for robust document search.
- **QA Workflow**: Uses LangGraph to orchestrate a multi-step process including relevance checking, answer generation, and verification with GPT-4o-mini via the Poe API.
- **User Interface**: Provides a Gradio-based web interface for uploading documents, asking questions, and viewing answers with verification reports.
- **Performance Optimization**: Implements caching to avoid reprocessing unchanged files and displays a "Processing..." status during LLM calls.

## Prerequisites
- Python 3.8 or higher
- Access to the Poe API (requires an API key for GPT-4o-mini)
- Internet connection for API calls and library downloads
