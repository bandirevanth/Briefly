# PDF Summarizer📄 

## Overview
This project is a Python-based Retrieval-Augmented Generation (RAG) pipeline that intelligently summarizes `.pdf` and `.txt` documents using a lightweight sentence embedding model and a locally hosted LLM (`ollama`). It leverages semantic search over chunked document text to extract the most relevant context before querying the language model.

## ⚙ Features
- ✅ Supports both `.txt` and `.pdf` inputs
- ✅ Automatically filters out irrelevant sections like **References** or **Bibliography**
- ✅ Splits large documents into context-friendly chunks
- ✅ Uses **sentence-transformers** (`all-MiniLM-L6-v2`) for vector similarity search
- ✅ Summarizes based on top-k relevant chunks using **Ollama + Gemma3:1b**
- ✅ Outputs concise, context-aware answers to a given question
- ✅ Saves results as `.txt`
  
## 📚 Tech Stack
- Python
- SentenceTransformers
- PyPDF2
- Ollama
- NumPy
- Pandas

## RAG Pipeline
1. text = read and clean input document
2. chunks = split text into retrievable pieces
3. chunk_embeddings = embed each chunk using SentenceTransformer
4. context = retrieve top-k relevant chunks via cosine similarity to query
5. answer = run LLM on prompt with query + context

## 🚀 How It Works
1. **File Reading**  
2. **Preprocessing**  
3. **Chunking**  
4. **Embedding**  
5. **Retrieval**  
6. **RAG Summarization**  
7. **Output**

## 🛠️ Usage
```bash
pip install -r requirements.txt
ollama run gemma3:1b
python pdf-summaizer.py
```

---

Don't forget to star me on GitHub and follow me! Thanks :)
