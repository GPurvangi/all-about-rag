# Progress Tracker

## Overall Status

| # | RAG Type | Branch | Theory | Build | Merged |
|---|----------|--------|--------|-------|--------|
| 1 | Naive RAG | `01-naive-rag` | ✅ Done | 🔄 In Progress | ❌ |
| 2 | Hybrid RAG | `02-hybrid-rag` | ❌ | ❌ | ❌ |
| 3 | HyDE | `03-hyde` | ❌ | ❌ | ❌ |
| 4 | Contextual RAG | `04-contextual-rag` | ❌ | ❌ | ❌ |
| 5 | Corrective RAG | `05-corrective-rag` | ❌ | ❌ | ❌ |
| 6 | Self-RAG | `06-self-rag` | ❌ | ❌ | ❌ |
| 7 | Adaptive RAG | `07-adaptive-rag` | ❌ | ❌ | ❌ |
| 8 | Agentic RAG | `08-agentic-rag` | ❌ | ❌ | ❌ |
| 9 | Graph RAG | `09-graph-rag` | ❌ | ❌ | ❌ |
| 10 | Multimodal RAG | `10-multimodal-rag` | ❌ | ❌ | ❌ |
| 11 | Text-to-SQL RAG | `11-text-to-sql-rag` | ❌ | ❌ | ❌ |
| 12 | Long-Context RAG | `12-long-context-rag` | ❌ | ❌ | ❌ |

---

## Current Session — RAG Type 1: Naive RAG

**Branch:** `01-naive-rag`

**Where we left off:**
Theory fully locked. Moving into build phase.

**Last question to user (unanswered):**
> "What files will you create inside `01-naive-rag/` and what will each do?"

**Next step when resuming:**
User answers file structure question → Jarvis validates → user creates files → builds each component step by step.

---

## Tech Stack Decided

| Layer | Tool |
|-------|------|
| LLM | OpenAI GPT-4o or Anthropic Claude API |
| Embeddings | `text-embedding-3-small` |
| Vector DB | Qdrant (local Docker) |
| Sparse/BM25 | `rank_bm25` |
| Graph | `networkx` or Neo4j |
| Framework | LangChain + LlamaIndex |
| Eval | RAGAS |
| Test Data | Same corpus across all 12 types |

---

## Repo

GitHub: https://github.com/GPurvangi/all-about-rag  
Local: `C:\Users\Purvangi\Documents\needs\all-about-rag`
