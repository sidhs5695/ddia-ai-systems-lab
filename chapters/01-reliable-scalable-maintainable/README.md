# Chapter 1 — Reliable, Scalable, and Maintainable Applications

## Lab: Production API Under Load
Start with a trivial Spring Boot API, then gradually introduce failure modes.

### Checkpoint 1 — One healthy endpoint
Implement `GET /documents/{id}` with an in-memory response.

Do **not** add PostgreSQL, Hibernate, Docker, Kafka, retries, circuit breakers, or AI yet.

Finish line: `curl` returns HTTP 200.

### Checkpoint 2 — Slow dependency
Add a fake metadata endpoint that sleeps ~2 seconds. Call it from the document endpoint.

### Checkpoint 3 — Dependency failure
Introduce occasional HTTP 500 responses. Compare a component fault with a user-visible failure.

### Checkpoint 4 — Timeout
Add a client timeout. If metadata is noncritical, return a degraded response.

### Checkpoint 5 — Retry carefully
Try one retry and observe the effect on reliability, traffic, and tail latency.

### Checkpoint 6 — Circuit breaker
Stop repeatedly calling a dependency that is known to be failing.

### Checkpoint 7 — Measure
Record throughput plus p50, p95, and p99 latency.

## Completion criteria
Both contributors can:
- [ ] explain fault vs failure
- [ ] reproduce latency propagation
- [ ] explain why timeouts are necessary
- [ ] explain why retries can worsen incidents
- [ ] describe graceful degradation
- [ ] interpret p50/p95/p99

## First study session
**Reading:** opening "Thinking About Data Systems" section.  
**Experiment:** make one endpoint return HTTP 200.  
**Takeaway:** If the endpoint later depends on PostgreSQL, Redis, and another HTTP service, what is the actual data system?

Stop after this checkpoint.
