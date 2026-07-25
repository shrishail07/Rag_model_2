# 📚 Advanced RAG Chatbot with Streamlit, FAISS & Groq

An enterprise-ready **Retrieval-Augmented Generation (RAG)** application built with **Streamlit**, **LangChain**, **FAISS**, **Hugging Face Embeddings**, and **Groq LLMs**. Upload one or more PDF documents, ask questions in natural language, and receive accurate, context-aware answers based only on the uploaded content.

This project demonstrates a modern RAG pipeline suitable for learning, research, and production deployments.

---

# 🚀 Features

* 📄 Upload one or multiple PDF documents
* 🔍 Semantic search using FAISS Vector Database
* 🧠 Context-aware responses powered by Groq LLM
* 🤖 Hugging Face sentence-transformer embeddings
* ✂️ Intelligent document chunking
* 💬 Interactive chat interface
* 📚 Display retrieved document chunks
* ⚡ Fast inference with Groq
* ☁️ Ready for Streamlit Community Cloud deployment
* 🔒 API key management using Streamlit Secrets
* 🏗️ Modular and scalable project structure

---

# 🏛️ Project Architecture

```
                +-------------------+
                |   Upload PDFs     |
                +---------+---------+
                          |
                          v
                +-------------------+
                | Extract Text       |
                | (PyMuPDF)          |
                +---------+---------+
                          |
                          v
                +-------------------+
                | Text Chunking      |
                | Recursive Splitter |
                +---------+---------+
                          |
                          v
                +-------------------+
                | Generate           |
                | Embeddings         |
                +---------+---------+
                          |
                          v
                +-------------------+
                | FAISS Vector DB    |
                +---------+---------+
                          |
                          v
                +-------------------+
                | Similarity Search  |
                +---------+---------+
                          |
                          v
                +-------------------+
                | Groq LLM           |
                +---------+---------+
                          |
                          v
                +-------------------+
                | Final Answer       |
                +-------------------+
```

---

# 📂 Project Structure

```
Advanced-RAG-Streamlit/
│
├── app.py
├── rag.py
├── utils.py
├── config.py
├── prompt.py
├── requirements.txt
├── README.md
│
└── .streamlit/
    └── secrets.toml
```

---

# 🛠️ Technologies Used

| Technology   | Purpose              |
| ------------ | -------------------- |
| Python       | Programming Language |
| Streamlit    | Web Application      |
| LangChain    | RAG Framework        |
| FAISS        | Vector Database      |
| Hugging Face | Text Embeddings      |
| Groq         | Large Language Model |
| PyMuPDF      | PDF Processing       |

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone https://github.com/yourusername/Advanced-RAG-Streamlit.git

cd Advanced-RAG-Streamlit
```

---

## 2. Create a Virtual Environment

### Windows

```bash
python -m venv venv

venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv

source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🔑 Configure API Key

Create the following file:

```
.streamlit/secrets.toml
```

Add your Groq API key:

```toml
GROQ_API_KEY="your_groq_api_key"
```

---

# ▶️ Run the Application

```bash
streamlit run app.py
```

The application will open automatically in your browser.

---

# ☁️ Deploy on Streamlit Community Cloud

1. Push your project to GitHub.
2. Sign in to Streamlit Community Cloud.
3. Click **New App**.
4. Select your repository.
5. Choose the main branch.
6. Set `app.py` as the entry point.
7. Add your `GROQ_API_KEY` in **Secrets**.
8. Click **Deploy**.

Your application will be publicly accessible within a few minutes.

---

# 💡 How It Works

### Step 1

Upload one or more PDF documents.

↓

### Step 2

The application extracts all text from the uploaded documents.

↓

### Step 3

The extracted text is divided into smaller chunks using a Recursive Character Text Splitter.

↓

### Step 4

Each chunk is converted into vector embeddings.

↓

### Step 5

The embeddings are stored inside a FAISS Vector Database.

↓

### Step 6

When a user asks a question, the application performs semantic similarity search to retrieve the most relevant chunks.

↓

### Step 7

The retrieved context and user question are sent to the Groq Large Language Model.

↓

### Step 8

The model generates an accurate answer based only on the uploaded documents.

---

# 📊 RAG Pipeline

```
User

↓

Upload PDF

↓

Extract Text

↓

Chunk Text

↓

Generate Embeddings

↓

Store in FAISS

↓

Similarity Search

↓

Retrieve Relevant Chunks

↓

Prompt Engineering

↓

Groq LLM

↓

Final Response
```

---

# 📦 Main Dependencies

```
streamlit
langchain
langchain-community
langchain-text-splitters
langchain-groq
langchain-huggingface
sentence-transformers
faiss-cpu
pymupdf
python-dotenv
```

---

# 📸 Application Workflow

```
📄 Upload Document

↓

📚 Build Vector Database

↓

❓ Ask Questions

↓

🔍 Retrieve Relevant Context

↓

🤖 Generate AI Answer

↓

📖 Display Retrieved Sources
```

---

# 🎯 Example Questions

* Summarize the uploaded document.
* What are the key findings?
* Explain Chapter 3.
* List all important dates.
* What is the conclusion?
* Compare two concepts mentioned in the document.
* What are the recommendations?
* Explain this topic in simple language.

---

# 📈 Future Enhancements

* Multi-document collections
* Persistent FAISS storage
* Hybrid search (BM25 + Vector Search)
* Cross-encoder reranking
* OCR support for scanned PDFs
* Conversation memory
* Streaming responses
* Source citations with page numbers
* User authentication
* Document metadata filtering
* Chat history export
* Feedback collection
* Docker support
* Kubernetes deployment
* Cloud storage integration (AWS S3, Azure Blob, Google Cloud Storage)
* Evaluation using Ragas

---

# 🧪 Testing

Before deployment, verify the following:

* PDF uploads successfully.
* Text extraction works correctly.
* Vector database is created.
* Similarity search retrieves relevant chunks.
* Answers are generated from document context.
* Empty or invalid PDFs are handled gracefully.
* API key is configured correctly.

---

# 🤝 Contributing

Contributions are welcome.

If you would like to improve this project:

1. Fork the repository.
2. Create a new feature branch.
3. Commit your changes.
4. Push the branch.
5. Open a Pull Request.

---

# 📄 License

This project is licensed under the MIT License. You are free to use, modify, and distribute it in accordance with the license terms.

---

# 👨‍💻 Author

**Shreeshail Goura**

Generative AI Engineer

Passionate about Artificial Intelligence, Large Language Models, Retrieval-Augmented Generation (RAG), Machine Learning, Deep Learning, Agentic AI, and scalable AI application development.

---

# ⭐ Support

If you found this project helpful:

* ⭐ Star the repository
* 🍴 Fork the project
* 🛠️ Contribute improvements
* 📢 Share it with others

Your support helps improve and maintain the project for the community.

---

## Thank You

Thank you for exploring this Advanced RAG project. We hope it helps you learn, build, and deploy powerful AI-powered document question-answering applications. Happy coding!
