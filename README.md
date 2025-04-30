![image](https://github.com/user-attachments/assets/1d2d6013-8f49-4306-95be-38f3e3743b24)
📘 Optimized Hybrid Search System
A powerful, privacy-focused hybrid search system combining semantic (FAISS) and lexical (BM25) search to extract intelligent answers from large text documents using Ollama LLM (phi3 or any local model).

🔧 Features
🔍 Combines BM25 (lexical) + FAISS (semantic) search

⚙️ Local Ollama LLM (phi3:latest by default)

📚 Embedding generation with caching

⚡ Asynchronous document processing

🧠 LRU caching for repeated questions

🔐 Offline & privacy-respecting architecture

📦 Requirements
Python 3.7+

ollama installed locally → https://ollama.com

Python packages in requirements.txt

📥 Installation
bash
Copy
Edit
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
pip install -r requirements.txt
📂 Prepare Your Files
Place your .txt documents in the working directory.
In the script, edit this line:

python
Copy
Edit
files = ["path_to_your_file_1.txt", "path_to_your_file_2.txt"]
Replace with actual paths, e.g.:

python
Copy
Edit
files = ["docs/report1.txt", "docs/manual.txt"]
Also replace [company] in the script with your actual org/project name.


python hybrid-search.py

Interact with it:
Type your question when prompted
Type quit to exit


Project Flow
If the image doesn't render on GitHub, upload it to your repo and update the filename above accordingly.

Privacy & Security
This project is designed for offline use. It does not upload data to any cloud service, ensuring maximum privacy for sensitive or proprietary documents.
