# CriminalLawAgent

An Agentic AI-powered legal assistant built using Django, Amazon Bedrock, ChromaDB, and Retrieval-Augmented Generation (RAG).

The goal of this project is to help users understand Indian criminal law provisions, retrieve relevant legal sections, generate legal document drafts, and provide contextual legal information using authoritative legal sources.

> **Disclaimer:** This project provides legal information and document assistance only. It is not a substitute for professional legal advice from a licensed advocate.

---

## Features

### Legal RAG Search

* Retrieve relevant sections from:

  * Bharatiya Nyaya Sanhita (BNS) 2023
  * Bharatiya Nagarik Suraksha Sanhita (BNSS) 2023
  * Bharatiya Sakshya Adhiniyam (BSA) 2023
* Semantic search using vector embeddings.
* Context-aware legal question answering.

### Agentic Workflow

* Legal Research Agent
* Retrieval Agent
* Draft Generation Agent
* Validation Agent
* PDF Generation Agent (Planned)

### Document Generation

Generate legal drafts such as:

* Police Complaints
* FIR Complaint Drafts
* Affidavits
* Legal Applications

### Vector Search

* ChromaDB persistent vector store
* Local embedding storage
* Fast semantic retrieval

### Amazon Bedrock Integration

* LLM-powered reasoning and drafting
* Bedrock model support
* Production-ready architecture

---

## Project Architecture

```text
User
 │
 ▼
Django Application
 │
 ▼
Agent Layer
 │
 ├── Legal Research Agent
 ├── Retrieval Agent
 ├── Draft Generation Agent
 └── Validation Agent
 │
 ▼
Amazon Bedrock
 │
 ▼
ChromaDB Vector Store
 │
 ▼
Legal Documents
(BNS / BNSS / BSA)
```

---

## Tech Stack

### Backend

* Python
* Django

### AI / RAG

* Amazon Bedrock
* LangChain
* ChromaDB

### Storage

* Chroma Persistent Vector Store

### Future Enhancements

* PostgreSQL + pgvector
* Amazon AgentCore
* Multi-Agent Orchestration
* User Authentication
* Conversation Memory

---

## Project Structure

```text
CriminalLawAgent/
│
├── agent/
├── CriminalAI/
├── templates/
├── notebook/
│
├── Documents/          # Local legal PDFs (ignored by git)
├── vector_store/       # ChromaDB storage (ignored by git)
│
├── manage.py
├── main.py
├── requirements.txt
├── pyproject.toml
├── uv.lock
└── README.md
```

---

## Setup

### Clone Repository

```bash
git clone <repository-url>
cd CriminalLawAgent
```

### Create Virtual Environment

```bash
python -m venv .venv
```

Windows:

```bash
.venv\Scripts\activate
```

Linux/Mac:

```bash
source .venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure Environment Variables

Create a `.env` file:

```env
AWS_ACCESS_KEY_ID=YOUR_ACCESS_KEY
AWS_SECRET_ACCESS_KEY=YOUR_SECRET_KEY
AWS_REGION=ap-south-1
BEDROCK_MODEL_ID=YOUR_MODEL_ID
```

### Run Django

```bash
python manage.py runserver
```

---

## Required Legal Documents

Place the following documents inside the local `Documents/` directory:

```text
Documents/
├── Bharatiya_Nyaya_Sanhita_2023.pdf
├── Bharatiya_Nagarik_Suraksha_Sanhita_2023.pdf
└── Bharatiya_Sakshya_Adhiniyam_2023.pdf
```

These files are intentionally excluded from Git.

---

## Development Roadmap

### Phase 1

* PDF ingestion
* Chunking
* Embeddings
* ChromaDB storage
* Basic legal Q&A

### Phase 2

* Complaint generation
* Affidavit generation
* Source citations

### Phase 3

* Multi-agent workflow
* Memory
* User sessions

### Phase 4

* AgentCore deployment
* PostgreSQL + pgvector
* Production deployment

---

## Future Vision

Build a full Agentic Legal Assistant capable of:

* Legal research
* Criminal law assistance
* Draft generation
* PDF automation
* Multi-agent reasoning
* AgentCore deployment on AWS

while maintaining transparency, traceability, and source-backed responses.
