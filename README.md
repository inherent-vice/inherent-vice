# AI Engineer — Regulated Finance + Audit-Grade Agentic Systems

I build production AI systems where correctness is not a vibe: ground truth, audit trails, regression gates, and human oversight decide whether an agent is allowed to act.

**Current focus:** Fieldguide-aligned agentic evaluation for regulated finance — term-sheet extraction, coupon validation, anomaly detection, and operator workflows that survive audit review.

**Start here**

- Portfolio: https://portfolio-ten-alpha-57.vercel.app
- Public companion repo: https://github.com/inherent-vice/termsheet-extraction-eval
- LinkedIn: https://www.linkedin.com/in/hyeonuk-lee-9203b6308/
- GitHub: https://github.com/inherent-vice

---

## Flagship proof

### termsheet-extraction-eval — public companion to my Fieldguide application

Reference architecture for evaluating LLM-extracted structured financial data against synthetic ground truth.

- Deterministic mock extractor: no API key required for the main benchmark.
- Type-aware comparison: rate, numeric amount, date, spread, currency, enum, text.
- Constraint + NULL inference stages catch silent extraction failures.
- CI gate runs lint, tests, and v1/v2/v3 ablation on Python 3.10 / 3.11 / 3.12.
- Synthetic benchmark: 20 products × 18 fields; v1 89.2% → v3 99.4% match rate.

Repo: https://github.com/inherent-vice/termsheet-extraction-eval

---

## Recent production work

### AITF — term-sheet OCR validation at audit scale

Built and operated an OCR → SQL Server validation pipeline for structured derivative term sheets at Korea Asset Pricing.

- 89 fields × 410 products = 48,443 field comparisons in the core benchmark.
- Raw LLM/OCR extraction 71.4% → post-processed field accuracy 94.5%.
- OQS 92.52% [A], F1 96.71%, Cohen's κ 0.47, PABAK 0.84.
- 7-stage pipeline: extraction, type-aware comparison, cross-field constraints, NULL inference, post-processing, schedule checks, audit metrics.
- Final verification path used an external vision pass rather than AI self-judgment.

### CouponCheck — zero-code-change autoresearch loop

Daily swap + foreign-bond coupon validator with defense-in-depth around silent parser failures.

- 469/469 rows converged within 5bp on a 484-sample ground-truth benchmark.
- Research loop improved 98.08% → 99.57% → 100% without changing engine code.
- 8-layer validation stack: consensus, archive priors, Hampel/STL, LSTM-VAE, HistGBR, walk-forward checks, HMM regime logic, RAG oracle.
- Production alarm lifecycle store with review states and expiry semantics.

### Bond anomaly detection — regulated on-prem operations

Scaled a KRW/FX/swap/CDS anomaly stack into a daily-runnable operations product.

- 9.4M rows across parquet caches.
- 30+ orthogonal detectors and 17 pipeline stages.
- 88.6% false-positive reduction on KRW bonds.
- Fully on-prem path with local LLM explanation for regulatory constraints.
- Textual TUI and operations modules for desk triage, drift watching, reports, and incident snapshots.

---

## How I build

- **External verification > AI self-judgment** — independent ground truth or human review decides completion.
- **Evaluation before automation** — agents get replay fixtures, regression tests, and explicit pass/fail semantics before tools become writable.
- **Traceability by default** — every recovery rule should leave an audit trail.
- **Defense-in-depth** — multiple weaker independent checks beat one impressive black box.
- **NDA-safe public proof** — proprietary systems are represented through sanitized fixtures, reference architectures, and reproducible benchmarks.

---

## Stack

- Languages: Python, TypeScript, C#, VBA, Bash
- Backend/data: FastAPI, Flask, Celery, SQL Server, PostgreSQL, Redis, ChromaDB, BigQuery, QuestDB
- AI/ML: Claude, Gemini, OpenAI, Ollama/Gemma, Genkit, MCP, SBERT, HMM, LSTM-VAE, HistGBR, TimesFM, Matrix Profile, IForest
- Frontend/operator surfaces: Next.js, React, Textual, WinForms, Tkinter, Alpine.js
- Quality gates: pytest, ruff, mypy, golden-file regression, benchmark ablations, CI
- Cloud/devops: Google Cloud Run, Firebase, Vercel, Docker Compose, GitHub Actions

---

## Portfolio map

If you have 30 seconds:
1. Open the portfolio: https://portfolio-ten-alpha-57.vercel.app
2. Read the Mirror + Three Systems sections.
3. Run the companion repo benchmark: `python -m termsheet_eval.cli benchmark --version all`.

If you have 5 minutes:
- Inspect the `termsheet-extraction-eval` README, tests, CI workflow, and regression tests.
- Compare the v1/v2/v3 ablation results.
- Look for the design pattern: model output is only the beginning; audit-grade systems need evaluation, constraints, inference, and traceability.

---

Based in Seoul. Open to AI Engineer / Senior AI Engineer roles in audit, risk, financial infrastructure, and agentic evaluation systems.
