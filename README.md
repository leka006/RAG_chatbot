SWS AI RAG Chatbot - Frontend

A React-based frontend for the **SWS AI RAG Chatbot**, designed to provide a simple and interactive interface for asking questions about company documents.

The frontend communicates with a **FastAPI backend**, which handles document ingestion, retrieval, and AI-powered response generation.

Features

-  Interactive AI chatbot interface
-  Question answering from company documents
-  Retrieval-Augmented Generation (RAG)
-  Displays sources used for generated answers
-  Supports conversation history
-  Provides suggested questions based on document content
-  Displays document/indexing status
-  Fast development and hot module replacement with Vite
-  REST API communication with FastAPI backend
-  Clean and responsive user interface

---

##  Tech Stack

### Frontend

- React
- JavaScript
- Vite
- CSS

### Backend

- FastAPI
- Python

### AI / RAG

- Sentence Transformers
- ChromaDB
- Ollama
- Llama 3.1 8B
- PDFPlumber

---

##  How It Works

The application follows a Retrieval-Augmented Generation workflow.


                Company PDFs
                     │
                     ▼
              PDF Text Extraction
                     │
                     ▼
                Text Chunking
                     │
                     ▼
             Sentence Embeddings
                     │
                     ▼
                 ChromaDB
              Vector Storage
                     │
                     │
User Question ───────┘
      │
      ▼
Question Embedding
      │
      ▼
Retrieve Top Relevant Chunks
      │
      ▼
Build Context + Conversation History
      │
      ▼
Ollama - Llama 3.1 8B
      │
      ▼
AI Generated Answer
      │
      ▼
Answer + Sources
      │
      ▼
React Frontend
