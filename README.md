# Rag_model_2

# The Product architecture looks like this:

                User Uploads PDF
                       │
                       ▼
              Read PDF (PyMuPDF)
                       │
                       ▼
         Recursive Text Splitter
                       │
                       ▼
        HuggingFace Embeddings
                       │
                       ▼
              FAISS Vector DB
                       │
             Similarity Search
                       │
                       ▼
                 Retrieved Chunks
                       │
                       ▼
          Prompt Template + LLM
             (Groq/OpenAI/Gemini)
                       │
                       ▼
                  Final Answer


# Project Structure

Advanced-RAG-Streamlit/
│
├── app.py
├── rag.py
├── requirements.txt
├── .streamlit
│      └── secrets.toml
├── utils.py
├── prompt.py
├── config.py
└── README.md

# Features

✅ Upload multiple PDFs

✅ FAISS Vector Database

✅ HuggingFace Embeddings

✅ Recursive Chunking

✅ Conversation Memory

✅ Source Documents

✅ Streaming Response

✅ Chat History

✅ Production Folder Structure

✅ Streamlit Cloud Ready

# Tech Stack

Streamlit

LangChain

FAISS

Sentence Transformers

Groq API

PyMuPDF

Python

