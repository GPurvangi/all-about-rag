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
**Last updated:** 2026-05-31

**Where we left off:**
Theory fully locked. Discussed project structure and branch strategy.

**Decisions made this session:**
1. Project file structure for each RAG type:
   ```
   01-naive-rag/
   ├── data/sample.txt       # knowledge base documents
   ├── indexer.py            # chunk → embed → store in vector DB
   ├── retriever.py          # embed query → similarity search → top-K chunks
   ├── generator.py          # chunks + query → LLM → answer
   ├── main.py               # ties all 3 stages together
   ├── eval.py               # measures precision, recall, latency
   ├── requirements.txt      # package dependencies
   └── README.md             # explanation + how to run + results
   ```

2. `requirements.txt` packages confirmed:
   ```
   openai
   qdrant-client
   langchain
   langchain-openai
   tiktoken
   python-dotenv
   ```

3. Branch strategy decision (PENDING USER CONFIRMATION):
   - Current: 1 branch per RAG type (13 branches created)
   - Recommended: folders on `main`, branches only for active work → merge when done
   - User will decide tomorrow before starting development

**Next step when resuming:**
1. Decide branch strategy (keep 13 branches as temp workspaces OR collapse to main+folders)
2. Create `01-naive-rag/` folder structure
3. Start writing `indexer.py` — user describes code, Jarvis grills

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
