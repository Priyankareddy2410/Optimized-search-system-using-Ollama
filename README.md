![image](https://github.com/user-attachments/assets/1d2d6013-8f49-4306-95be-38f3e3743b24)




🧠 Optimized Hybrid Search System
A privacy-first hybrid search engine that combines semantic search (via FAISS & embeddings) and lexical search (via BM25) to intelligently retrieve and answer queries from large text documents using a local Ollama LLM.

🚀 Key Features
🔎 Dual Search Engine: Combines BM25 (exact term matching) and FAISS (vector similarity) for better relevance.

🧱 Document Chunking: Splits and preprocesses large documents for efficient indexing.

🧠 Ollama LLM Integration: Uses phi3:latest (or any local model) for generating answers.

🧰 Asynchronous Processing: Faster loading with async operations.

♻️ LRU Caching: Caches repeated LLM queries to improve response time.

🔐 Runs Locally: No cloud usage—ideal for sensitive or proprietary data.

🧑‍💻 Installation
Prerequisites
Python 3.7+

Ollama (Download from ollama.com)

Setup

git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
pip install -r requirements.txt
📁 Preparing Your Documents
Place your .txt files in the project directory.
Update the files list in the Python script:


files = ["docs/report1.txt", "docs/manual.txt"]
Also, replace placeholder text like [company] with your actual organization or context.

▶️ Running the Search

python hybrid-search.py
You'll be prompted to enter your query.

Type quit to exit the session.

🧩 Project Architecture

           User Query
                │
      ┌─────────┴──────────┐
      ▼                    ▼
    Lexical Search        Semantic Search
    (BM25)          (FAISS + Embeddings)
      │                    │
      └────────┬───────────┘
               ▼
    Combined Weighted Context
               ▼
        Ollama (phi3:latest)
               ▼
        Generated Answer


🔐 Why Local Matters
This solution is 100% offline. It does not send any data to external APIs or cloud services—perfect for secure environments with confidentiality requirements.

💡 Example Use Cases
Internal enterprise knowledge search

Legal or healthcare document querying

Offline AI assistants for local data

