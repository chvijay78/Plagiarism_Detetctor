# 🧠 Semantic Plagiarism Detection Tool

This project is an **AI-powered semantic plagiarism detector** built using **Sentence Transformers (SBERT)**. Unlike traditional methods that rely on matching words, this tool checks for **meaning-level similarity** using **sentence embeddings** and **cosine similarity**.

---

## 🚀 Features

- ✅ Upload plain `.txt` files via an interactive widget (Jupyter Notebook)
- 🔍 Semantic similarity check using `all-MiniLM-L6-v2` model
- 💾 Stores uploaded content and filename in a **local SQLite database**
- ⚠️ Flags plagiarism if similarity exceeds a threshold (default: `0.70`)
- 🔒 Prevents storing semantically similar or duplicate files

---

## 🛠️ Technologies Used

- Python 3.x  
- [SentenceTransformers](https://www.sbert.net/)  
- `sqlite3`  
- `ipywidgets`  
- `IPython.display`  

---

## 💡 How to Use

1. **Open the Notebook**  
   Launch the `Plagiarism_Detector.ipynb` file in Jupyter Notebook.

2. **Run All Cells**  
   Run the notebook cells sequentially to initialize models, database, and UI.

3. **Upload Files**  
   Use the file upload widget to add a `.txt` file.

4. **What Happens Behind the Scenes**  
   - Text is extracted and encoded into sentence embeddings
   - Compared to previously stored documents using **cosine similarity**
   - If similarity > threshold → flagged as **plagiarized**
   - If unique → stored in the database

---

## ⚙️ Configuration

You can adjust the similarity detection sensitivity:

```python
PLAGIARISM_THRESHOLD = 0.75  # Default: 0.70
