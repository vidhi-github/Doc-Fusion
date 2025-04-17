# 📄 Doc-Fusion

**Doc-Fusion** is a robust, intelligent application that transforms collections of academic or technical PDFs into semantically searchable and structured outputs—including **LaTeX-based review papers**—with minimal effort. Powered by **LlamaParse**, **Google Gemini**, and **Milvus**, Doc-Fusion extracts, summarizes, and indexes documents into a vector database, enabling **natural language querying** and **automated review generation**.

---

## 🚀 Features

- 🔍 AI-powered PDF extraction and chunking using **LlamaParse**
- 🤖 Summarization via **Google Gemini**
- 🧠 Keyword-driven **semantic similarity search**
- 📚 Embedding & vector search with **Milvus**
- 🧾 **Automated LaTeX review paper generation**
- 📄 Compile LaTeX into **polished, formatted PDF outputs**
- 🌐 Streamlit web app interface
- 🐳 Full Docker container support
- 📂 Works with multiple PDFs
- 🧱 Modular architecture for easy scaling and extension

---

## 🧠 How It Works

1. **Multi-PDF Ingestion**  
   Upload multiple PDF documents as raw inputs.

2. **Keyword-Based Similarity Search**  
   A user-defined keyword query drives a **semantic similarity search**, extracting the most relevant content from the dataset.

3. **Dynamic LaTeX Generation**  
   Retrieved content is automatically converted into structured **LaTeX snippets**—including sections, figures, citations.

4. **Review Paper PDF Output**  
   Compiled LaTeX is rendered into a **professionally formatted review paper** with customized styling.

---

## ⚙️ Installation Steps

1. **Clone the repository**
```bash
git clone https://github.com/vidhi-github/doc-fusion.git
cd doc-fusion
```

2. **Generate API Keys**
- LlamaParse (LlamaIndex Cloud): https://cloud.llamaindex.ai  
- Google Gemini: https://makersuite.google.com/app  

3. **Create a `.env` file** in the root directory and paste:
```env
LLAMA_CLOUD_API_KEY=your_llama_key
GEMINI_API_KEY=your_gemini_key
```

4. **Create and activate a virtual environment**
```bash
python -m venv myenv
myenv\Scripts\activate       # On Windows
```

5. **Install dependencies**
```bash
pip install -r requirements.txt
```

6. **Parse and dump PDFs**
```bash
python automation.py dump data/cnn1.pdf data/cnn2.pdf output
```

7. **(Optional) Run with Docker**
```bash
docker compose up -d
```

8. **Search using a query**
```bash
python automation.py search "Convolutional Neural Network"
```

9. **Launch Streamlit app**
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
├── requirements.txt           # Python dependencies
├── .env                       # API keys (create manually)
│
├── data/                      # Input PDFs
├── output/                    # JSON summaries
├── myenv/                     # Virtual environment
├── static/                    # Optional LaTeX assets
│
├── Dockerfile                 # Docker configuration
├── docker-compose.yml         # Docker service runner
│
├── parser.py                  # LlamaParse-based PDF parser
├── retrieval.py               # Vector DB handling (Milvus)
├── ToLatex.py                 # LaTeX generator module
├── usegemini.py               # Gemini summarizer
├── llm_prompt.py              # Prompt templates for LLMs
└── README.md                  # You're reading it!
```

---

## 🌍 Applications

- 🧠 **Academic Research**: Streamlined review paper generation and literature analysis.
- 📚 **Document Management**: Ideal for law firms, universities, or corporate knowledge bases.
- 🔍 **AI-Powered PDF Search Engines**: Semantically index and search documents using natural queries.
- 🏥 **Healthcare & Legal**: Summarize case files, reports, or records with AI.
- 💼 **Enterprise Knowledge Extraction**: Convert legacy documentation into structured insights.

---

## 🛠️ Tech Stack

- Python 3.12  
- LlamaParse (LlamaIndex Cloud)  
- Google Gemini  
- Milvus (Vector DB)  
- PyMuPDF (for layout-preserving parsing)  
- Streamlit  
- Docker

---

## 🚀 Future Scope

- 🔧 Drag-and-drop GUI for PDF uploads  
- 🤖 Voice-enabled chatbot for reading summaries aloud  
- 🌐 Multilingual support for translation and search  
- 📄 OCR support for scanned PDFs  
- ☁️ Cloud upload (AWS S3, Firebase, etc.)  
- 📊 Analytics dashboard for document insights  
- 🧩 Plug-in support for other LLMs (GPT-4, Claude, etc.)  
- 📱 Cross-platform mobile app  
- 🧠 Fine-tuned models for domain-specific outputs  
- 🧪 Auto-evaluation of summary quality and key insights

---

## 🙌 Contributing

Pull requests are welcome!  
To contribute:

```bash
# Fork the repo
git checkout -b feature/your-feature
# Make your changes
# Submit a pull request to the main branch
```

---

## 📬 Contact

Built with ❤️ by **Vidhi Jindal**  
Feel free to reach out for collaborations or feedback!
Thank You for going throug my project.

---
