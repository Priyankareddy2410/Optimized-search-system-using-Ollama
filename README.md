![image](https://github.com/user-attachments/assets/1d2d6013-8f49-4306-95be-38f3e3743b24)

🔍 Optimized Hybrid Search System using AI (FAISS + BM25 + Ollama)
This project implements a hybrid information retrieval system that combines semantic search (FAISS + embeddings) and lexical search (BM25). It enables querying large text documents locally and generates context-aware responses using a local language model served via Ollama.

🚀 Features
Hybrid Search: Combines semantic and lexical scoring for accurate retrieval

FAISS-based Embeddings: Fast vector similarity search using local embeddings

BM25 Scoring: Traditional keyword-based document ranking

AI-Powered Answering: Uses Ollama with phi3:latest or any installed model for generating natural language responses

Local-first & Secure: Ideal for proprietary, sensitive document handling

Dynamic Weighting: Balances semantic and lexical relevance scores automatically

Async Processing & Caching: Fast, responsive interactions with minimal recomputation

🧰 Requirements
Python 3.7+

Ollama installed locally: https://ollama.com

Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
📂 Usage
Prepare Text Files:
Place your .txt documents in your working directory. In the script, replace:

python
Copy
Edit
files = ["path_to_your_file_1.txt", "path_to_your_file_2.txt"]
with actual file paths like:

python
Copy
Edit
files = ["docs/report1.txt", "docs/manual.txt"]
Customize for Your Use Case:
Replace any placeholder like [company] with your organization or scenario-specific context.

Run the Script:

bash
Copy
Edit
python hybrid-search.py
Interact with It:

Type your query when prompted.

Type quit to exit the session.

🧠 Project Flow
pgsql
Copy
Edit
User Query
   │
   ├─> Lexical Search (BM25)
   │       │
   │       └──┐
   │          └────┐
   └─> Semantic Search (FAISS + Embeddings)
               │
   ┌───────────┘
   ▼
Combine Semantic + Lexical Scores
   │
   ▼
Ollama (phi3:latest or other local LLM)
   │
   ▼
Generated Answer
🔒 Note on Privacy
This solution is designed for offline/local usage. It does not upload data to any cloud services, making it suitable for secure environments.
