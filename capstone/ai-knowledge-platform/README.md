# Capstone — AI Knowledge Platform

This project combines the DDIA labs into one production-style architecture.

## Conceptual architecture

```text
Upload
  |
  v
Knowledge API ----> source metadata / documents
  |
  v
Kafka / event log
  |
  v
Parser -> chunker -> embedding workers
                       |
                       v
                    Vector DB

Query
  |
  v
Retriever -> relevant chunks -> LLM -> answer

Redis may be used for caching.
```

## Design principle

Search indexes, vector stores, caches, and analytics should be treated as **derived data** where possible. Keep enough source-of-truth data and metadata to rebuild them.

## Capstone questions

- What is the source of truth?
- Which state is derived?
- How do we rebuild derived state?
- What happens if an embedding model changes?
- How do we version chunks and embeddings?
- How do we avoid duplicate processing?
- How do we recover after partial failure?
- How do we measure retrieval and answer quality?
