<h1 align="center">Hi, I'm Shivansh Hingve 👋</h1>

<p align="center">
  <strong>Backend, Analytics &amp; AI Systems Engineer</strong><br>
  Fault-Tolerant Distributed Systems · High-Throughput Data Pipelines · Reproducible AI Evaluation
</p>

<p align="center">
  <a href="https://linkedin.com/in/shivansh-hingve-6a18a7258"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="https://codedebugarena-sf2pdj.v2.appdeploy.ai/"><img src="https://img.shields.io/badge/Live%20Benchmark-CodeDebugArena-EA580C?style=for-the-badge" alt="CodeDebugArena Live"/></a>
  <a href="https://huggingface.co/ShivanshSenpai"><img src="https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-ShivanshSenpai-FFD21F?style=for-the-badge" alt="Hugging Face"/></a>
  <a href="mailto:shivanshhingve@gmail.com"><img src="https://img.shields.io/badge/Email-shivanshhingve@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
</p>

---

## About

B.Tech in Computer Science (AI & ML), LNCT University (May 2026) · Pune, India · **Open to full-time Founding / Backend / AI Systems roles (relocation or remote)**.

I build production-grade distributed backends, PostgreSQL analytics pipelines, and reproducible evaluation infrastructure for AI systems. My recent work focuses on the core systems problems behind modern AI products:

- **Durable Multi-Step Orchestration & Saga Rollback** ([AdOrchestrator](https://github.com/ShivanshHingve2804/adorchestrator))
- **Race-Safe Concurrency & Distributed Locking** ([AdOrchestrator](https://github.com/ShivanshHingve2804/adorchestrator), [PayFlow](https://github.com/ShivanshHingve2804/PayFlow), [FlowGuard](https://github.com/ShivanshHingve2804/FlowGuard))
- **AI Agent Benchmarking & Deterministic Evaluation** ([CodeDebugArena](https://github.com/ShivanshHingve2804/CodeDebugArena), [RAG System](https://github.com/ShivanshHingve2804/RAG-Document-Analysis-System), [PyAudit](https://github.com/ShivanshHingve2804/PyAudit))

---

## Flagship Systems

### Distributed Backend & Analytics Engineering

| Project | Stack | Engineering Highlights |
|---|---|---|
| [**AdOrchestrator**](https://github.com/ShivanshHingve2804/adorchestrator) | Python · Django · Temporal · Celery · PostgreSQL 16 · Redis · RabbitMQ · Docker | **Fault-tolerant campaign orchestration & analytics engine.** Durable Temporal saga workflows across flaky platform simulators; two-layer Redis `SET NX` + PostgreSQL `SELECT FOR UPDATE` budget locking (proven in 20-thread races); UTC-day partitioned `AdEvent` table with concurrently refreshed materialized views (`1.26 ms` cold / `0.21 ms` warm on 25k events); Celery Beat anomaly auto-remediation; VLM/LLM creative correlation. **39 tests + live `SIGKILL` worker crash-recovery verified.** |
| [**PayFlow**](https://github.com/ShivanshHingve2804/PayFlow) | Python · FastAPI · SQLAlchemy · PostgreSQL 16 · Alembic · Kafka · Airflow · Docker | **ACID-compliant 8-currency fintech API (56 FX pairs).** Ordered `SELECT ... FOR UPDATE` row locking preventing AB-BA deadlocks (proven in 20-thread Postgres contention & overdraft races), SHA-256 idempotency fingerprinting (`409` conflict on payload mismatch), transactional Kafka/Redpanda outbox with PK-deduplicating consumer (`52/52` end-to-end verified; `24.18 ms` p50 HTTP transfer), and Airflow daily ledger reconciliation DAGs. **43 tests (`87.16%` coverage) + CI container build verified.** |
| [**FlowGuard**](https://github.com/ShivanshHingve2804/FlowGuard) | Python · FastAPI · Starlette ASGI · Redis 7 Lua · pytest · AsyncIO | **Thread-safe & Redis-distributed rate limiter.** Implements Token Bucket, Leaky Bucket, Sliding Window Log, and Sliding Window Counter with sync/async APIs, 64-stripe `CRC32` LRU sharding (`39.7k` QPS in-memory), atomic Redis 7 Lua scripts (`4.29k` QPS distributed), and pure ASGI middleware (`X-RateLimit-*`, HTTP 429 `Retry-After`, spoof-safe proxy handling). **32 tests (`89.58%` coverage) + live Redis contention verified.** |

### AI Evaluation, Retrieval & Developer Tooling

| Project | Stack | Engineering Highlights |
|---|---|---|
| [**CodeDebugArena**](https://github.com/ShivanshHingve2804/CodeDebugArena) ([Live](https://codedebugarena-sf2pdj.v2.appdeploy.ai/)) | Python · pytest · Docker · FastAPI | **Reproducible benchmark of 12 real-world Python bugs for AI coding agents.** Covers race conditions, IEEE 754 precision, iterator invalidation, and cache poisoning — each paired with verified ground-truth fixes, root-cause analyses, sandboxed Docker + Landlock execution, auto-graded pytest suites, and a live evaluation leaderboard. |
| [**RAG Document Analysis**](https://github.com/ShivanshHingve2804/RAG-Document-Analysis-System) | Python · LangChain · FAISS · Ollama · Streamlit | **Local, privacy-first RAG pipeline with quantitative evaluation.** Automated benchmark harness scoring ground-truth Q&A pairs via deterministic keyword coverage and semantic cosine similarity (`>90%` query relevance without cloud APIs). |
| [**PyAudit**](https://github.com/ShivanshHingve2804/PyAudit) | Python · AST · CLI | **Zero-dependency Python static code & security analyzer.** Inspects AST directly without executing target code across 20 bug, security, and code-quality rules built for frictionless CI gating. |

<details>
<summary><b>Additional Applied ML & Data Projects</b></summary>

- [**GPT-2 Instruction & Classification Fine-Tuning**](https://github.com/ShivanshHingve2804/Demo-Gpt2-small-Model-with-Instruction-and-Classification-Fine-Tuning) — PyTorch transformer fine-tuning on GPT-2 (124M) with cross-model output comparison against local Llama 3 via Ollama.
- [**Polymer Property Prediction (MPNN)**](https://github.com/ShivanshHingve2804/Polymer-property-prediction-model) — Multi-target Graph Neural Network (PyTorch Geometric) predicting 5 physical properties from SMILES molecular graphs.
- [**Real-Time Face Liveness Detection**](https://github.com/ShivanshHingve2804/Face_Liveness_Detection_using_CNN_and_EAR_or_MAR) — Hybrid CNN + Eye/Mouth Aspect Ratio pipeline distinguishing live faces from spoofs.

</details>

---

## Experience & Open Source

- **Data Analytics Process Automation Intern** · *AICTE-EduSkills / Alteryx SparkED (Remote, Jan–Mar 2025)* — Automated Python & Alteryx ETL workflows cutting manual processing time by ~35%.
- **Machine Learning Intern** · *8bit Warriors (Remote, Jan–Feb 2024)* — Built supervised/unsupervised `scikit-learn` models improving accuracy by ~18% and cutting preprocessing time by ~30%.
- **Open Source — `binance/binance-skills-hub`**: Contributed market anomaly detection AI-agent skill & documentation PRs ([#280](https://github.com/binance/binance-skills-hub/pull/280), [#281](https://github.com/binance/binance-skills-hub/pull/281)).

---

## Technical Stack

| Domain | Technologies |
|---|---|
| **Backend & Distributed Systems** | Python 3.12, Django / DRF, FastAPI, Temporal, Celery, RabbitMQ, Redis, Kafka, AsyncIO |
| **Databases & Analytics** | PostgreSQL 16 (partitioning, materialized views, `SELECT FOR UPDATE`), SQLAlchemy, SQL, Pandas, NumPy, Airflow |
| **AI, LLMs & Evaluation** | PyTorch, LangChain, FAISS, Ollama, OpenAI / Gemini APIs, RAG, VLM pipelines, reproducible agent benchmarks |
| **Infra & Quality** | Docker & Compose, GitHub Actions CI/CD, AWS ECS (Fargate), pytest, Ruff, Locust, k6 |

---

<p align="center">
  <i>Building reliable backends &amp; measurable AI systems — <a href="mailto:shivanshhingve@gmail.com">shivanshhingve@gmail.com</a></i>
</p>
