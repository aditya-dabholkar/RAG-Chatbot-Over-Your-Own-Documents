# Production RAG Chatbot Over Your Own Documents

A retrieval-augmented generation (RAG) chatbot that answers questions strictly from a supplied
document collection — with inline citations, hybrid retrieval, re-ranking, and a measured evaluation
of answer quality against a labelled question set. Built to prove practical, deployable AI engineering
skill rather than a notebook demo.

**Status:** 🚧 In progress — repository scaffolded, build starting soon.

## Planned stack
- Python, FastAPI
- LangChain or LlamaIndex
- pgvector (or Qdrant/Chroma) for vector storage
- Hybrid retrieval: BM25 + vector similarity, with cross-encoder re-ranking
- Streamlit or Next.js for the chat UI

## Planned features
- [ ] Document ingestion (PDF, DOCX, HTML, Markdown)
- [ ] Chunking with overlap (comparing at least two chunking strategies)
- [ ] Hybrid retrieval (BM25 + vector) with metadata filtering
- [ ] Cross-encoder re-ranking of retrieved candidates
- [ ] Answers with inline citations to the source chunk
- [ ] Refusal behavior when context doesn't contain the answer
- [ ] Evaluation harness measuring retrieval hit rate and answer faithfulness
- [ ] Token/cost tracking per query

## Build log
Progress and design decisions are tracked in [`SKILL.md`](./SKILL.md) as the project develops.

## Credits
Project structure and build plan adapted from "The Resume Project Vault 2026" by @pratham.codes.
