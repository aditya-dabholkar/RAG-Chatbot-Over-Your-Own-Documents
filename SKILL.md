---
project: Production RAG Chatbot Over Your Own Documents
track: ai-ml
level: beginner-to-intermediate
started: 2026-09-17
shipped: <fill in when deployed>
repo: https://github.com/adi5677303/rag-chatbot-capgemini
live: <fill in demo URL when deployed>
---

# 1. What this project is
A chatbot that answers questions strictly from a set of documents I provide, using retrieval-augmented
generation (RAG). It cites which source chunk each answer came from and refuses to answer when
the documents don't contain the information, instead of making something up.

# 2. Problem it solves
Plain LLMs hallucinate and don't know about private/specific documents. This lets me ask questions
directly against a real document collection (e.g. college notes, a company's docs, or a personal
knowledge base) and get grounded, source-cited answers instead of generic LLM guesses.

# 3. Architecture
<Fill in once built — an ASCII or image diagram showing: document ingestion -> chunking ->
embedding -> vector store -> retrieval -> re-ranking -> LLM answer generation -> citation.>

Components:
- Ingestion pipeline -> parses PDF/DOCX/Markdown into text -> handles real-world messy documents
- Chunker -> splits text into overlapping chunks -> balances context size vs retrieval precision
- Vector store (pgvector) -> stores embeddings for similarity search -> <why this over alternative>
- Retriever (hybrid BM25 + vector) -> finds relevant chunks -> <why hybrid over vector-only>
- Re-ranker (cross-encoder) -> re-orders retrieved chunks by relevance -> <why needed>
- FastAPI backend -> serves the chat API -> <why this over alternative>
- Frontend (Streamlit/Next.js) -> chat UI -> <why this over alternative>

# 4. Key decisions and trade-offs
| Decision | Options I considered | What I chose | Why | What I gave up |
|---|---|---|---|---|
| | | | | |

# 5. Skills demonstrated
- [ ] Embeddings & vector similarity search — evidence: <file / commit>
- [ ] Chunking strategy and its effect on retrieval quality — evidence: <file / commit>
- [ ] Hybrid retrieval (BM25 + vector) and re-ranking — evidence: <file / commit>
- [ ] Prompt engineering and grounding constraints (refusal behavior) — evidence: <file / commit>
- [ ] Evaluation methodology for LLM systems — evidence: <file / commit>
- [ ] Cost and latency tracking — evidence: <file / commit>

# 6. Numbers I measured
| Metric | Before | After | How I measured it |
|---|---|---|---|
| Retrieval hit rate | | | 30-question labelled evaluation set |
| Answer latency | | | |
| Token cost per query | | | |

# 7. Things that broke and how I fixed them
1. Symptom:
   Cause:
   Fix:
   Lesson:

# 8. What I would do differently at 100x scale
-
-
-

# 9. Interview answers I have rehearsed
Q: How do you know your RAG system is good? Give me a number and tell me how you measured it.
A:

Q: Your chunk size is 500 tokens. What breaks at 100 and what breaks at 2000?
A:

Q: The model confidently answers a question your documents do not cover. How did you stop that?
A:

# 10. Honest limitations
<Fill in once built — e.g. what document types aren't supported, what happens at scale, etc.>

# 11. How to run it
```bash
git clone https://github.com/adi5677303/rag-chatbot-capgemini
cd rag-chatbot-capgemini
cp .env.example .env  # fill in the values listed below
docker compose up --build
# open http://localhost:3000
```
Required environment variables: <list them once decided — e.g. OPENAI_API_KEY, DATABASE_URL>

# 12. Credits
- Build guide: "The Resume Project Vault 2026" by @pratham.codes
- <add any tutorial, repo, or article referenced during build>
