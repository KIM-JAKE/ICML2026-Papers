# ICML 2026 · Paper Guide

A fast, browsable guide to **all ICML 2026** (Seoul, Jul 6–11) accepted papers with poster/oral schedules, organized by the **official ICML topic areas**. Search, filter by area or day, and see exactly when and where each paper is presented (times in **KST**). Includes an interactive **COEX floor map** with every poster board.

**Live page:** once deployed, `https://kim-jake.github.io/ICML2026-Papers/`

## What's inside

- **All 6,628 accepted papers** (168 orals) from the official ICML 2026 feed.
- Each paper card shows: title (linked to its icml.cc page), authors + institution, its **poster session** (day / time / room / board #), its **oral slot** if any (day / time / room), plus an official topic badge. 759 papers without a published schedule show "Schedule TBD".
- Filter by **area** (top-level) and **subtopic**, **day** (Jul 7–9), **orals only**, and free-text **search**; sort by schedule, area, or title.
- `map.html` — interactive COEX venue map (halls, oral rooms) + Hall A poster board map (rows 1–46 × positions 0–26), dots colored by area, click for paper details.

### Topic areas (official ICML tags)

Top-level area → subtopic (e.g. `Deep Learning->Large Language Models`), straight from the icml.cc feed.

| Area | Count | Example subtopics |
|---|---|---|
| Deep Learning | 2,459 | Large Language Models, Generative Models, Foundation Models, GNNs, Theory, Algorithms |
| Applications | 1,506 | Computer Vision, Chemistry/Physics/Earth, Health/Medicine, Robotics, Time Series, Neuroscience |
| General Machine Learning | 747 | Evaluation, Representation Learning, Causality, Transfer/Multitask/Meta-learning |
| Social Aspects | 700 | Interpretability, Safety, Alignment, Fairness, Privacy |
| Reinforcement Learning | 410 | Deep RL, theory, bandits |
| Theory | 405 | Learning theory, statistics |
| Optimization | 227 | Convex/non-convex, stochastic |
| Probabilistic Methods | 174 | Bayesian methods, variational inference, sampling |

589 papers had no area tag in the feed; those were classified into the official tag set from their titles (LLM-assisted), so their tags are best-effort.

## Deploy to GitHub Pages

1. Put `index.html`, `map.html`, and `papers.js` in the root of the **KIM-JAKE/ICML2026-Papers** repo (keep them in the same folder).
2. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**, pick `main` / `root`, Save.
3. Wait ~1 minute → the site is live at `https://kim-jake.github.io/ICML2026-Papers/`.

Opening `index.html` directly in a browser also works (no server needed).

## Files

- `index.html` — the list app (HTML/CSS/JS, no dependencies, no build step).
- `map.html` — the COEX floor map + Hall A board map app.
- `papers.js` — the data (`window.ICML_PAPERS`, `window.ICML_META`). Regenerate to refresh.

## How it was built & caveats

- Data pulled from the official ICML 2026 feed (`icml.cc/static/virtual/data/icml-2026-orals-posters.json`); poster and oral entries were merged per paper and schedule times converted to **KST**. Categories are the official ICML area tags (top-level area + subtopic); 589 papers without a tag in the feed were assigned one from their titles (LLM-assisted, best-effort).
- **TLDRs** exist for ~2,867 LLM-adjacent papers (auto-generated from titles in an earlier pass — abstracts aren't in the feed) and may be approximate; other papers have no TLDR. Always check the linked paper page.
- On the floor map, the Hall B1/B2 and D1/D2 left–right split is an assumption (the official venue map doesn't subdivide them) — verify on site.
- Snapshot date: **2026-07-06**. Poster board numbers and rooms follow the ICML schedule at that time.
