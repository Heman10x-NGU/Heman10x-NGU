# Hey, I'm Hemant

Backend / distributed systems engineer at **BNY Mellon**, working on high-throughput event pipelines, financial data systems, and reliable workflow-driven services.

I build around three themes:

- **LLM reliability and agent guardrails** - evals, calibration, logprobs, structured outputs, MCP-style workflows
- **Distributed systems and backend infrastructure** - Kafka, gRPC, Redis, queues, caches, concurrency, observability
- **Developer tools** - small, practical tools that help engineers validate, debug, or ship faster

Currently exploring: LLM evaluation, hallucination risk scoring, agent preflight checks, MCP integrations, and production-grade distributed systems.

---

## Featured Projects

### [Hallucination Sentinel](https://github.com/Heman10x-NGU/hallucination-sentinel) - LLM Output Risk Scoring

Open-source Python toolkit that scores LLM output risk using calibrated token entropy. It implements the Calibrated Entropy Score (CES) method from arXiv:2605.28264 and is designed for developers building RAG, agent, and batch QA systems.

- CLI + Python API for scoring entropy sequences and provider outputs
- Calibration workflow, thresholding, evaluation harness, and provider logprob smoke tests
- Agent/RAG guardrail examples with clear limitations: this is a risk signal, not a truth oracle

### [ThreadGraph](https://github.com/Heman10x-NGU/threadgraph) - Goroutine Leak & Deadlock Detector for Go

Static + dynamic analysis tool for finding goroutine leaks, deadlocks, and lock bugs in Go programs using execution traces.

- Detects goroutine leaks and deadlock patterns without application instrumentation
- Goroutine provenance tree, Tarjan SCC deadlock detection, go/ssa static analysis, CI baseline flags
- Built for debugging real concurrency failures, not just toy examples

### [NexusCache](https://github.com/Heman10x-NGU/NexusCache) - Distributed Cache in Go

Distributed caching system with etcd service discovery, gRPC communication, consistent hashing, singleflight deduplication, and Prometheus monitoring.

- Thread-safe LRU cache with concurrent access
- Consistent hashing and hot data replication across nodes
- Benchmarked locally at 23K+ ops/sec with sub-1ms P50 latency

### [TitanQueue](https://github.com/Heman10x-NGU/TitanQueue) - Distributed Task Queue in Go

Task queue built with Redis and Go, designed around reliability and at-least-once delivery semantics.

- Concurrent worker pool with lease-based ownership and automatic recovery
- Priority queues, retries with exponential backoff, graceful shutdown
- Web dashboard for queue and worker monitoring

### [PhronAi](https://github.com/Heman10x-NGU/PhronAi) - Voice-Powered AI Diagramming

Voice-controlled AI diagramming app that turns spoken architecture descriptions into system diagrams.

- Django + React + Groq + Deepgram
- Structured output validation with Pydantic / Instructor
- Built around real-time AI workflow UX, not just chat

### [ListFix](https://github.com/Heman10x-NGU/listfix) - Marketplace Listing Optimizer

Open-source tool for improving Facebook Marketplace listings from raw item descriptions.

- Generates clearer titles, descriptions, and pricing suggestions
- Practical AI utility for sellers and resellers
- Small product-shaped project focused on immediate usefulness

---

## Tech Stack

**Languages:** Go · Java · Python · C++ · TypeScript

**Systems & infra:** Kafka · gRPC · Redis · etcd · Temporal · Postgres · Elasticsearch · Docker

**AI & LLM:** OpenAI · Claude · Groq · Deepgram · Instructor · Pydantic · MCP · evals · logprobs

**Patterns:** Consistent hashing · Singleflight · At-least-once delivery · Lease-based ownership · Exponential backoff · Goroutines · Worker pools · Structured outputs

---

**Building LLM reliability tools, AI agents, or real-time backend systems? [Let's talk](https://www.linkedin.com/in/heman10x/).**

---

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/heman10x/) [![Email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:heman10x@gmail.com)

---

<details>
<summary>GitHub Stats</summary>

![](https://github-readme-stats.vercel.app/api?username=heman10x-NGU&theme=dark&hide_border=false&include_all_commits=true&count_private=true)
![](https://github-readme-streak-stats.vercel.app/?user=heman10x-NGU&theme=dark&hide_border=false)
![](https://github-readme-stats.vercel.app/api/top-langs/?username=heman10x-NGU&theme=dark&hide_border=false&include_all_commits=true&count_private=true&layout=compact)

</details>
