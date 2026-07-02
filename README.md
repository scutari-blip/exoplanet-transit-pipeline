# Exoplanet Transit Pipeline

Detecting exoplanet transits — periodic dips in stellar brightness — in publicly
available NASA Kepler/TESS light curves.

> **Status:** in active development. Architecture and design rationale are being
> documented in `DESIGN.md` as the project is built.

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
nbstripout --install   # strips notebook outputs on commit (per-clone git filter)
```

Requires Python 3.13+. The `nbstripout --install` step must be re-run in every
fresh clone — the git filter lives in local git config, not in the repo.

## Use of AI assistance

I used Claude as a **scaffolding assistant**, not a ghostwriter. The
division of labor is deliberate and documented:

- **My own work:** the transit-detection and period-folding algorithms, the
  underlying math, and the validation methodology. These are written so I can
  defend every line.
- **Assistant-scaffolded:** data ingestion, plotting and interactive
  visualizations, test harnesses, and project boilerplate.
- **Assistant as reviewer / sounding board:** pressure-testing design decisions,
  which are recorded in `DESIGN.md`.

AI assistance is disclosed here, at the project level — not claimed as
authorship. Claude is a tool, not an author, so commits are not co-attributed to
it. The guardrails the assistant operates under live in [`CLAUDE.md`](CLAUDE.md).
