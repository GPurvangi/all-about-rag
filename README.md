# All About RAG

Upload audio recordings → build a searchable knowledge base → **chat** or **talk** to it. Answers cite the exact spoken moment (timestamp + speaker) and honestly label anything that comes from general knowledge, not the recording.

## Status

Early scaffold. Phase A (text chat RAG) in progress.

## Stack

| Layer | Tech |
|-------|------|
| Backend | Python 3.12, FastAPI |
| Frontend | Next.js, TypeScript |
| Database | PostgreSQL + pgvector |
| Jobs | Redis + ARQ |
| Providers | Swappable STT / embedding / LLM adapters (OpenAI default) |

## Project structure

```
all-about-rag/
├── backend/          # FastAPI app, RAG core, workers
├── frontend/         # Next.js UI (chat + voice)
├── data/audio/       # Local audio storage (dev)
├── ARCHITECTURE.md   # Full design + build phases
└── SETUP.md          # Scaffold reference
```

## Getting started

**Prerequisites:** Python 3.12+, Node.js 20+ (for frontend, later), Docker (for Postgres/Redis, later)

```bash
# Clone
git clone https://github.com/GPurvangi/all-about-rag.git
cd all-about-rag

# Backend
cd backend
python3.12 -m venv .venv
source .venv/bin/activate
pip install -r requirements-dev.txt

# Config
cp ../.env.example ../.env
# Edit .env with your API keys
```

## Build phases

1. **Phase A** — RAG brain + text chat (upload → transcribe → retrieve → answer with citations)
2. **Phase B** — Voice mode (turn-based → streaming → barge-in)
3. **Phase C** — Model routing, prompt caching, speaker intelligence, observability

See [ARCHITECTURE.md](ARCHITECTURE.md) for the full plan, data model, and API design.

## License

MIT — see [LICENSE](LICENSE).
