# Q&A Log — Theory Sessions

---

## RAG Type 1 — Naive RAG

**Session date:** 2026-05-30

### Q1: Two problems LLMs had before RAG?
**Answer:** Knowledge cutoff (LLM frozen at training date, can't answer recent events) + no private/domain knowledge (LLM never saw your internal docs, can't answer about YOUR data).
**Status:** ✅ Correct

### Q2: Three pipeline stages of Naive RAG?
**Answer:** Indexing (chunk → embed → store in vector DB) → Retrieval (embed query → similarity search → top-K chunks) → Generation (chunks + query → LLM → answer).
**Status:** ✅ Correct

### Q3: Why chunk documents instead of embed whole doc?
**Answer:** Semantic dilution (one vector averages all topics → weak similarity), context window limit (embedding models have token max), precision (less noise in LLM prompt).
**Status:** ✅ Correct after teaching. Key addition: chunk_overlap prevents answers split across boundaries.

### Q4: What is an embedding vector? Why cosine similarity?
**Answer:** Needed teaching. Key facts locked:
- Embedding = list of 1536 floats representing meaning-position in high-dimensional space
- Similar meaning → similar direction → high cosine similarity
- Cosine = angle between vectors = (A·B)/(|A|×|B|), range -1 to 1
- Cosine beats euclidean because it ignores vector magnitude (length), only cares about direction = meaning
**Status:** ✅ Taught and locked

### Q5: Naive RAG's 3 core weaknesses?
**Answer:** Needed teaching. Three failures:
1. Semantic mismatch — "cancel subscription" vs "terminate membership" → low cosine → wrong chunk → Fixed by Hybrid RAG
2. No retrieval quality check — bad chunks passed to LLM anyway → hallucination → Fixed by Corrective RAG
3. Single-shot no reasoning — one retrieval, no iteration → can't answer multi-hop questions → Fixed by Agentic RAG
**Status:** ✅ Taught and locked

---

### Theory Status: LOCKED ✅
### Build Status: IN PROGRESS 🔄
### Last question asked to user: "What files will you create inside `01-naive-rag/` and what will each do?"
