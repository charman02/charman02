# Charles Man

Software engineer working across full-stack and applied ML. I care most about the
part after the demo — the tests, the authorization model, the thing that happens
when two people click the same link.

Looking for roles in applied AI/ML engineering — agentic systems, evaluation, and
the full-stack work that makes them usable.

Currently at **Amazon** (AGI), evaluating agentic AI output within Amazon's Nova
portfolio — 3000+ task evaluations to date — and generating training data.
Previously ML Research Intern at **Output Inc.**, adapting self-supervised models
for musical key estimation.

**MSc Data Science & AI** (Distinction), Queen Mary University of London  
**BS Biology**, CS minor, Tufts University · Boston, MA

---

## 🍱 Issei — [live app](https://issei-delta.vercel.app) · [repo](https://github.com/charman02/issei) · [API docs](https://family-recipe-library.onrender.com/docs)

**Someone cooked you something you'd never had before, you asked for the recipe.
Issei is how they send it to you.**

Not a scrubbed list of grams — the dish the way they actually make it, with "a
good splash" left as "a good splash." They write it down once; you get a link and
read the whole thing without making an account.

`FastAPI` · `SQLAlchemy` · `PostgreSQL` · `React` · `Vite` · `Tailwind` · deployed on Vercel + Render + Neon

**21 REST endpoints · 8 data models · 474 automated tests (136 pytest + 338 Vitest) · 240 commits over 3 months, solo**

Three things in here I'd want to be asked about:

**A capability-token share flow.** Holding an unguessable link *is* the read
permission — `GET /recipes/invite/{token}` serves the full recipe, ingredients
and steps and all, with no account. The recipient has never tasted the dish and
wants to cook it, so a signup wall at that moment is friction at peak intent.
A separate response schema withholds the owner's private notes and every
account ID.

**A revocation bug I found and fixed.** Claiming an invite reassigned
`to_user_id` on a single shared row — so when a second person claimed the same
link, the first person silently lost access, because read authorization matches
on that column. Now every claimer gets an independent grant. Locked in with a
regression test that asserts *both* recipients still see the recipe.
([`39e9934`](https://github.com/charman02/issei/commit/39e9934))

**Two shipped subsystems I deleted on purpose.** A consolidating shopping list
summed amounts across recipes — which means normalizing them, which is exactly
what this app exists to refuse; on real data it produced `"a good splash + a
glug"`. And a lineage tree modeled recipes as a generational graph when the
product is one dish handed to one person. I verified the removal safe against
production first (zero rows had a parent, so the tree-walk was already the
identity function), which collapsed authorization from a parent-chain walk to a
single predicate.

There are also **five tests that assert the UI makes no claim the product can't
back** — four fail if any screen mentions voice or audio, because `voice_note`
is typed text and no recording exists anywhere in the app.

---

## 🛠️ Selected projects

| Project | What it is | Result | Stack |
|---|---|---|---|
| **[issei](https://github.com/charman02/issei)** | Recipe app for dishes nobody wrote down — deployed, capability-token sharing, three visibility tiers | 21 endpoints · 474 tests | FastAPI · React · Postgres |
| **[short-loop-key-estimation](https://github.com/charman02/short-loop-key-estimation)** | Fine-tuned S-KEY for short audio loops — 24-way key classification trained with **zero ground-truth labels** via a transposition-equivariance objective | **64.8** MIREX weighted (GiantSteps) · **63.6** (FMAKv2) · +17.6 pts over my own SSL baseline | PyTorch · nnAudio · madmom |
| **[amazon-fine-food-reviews-search-engine](https://github.com/charman02/amazon-fine-food-reviews-search-engine)** | BM25 retrieval over Amazon Fine Food Reviews, with Precision/Recall/NDCG implemented from scratch | 568K → **393,576** deduped docs at ~1,035/sec | Elasticsearch · NLTK |
| **[cifar10-image-classifier](https://github.com/charman02/cifar10-image-classifier)** | CNN whose conv blocks are **softmax-weighted by the input itself** — each block learns per-image which of its convolutions to trust, plus residual connections | **86.9%** test accuracy | PyTorch |

Also some C++ from earlier: an [RPN calculator](https://github.com/charman02/rpn-calculator),
a [Huffman compressor](https://github.com/charman02/text-file-huffman-compressor),
and an [MBTA train simulation](https://github.com/charman02/mbta-train-simulation) —
data structures built from scratch, each with its own unit-test harness.

---

## 💻 Tools

**Languages:** Python · JavaScript · C++ · SQL  
**Backend:** FastAPI · SQLAlchemy · PostgreSQL · Alembic · JWT · REST  
**Frontend:** React · Vite · Tailwind (no UI kit — 5 runtime dependencies total)  
**ML / Data:** PyTorch · scikit-learn · NumPy · pandas · Elasticsearch · NLTK  
**Practice:** pytest · Vitest · Docker · Git · Claude Code

---

**[LinkedIn](https://www.linkedin.com/in/charlie-man/)**
