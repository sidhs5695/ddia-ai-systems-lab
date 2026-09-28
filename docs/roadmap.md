# DDIA + AI Systems Roadmap

This roadmap connects every DDIA chapter to a small engineering lab. The projects are intentionally cumulative in difficulty, not necessarily in codebase.

## Chapter 1 — Reliable, Scalable, and Maintainable Applications
**Lab:** Production API Under Load  
Observe latency propagation, faults vs failures, timeouts, retries, graceful degradation, circuit breaking, and p50/p95/p99.

## Chapter 2 — Data Models and Query Languages
**Lab:** Multi-tenant Document & Permission Service  
Model users, teams, documents, tags, and permissions. Compare relational, document, and graph-shaped representations.

## Chapter 3 — Storage and Retrieval
**Lab:** Mini Storage Engine  
Build an append-only log, in-memory hash index, segments, and compaction.

## Chapter 4 — Encoding and Evolution
**Lab:** Versioned Event/API Platform  
Evolve payloads while old/new producers and consumers coexist. Compare JSON with a schema-based format.

## Chapter 5 — Replication
**Lab:** Replicated Profile Service  
Reproduce replication lag and stale reads. Explore read-your-writes and failover behavior.

## Chapter 6 — Partitioning
**Lab:** Sharded Key-Value Store  
Partition by hash, create hotspots, rebalance, and discuss range-query consequences.

## Chapter 7 — Transactions
**Lab:** Wallet / API Quota Service  
Reproduce lost updates and compare locking/isolation choices.

## Chapter 8 — The Trouble with Distributed Systems
**Lab:** Resilient Microservice Chaos Lab  
Inject delay, dropped requests, duplicated delivery, and process failure. Practice deadlines and idempotency.

## Chapter 9 — Consistency and Consensus
**Lab:** Distributed Job Coordinator  
Implement a lease-based leader, reproduce split brain, then add fencing tokens. Connect observations to linearizability, ordering, and consensus.

## Chapter 10 — Batch Processing
**Lab:** AI Document Batch Pipeline  
Extract, clean, chunk, and embed documents with parallel workers and safe reprocessing.

## Chapter 11 — Stream Processing
**Lab:** Kafka Real-time Ingestion  
Work with partitions, consumer groups, offsets, retries, DLQs, duplicate delivery, and idempotent consumers.

## Chapter 12 — The Future of Data Systems
**Lab:** Derived-data / RAG Knowledge Platform  
Treat search indexes, vector stores, caches, and analytics as derived state that can be rebuilt from source-of-truth data and events.

# AI Track

AI is an application layer layered onto the systems work:

1. LLM fundamentals and inference
2. Prompting and structured outputs
3. Embeddings
4. Vector search
5. Retrieval-augmented generation
6. Tool/function calling
7. Evaluation, latency, token cost, and versioning
8. Production RAG/agent architecture

The goal is AI engineering for software engineers, not model research.
