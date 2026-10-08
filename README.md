![Chaitanya Sai — Applied AI Engineer](assets/github-profile-header.png)

# Chaitanya Sai

### Applied AI Engineer | Agentic AI · RAG · AI Platform & Backend · Python & FastAPI

[![Portfolio](https://img.shields.io/badge/Portfolio-111827?style=flat-square&logo=vercel&logoColor=white)](https://chaitanya-sai-portfolio.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chaitanyaai-careers/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:chaitanya.careerpaths@gmail.com)

I’m a software engineer with **3+ years of experience across enterprise and regulated pharmaceutical systems**, now focused on production-oriented Applied AI.

Most of my recent work comes back to two engineering questions: **how do you let AI systems act without making model output the authority, and how do you make retrieval/generation measurable enough to trust?** That has led me into governed agent workflows, hybrid RAG, AI backends, evaluation, observability, identity/security, and full-stack AI products.

My earlier work was in Python/SQL data workflows, enterprise search, document processing, ETL, validation, and regulated software. I use that systems background when building AI features that still need clear state, permissions, failure handling, testing, and recovery.

---

## Engineering Focus

- **Agentic AI & Orchestration** — LangGraph typed-state workflows, multi-agent routing, human approvals, policy gates, MCP tool/context integration, checkpointing, rollback and recovery
- **Retrieval & RAG** — BM25 + PostgreSQL/pgvector hybrid retrieval, HNSW/IVFFlat, query rewriting, metadata filtering, caching, reranking, citations and retrieval evaluation
- **AI Platform & Backend** — Python, async FastAPI, Pydantic, SSE/WebSockets, PostgreSQL, Redis, Kafka, service boundaries and asynchronous execution
- **LLM Runtime** — LiteLLM routing across AWS Bedrock, Anthropic, OpenAI and Ollama, provider failover, structured outputs and token/cost tracing
- **Identity, Security & Governance** — OAuth2/OIDC/JWT, RBAC, SSO-ready patterns, AWS IAM/Secrets Manager, human-in-the-loop controls, PII protection and audit lineage
- **Observability & Delivery** — Langfuse, OpenTelemetry, CloudWatch, Docker, Kubernetes, Helm, Terraform, GitHub Actions and CI/CD
- **Regulated Systems** — pharmaceutical software, GxP, 21 CFR Part 11, ALCOA+, QMS, CAPA, deviations, change control and traceability

---

## Verified Engineering Signals

| Area | Evidence |
|---|---|
| **Agentic AI** | **94.8% task completion** across evaluation suites · **3,950+ passing regression tests** in the broader implementation |
| **RAG / Retrieval** | **91.4% Recall@10 · 0.86 MRR · 0.89 NDCG** |
| **Retrieval performance** | **140 ms P50 retrieval · <420 ms P95 end-to-end** |
| **PharmaAI corpus** | **1,000+ pages · 200 openFDA validation records** |
| **Public engineering evidence** | **66 automated tests across six public showcases with GitHub Actions CI** |
| **Job Copilot** | **11-entity relational source-of-truth model · 19 Vitest cases across 7 files** |

---

## Flagship Engineering

### [Agentic AI Platform](https://github.com/chaitanyaAI-careers/Agentic-ai-platform)

**Problem:** an agent proposing an action should not automatically mean the machine is allowed to execute it.

The broader implementation separates planning, authorization, execution, validation and recovery across LangGraph Planner/Coder/Reviewer/Tester workflows. Higher-risk actions can pause for approval; MCP tool discovery is separate from tool permission; durable checkpoints and rollback make interrupted runs recoverable.

**Current engineering:** LangGraph typed state, MCP JSON-RPC, PostgreSQL workflow state, LiteLLM routing, Redis/Kafka asynchronous execution, OAuth2/OIDC/JWT, Langfuse/OpenTelemetry, FastAPI, Terraform and Kubernetes/Helm on AWS.

**Measured signal:** 94.8% task completion with 3,950+ passing regression tests.

### [Pharma AI Platform](https://github.com/chaitanyaAI-careers/Pharma-ai-platform)

**Problem:** semantic similarity can return text that is related to a regulatory question without returning the evidence that actually answers it.

The retrieval pipeline combines BM25 + PostgreSQL/pgvector hybrid search, HNSW/IVFFlat indexing, query rewriting, metadata filtering, Redis caching and reranking. Bedrock-backed generation stays downstream of retrieved evidence and ties answers back to stable citations.

**Measured signal:** 91.4% Recall@10 · 0.86 MRR · 0.89 NDCG · 140 ms P50 retrieval · <420 ms P95 end-to-end across a 1,000+ page corpus and 200 openFDA validation records.

### [Job Copilot](https://github.com/chaitanyaAI-careers/Job-copilot)

**Problem:** AI can help with matching and preparation, but it should not silently become the source of truth for application state or add unsupported resume claims.

The product keeps an 11-entity relational model and deterministic rules authoritative for freshness, deduplication and workflow transitions, while pgvector adds semantic matching and LiteLLM-backed AI assistance stays behind observable service boundaries.

**Engineering:** Next.js/TypeScript, FastAPI, Prisma/PostgreSQL/pgvector, Redis/Kafka, OAuth2/OIDC/JWT, Vercel and AWS delivery. **19 Vitest cases across 7 files.**

### [HR AI Content System](https://github.com/chaitanyaAI-careers/HR-ai-content-system)

**Problem:** a document can be relevant to a query and still be the wrong information to show a particular requester.

Governed retrieval using SentenceTransformer embeddings, deterministic chunking/metadata, role-conditioned PII controls and grounded extractive answers. **17 tests**, a **21-question evaluation set**, and **10 policy areas**. The public build intentionally does not claim full RBAC-aware retrieval.

### [Medicine Verification Service](https://github.com/chaitanyaAI-careers/Medicine-verification-platform)

**Problem:** finding a regulatory record does not prove that a physical medicine package is authentic.

The API therefore reports only what it can actually know: **matched, not found, or ambiguous**. FastAPI/Pydantic service with explicit API/service/source/repository boundaries, synthetic in-memory adapters, **2 endpoints** and **7 tests**.

### [Nudge](https://github.com/chaitanyaAI-careers/Nudge)

Workflow-reliability showcase built around explicit lifecycle states, idempotency requirements and controlled transitions. The public build models **PENDING / QUEUED / COMPLETED / FAILED** with **8 tests**; scheduler/worker runtime and notification delivery are intentionally outside the current scope.

---

## Evidence Model

The public repositories are intentionally recruiter-safe showcases. I distinguish:

- **Public implementation** — code and tests directly inspectable in these repositories
- **Verified broader implementation** — implemented engineering maintained outside the smaller public showcases
- **In progress / platform direction** — capabilities not represented as completed until supported by reproducible evidence

That distinction is deliberate: the portfolio should make the engineering inspectable without overstating what a public repository contains.

---

## Core Technologies

**AI / LLM:** Generative AI · LLM applications · LangGraph · MCP · LiteLLM · AWS Bedrock · Anthropic · OpenAI · Ollama · structured outputs

**Retrieval:** RAG · BM25 · PostgreSQL/pgvector · SentenceTransformers · HNSW · IVFFlat · metadata filtering · reranking · citations · retrieval evaluation

**Backend / Data:** Python · async FastAPI · Pydantic · PostgreSQL · SQLAlchemy · Prisma · Redis · Kafka · REST · SSE · WebSockets

**Security / Observability:** OAuth2 · OIDC · JWT · RBAC · AWS IAM · Secrets Manager · Langfuse · OpenTelemetry · CloudWatch

**Cloud / DevOps:** Docker · Kubernetes · Helm · Terraform · GitHub Actions · AWS · Vercel

**Product:** TypeScript · React · Next.js · full-stack AI workflows · deterministic policy + AI-assisted services

---

## Professional Direction

I’m targeting roles across **Applied AI Engineering, Agentic AI, Generative AI / LLM Applications, RAG / Retrieval, AI Platform & Backend Engineering, AI Product Engineering, AI Solutions / Forward-Deployed AI, and AI Evaluation & Governance**.

**Texas, USA · Open to Remote, Hybrid & Relocation**

---

## Connect

[![Portfolio](https://img.shields.io/badge/Portfolio-111827?style=flat-square&logo=vercel&logoColor=white)](https://chaitanya-sai-portfolio.vercel.app)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/chaitanyaAI-careers)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chaitanyaai-careers/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:chaitanya.careerpaths@gmail.com)
