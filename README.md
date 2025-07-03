Retrieval-Augmented Generation (RAG) with LangChain & Gemini

This project implements a Retrieval-Augmented Generation (RAG) pipeline using LangChain, Google Gemini 1.5 Flash, and Chroma Vector Store. It scrapes structured content from the web, generates vector embeddings, stores them in a database, and allows the LLM to retrieve and respond intelligently.

🚀 Features
✅ Google Gemini 1.5 Flash LLM via LangChain
✅ Embedding using GoogleGenerativeAIEmbeddings
✅ ChromaDB for storing and searching document chunks
✅ Web scraping using BeautifulSoup via WebBaseLoader
✅ .env based secure API key management
✅ Full end-to-end RAG workflow

🧠 How It Works
1. Loads content from a web URL (in this case, Lilian Weng's blog post)
2. Filters and parses relevant sections using BeautifulSoup
3. Splits the content into chunks for efficient embedding
4. Generates embeddings using Google Generative AI
5. Stores embeddings in ChromaDB (vector store)
6. Retrieves relevant chunks using a similarity search
7. Feeds the retrieved text into Gemini 1.5 Flash for final output

🛠️ Tech Stack
Tool / Library	Purpose
LangChain	Orchestration framework
Google Generative AI	Embedding + LLM (Gemini)
ChromaDB	Vector database
BeautifulSoup4	Web scraping
python-dotenv	Secure environment config


📁 Project Structure

RAG-LangChain/
├── rag_pipeline.ipynb        # Main notebook
├── .env                      # API keys (DO NOT push to GitHub)
├── .gitignore                # Hides .env and checkpoints
├── requirements.txt          # Required Python packages
└── README.md                 # This file!

🔐 Environment Setup
Create a file named .env in your project root with the following contents:

LANGCHAIN_TRACING_V2=true
LANGCHAIN_ENDPOINT=https://api.smith.langchain.com
LANGCHAIN_API_KEY=your_langchain_api_key_here
LANGCHAIN_PROJECT=RAG
GOOGLE_API_KEY=your_google_api_key_here

🛡️ Make sure .env is listed in .gitignore to prevent accidental upload.

📦 Installation
8.Clone the repo:
  git clone https://github.com/YOUR_USERNAME/RAG-LangChain.git
  cd RAG-LangChain
  
9.Create a virtual environment (optional):
  python3 -m venv venv
  source venv/bin/activate
  
10.Install dependencies:
  pip install -r requirements.txt
📌 Run the Notebook

Open rag_pipeline.ipynb in Jupyter Notebook or VS Code, and run the cells.

The notebook will:
- Load the web content
- Generate embeddings
- Save chunks to ChromaDB
- Allow you to query with Gemini

🧪 Example Queries

model.invoke("What is an LLM agent?")
model.invoke("Summarize the article.")

✅ TODOs / Extensions
- [ ] Add support for PDF/Markdown files
- [ ] Deploy with Streamlit or Gradio
- [ ] Build multi-source RAG pipeline
- [ ] Switch to Gemini 1.5 Pro for deep reasoning
      
🤝 Credits
- LangChain
- Google AI
- Chroma
- BeautifulSoup4
  
📄 License
MIT License — use it freely and responsibly 🚀
