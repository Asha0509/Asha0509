# Asha Jyothi Boddu

**AI/ML & Full-Stack Engineer · B.Tech CS-AIML @ BVRIT Hyderabad · CGPA 8.89**

📄 [Resume](#) &nbsp;·&nbsp; 💼 [LinkedIn](https://linkedin.com/in/asha-jyothi-b4186428a) &nbsp;·&nbsp; 📬 ashajyothi0509@gmail.com

---

## About Me

I'm a final-year Computer Science (AI/ML) student who builds things end-to-end — from
designing system architecture and training ML models to shipping full-stack applications
on cloud infrastructure. I don't stop at "it works on my machine."

My projects tend to be ambitious by choice. A2S involved four independently deployed
services, seven vendor scrapers, a multi-agent AI system, and a 3D room visualizer.
HealthAI required me to preprocess a 377-symptom × 773-disease dataset, train two
classifiers, wire up a Gemini-powered NLP layer, and write a formal test suite covering
crisis detection edge cases — all solo. I like problems that require holding a lot of
complexity at once and making deliberate decisions about what to build, what to cut,
and why.

Outside of building, I co-founded A.S.P.I.R.E, BVRIT Hyderabad's first student AI/ML
club, where I've organized 9 events and run workshops reaching 100+ students. I presented
research at an international conference in Thailand, and I'm currently in a structured
mentorship program focused on scalable system design and backend engineering.

I'm looking for internship or entry-level roles in **AI/ML engineering**, **full-stack
development**, or **backend engineering** where I can contribute to real systems and
keep learning fast.

---

## Featured Projects

### [A2S – Aesthetics To Spaces](https://github.com/AestheticsToSpaces/A2S_Beta)
*December 2025 – Present*

An AI-powered interior design platform that recommends furniture and décor based on
room aesthetics, budget, and style preferences — sourced live from major Indian and
global marketplaces.

**What makes it complex:**
- 4 independently deployed services: React frontend, Spring Boot API, Python LLM
  service, Streamlit admin dashboard — orchestrated with Docker Compose and deployed
  to Azure Container Apps via GitHub Actions CI/CD
- Multi-agent AI system (Stylist, Vastu, Consultant agents) built on Google Gemini,
  each with distinct reasoning responsibilities
- 7 scrapers across Amazon, Flipkart, IKEA, Urban Ladder, and Pepperfry aggregating
  28,000+ products with ML-based relevance ranking across room type, budget, style,
  and material
- 44 REST endpoints across 8 Spring Boot controllers and 12 JPA entities
- 3D room visualization built with Three.js; secured with OAuth2, JWT, Spring Security,
  and rate limiting
- Achieved <600ms average API response time with ~70% cache hit rate

**Stack:** React · Spring Boot · Java · Python · LangChain · PostgreSQL · Docker · Azure · GitHub Actions

---

### [HealthAI – Clinical Triage System](https://github.com/Asha0509/IOMP_HealthCare)
*January 2026*

A multi-service clinical triage system that uses conversational NLP to gather symptoms,
classify urgency, and predict likely diseases — with safety guardrails for crisis detection.

**What makes it complex:**
- Sole developer across the full stack: FastAPI backend, React frontend, SQLAlchemy ORM
  with MySQL/SQLite persistence, Gemini-powered NLP, and two independently trained ML
  classifiers
- Preprocessed a 377-symptom × 773-disease dataset using NumPy and Pandas for feature
  engineering and stratified splits
- XGBoost triage classifier: macro ROC-AUC ≈ 0.95, Emergency recall ≈ 0.92
- Random Forest disease classifier: Top-1 accuracy 82%, Top-3 accuracy 92%
- Formal test suite (pytest + pytest-asyncio) covering symptom extraction, adaptive
  question flow, crisis/guardrail detection, and end-to-end session lifecycle — all
  sessions complete in under 2 seconds
- Fallback heuristics validated for when Gemini API is unavailable, ensuring
  zero-downtime classification

**Stack:** Python · FastAPI · React · SQLAlchemy · MySQL/SQLite · XGBoost · Random Forest · Gemini API

---

### [NexusDocs – RAG Document Intelligence](https://github.com/Asha0509/Nexus_Docs)
*March 2026*

A document intelligence platform where you upload files and ask questions — getting
context-grounded answers with source citations, not hallucinated responses.

**What makes it complex:**
- RAG pipeline: PDF, DOCX, TXT, and Markdown ingestion → chunking with
  RecursiveCharacterTextSplitter → OpenAI text-embedding-3-small → ChromaDB vector index
- FastAPI backend with folder-scoped retrieval: cosine similarity search over top-5
  chunks fed into GPT-4o-mini for grounded answers
- Next.js frontend with document library management, folder organization, and a chat
  interface with expandable source passage references — so users can verify every answer

**Stack:** Python · FastAPI · LangChain · ChromaDB · Next.js · OpenAI API

---

### [YogaAlign](https://github.com/Asha0509/YogaAlign)
*July – August 2025 · Built during AI/ML Internship at AptPath*

Real-time yoga pose classification system with live camera inference and per-frame
corrective feedback.

**What makes it complex:**
- 92% accuracy across 15 pose categories on 248 annotated images
- NumPy and Pandas used for annotation preprocessing and feature normalization
- Random Forest and SVM classifiers with a live camera inference endpoint returning
  per-frame corrective feedback via JSON API
- 30% reduction in real-time frame processing latency through optimized preprocessing
  pipelines and modular model architecture
- Full-stack web app with user authentication, video upload history, and per-user
  prediction dashboards

**Stack:** Python · Flask · OpenCV · MediaPipe · NumPy · Pandas

---

## Skills

| Category | Technologies |
|---|---|
| **Languages** | Python · Java · JavaScript · TypeScript · C · SQL |
| **Frontend** | React · Next.js · Three.js |
| **Backend** | Spring Boot · FastAPI · Flask · Node.js · SQLAlchemy |
| **ML / AI** | XGBoost · scikit-learn · TensorFlow · MediaPipe · LangChain · RAG |
| **Databases** | PostgreSQL · MySQL · SQLite · ChromaDB |
| **Infrastructure** | Docker · Azure · GitHub Actions · Git |
| **Testing** | pytest · pytest-asyncio · Vitest · System Integration Testing |

---

## Research & Recognition

- 📄 **ICIARD 2024** — Presented *Significance of Emergent Technologies in Teaching Learning Processes* at Metarath University, Thailand (February 2024)
- 🏆 **SAP Hackfest 2024** — Semifinalist; built a sustainable solar energy technology solution
- 🎓 **Ananya's Atlassian Mentorship Program** — Selected for a 6-month structured mentorship in scalable system design and backend engineering (November 2025 – Present)

---

## Leadership

**Founding Member & Joint Secretary — A.S.P.I.R.E** *(2024 – Present)*
*First student-led AI/ML club, BVRIT Hyderabad*

Co-founded the club with a 19-member core team. Personally led 2 workshops and
co-organized 7+ sessions on ML, computer vision, and applied AI, reaching 100+ students.
Organized 9 events total, including an inter-college technical competition with 200+
participants as Technical Event Organizer for the Annual Fest (2025 & 2026).

---

## GitHub Stats

<p align="left">
  <img src="https://github-readme-stats.vercel.app/api?username=Asha0509&theme=default&hide_border=true&include_all_commits=false&count_private=false" height="150"/>
  &nbsp;&nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Asha0509&theme=default&hide_border=true&layout=compact" height="150"/>
</p>

<img src="https://nirzak-streak-stats.vercel.app/?user=Asha0509&theme=default&hide_border=true" height="150"/>

---

## GitHub Trophies

![](https://github-profile-trophy.vercel.app/?username=Asha0509&theme=flat&no-frame=true&no-bg=true&margin-w=6&column=7)
