# Python backend / AI engineer

I build backend services, AI pipelines and internal tools: FastAPI and PostgreSQL on the
service side, LLM agents where they earn their place, Docker Compose for everything that has to
run somewhere.

**Core stack:** Python · FastAPI · PostgreSQL · SQLAlchemy · Docker · LLM APIs · integrations · pytest

## Selected work

**[mtbank-ai-call-analytics](https://github.com/bigidulka/mtbank-ai-call-analytics)** — call
analytics service: local ASR and diarization, four bounded LLM agents, deterministic scoring
and grounding, OpenWebUI Pipeline plus REST, 577 offline tests.

**[crypto-payment-gateway](https://github.com/bigidulka/crypto-payment-gateway)** — payment
service: invoices and hosted checkout, merchant API and Python SDK, signed webhooks with
retries, deposit-address leases, chain confirmations, sweeping, and an append-only ledger that
the runtime database role cannot alter.

**[balance-tracker](https://github.com/bigidulka/balance-tracker)** — multi-tenant crypto
portfolio tracker: exchange balances via CCXT and on-chain wallets, integrity checks before
any write, a refresh pipeline with caching and circuit breakers, REST API plus a Telegram bot
with plan limits. 280 tests run offline.

**[tg-radar](https://github.com/bigidulka/tg-radar)** — index of public Telegram channels:
keyword and graph discovery, `t.me/s` crawling, PostgreSQL state, Vespa hybrid retrieval
(BM25 + HNSW) with a PostgreSQL full-text fallback, FastAPI surface for agents.

**[rag-tender-sql](https://github.com/bigidulka/rag-tender-sql)** — a RAG service that runs
without API keys (local embeddings, extractive answers with citations) next to a PostgreSQL
tender-platform schema where integrity rules and analytical SQL live in the database.

## What I care about

- Fail-closed contracts: a model response that does not match its schema should break the run,
  not silently degrade it.
- Deterministic checks around probabilistic parts: scores, money and permissions are computed
  by code, not by an LLM.
- Reproducible local runs: each project above starts or demos without my credentials.
