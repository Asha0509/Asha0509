# Asha Jyothi Boddu

**AI/ML & Backend Engineer · B.Tech CS (AI & ML) @ BVRIT Hyderabad · 2023 – 2027 · CGPA 8.80**

📄 [Resume (PDF)](AshaJyothi_Resume.pdf) &nbsp;·&nbsp; 💼 [LinkedIn](https://linkedin.com/in/asha-jyothi-b4186428a) &nbsp;·&nbsp; 📬 ashajyothi0509@gmail.com

---

## About

I build AI systems that can be checked, not just demoed. My recent projects are all deployed, each with a test suite, a published evaluation and a plain write-up of what did not work. I put models where they add value (explaining, summarising, answering) and keep decisions that must be right in plain, testable code, with a safe fallback when a model is down.

Outside of building, I co-founded A.S.P.I.R.E, BVRIT Hyderabad's first student AI/ML club (9 events, workshops for 100+ students), presented a paper at an international conference in Thailand, and am a mentee in Ananya's Atlassian Mentorship Program (scalable distributed systems and backend design).

I'm looking for **AI/ML engineering**, **backend** or **full-stack** internships and entry-level roles.

---

## Featured projects

Every project below is live, and each app has a built-in guided tour of its pages. Numbers come from the repositories' own evaluation harnesses.

### [Retry Budget Allocator](https://github.com/Asha0509/retry-budget-allocator) · [Live](https://retry-allocator.onrender.com)
*September 2026*

When a UPI AutoPay payment fails, the rules allow only three more tries. This decides how to spend them: ask the customer, retry at a chosen legal time, or stop early.

- **50% fewer attempts** than a fixed schedule (70 vs 141) with **0 wasted attempts** and **0 rule violations**, under a stated, published outcome model. It reports where it loses: 30 vs 35 recoveries, and it only wins on money above Rs 147.82 per attempt.
- The model never decides: failure cause, timing and stop are deterministic, enforced by an AST test; the model only writes the customer-facing wording, with a template fallback.
- Pandera data contract, **mutation testing (31/32 mutants killed)**, property-based fuzzing (1200+ cases), CodeQL and CI gates that fail on any violation.

**Stack:** Python · FastAPI · Pydantic · Pandera · React · Tailwind · mutmut · Hypothesis · GitHub Actions

---

### [VidyutDrishti – AT&C Loss Detection](https://github.com/Asha0509/VidyutDrishti) · [Live](https://vidyutdrishti.onrender.com)
*May 2026*

Finds likely electricity theft and metering loss on a distribution network and ranks inspections by the money they would recover.

- 4-layer detection (transformer energy balance, own-history baseline, peer comparison, Isolation Forest). On 20 unseen simulated networks: **0.82 precision, 0.93 recall, F1 0.87**, recall gated in CI.
- Tool-calling **copilot**, inspection-brief agent and smart alerts. Groq with NVIDIA NIM failover and a rule-based fallback; every number comes from read-only tools (0 invented meter ids in the eval).
- **MCP server** exposing the 8 read-only tools to any MCP client, plus an LLM observability page.
- Checked the simulator against real London smart-meter data (realism 61% → 84%) and benchmarked forecasters on real feeders (MASE 1.52 → 0.83).

**Stack:** Python · FastAPI · scikit-learn · Pandas · React · TypeScript · TanStack Query · Groq · NVIDIA NIM · MCP

---

### [HealthAI – Triage Agent with Safety Evals](https://github.com/Asha0509/HealthCare) · [Live](https://healthai-triage.onrender.com)
*August 2026*

A symptom-triage agent over a RAG knowledge base, built so a model error cannot downgrade an emergency.

- Deterministic red-flag rules **can only raise a level**; the model's free-text action is ignored in favour of a fixed table with the emergency number.
- 60-case eval harness gated in CI on missed emergencies: rules-only baseline catches **100% of red-flag cases and 85% of all emergencies**, and the 2 misses are reported.
- Hybrid retrieval (dense + keyword), Groq/NIM failover, an Ops page logging every model call, and an optional conformal-prediction second opinion (escalate-only) behind a provider-agnostic adapter for external decision models (e.g. Jev, Laya). 135 tests with a fake LLM transport, so CI never needs a key.

**Stack:** Python · FastAPI · React · RAG (model2vec) · Groq / NVIDIA NIM · SQLite · GitHub Actions

---

### [Since – Smart Market Watchlist](https://github.com/Asha0509/Groww_Hackathon)
*September 2026 · Code by Groww 2026 finalist (9 of 2,900+ registrations)*

A watchlist that shows only what meaningfully changed since you last looked, using per-user, per-instrument watermarks that survive restarts.

- Corporate-action adjustment: a 1:10 split reads −0.1% instead of a false −90%; five per-instrument session states tell a closed market from a dead feed.
- Shared per-instrument ingest costs 14 ms once vs 14 s if recomputed per user (3,000 instruments × 1,000 users); 52-test suite.

**Stack:** Python · FastAPI · SQLite · pytest · HTML/CSS/JavaScript

---

### More work

- **[A2S – Aesthetics To Spaces](https://github.com/AestheticsToSpaces/A2S_Beta)** (Dec 2025 – present): AI interior-design platform; React, Spring Boot, Python LLM service, 28,000+ products from 7 scrapers, Gemini multi-agent system, Docker and Azure CI/CD.
- **[NexusDocs](https://github.com/Asha0509/Nexus_Docs)** (Mar 2026): RAG document Q&A with source citations; FastAPI, LangChain, ChromaDB, Next.js.
- **[YogaAlign](https://github.com/Asha0509/YogaAlign)** (Jul – Aug 2025, AptPath internship): real-time pose classification, 92% accuracy across 15 poses and 30% lower frame latency; Flask, OpenCV, MediaPipe.

> **How to read the numbers:** results for the first two projects are from simulated data and test-mode outcomes I authored, so they measure how well a scarce budget is spent under a stated model, not real-world recovery rates. Each repository's README says so and links its full results write-up, including what did not work.

---

## Skills

| Category | Technologies |
|---|---|
| **Languages** | Python · Java · JavaScript · TypeScript · C · SQL |
| **Frontend** | React · Vite · Tailwind CSS · TanStack Query · Next.js · Three.js |
| **Backend** | FastAPI · Flask · Spring Boot · Pydantic · Pandera · SQLAlchemy · Node.js |
| **ML / Data** | scikit-learn · XGBoost · TensorFlow · OpenCV · MediaPipe · NumPy · Pandas · Isolation Forest · Prophet · Chronos |
| **LLM / AI** | Tool-calling agents · RAG · Model Context Protocol (MCP) · LangChain · Groq · NVIDIA NIM · OpenRouter · conformal prediction · Jev · Laya · evaluation harnesses |
| **Databases** | PostgreSQL · MySQL · SQLite · ChromaDB |
| **DevOps** | Git · GitHub Actions (CI/CD) · CodeQL · Dependabot · OpenSSF Scorecard · Docker · Render · Azure |
| **Testing** | pytest · Hypothesis (property-based) · mutmut (mutation testing) · pytest-asyncio · Vitest · ruff |
| **Concepts** | DSA · OOP · Distributed Systems · LLM evaluation & guardrails · Provider failover · Hybrid retrieval · UPI payments · Observability |

---

## Research & recognition

- 🏆 **Code by Groww 2026:** finalist, one of 9 out of 2,900+ registrations
- 🏆 **Flipkart GRiD 8.0:** Round 3 qualifier, top 0.5% of 400,000+ applicants
- 🏆 **SAP Hackfest 2024:** semifinalist
- 💻 **CodeChef 3-Star**, 850+ problems solved across LeetCode, CodeChef and Codeforces
- 📄 **ICIARD 2024:** presented *Significance of Emergent Technologies in Teaching Learning Processes*, Metarath University, Thailand (Feb 2024)
- 🎓 **Aspire Leaders Program** (Aspire Institute, Harvard-affiliated), completed March 2025
- 🎓 **Ananya's Atlassian Mentorship Program:** DSA and backend track, Nov 2025 – May 2026

---

## Leadership

**Founding Member & Joint Secretary, A.S.P.I.R.E** *(2024 – present)*: first student-led AI/ML club at BVRIT Hyderabad. Led workshops reaching 100+ students and organised 9 events, including an inter-college competition with 200+ participants (2025, 2026).

---

## GitHub stats

<p align="left">
  <img src="https://github-readme-stats.vercel.app/api?username=Asha0509&theme=default&hide_border=true&include_all_commits=false&count_private=false" height="150"/>
  &nbsp;&nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Asha0509&theme=default&hide_border=true&layout=compact" height="150"/>
</p>

<img src="https://nirzak-streak-stats.vercel.app/?user=Asha0509&theme=default&hide_border=true" height="150"/>
