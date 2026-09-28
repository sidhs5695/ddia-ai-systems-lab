# DDIA + AI Systems Lab

A two-person study and engineering lab built around **Designing Data-Intensive Applications (DDIA)** and practical AI systems engineering.

The goal is not to race through the book. We use small experiments to make distributed-systems ideas observable, discuss the trade-offs together, and leave behind a repository that shows how our understanding evolved.

## Study rhythm

- 3 sessions per week
- 25–30 minutes per session by default
- one reading target
- one tiny experiment
- one written takeaway/question
- one unfinished project at a time
- no streak pressure: if a session is missed, resume from the smallest unfinished step

## Collaboration loop

1. Pick or create a GitHub issue.
2. Create a small branch from `main`.
3. Make one focused change.
4. Open a pull request and link the issue.
5. The other study partner reviews the reasoning as well as the code.
6. Discuss trade-offs in the PR.
7. Merge only when both people can explain what the experiment demonstrated.

See [CONTRIBUTING.md](CONTRIBUTING.md) for the full workflow.

## Roadmap

| DDIA chapter | Engineering lab | Status |
|---|---|---|
| 1. Reliable, Scalable, and Maintainable Applications | Production API Under Load | Start here |
| 2. Data Models and Query Languages | Multi-tenant Document & Permission Service | Planned |
| 3. Storage and Retrieval | Mini Storage Engine | Planned |
| 4. Encoding and Evolution | Versioned Event/API Platform | Planned |
| 5. Replication | Replicated Profile Service | Planned |
| 6. Partitioning | Sharded Key-Value Store | Planned |
| 7. Transactions | Wallet / API Quota Service | Planned |
| 8. The Trouble with Distributed Systems | Resilient Microservice Chaos Lab | Planned |
| 9. Consistency and Consensus | Distributed Job Coordinator | Planned |
| 10. Batch Processing | AI Document Batch Pipeline | Planned |
| 11. Stream Processing | Kafka Real-time Ingestion | Planned |
| 12. The Future of Data Systems | Derived-data / RAG Knowledge Platform | Planned |

The AI track is intentionally layered on top of the systems foundation: embeddings, vector search, RAG, tool calling, evaluation, and production concerns are introduced when the underlying storage/streaming concepts are useful.

## Repository map

```text
.
├── docs/                     # roadmap, progress, study method, ADRs
├── chapters/                 # one lab per DDIA chapter
├── ai-track/                 # practical AI engineering modules
├── capstone/                 # final AI knowledge platform
└── .github/                  # PR template, study issue template, CI
```

## Start here

Go to [Chapter 1](chapters/01-reliable-scalable-maintainable/README.md).

The first checkpoint is deliberately tiny: get the Spring Boot app running and add a single `GET /documents/123` endpoint. Do not add a database, retries, or another service yet.

## What counts as a good contribution?

A contribution does not need to be large. A useful PR can be:

- one reproducible failure
- one measurement
- one test
- one diagram
- one trade-off note
- one fix with before/after evidence
- one question that led to a useful discussion

The repository should show **learning**, not just finished code.
