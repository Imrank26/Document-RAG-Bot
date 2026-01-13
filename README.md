This README is designed to be professional and technical, making it perfect for your GitHub profile. It reflects the architecture and workflow found in your project files.

---

# Document-Based RAG Chatbot

An end-to-end **Retrieval-Augmented Generation (RAG)** pipeline designed to provide context-aware answers from local PDF datasets. This system leverages **Mistral-7B** and **FAISS** to ensure accurate document retrieval and response generation.

## Key Features

* 
**Automated Data Ingestion**: Loads and processes PDF files using `DirectoryLoader` and `PyPDFLoader`.


* 
**Semantic Chunking**: Implements `RecursiveCharacterTextSplitter` to create manageable text segments while preserving context.


* 
**Vector Storage**: Utilizes **FAISS** for efficient similarity search and local embedding storage.


* 
**Mistral-7B Integration**: Connects with **Hugging Face** endpoints to use Mistral-7B for inference.


* 
**Streamlit UI**: Provides a clean, interactive chat interface for real-time user engagement.



## Technical Stack

* 
**Language**: Python 


* 
**Framework**: LangChain 


* 
**LLM**: Mistral-7B-Instruct-v0.3 


* 
**Embeddings**: sentence-transformers/all-MiniLM-L6-v2 


* 
**Vector Database**: FAISS (Facebook AI Similarity Search) 


* 
**Interface**: Streamlit 



## Project Workflow

1. 
**Phase 1 (Memory Setup)**: Raw PDFs are loaded, split into 500-character chunks, and converted into vector embeddings.


2. 
**Phase 2 (LLM Chain)**: A `RetrievalQA` chain is established, connecting the FAISS index with the Mistral model using custom prompt templates.


3. 
**Phase 3 (UI Deployment)**: The application is served via Streamlit, utilizing `@st.cache_resource` for optimized vector store loading.



## Getting Started

### Prerequisites

* Python 3.9+
* Pipenv

### Installation

1. Clone the repository and install dependencies:
```bash
pipenv install langchain langchain_community langchain_huggingface faiss-cpu pypdf streamlit

```


2. Set up your environment variables:
```bash
export HF_TOKEN="your_huggingface_token"

```


3. Build the vector database:
```bash
python create_memory_for_llm.py

```

4. Run the application:
```bash
streamlit run medibot.py

```
---

**Would you like me to help you create a "Performance & Evaluation" section for this README to showcase your model's 
