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

A deployed full-stack app for preserving the family recipes that were never
written down — the cooking knowledge immigrant elders carry in memory, one
generation from being lost. Instead of a static list of grams and steps, Issei
treats a recipe as a **living vessel for a person**: the cook's own voice and
their imprecise measurements ("a dash," "three soup spoons," "until it smells
right") are preserved verbatim rather than normalized away, and each recipe
**grows from a seed into a tree** as it's cooked, enriched, and handed down.

- **Fuzzy-quantity model:** ingredients are typed as precise, imprecise, or
  unmeasured, and the scaling engine treats each differently — so a recipe can
  be resized without pretending "a pinch" is a number.
- **Lineage & handoff:** recipes branch across relatives with per-recipe
  private → shared → public visibility, tracking how a dish is inherited and
  adapted over generations.
- **Backend:** FastAPI + SQLAlchemy, ~20 REST endpoints in a layered
  routers → services → models architecture, JWT auth, and soft deletes.
- **Frontend:** React + Vite + Tailwind, custom components (no UI kit).
- **Quality & deploy:** 62 backend + 81 frontend automated tests; live on
  Vercel (web) + Render (API) + Neon (Postgres), SQLite locally.

Next up: **multi-user family sharing** — a proper families model so a recipe one
relative adds is visible to the whole family without manual copying.

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

📫 **[LinkedIn](https://www.linkedin.com/in/charlie-man/)**
