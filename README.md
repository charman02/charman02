# Hi, I'm Charles 👋

Software engineer working at the intersection of full-stack development and
applied ML. I like building things that actually work for the people using them
— and I care as much about the tests, the architecture, and the deploy as I do
about the demo.

Currently at **Amazon AGI Data Services**, evaluating agentic AI outputs and
generating training data for Amazon Nova. Previously an ML Research Intern at
**Output Inc.**, where I investigated self-supervised model adaptation for
musical key estimation.

## 🍱 What I'm building

**[Issei](https://github.com/charman02/issei)** · [live demo](https://issei-delta.vercel.app)

A full-stack app for preserving family recipes — the kind that live as oral
tradition, measured in "a dash" or "about 3 soup spoons," never anything
precise. Issei models that imprecision as a first-class idea: ingredients are
typed as precise, imprecise, or unmeasured, and the scaling engine treats each
differently, so a recipe can be resized without pretending "a pinch" is a number.

- **Backend:** FastAPI + SQLAlchemy, ~20 REST endpoints in a layered
  routers → services → models architecture, JWT auth, soft deletes, and a
  three-tier visibility model.
- **Frontend:** React + Vite + Tailwind, custom components (no UI kit).
- **Quality:** 62 backend and 81 frontend automated tests.
- **Deployed:** Vercel (web) + Render (API) + Neon (Postgres); SQLite locally.

Currently building a **recipe lineage** feature that tracks how a dish is
inherited and adapted across a family over time.

## 🛠️ Featured projects

| Project | What it is | Stack |
|---|---|---|
| **[Issei](https://github.com/charman02/issei)** | Full-stack recipe-preservation app (deployed) | FastAPI · React · Postgres |
| **[short-loop-key-estimation](https://github.com/charman02/short-loop-key-estimation)** | Self-supervised ML for musical key estimation on short audio loops | PyTorch · nnAudio |
| **[amazon-fine-food-reviews-search-engine](https://github.com/charman02/amazon-fine-food-reviews-search-engine)** | BM25 search engine over ~568K reviews with an NLP pipeline + IR evaluation | Elasticsearch · NLTK |
| **[cifar10-image-classifier](https://github.com/charman02/cifar10-image-classifier)** | Custom CNN with learned, input-weighted conv blocks (~87% accuracy) | PyTorch |

## 💻 Tech I work with

- **Languages:** Python · JavaScript · C++ · SQL
- **Backend:** FastAPI · SQLAlchemy · PostgreSQL · REST APIs
- **Frontend:** React · Vite · Tailwind CSS
- **ML / Data:** PyTorch · scikit-learn · NumPy · pandas
- **Tooling:** Git · pytest · Vitest · Docker · Claude (Anthropic)

## 🎓 Background

- **MSc, Data Science & AI** (Distinction) — Queen Mary University of London
- **BS, Biology** (Minor in Computer Science) — Tufts University

---

📫 **[LinkedIn](https://www.linkedin.com/in/YOUR-HANDLE)** · _replace with your profile URL_
