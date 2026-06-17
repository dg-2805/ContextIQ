# ContextIQ – Backend Schema

## Overview

The system uses PostgreSQL for application data and ChromaDB for vector storage.

PostgreSQL stores:

* Users
* Documents
* Conversations
* Messages
* Retrieval Logs

ChromaDB stores:

* Embeddings
* Chunk Metadata
* Similarity Search Indexes

---

# Users Table

Table Name:
users

Fields:

id UUID PRIMARY KEY

email VARCHAR UNIQUE NOT NULL

name VARCHAR NOT NULL

avatar_url TEXT

oauth_provider VARCHAR

created_at TIMESTAMP

updated_at TIMESTAMP

---

# Knowledge Sources Table

Table Name:
knowledge_sources

Fields:

id UUID PRIMARY KEY

user_id UUID

source_name VARCHAR

source_type VARCHAR

file_path TEXT

raw_text TEXT

status VARCHAR

created_at TIMESTAMP

updated_at TIMESTAMP

Supported Types:

* pdf
* docx
* txt
* pasted_text

Status Values:

* uploaded
* processing
* indexed
* failed

---

# Chunks Table

Table Name:
chunks

Fields:

id UUID PRIMARY KEY

source_id UUID

chunk_index INTEGER

chunk_text TEXT

token_count INTEGER

chroma_document_id VARCHAR

created_at TIMESTAMP

---

# Conversations Table

Table Name:
conversations

Fields:

id UUID PRIMARY KEY

user_id UUID

title VARCHAR

created_at TIMESTAMP

updated_at TIMESTAMP

---

# Messages Table

Table Name:
messages

Fields:

id UUID PRIMARY KEY

conversation_id UUID

role VARCHAR

content TEXT

created_at TIMESTAMP

Roles:

* user
* assistant
* system

---

# Retrieval Logs Table

Table Name:
retrieval_logs

Fields:

id UUID PRIMARY KEY

conversation_id UUID

query TEXT

source_id UUID

chunk_id UUID

similarity_score FLOAT

retrieved_at TIMESTAMP

---

# Verification Logs Table

Table Name:
verification_logs

Fields:

id UUID PRIMARY KEY

message_id UUID

verification_result BOOLEAN

confidence_score FLOAT

reason TEXT

created_at TIMESTAMP

---

# Relationships

users
│
├── knowledge_sources
│
└── conversations
│
└── messages

knowledge_sources
│
└── chunks

messages
│
└── verification_logs

retrieval_logs
│
├── chunks
└── knowledge_sources
