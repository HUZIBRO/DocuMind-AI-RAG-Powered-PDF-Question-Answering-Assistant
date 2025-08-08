# 📄 DocuMind AI: RAG-Powered PDF Question Answering Assistant

**PDF Insight AI** is an intelligent PDF assistant built with **LangChain**, **LLMs**, and **Retrieval-Augmented Generation (RAG)**.  
It allows you to **summarize**, **explore**, and **ask questions** about your document — all while ensuring answers are grounded in the uploaded content.

---

## 🚀 Features

- 📤 **Upload PDF** – Works with any text-based PDF document.  
- 🧠 **Prompt Engineering** – Instruction-tuned responses with predefined and custom formats.  
- 🧩 **Chunking** – Splits documents into smaller, overlapping chunks for better context retrieval.  
- 🧠 **Embedding + Vector Store** – Uses HuggingFace sentence transformers + FAISS for fast, in-memory vector similarity search optimized for QA systems.
- 📑 **About the File** – Generates a concise summary of the uploaded document.  
- 💡 **Recommended Questions** – Suggests relevant questions to guide exploration.  
- 🎯 **Customizable Instructions** – Choose from predefined answer styles or create your own.  
- 🔍 **Context-Aware Answers** – Only answers from the document; no hallucinations.  
- ⚡ **Session Optimization** – Caches processed document and retriever in session state to avoid reprocessing.  

---

## 🛠 Tech Stack

- **Python 3.10+**
- [Streamlit](https://streamlit.io/) – UI for interactive exploration.
- [LangChain](https://www.langchain.com/) – Framework for LLM applications.
- [ChatGroq](https://groq.com/) – LLM provider for fast inference.
- [HuggingFace Embeddings](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2) – Semantic text embeddings.
- [FAISS](https://faiss.ai/) – Vector database for efficient similarity search.
- [PyPDFLoader](https://api.python.langchain.com/en/latest/document_loaders/langchain.document_loaders.pdf.PyPDFLoader.html) – PDF parsing.

---

## 🔍 Why RetrievalQA?

We specifically use **LangChain's `RetrievalQA` chain** because the system is **designed as a focused QA assistant**.  
`RetrievalQA` ensures that:

1. **Questions are answered using only relevant retrieved chunks** from the vector store.  
2. **Context injection** happens automatically, without manual prompt construction for each query.  
3. It integrates **retrieval + LLM reasoning** in one unified pipeline, making it ideal for question answering use cases.

This approach is perfect for **QA systems** where **precision** and **relevance** are more important than creative or open-ended responses.

---

## 📦 Installation

# Install dependencies
pip install -r requirements.txt
