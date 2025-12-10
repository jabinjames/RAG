# RAG (Retrieval-Augmented Generation)

Overview

RAG is a technique used to improve the accuracy and reliability of Large LanguageModels (LLMs).Instead of generating answers purely from their training data, LLMs in a RAG pipeline retrieve relevant information from an external, 
authoritative knowledge base before generating a response.This allows the model to access updated, domain-specific, or private organizational data 
without needing to retrain the LLM.The retrieved documents are first converted into embeddings and stored in a vector database. At query time, the system
retrieves the most relevant chunks and supplies them to the LLM as context, reducing hallucinations and improving factual correctness.

Features

* **Gemini Integration:** Utilizes Gemini for powerful text generation.
* **ChromaDB:** Employs for fast and scalable vector indexing and retrieval.
* **[LangChain Framework:** Built using the LangChain framework for efficient pipeline construction.
* * **Document Ingestion:** Supports ingestion of [e.g., PDF, DOCX, TXT, Markdown] files.
* **Custom Splitter:** Implements a Recursive Character Text Splitter for optimal document chunking.
