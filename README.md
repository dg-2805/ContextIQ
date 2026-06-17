# ContextIQ

ContextIQ is a Context-Aware Document Intelligence Platform that enables users to upload PDFs, DOCX, TXT files or provide pasted text as a knowledge source and receive accurate, source-grounded answers using Retrieval-Augmented Generation (RAG).

The platform combines semantic retrieval, vector search, answer verification, and citation-based responses to ensure that answers are generated strictly from user-provided documents. When sufficient evidence cannot be found, ContextIQ explicitly responds with:

> "This information is not available in the document."

## Key Features

* Multi-document semantic search
* PDF, DOCX, and TXT support
* Retrieval-Augmented Generation (RAG)
* ChromaDB vector storage
* BGE embedding models
* Groq-powered LLM responses
* Answer verification layer
* Source citations and evidence tracing
* Google & GitHub OAuth
* Dockerized deployment
* Next.js + FastAPI architecture

## Tech Stack

**Frontend**

* Next.js
* TypeScript
* Tailwind CSS
* shadcn/ui

**Backend**

* FastAPI
* PostgreSQL
* ChromaDB
* SQLAlchemy

**AI Stack**

* BAAI/bge-small-en-v1.5
* Groq LLM API
* Hybrid Retrieval
* Verification Pipeline

**Infrastructure**

* Docker
* Docker Compose

ContextIQ demonstrates production-oriented AI application engineering practices including retrieval pipelines, vector databases, authentication, observability, and hallucination-resistant answer generation.

