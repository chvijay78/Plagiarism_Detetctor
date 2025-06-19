# 🧠 Semantic Plagiarism Detection Tool

This project is an AI-powered semantic plagiarism detection tool that uses **Sentence Transformers (SBERT)** to identify content similarity at the meaning level, not just keywords or phrases. It stores submitted `.txt` documents in a local SQLite database and checks new uploads for plagiarism based on cosine similarity between sentence embeddings.

🚀 Features
- ✅ Upload plain `.txt` files via an interactive widget (in Jupyter Notebook).
- 🔍 Semantic similarity check using `all-MiniLM-L6-v2` model.
- 💾 Stores uploaded document content and filename in an SQLite database.
- ⚠️ Detects plagiarism if semantic similarity exceeds a defined threshold (default: 0.7).
- 🔒 Prevents duplicate or similar content from being stored again.

🛠️ Technologies Used
- Python 3.x
- [SentenceTransformers](https://www.sbert.net/)
- [sqlite3](https://docs.python.org/3/library/sqlite3.html)
- [ipywidgets](https://ipywidgets.readthedocs.io/en/latest/)
- [IPython.display](https://ipython.readthedocs.io/en/stable/api/generated/IPython.display.html)

💡 Usage
Open the Jupyter Notebook (.ipynb file).
Run all the cells.
Use the file upload widget to upload a .txt file.

The script will:
Extract and encode the content.
Compare it with previously saved documents using cosine similarity.
Notify if plagiarism is detected or save the document to the database.

⚙️ Configuration
Threshold: You can adjust the similarity threshold by modifying the PLAGIARISM_THRESHOLD variable:
PLAGIARISM_THRESHOLD = 0.75  (Increase or decrease for strictness)

📌 Limitations
Designed for .txt file uploads only.
Only works in Jupyter Notebook due to ipywidgets integration.
Requires a GPU for faster processing if working with large files or many documents.
