# Exoplanet Transit Pipeline

Detecting exoplanet transits — periodic dips in stellar brightness — in publicly
available NASA Kepler/TESS light curves.

> **Status:** in active development. Architecture and design rationale are being
> documented in `DESIGN.md` as the project is built.

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
