# ContextIQ – Technical Requirements Document (TRD)

## System Architecture

Frontend (Next.js)
↓
Authentication Layer
↓
FastAPI Backend
↓
Knowledge Processing Pipeline
↓
Embedding Service
↓
Vector Database
↓
Retrieval Engine
↓
Groq LLM
↓
Verification Layer

---

## Technology Stack

### Frontend

Framework:

* Next.js 15

Language:

* TypeScript

UI:

* Tailwind CSS
* shadcn/ui

State Management:

* React Context
* TanStack Query

---

### Backend

Framework:

* FastAPI

Language:

* Python 3.12

Validation:

* Pydantic

Server:

* Uvicorn

---

### Authentication

Provider:

* Google OAuth
* GitHub OAuth

Framework:

* Auth.js

---

### Database

Database:

* PostgreSQL

ORM:

* SQLAlchemy

Migration:

* Alembic

---

### Embedding Model

Model:

* BAAI/bge-small-en-v1.5

Purpose:

* Semantic vector generation

---

### Vector Database

Database:

* ChromaDB

Purpose:

* Store embeddings
* Metadata indexing
* Similarity retrieval

---

### LLM

Provider:

* Groq

Model:

* Llama 3.3 70B

Purpose:

* Context-aware answer generation

---

## Knowledge Processing Pipeline

Knowledge Source
↓
Text Extraction
↓
Chunking
↓
Embedding Generation
↓
Vector Storage

Supported Sources:

* PDF
* DOCX
* TXT
* Pasted Text

---

## Retrieval Pipeline

Question
↓
Query Embedding
↓
Hybrid Search
↓
Top-K Retrieval
↓
Context Assembly
↓
Answer Generation
↓
Verification Layer

---

## Verification Layer

### Stage 1

Similarity Threshold Validation

Purpose:

* Ensure retrieved chunks are relevant

### Stage 2

LLM-Based Verification

Purpose:

* Validate answer grounding

### Failure Handling

If evidence is insufficient:

"This information is not available in the document."

---

## Logging

Log Types:

* Authentication Logs
* Upload Logs
* Retrieval Logs
* API Logs
* Error Logs
* LLM Request Logs

---

## Containerization

Docker

Containers:

* Frontend
* Backend
* PostgreSQL

---

## Future Enhancements

* AWS S3 Storage
* Redis Caching
* Qdrant Migration
* Re-ranking Models
* Multi-modal Retrieval
