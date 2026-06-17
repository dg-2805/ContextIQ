# ContextIQ – Application Flow

## High-Level User Journey

Landing Page
↓
Authentication
↓
Dashboard
↓
Add Knowledge Sources
↓
Processing
↓
Chat Interface
↓
Verified Answers

---

## Authentication Flow

Landing Page
↓
Sign In
↓
Select Provider

Google OAuth
OR
GitHub OAuth

↓

Authentication Success
↓
Dashboard

---

## Knowledge Source Flow

Dashboard
↓
Choose Input Method

├── Upload Documents
└── Paste Text

↓

Validation

↓

Processing

* Text Extraction
* Chunking
* Embedding Generation
* Vector Storage

↓

Processing Complete

↓

Ready For Questions

---

## Multi-Document Flow

Upload:

* PDF
* DOCX
* TXT

Paste:

* Direct Text

↓

Unified Knowledge Base

↓

Questions Search Across All Sources

---

## Question Answering Flow

User Question
↓
Generate Query Embedding
↓
Hybrid Retrieval
↓
Top-K Chunks
↓
Context Assembly
↓
Groq Generation
↓
Verification Layer
↓
Answer Display

---

## Source Citation Flow

Answer
↓
View Sources
↓
Source Name
↓
Chunk Preview
↓
Supporting Evidence

---

## History Flow

Dashboard
↓
Conversation History
↓
Select Session
↓
Restore Chat
↓
Continue Conversation

---

## Error Flow

Question Submitted
↓
No Relevant Context
OR
Verification Failed
↓
Display:

"This information is not available in the document."

---

## Logout Flow

Profile Menu
↓
Logout
↓
Session Ended
↓
Landing Page
