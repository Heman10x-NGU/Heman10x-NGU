# Hey, I'm Hemant

Backend / distributed systems engineer at **Bank of New York Mellon** building high-throughput event pipelines and reliable workflow-driven services (Kafka, gRPC, Redis, Temporal).

I solve performance + reliability problems — low-latency APIs, idempotency, retries, observability, **concurrent systems** — and build side-projects around **distributed caches**, **task queues**, **developer tools**, and **real-time AI agents**.

Currently exploring: storage systems, real-time architectures, MCP server development, and LLM integrations with strict structured outputs.

---

## Featured Projects

### [ThreadGraph](https://github.com/Heman10x-NGU/threadgraph) — Goroutine Leak & Deadlock Detector for Go

Static + dynamic analysis tool that finds goroutine leaks, deadlocks, and lock bugs in Go programs using execution traces — no instrumentation or code changes needed.

- **94% accuracy on GoBench GoKer** — 64/68 real production bugs detected (Kubernetes, etcd, CockroachDB, gRPC, Docker)
- **0 false positives** on `net/http/httptest` with 224 goroutines
- Goroutine provenance tree, Tarjan's SCC N-way deadlock detection, go/ssa static analysis, CI baseline flags

### [PhronAi](https://github.com/Heman10x-NGU/PhronAi) — Voice-Powered AI Diagramming

Voice-controlled AI agent that turns speech into system diagrams in real-time.

- Django + React + Groq LLaMA 3.3 + Deepgram
- **Zero hallucination** via Pydantic schema validation + Instructor
- ~4s end-to-end latency, 95%+ transcription accuracy

### [prelaunch-mcp](https://github.com/Heman10x-NGU/prelaunch-mcp) — Startup Idea Validator for AI Agents

MCP server that gives AI agents (Claude Code, Cursor, Windsurf) a pre-build reality check — scans 6 sources with LLM-powered intent parsing before you write a line of code.

- Scans **GitHub, HN, npm, PyPI, Reddit, Google/DDG** in parallel
- Outputs `competition_score` + `demand_score` + gap analysis with dynamic insights
- Drop-in for any MCP-compatible client: `claude mcp add prelaunch -- uvx prelaunch-mcp`

### [NexusCache](https://github.com/Heman10x-NGU/NexusCache) — Distributed Cache in Go

High-performance distributed caching system with **etcd service discovery**, **gRPC** communication, **consistent hashing**, and **Prometheus monitoring**.

- **23,400 ops/sec** with sub-1ms P50 latency (macOS M4)
- **Thread-safe** LRU cache with singleflight deduplication and **concurrent access**
- Hot data replication across nodes

### [TitanQueue](https://github.com/Heman10x-NGU/TitanQueue) — Distributed Task Queue in Go

Production-ready task queue with **Redis**, designed for reliability through **at-least-once delivery**.

- **Concurrent worker pool** with lease-based ownership and automatic recovery
- Priority queues, retry with exponential backoff, graceful shutdown
- Built-in Web UI dashboard for monitoring

---

## Tech Stack

**Languages:** Go · Java · Python · C++ · TypeScript

**Systems & infra:** Kafka · gRPC · Redis · etcd · Temporal · Postgres · Elasticsearch · Docker

**AI & LLM:** Claude API · Groq LLaMA · Deepgram · Instructor · Pydantic · MCP

**Patterns:** Consistent hashing · Singleflight · At-least-once delivery · Lease-based ownership · Exponential backoff · Goroutines · Worker pools · Thread-safe data structures

---

**Building AI infra or real-time systems? [Let's talk](https://www.linkedin.com/in/heman10x/).**

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
