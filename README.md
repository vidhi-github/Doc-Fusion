# 📄 Doc-Fusion

**Doc-Fusion** is an intelligent PDF parsing and searching application powered by LlamaParse and Google Gemini. It extracts, summarizes, and indexes academic or technical documents into vector databases for seamless semantic search using natural language.

---

## 🚀 Features

- 🔍 AI-powered PDF extraction and chunking
- 🤖 Summarization via Google Gemini
- 📚 Embedding & vector search with Milvus
- 🌐 Streamlit web app interface
- 🐳 Docker container support
- 📂 Works with multiple PDFs

---

## ⚙️ Installation Steps

Follow these steps to set up and run the project locally:

### 1. Clone the repository

```bash
git clone https://github.com/vidhi-github/doc-fusion.git
cd doc-fusion
```

### 2. Generate API Keys

- **LlamaParse (LlamaIndex Cloud)** – https://cloud.llamaindex.ai
- **Google Gemini** – https://makersuite.google.com/app

### 3. Create a `.env` file in the root directory and paste:

```
LLAMA_CLOUD_API_KEY=your_llama_key
GEMINI_API_KEY=your_gemini_key
```

### 4. Create and activate a virtual environment

```bash
python -m venv myenv
myenv\Scripts\activate       # On Windows
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Parse and dump PDFs

```bash
python automation.py dump data/cnn1.pdf data/cnn2.pdf output
```

### 7. (Optional) Run with Docker

```bash
docker compose up -d
```

### 8. Search using a query

```bash
python automation.py search "Convolutional Neural Network"
```

### 9. Launch Streamlit app

```bash
streamlit run app.py
```

---

## 📁 Directory Structure

```
Doc-Fusion/
│
├── automation.py              # Main automation script for dumping/searching PDFs
├── app.py                     # Streamlit app interface
├── requirements.txt           # Python dependency file
├── .env                       # API keys (create manually)
│
├── data/                      # Folder containing input PDFs
│   ├── cnn1.pdf
│   ├── cnn2.pdf
│   └── ...
│
├── output/                    # Folder to store JSON summaries
│   └── summaries.json
│
├── myenv/                     # Virtual environment (excluded from Git)
│
├── static/                    # Optional static files
│   └── arxiv.sty
│
├── Dockerfile                 # Docker image config
├── docker-compose.yml         # Docker service runner
│
├── llm_prompt.py              # LLM prompt templates or handlers
├── parser.py                  # PDF parsing logic using LlamaParse
├── retrieval.py               # Embedding and vector store management
├── ToLatex.py                 # LaTeX converter module
├── usegemini.py               # Google Gemini integration
│
└── README.md                  # This file
```

---

## 💡 Usage

You can parse and store PDFs for semantic search using:

```bash
python automation.py dump data/file1.pdf data/file2.pdf output
```

To search documents:

```bash
python automation.py search "Your question or keyword"
```

Or access a beautiful UI:

```bash
streamlit run app.py
```

---

## 🐳 Docker Setup

If you'd rather containerize the app:

```bash
docker compose up -d
```

---

## 🛠️ Tech Stack

- **Python 3.12**
- **LlamaParse (LlamaIndex Cloud)**
- **Google Gemini**
- **Milvus / Vector DB**
- **Streamlit**
- **Docker**

---

## 🌍 Applications

- 🧠 **Academic Research:** Quickly extract and search through large research papers using natural queries.
- 📚 **Document Management Systems:** Useful in law firms, universities, or any organization dealing with extensive PDFs.
- 🔍 **Intelligent PDF Search Engines:** Build a search system where PDFs are indexed semantically.
- 🏥 **Healthcare & Legal:** Analyze medical records or legal case files with summaries and Q&A.
- 💼 **Enterprise Knowledge Base:** Extract institutional knowledge buried in legacy documentation.

---

## 🚀 Future Scope

- 🔧 **GUI-based PDF Upload:** Add drag-and-drop or file upload UI for non-technical users.
- 🤖 **Voice ChatBot Integration:** Add a voice-enabled chatbot for summaries.
- 🌐 **Multilingual Support:** Integrate translation and multilingual search features.
- 📄 **OCR Integration:** Use OCR to process scanned PDFs (e.g., using Tesseract or Google Vision API).
- 📦 **Cloud Integration:** Upload parsed data directly to cloud storage (e.g., AWS S3 or Firebase).
- 📊 **Analytics Dashboard:** Visualize PDF metadata, document frequency, topic modeling, etc.
- 🤝 **Collaboration Features:** Real-time annotations, comments, and multi-user editing.
- 🧠 **Model Fine-tuning:** Customize Gemini responses using domain-specific training data.
- 📱 **Mobile App:** Build a cross-platform app using Flutter or React Native.
- 🧩 **Plug-in Architecture:** Allow plug-and-play for other LLMs like Claude, GPT-4, etc.
- 🧪 **Auto Evaluation:** Automatically evaluate document quality, summarize chapters, or highlight key insights.

---

## 🙌 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## 📬 Contact

Built with ❤️ by Vidhi Jindal. Feel free to reach out for collaborations!
Thank you for going through my project.

---
