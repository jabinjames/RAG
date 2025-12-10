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
* **Document Ingestion:** Supports ingestion of [e.g., PDF, DOCX, TXT, Markdown] files.
* **Custom Splitter:** Implements a Recursive Character Text Splitter for optimal document chunking.

The RAG pipeline follows four main steps:

1.  **Load:** Documents are loaded from the `[data/]` directory.
2.  **Chunk & Embed:** Documents are split into chunks, converted to vector embeddings using **[Embedding Model Name, e.g., `BAAI/bge-small-en-v1.5`]**, and stored in the **[Vector DB]** index.
3.  **Retrieve:** On a user query, a similarity search retrieves the top **`k`** most relevant chunks.
4.  **Augment & Generate:** The user query and the retrieved context are combined into a prompt, which is sent to the LLM for a final, grounded answer.

Project Structure

RAG/
│── data/    

│── notebook/  

│── requirements.txt

│── .env

│── README.md

5.  Follow these steps to set up and run the project locally.

### Prerequisites

* Python **3.10+**
* **`pip`** (Python package installer)

### 1. Clone the Repository

```bash
git clone https://github.com/jabinjames/RAG.git
```
### 2. Install Dependencies
```bash
pip install -r requirments.txt
```
