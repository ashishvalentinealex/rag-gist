# LangChain + Pinecone RAG

![LangChain Pinecone Screenshot](./docs/assets/langchain-pinecone.png)

This project demonstrates a **Retrieval-Augmented Generation (RAG)** pipeline using [LangChain](https://www.langchain.com/), [OpenAI](https://platform.openai.com/), and [Pinecone](https://www.pinecone.io/).  
It includes two main scripts:  

- **Ingestion Pipeline** → Loads documents, splits them into chunks, generates embeddings, and stores them in Pinecone.  
- **Retrieval Pipeline** → Queries Pinecone, retrieves relevant chunks, and uses an LLM to answer natural language questions.  

> [!WARNING]  
> Running the ingestion script will **consume embedding API credits** and insert data into your Pinecone index. Ensure your API keys and index settings are correctly configured before running.

---

## Key Features

- **Document Ingestion** – Load `.txt` files and split them into manageable chunks  
- **Embeddings with OpenAI** – Generate vector representations of text data  
- **Vector Storage with Pinecone** – Store and query embeddings efficiently  
- **RAG Retrieval** – Retrieve context-aware answers with `ChatOpenAI`  

---

## Quick Start

### Prerequisites

- Python **3.9+**
- OpenAI API Key
- Pinecone API Key & Index  

Install dependencies:

```bash
pip install -r requirements.txt
```

## Installation

Clone the repo:

```bash
git clone https://github.com/your-username/langchain-pinecone-rag.git
cd langchain-pinecone-rag
```

## Set up environment variables in a .env file:
```bash
OPENAI_API_KEY="your_openai_api_key"
PINECONE_API_KEY="your_pinecone_api_key"
INDEX_NAME="your_pinecone_index_name"
```
