# Capstone — AI Knowledge Platform

## Conceptual architecture

```text
Upload
  |
  v
Knowledge API ---> source documents / metadata
  |
  v
Kafka / event log
  |
  v
Parser -> chunker -> embedding workers -> Vector DB

Query -> Retriever -> relevant chunks -> LLM -> answer

Redis may be used for caching.
```

## Core principle
Treat search indexes, vector stores, caches, and analytics as derived data where possible. Preserve enough source-of-truth data and metadata to rebuild them.

## Questions
- What is the source of truth?
- Which state is derived?
- How do we rebuild it?
- What happens when an embedding model changes?
- How do we version chunks and embeddings?
- How do we avoid duplicate processing?
- How do we recover after partial failure?
- How do we measure retrieval and answer quality?
