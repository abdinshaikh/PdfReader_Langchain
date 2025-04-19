# PDF Reader – LangChain-based Question Answering App
This is a beginner-level project that uses **LangChain** and **OpenAI GPT** to enable intelligent querying over PDF documents. The system allows users to upload a PDF, ask natural language questions about its content, and get context-aware answers based on the document.
## Features
- Upload any PDF file and extract its content
- Automatically split large documents into manageable text chunks
- Convert chunks into embeddings using OpenAI's API
- Store and retrieve document chunks using **FAISS vector search**
- Ask questions and receive accurate, context-aware answers from the PDF content
## Tech Stack
- **LangChain** – for chaining LLM logic
- **OpenAI GPT-3.5** – for answering questions
- **FAISS** – for fast semantic search
- **PyPDF2** – to read and extract text from PDF
- **Python** – core language
  
##  Project Structure
pdf-reader-langchain/ ├── main.py # Core logic ├── README.md # Project overview (this file) ├── requirements.txt # Dependencies └── sample.pdf # (Your PDF for testing)
##  How It Works

1. **Load PDF** using `PyPDF2`
2. **Split Text** into chunks using LangChain's `CharacterTextSplitter`
3. **Embed Chunks** using `OpenAIEmbeddings`
4. **Store Vectors** in FAISS
5. **Retrieve & Answer** user questions with `RetrievalQA` chain

---

##  Example Query

> Upload a PDF (e.g., lecture notes), and ask:  
> `"What is Electromagnetic Induction in the Earth?"`  
> → The app will return a context-aware answer from the uploaded file.

---

## Installation

```bash
pip install langchain langchain-community openai faiss-cpu PyPDF2 tiktoken python-dotenv
