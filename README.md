# AI Engineer — Regulated Finance + Agentic Systems

I build production agentic AI for regulated financial workflows.
Based in Seoul. Currently at a Korean bond valuation firm.

---

## Recent production work

**Term-sheet extraction & validation** — OCR → SQL Server comparison across
89 fields × 410 derivative products. Lifted raw accuracy from **71.4% → 94.5%**
via multi-stage constraint + NULL inference engines. OQS **92.52% [A grade]**.

**8-layer ML defense for daily coupon validation** — Consensus, Archive Prior,
Hampel+STL, LSTM-VAE, HistGBR, Walk-Forward drift, HMM regime, RAG oracle
(ChromaDB + multilingual SBERT over 470 ground-truth descriptions). Detects
silent parser bugs that engine+verifier cross-checks miss, in **under 1 second**
(previously 20 minutes of manual debugging).

**Bond-anomaly detection with Google TimesFM 2.5** — 6-axis / 7-detector /
11 analytical perspectives. Fully on-prem (regulatory constraint).
Internal AI competition entry.

**ARTPLEX e-commerce platform** — 22,815 products, 99.8% IP classification,
86.2% character matching over 2,800+ master DB. Genkit + Gemini multi-agent
marketing, 3 Cloud Run microservices, 100% Shopify migration (22,711 products).

---

## Stack (production experience)

**Languages** — Python · TypeScript · VBA · Bash
**Frameworks** — FastAPI · Next.js 15 · Celery · Genkit · NautilusTrader
**Data** — PostgreSQL + pgvector · ChromaDB · SQL Server · TimescaleDB · Redis · Supabase · QuestDB
**AI** — Claude (API + Code) · Gemini · OpenAI · Ollama · MCP · Google ADK · LSTM-VAE · HMM · SBERT
**Cloud** — Google Cloud Run · Firebase · Palantir Foundry · Vercel
**Tooling** — Docker Compose · Turborepo · pnpm · Playwright · Selenium

---

## Philosophy

- **External verification > AI self-judgment** — external authority, not AI confidence, decides completion
- **Defense-in-depth > single source of truth** — multiple independent layers catch silent bugs
- **Documentation-first** — paired `CLAUDE.md` + `AGENTS.md` guides in 15+ repositories, enabling AI-native workflows

---

## About the pinned repos

Pinned repositories are **sanitized reference architectures** extracted from
proprietary production systems. Code patterns and evaluation frameworks are
public; domain-specific implementations available under NDA.

---

📍 Seoul · Open to AI Engineer / Senior AI Engineer roles
