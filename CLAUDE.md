# CLAUDE.md

Guardrails for any AI assistant working in this repository. These rules exist so
that the author can defend every algorithmic decision in person. Follow
them exactly.

## Project

Exoplanet Transit Pipeline — detecting transit dips in NASA Kepler/TESS stellar
light curves. This is a portfolio piece for an undergraduate astronomy
data-science lab application. The author is a UC Berkeley sophomore; code should
reflect an introductory background (CS 61A/B, CS 70, DATA 8/100, MATH 51–54).
Favor clear, defensible, intro-level code over clever or advanced constructs.

## The core rule: scaffold, don't ghostwrite

The value of this project is the author's ability to explain it. Therefore:

**The assistant MAY:**
- Write boilerplate: project skeleton, `src/` module stubs, config, packaging.
- Build data ingestion pipelines (downloading/parsing Kepler/TESS data).
- Write plotting and visualization code, including `ipywidgets` interactives.
- Write test harnesses and the *scaffolding* for injection-recovery experiments.
- Act as a rubber duck during design, and review/critique code *after* the
  author has written it ("is this loop really O(n·p)?").

**The assistant MUST NOT:**
- Author the core algorithmic logic — transit detection, period-folding /
  phase-folding, BLS, detrending math. The author writes these by hand.
- Silently "fix" or rewrite the author's algorithm. Suggest in prose; let the
  author make the change.

When asked to do something in the forbidden list, scaffold around it instead and
hand the author a clearly-marked stub to fill in.

## Conventions

- **Modular, not monolithic.** Heavy lifting lives in pure Python modules under
  `src/`. Notebooks import from `src/` and tell a clean narrative — they do not
  contain hundreds of lines of logic.
- **Document complexity.** Period-folding / search algorithms get an explicit
  Big-O note (time and space) in their docstring.
- **Embrace messy data.** Document how real-world anomalies (cosmic-ray hits,
  thruster firings, stellar variability) are handled, not idealized data.
- **Validate, don't just demo.** Injection-recovery and known-planet recovery
  are first-class deliverables, not afterthoughts.
- **Clean notebook diffs.** Strip notebook output/metadata before committing
  (nbstripout or jupytext). Keep commit history readable.

## Honesty in the record

- Commit messages describe the change plainly and honestly. Do NOT add a
  `Co-Authored-By` trailer or otherwise credit the assistant as an author — it
  is a tool, not an author. AI assistance is disclosed at the project level in
  the README, not by claiming co-authorship of commits.
- Design decisions and dead ends are recorded by the author in the journal /
  DESIGN.md. The assistant does not invent reasoning the author didn't have.
