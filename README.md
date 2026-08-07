# Hemant Kumar

**Applied AI engineer — agent orchestration, RAG, evals, and LLM inference.**
I build agentic systems and the inference and evaluation infrastructure underneath them, then
publish the measurements — including the ones that came out negative.

At **BNY Mellon** (Applied AI Engineer, 2024–present) I ship RAG assistants, agentic workflows,
MCP servers, and evaluation harnesses on a Python/Go distributed-systems foundation.

**[→ Interactive portfolio](https://heman10x-ngu.github.io/)** · <heman10x@gmail.com>

Open to **remote** roles: *Applied AI Engineer ·  Fullstack AI Engineer · Forward Deployed Engineer ·
Inference / Model Performance Engineer.* Based in India, 4–6h overlap with EU and US-East.

`Python` `Go` `TypeScript` · `agent orchestration` `multi-agent systems` `RAG` `hybrid retrieval`
`context engineering` `evals` `LLM guardrails` `LLM inference` `KV cache` `observability`
`distributed systems` `MCP`

---

## Featured

### [nanoserve](https://github.com/Heman10x-NGU/nanoserve) — LLM inference engine
`inference optimization` · `model serving` · `KV cache` · `continuous batching` · `latency optimization`

A from-scratch **LLM inference engine** for Apple Silicon: hand-written autoregressive **decode
loop**, block-hashed **KV-cache prefix reuse**, **continuous batching**, and an
**OpenAI-compatible SSE streaming** server. Not a wrapper around `mlx_lm.generate` — the scheduler,
cache ownership, and admission path are all readable in one sitting.

> **67.7% lower median TTFT** on a reusable 576-token prefix (240.50 → 77.76 ms), verified
> token-identical across 5 paired runs · **80.76 ms p95 TTFT at concurrency 8** (24 requests, one
> model forward per step) · **178.79 tok/s** p50 vs 173.50 for `mlx_lm.generate` in an
> alternating-order paired baseline. M4, Qwen2.5-0.5B-Instruct-4bit, raw per-request JSON committed.

---

### [threadgraph](https://github.com/Heman10x-NGU/threadgraph) — Go concurrency debugger
`distributed systems` · `observability` · `static analysis` · `Go`

Detects **goroutine leaks and deadlocks** from Go execution traces — no instrumentation, no code
changes. Reconstructs goroutine provenance and runs leak, lock-cycle, channel-lock, orphan, and
static-release analyses over the blocked runtime state that ordinary tests never reach.

> **94% on GoBench GoKer — 64/68 real production bugs** · **0 false positives** on a 224-goroutine
> `net/http/httptest` control.

---

### [palimp](https://github.com/Heman10x-NGU/palimp) — agent memory & context engineering
`context engineering` · `agent memory` · `knowledge graph` · `provenance` · `MCP`

Local-first **context graph for AI agents**. Most memory layers help an agent remember; Palimp helps
it remember *safely*. Every fact is namespace-scoped, **source-linked with provenance**, temporally
versioned (`valid_from` / `valid_until` / `as_of`), and returned as data — **never as hidden
instruction** (`treat_as_instruction: false`).

> **2–3 hop** graph recall with depth decay · **token-budgeted** retrieval · contradiction tracking ·
> **8 MCP tools** · one inspectable SQLite file, zero external dependencies.

---

### [router-outcome-ledger](https://github.com/Heman10x-NGU/router-outcome-ledger) — eval harness
`evals` · `LLM evaluation` · `cost optimization` · `observability` · `deterministic replay`

An **evaluation harness for model-routing decisions**. A router reports gross savings from picking a
cheaper model; that number says nothing about whether the request survived invalid tool calls,
retries, failovers, or loop escalations. Ledger mines those **failure signals** from redacted
telemetry, HMAC-pseudonymises identities, records Git/CI provenance, and **deterministically replays**
content-free routing envelopes.

> **45/45 tests** across privacy validation, telemetry mining, provenance, replay, and CLI ·
> **stores no prompts** · reports recovery rows as correlated candidates, never as proven causation.

---

### [context-rag](https://github.com/Heman10x-NGU/context-rag) — RAG / hybrid retrieval
`RAG` · `hybrid search` · `embeddings` · `reranking` · `retrieval` · `MCP`

Local-first **RAG pipeline** for agent context: dense embeddings **plus BM25**, fused with
**reciprocal-rank fusion**, optional **FlashRank cross-encoder reranking**, HyDE query expansion,
and incremental hash-based reindexing. Explicit data roots — it never scans your home directory,
and the corpus never leaves your machine.

> **6 MCP tools** for collection and cross-collection search · every result returns a cited local
> source path and timestamp · two independent ranking signals fused before reranking.

---

### [hallucination-sentinel](https://github.com/Heman10x-NGU/hallucination-sentinel) — LLM guardrails
`LLM guardrails` · `evals` · `uncertainty quantification` · `calibration` · `logprobs`

**Single-pass uncertainty firewall** for LLM output. Computes per-token Shannon entropy from provider
**logprobs**, scores it against a **calibrated** reference distribution (CES, Villani et al. 2026),
and returns a risk level a **policy engine routes to allow / warn / block**. Uses probabilities the
provider already emits — no second judge-model call.

> **1 generation pass**, not 2 · calibrated thresholds kept separate from raw scores · CLI, MCP, and
> RAG-guardrail surfaces. **A risk signal, not a truth oracle** — confident falsehoods still score low.

---

## Also public

**[agent-board](https://github.com/Heman10x-NGU/agent-board)** — `agent orchestration`
`multi-agent systems`. A multi-agent control loop where an executor can never commit its own work:
a planner writes tasks to a board, executors claim and build, and an orchestrator **reviews every
result**. `TODO → IN_PROGRESS → IN_REVIEW → DONE`, failed reviews re-queued with a concrete fix note,
bounded retries before `ABANDONED`. ~150 lines, standard library only.

**[agent-atlas-trust-audit](https://github.com/Heman10x-NGU/agent-atlas-trust-audit)** — `evaluation`
`provenance` `audit trail`. Deterministic **claim-to-evidence audit engine**: extracts every claim
from a document, traces it to local source packets, **hard-stops on contradictions** instead of
averaging them away, and exports a **replayable audit bundle** with SHA-256 fingerprints. 8/8 tests.

**[NexusCache](https://github.com/Heman10x-NGU/NexusCache)** — `distributed systems` `caching`
`gRPC` `observability`. Distributed Go cache: consistent hashing, etcd discovery, singleflight
stampede control, Prometheus metrics. **23.4K ops/s at 713 µs p50**, 3-node cluster.

**[TitanQueue](https://github.com/Heman10x-NGU/TitanQueue)** — `distributed systems` `Redis`.
Fault-tolerant task queue: at-least-once delivery, lease-expiry recovery, priorities, retries,
uniqueness, graceful shutdown.

**[unslop](https://github.com/Heman10x-NGU/unslop)** — `prompt engineering` `agent skills`.
An agent skill that strips AI tells from prose without inventing facts to replace vague ones.

## AI Research — results

**[still-mini-kv-compactor](https://github.com/Heman10x-NGU/still-mini-kv-compactor)** —
`KV cache` `long context` `inference optimization`. Trained a 1.3M-param Perceiver KV compactor
against a frozen Qwen2.5-0.5B teacher. At 8× compression it landed at **0.12 retrieval accuracy vs
0.54 for plain sink+recent**. The write-up isolates *why*: compacting in rotated (RoPE) key space
destroys the positional geometry queries retrieve against.

**[dag-moe-reproduction](https://github.com/Heman10x-NGU/dag-moe-reproduction)** —
`mixture of experts` `reproducibility`. DAG-MoE (ICML 2026) on an M4. Mechanism verified;
**7.64 val loss vs 7.59 matched baseline** — a null result, and an argument for why laptop scale
can't test the paper's actual claim.
