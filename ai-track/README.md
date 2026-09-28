# Practical AI Engineering Track

This track complements DDIA. It is aimed at software engineers building AI-backed products, not researchers training foundation models.

## Modules

1. **LLM fundamentals** — tokens, context, inference, model APIs
2. **Structured outputs** — reliable machine-readable responses
3. **Embeddings** — turning text into vectors for similarity
4. **Vector search** — indexing and retrieval
5. **RAG** — retrieval + prompt construction + generation
6. **Tool calling** — letting models invoke application capabilities
7. **Evaluation** — correctness, relevance, regressions
8. **Production concerns** — latency, cost, caching, observability, model/embedding versioning

## Rule

Do not let the AI layer hide the distributed-systems layer.

When an AI feature fails, ask whether the cause is:

- model behavior,
- retrieval quality,
- stale/incorrect derived data,
- storage,
- networking,
- concurrency,
- retries,
- backpressure,
- rate limits,
- versioning,
- or observability.

That distinction is a core goal of this repository.
