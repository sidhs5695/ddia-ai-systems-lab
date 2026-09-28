# Chapter 1 — Reliable, Scalable, and Maintainable Applications

## Lab: Production API Under Load

We start with an almost trivial Spring Boot API and gradually introduce realistic failure modes.

The point is not Spring Boot mastery. The point is to observe how reliability and performance change as dependencies and load are introduced.

## Reading themes

- Thinking About Data Systems
- Reliability
- Scalability
- Load and performance
- Maintainability

## Lab progression

### Checkpoint 1 — One healthy endpoint

Implement:

```
GET /documents/{id}
```

Return a small in-memory response.

**Do not add yet:** PostgreSQL, Hibernate, Docker, Kafka, retries, circuit breakers, or AI.

Finish line: `curl` returns HTTP 200.

### Checkpoint 2 — Add a slow dependency

Add a fake metadata endpoint that sleeps for about 2 seconds. Call it from the document endpoint.

Observe: a slow dependency makes the upstream request slow.

### Checkpoint 3 — Make the dependency fail

Introduce occasional HTTP 500 responses.

Observe the difference between a component fault and a user-visible service failure.

### Checkpoint 4 — Timeout

Add a client timeout shorter than the fake delay.

Decide whether metadata is critical. If it is not, return a degraded response.

### Checkpoint 5 — Retry carefully

Try one retry. Observe how retries can improve transient reliability but also increase traffic and tail latency.

### Checkpoint 6 — Circuit breaker

Stop repeatedly calling a dependency that is known to be failing.

### Checkpoint 7 — Measure

Load test the API and record at least:

- throughput
- p50
- p95
- p99

Discuss why averages hide tail latency.

## Completion criteria

Both contributors can:

- [ ] explain fault vs failure
- [ ] reproduce downstream latency propagation
- [ ] explain why timeouts are necessary
- [ ] explain why retries can make incidents worse
- [ ] describe graceful degradation
- [ ] interpret p50/p95/p99
- [ ] name one maintainability improvement made during the lab

## First study session

### Reading
Read only the opening **Thinking About Data Systems** section.

### Experiment
Create/start the Spring Boot project and make one endpoint return HTTP 200.

### Takeaway
> If this endpoint later depends on PostgreSQL, Redis, and another HTTP service, is the endpoint itself the data system—or is the combination the data system? Why?

Stop after this checkpoint.
