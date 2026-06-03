# 📄 PDF Question Answering System using RAG

## 📌 Project Overview

This project implements a simple Retrieval-Augmented Generation (RAG) pipeline that allows users to upload a PDF document and ask questions about its content.

The system extracts text from the PDF, converts it into embeddings, stores the embeddings in a FAISS Vector Database, and retrieves the most relevant information based on the user's query.

---

## 🚀 Workflow

```text
PDF Document
      ↓
PDF Loader (PyPDFLoader)
      ↓
Text Chunking
      ↓
Embedding Generation
(HuggingFace MiniLM)
      ↓
FAISS Vector Database
      ↓
Similarity Search
      ↓
Relevant Chunks Retrieved
      ↓
Answer Generation / Output
```

---

## 🛠 Technologies Used

* Python
* Google Colab
* LangChain
* PyPDF
* HuggingFace Embeddings
* Sentence Transformers
* FAISS Vector Database

---

## 📂 Project Structure

```text
project/
│
├── PDF Upload
├── PDF Loader
├── Text Chunking
├── Embedding Generation
├── FAISS Vector Store
├── Similarity Search
└── Question Answering
```

---

## ⚙️ Installation

Install required libraries:

```bash
pip install langchain
pip install langchain-community
pip install langchain-huggingface
pip install langchain-text-splitters
pip install faiss-cpu
pip install sentence-transformers
pip install pypdf
```

---

## 📖 Implementation Steps

### Step 1: Upload PDF

The user uploads a PDF document through Google Colab.

### Step 2: Load PDF

PyPDFLoader extracts text from the uploaded PDF.

### Step 3: Chunking

The document is divided into smaller chunks using RecursiveCharacterTextSplitter.

```python
chunk_size = 500
chunk_overlap = 100
```

### Step 4: Generate Embeddings

Text chunks are converted into vector representations using:

```python
sentence-transformers/all-MiniLM-L6-v2
```

### Step 5: Create Vector Database

FAISS stores the embeddings for efficient similarity search.

### Step 6: Query Processing

The user enters a question related to the PDF.

### Step 7: Retrieve Relevant Content

FAISS retrieves the most relevant chunks based on semantic similarity.

### Step 8: Display Output

The retrieved content is displayed as the answer.

---

## 🎯 Features

✅ Upload any PDF document

✅ Automatic text extraction

✅ Text chunking

✅ Semantic embeddings

✅ Fast vector search using FAISS

✅ Context-based document retrieval

✅ Simple and lightweight implementation

---

## 📊 Sample Input

```text
What is Artificial Intelligence?
```

## 📊 Sample Output

```text
Artificial Intelligence refers to the simulation of human intelligence in machines that are programmed to think and learn.
```

---

## 📚 Learning Outcomes

Through this project, the following concepts were explored:

* Retrieval-Augmented Generation (RAG)
* Vector Databases
* Embeddings
* Semantic Search
* Document Processing
* LangChain Framework
* Information Retrieval Systems

---
