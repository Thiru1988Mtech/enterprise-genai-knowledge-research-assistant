# Enterprise GenAI Knowledge & Research Assistant

Enterprise GenAI application using RAG, Multi-Agent Architecture, LLM, and Production Engineering.

## Architecture

RAG + Multi-Agent + LLM + Production Engineering

## Technology Stack

- Python 3.11
- FastAPI
- LangChain
- LangGraph
- RAG
- Qdrant
- PostgreSQL
- Ollama
- Docker
- Kubernetes
- Azure
- GitHub Actions

## Project Lifecycle

PLAN → DESIGN → BUILD → TEST → DEPLOY → SECURE → MONITOR → SCALE → IMPROVE → CONTINUE

## Project Structure

### Purpose

The project follows separation of responsibilities.
Each folder has a specific responsibility so the application
can grow without putting all logic into one file.

### Current Structure

```text
Enterprise GenAI Knowledge & Research Assistant
│
├── app/
│   ├── __init__.py
│   └── main.py
│
├── api/
│   ├── __init__.py
│   └── routes.py
│
├── services/
│   ├── __init__.py
│   └── health_service.py
│
├── models/
│   └── __init__.py
│
├── config/
│   └── settings.py
│
├── tests/
│
├── docs/
│   └── ARCHITECTURE.md
│
├── .gitignore
├── README.md
├── PROGRESS.md
├── GIT_COMMANDS.md
├── requirements.txt
└── .venv/