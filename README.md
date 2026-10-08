<div align="center">

<img src="assets/header.svg" alt="Asha Jyothi Boddu, AI/ML and Backend Engineer" width="100%"/>

<br/>

[![Resume](https://img.shields.io/badge/Resume-PDF-f472b6?style=for-the-badge&logo=readthedocs&logoColor=white)](AshaJyothi_Resume.pdf)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/asha-jyothi-b4186428a)
[![Email](https://img.shields.io/badge/Email-Say_hi-ea4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ashajyothi0509@gmail.com)
![Open to](https://img.shields.io/badge/Open_to-AI%2FML_%C2%B7_Backend_%C2%B7_Full--stack_internships-34d399?style=for-the-badge)

**B.Tech CS (AI & ML) · BVRIT Hyderabad · 2023 – 2027 · CGPA 8.80**

</div>

<br/>

> **I build AI systems you can check, not just demo.** Every project below is deployed, has a test suite, a published evaluation and an honest write-up of what did not work. Models write the words; plain, tested code makes the decisions that have to be right.

<br/>

## ⚡ By the numbers

<div align="center">
<img src="assets/stats.svg" alt="50% fewer attempts, 0.93 recall, 31 of 32 mutants killed, 100% of red-flag cases caught" width="100%"/>
</div>

<sub>Retry Budget Allocator numbers are measured under a stated outcome model on simulated payments, and VidyutDrishti on simulated networks. They show how well a scarce budget is spent, not real-world recovery rates. Each repo's write-up says so.</sub>

<br/>

## 🚀 Flagship projects

Each app is live and opens with a built-in guided tour of every page.

<table>
<tr>
<td width="33%" valign="top" align="center">
<a href="https://retry-allocator.onrender.com"><img src="assets/retry.png" alt="Retry Budget Allocator landing page"/></a>
<h3>Retry Budget Allocator</h3>
<sub><b>Spend 3 retries on purpose</b></sub><br/><br/>
<a href="https://retry-allocator.onrender.com"><img src="https://img.shields.io/badge/Live-demo-22d3ee?style=flat-square"/></a>
<a href="https://github.com/Asha0509/retry-budget-allocator"><img src="https://img.shields.io/badge/Source-GitHub-181717?style=flat-square&logo=github"/></a>
</td>
<td width="33%" valign="top" align="center">
<a href="https://vidyutdrishti.onrender.com"><img src="assets/atc.png" alt="VidyutDrishti landing page"/></a>
<h3>VidyutDrishti</h3>
<sub><b>Find the meter hiding the missing energy</b></sub><br/><br/>
<a href="https://vidyutdrishti.onrender.com"><img src="https://img.shields.io/badge/Live-demo-a78bfa?style=flat-square"/></a>
<a href="https://github.com/Asha0509/VidyutDrishti"><img src="https://img.shields.io/badge/Source-GitHub-181717?style=flat-square&logo=github"/></a>
</td>
<td width="33%" valign="top" align="center">
<a href="https://healthai-triage.onrender.com"><img src="assets/healthai.png" alt="HealthAI emergency result page"/></a>
<h3>HealthAI Triage</h3>
<sub><b>An agent that can never downgrade an emergency</b></sub><br/><br/>
<a href="https://healthai-triage.onrender.com"><img src="https://img.shields.io/badge/Live-demo-34d399?style=flat-square"/></a>
<a href="https://github.com/Asha0509/HealthCare"><img src="https://img.shields.io/badge/Source-GitHub-181717?style=flat-square&logo=github"/></a>
</td>
</tr>
</table>

### 🔁 Retry Budget Allocator
When a UPI AutoPay payment fails, the rules allow only three more tries. This decides how to spend them: **ask the customer, retry at a legal time, or stop early.**
- **50% fewer attempts** than a fixed schedule (70 vs 141), **0 wasted**, **0 rule violations**. It also reports where it loses: 30 vs 35 recoveries, and it only wins on money above Rs 147.82 per attempt.
- Cause, timing and stop are **deterministic and enforced by an AST test**; the model only writes customer wording, with a template fallback.
- Pandera data contract · **mutation testing (31/32 killed)** · 1,200+ property-based cases · CodeQL · CI gates that fail on any violation.

`Python` `FastAPI` `Pydantic` `Pandera` `React` `Tailwind` `mutmut` `Hypothesis` `GitHub Actions`

### ⚡ VidyutDrishti: AT&C Loss Detection
Finds likely electricity theft and metering loss, then ranks inspections by the money they would recover.
- **4 independent checks** (transformer balance, own history, peers, Isolation Forest). On 20 unseen networks: **0.82 precision · 0.93 recall · F1 0.87**, with recall gated in CI.
- Tool-calling **copilot**, inspection-brief agent and smart alerts, on Groq → NVIDIA NIM → rules failover. Every number comes from read-only tools (**0 invented meter ids**).
- An **MCP server** exposes the 8 tools to any MCP client, plus an LLM observability page.
- Simulator checked against **real London smart-meter data** (realism 61% → 84%); forecaster benchmarked on real feeders (MASE 1.52 → 0.83).

`Python` `FastAPI` `scikit-learn` `React` `TypeScript` `TanStack Query` `Groq` `NVIDIA NIM` `MCP`

### 🩺 HealthAI: Triage Agent with Safety Evals
A symptom-triage agent over a RAG knowledge base, built so a model error cannot make an emergency look safe.
- Red-flag rules **can only raise a level**, and the model's free-text advice is ignored in favour of a fixed table with the emergency number.
- **60-case eval gated in CI**: rules alone catch **100% of red-flag cases and 85% of all emergencies**; the 2 misses are published.
- Hybrid retrieval, provider failover, an Ops page logging every model call, and an optional conformal-prediction second opinion (escalate-only) behind an adapter for external decision models (e.g. Jev, Laya). **135 tests** run with no network.

`Python` `FastAPI` `React` `RAG` `Groq` `NVIDIA NIM` `SQLite` `GitHub Actions`

<br/>

## 🧠 How I think about AI systems

<div align="center">
<img src="assets/pipeline.svg" alt="Animated pipeline: six deterministic stages and one model call" width="100%"/>
</div>

1. **Deterministic where it must be right.** Anything about money, safety or rules is plain code with tests.
2. **Models where they add value.** Explaining, summarising and answering, always with a fallback.
3. **Prove it.** Evals, mutation tests, CI gates, and a "what did not work" section.

<br/>

## 🛠️ Toolbox

<div align="center">
<img src="assets/skills.svg" alt="Scrolling list of technologies" width="100%"/>
</div>

| | |
|---|---|
| **Languages** | Python · Java · JavaScript · TypeScript · C · SQL |
| **Web & APIs** | FastAPI · Flask · Spring Boot · React · Vite · Tailwind · Next.js · TanStack Query · Pydantic · Pandera · SQLAlchemy |
| **ML / AI** | LLM tool-calling agents · RAG · MCP · conformal prediction · Isolation Forest · scikit-learn · XGBoost · TensorFlow · OpenCV · MediaPipe · Prophet · Chronos |
| **Quality & DevOps** | pytest · Hypothesis · mutmut · ruff · GitHub Actions · CodeQL · Dependabot · OpenSSF Scorecard · Docker · Render · Azure |
| **Data** | PostgreSQL · MySQL · SQLite · ChromaDB · Pandas · NumPy |

<br/>

## 🏆 Recognition & leadership

| | |
|---|---|
| 🥇 **Code by Groww 2026** | Finalist, one of 9 out of 2,900+ registrations (project: [Since](https://github.com/Asha0509/Groww_Hackathon), a smart market watchlist) |
| 🛒 **Flipkart GRiD 8.0** | Round 3 qualifier, top 0.5% of 400,000+ applicants |
| ☀️ **SAP Hackfest 2024** | Semifinalist |
| 💻 **CodeChef 3-Star** | 850+ problems solved across LeetCode, CodeChef and Codeforces |
| 📄 **ICIARD 2024, Thailand** | Presented *Significance of Emergent Technologies in Teaching Learning Processes* |
| 🎓 **Mentorship & leadership programs** | Ananya's Atlassian Mentorship (DSA and backend) · Aspire Leaders Program (Aspire Institute, Harvard-affiliated) |
| 🤖 **A.S.P.I.R.E** | Co-founder and Joint Secretary of BVRIT Hyderabad's first student-led AI/ML club: 9 events, workshops for 100+ students, a 200+ participant inter-college competition |

<details>
<summary><b>More projects</b></summary>

- **[A2S – Aesthetics To Spaces](https://github.com/AestheticsToSpaces/A2S_Beta)**: AI interior-design platform. React, Spring Boot and a Python LLM service, 28,000+ products from 7 scrapers, a Gemini multi-agent system, Docker and Azure CI/CD.
- **[NexusDocs](https://github.com/Asha0509/Nexus_Docs)**: RAG document Q&A with source citations. FastAPI, LangChain, ChromaDB, Next.js.
- **[YogaAlign](https://github.com/Asha0509/YogaAlign)**: real-time yoga pose classification, 92% accuracy across 15 poses and 30% lower frame latency (AptPath internship). Flask, OpenCV, MediaPipe.

</details>

<br/>

## 📊 GitHub

<div align="center">
<img src="https://github-readme-stats.vercel.app/api?username=Asha0509&theme=tokyonight&hide_border=true&include_all_commits=false&count_private=false" height="165"/>
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Asha0509&theme=tokyonight&hide_border=true&layout=compact" height="165"/>
<br/>
<img src="https://nirzak-streak-stats.vercel.app/?user=Asha0509&theme=tokyonight&hide_border=true" height="165"/>
</div>

<img src="assets/footer.svg" alt="" width="100%"/>
