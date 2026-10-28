<div align="center">

<img src="assets/header.svg" alt="Hi, I'm Asha Jyothi Boddu. I make LLMs explain while plain code decides. Agents, RAG and evals, shipped live. Open to AI/ML and SDE internships, 2027. B.Tech CS (AI and ML), BVRIT Hyderabad, CGPA 8.80." width="100%"/>

<br/>

[![Resume](https://img.shields.io/badge/Resume-PDF-f472b6?style=for-the-badge&logo=readthedocs&logoColor=white)](AshaJyothi_Resume.pdf)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/asha-jyothi-b4186428a)
[![Email](https://img.shields.io/badge/Email-Say_hi-ea4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ashajyothi0509@gmail.com)
![Open to](https://img.shields.io/badge/Open_to-AI%2FML_%C2%B7_SDE_internships-34d399?style=for-the-badge)

</div>

<br/>

> **I build AI systems you can check, not just demo.** Every project below is deployed, has a test suite, a published evaluation and an honest write-up of what did not work. Models write the words; plain, tested code makes the decisions that have to be right.

<img src="assets/code.svg" width="100%" alt="asha.py: open to AI/ML and SDE roles in 2027. class Asha(Engineer) builds AI you can check. Stack: agents, RAG, MCP, evals, FastAPI, Spring Boot. Shipped Retry Allocator, VidyutDrishti and HealthAI. Research: Apart model-swap study. Wins: Code by Groww finalist, Flipkart GRiD top 0.5%. decide() uses deterministic tested rules; explain() uses an LLM with a template fallback. Running it prints 3 systems live, 0 rule violations, 0.93 recall, 100% red flags caught."/>

<br/>

## ⚡ By the numbers

<img src="assets/stats.svg" width="100%" alt="50% fewer attempts than a fixed schedule (70 vs 141), 0 wasted, 0 rule violations. 0.93 recall on theft, precision 0.82, F1 0.87 on 20 unseen networks. 31 of 32 mutants killed. 100% of red-flag cases caught in a 60-case safety eval."/>

<sub>Retry Budget Allocator numbers come from simulated payments under a stated outcome model, and VidyutDrishti's from simulated networks. They show how well each system decides, not real-world rates. Each repo's write-up says so.</sub>

<br/>

## 🚀 Flagship projects

Each app is live and opens with a built-in guided tour of every page.

### 🔁 Retry Budget Allocator &nbsp;·&nbsp; <sub>spend 3 retries on purpose</sub>

<table><tr>
<td width="56%" valign="top">
<a href="https://retry-allocator.onrender.com"><img src="assets/shot-retry.svg" alt="Retry Budget Allocator landing page" width="100%"/></a>
</td>
<td width="44%" valign="top">

**In plain words:** when a UPI AutoPay payment fails, the rules allow three more tries. This works out *why* it failed, then asks the customer, retries at a legal time, or stops.

- **50% fewer attempts** (70 vs 141), **0 wasted**, **0 rule violations**
- Reports where it loses: 30 vs 35 recoveries; wins on money only above ₹147.82/attempt
- Decisions **deterministic, enforced by an AST test**; LLM writes wording only
- Pandera contract · **mutation testing 31/32** · 1,200+ property-based cases · CodeQL

[![Live](https://img.shields.io/badge/Live-demo-22d3ee?style=flat-square)](https://retry-allocator.onrender.com) [![Code](https://img.shields.io/badge/Source-GitHub-181717?style=flat-square&logo=github)](https://github.com/Asha0509/retry-budget-allocator)

</td></tr></table>

`Python` `FastAPI` `Pydantic` `Pandera` `React` `Tailwind` `mutmut` `Hypothesis` `GitHub Actions`

### ⚡ VidyutDrishti &nbsp;·&nbsp; <sub>find the meter hiding the missing energy</sub>

<table><tr>
<td width="44%" valign="top">

**In plain words:** compares what each transformer sends out with what its homes' meters record, then tells inspectors which homes to visit first, ranked by rupees at stake.

- **4 independent checks**: transformer balance, own history, peers, Isolation Forest
- **0.82 precision · 0.93 recall · F1 0.87** on 20 unseen networks, recall gated in CI
- Tool-calling **copilot** + **MCP server** over 8 read-only tools (**0 invented meter ids**)
- Checked against **real London smart-meter data** (realism 61% → 84%)

[![Live](https://img.shields.io/badge/Live-demo-a78bfa?style=flat-square)](https://vidyutdrishti.onrender.com) [![Code](https://img.shields.io/badge/Source-GitHub-181717?style=flat-square&logo=github)](https://github.com/Asha0509/VidyutDrishti)

</td>
<td width="56%" valign="top">
<a href="https://vidyutdrishti.onrender.com"><img src="assets/shot-vidyut.svg" alt="VidyutDrishti landing page" width="100%"/></a>
</td>
</tr></table>

`Python` `FastAPI` `scikit-learn` `React` `TypeScript` `TanStack Query` `Groq` `NVIDIA NIM` `MCP`

### 🩺 HealthAI Triage &nbsp;·&nbsp; <sub>an agent that can never downgrade an emergency</sub>

<table><tr>
<td width="56%" valign="top">
<a href="https://healthai-triage.onrender.com"><img src="assets/shot-healthai.svg" alt="HealthAI emergency result page" width="100%"/></a>
</td>
<td width="44%" valign="top">

**In plain words:** describe your symptoms and get *home care*, *see a doctor today* or *emergency*, with reasons and sources. Fixed safety rules check every case and the most cautious answer always wins.

- Red-flag rules **can only raise a level**; final level = `max(rules, agent, conformal)`
- **60-case eval gated in CI**: 100% of red-flag cases, 85% of emergencies, 2 misses published
- Hybrid RAG, provider failover, Ops page, **135 tests** with no network

[![Live](https://img.shields.io/badge/Live-demo-34d399?style=flat-square)](https://healthai-triage.onrender.com) [![Code](https://img.shields.io/badge/Source-GitHub-181717?style=flat-square&logo=github)](https://github.com/Asha0509/HealthCare)

</td></tr></table>

`Python` `FastAPI` `React` `RAG` `Groq` `NVIDIA NIM` `Conformal prediction` `SQLite` `GitHub Actions`

<br/>

## 🧠 One design, three systems

<div align="center">
<img src="assets/pipeline.svg" alt="Animated pipelines of Retry Budget Allocator, VidyutDrishti and HealthAI" width="100%"/>
</div>

1. **Deterministic where it must be right.** Money, safety and rules are plain code with tests.
2. **Models where they add value.** Explaining, summarising and answering, always with a fallback.
3. **Prove it.** Evals, mutation tests, CI gates, and a "what did not work" section.

<br/>

## 🔬 Research

<a href="https://github.com/Asha0509/Apart-AI-Collusion-Research-Sprint"><img src="assets/research.svg" width="100%" alt="Research: Swapping the Model Does Not Reset the Price. Apart Research AI Collusion Research Sprint, October 2026, pre-registered. If AI pricing agents start colluding and you replace the model behind one of them, prices don't reset: with the old agent's notes the new model resumes the old price in 18 of 18 markets; without them it takes about 16 rounds to settle."/></a>

<br/>

## 🏆 Recognition & leadership

<img src="assets/achievements.svg" width="100%" alt="Finalist, Code by Groww 2026, 9 finalists from 2,900+ registrations. Top 0.5%, Flipkart GRiD 8.0, Round 3 of 400,000+ applicants. 3-star CodeChef, 850+ problems. Paper at ICIARD 2024, Thailand. Co-founder of the A.S.P.I.R.E AI club, 9 events, 100+ students, a 200+ person contest."/>

<details>
<summary><b>Experience & programs</b></summary>
<br/>

| | |
|---|---|
| 💼 **AptPath** · AI/ML Development Intern · Jul – Aug 2025 | Built [YogaAlign](https://github.com/Asha0509/YogaAlign): MediaPipe landmarks → SVM and Random Forest classifiers for yoga poses from video and live camera |
| 🎓 **Ananya's Atlassian Mentorship** · DSA & Backend · Nov 2025 – May 2026 | 6-month mentorship in distributed system design, OOP and team Git workflows |
| 🌍 **Aspire Leaders Program** · Aspire Institute (Harvard-affiliated) | Global leadership development, completed March 2025 |

</details>

<br/>

## 🛠️ Toolbox

<div align="center">
<img src="assets/skills.svg" alt="Toolbox by category: languages, web and APIs, ML and data, LLM and agents, quality and DevOps, databases" width="100%"/>
</div>

<details>
<summary><b>More projects</b></summary>
<br/>

- **[A2S – Aesthetics To Spaces](https://github.com/AestheticsToSpaces/A2S_Beta)** · [HyKr Build Challenge MVP](https://github.com/Asha0509/A2S-MVP-Hykr): AI interior design for homebuyers. Spring Boot backend (Spring Security + OAuth, JPA on PostgreSQL, cached catalog, rate limiting), Python AI service with image fallbacks, React + Three.js 3D walkthrough, Docker Compose. 28,000+ products.
- **[NexusDocs](https://github.com/Asha0509/Nexus_Docs)**: chat with your PDFs and notes; every answer cites its source passage. FastAPI, LangChain, ChromaDB, Next.js.
- **[YogaAlign](https://github.com/Asha0509/YogaAlign)**: yoga pose classification from video or webcam (AptPath internship). Flask, OpenCV, MediaPipe.
- **[Since](https://github.com/Asha0509/Groww_Hackathon)**: smart market watchlist, Code by Groww 2026 finalist project.
- **[Multi-tenant E-commerce API](https://github.com/Asha0509/Ecommerce_FullStack)**: Spring Boot + JPA backend with carts, orders and Stripe payment intents.

</details>

<br/>

## 📊 GitHub

<div align="center">
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Asha0509&layout=compact&bg_color=0b1020&title_color=22d3ee&text_color=c9d6f2&hide_border=true&border_radius=16" height="170" alt="Most used languages"/>
<img src="https://streak-stats.demolab.com/?user=Asha0509&background=0b1020&ring=a78bfa&fire=f472b6&currStreakNum=eaf0ff&sideNums=eaf0ff&currStreakLabel=22d3ee&sideLabels=8aa0c8&dates=6b7da3&stroke=1f2a44&hide_border=true&border_radius=16" height="170" alt="GitHub streak"/>
</div>

<img src="assets/footer.svg" alt="Thanks for stopping by. Open any live link above and take the in-app tour." width="100%"/>
