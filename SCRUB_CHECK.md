# Privacy & content review

This repository publishes research about a sensitive topic (self-reported drug relapse) built on public Reddit data. It is deliberately limited to anonymized, aggregate materials. This file documents what was reviewed and what was withheld.

## Included (reviewed, publication-safe)

- **`Anders_LLM_Relapse_Labeling_paper.pdf`** — the full paper. Reviewed page by page: contains only aggregate results (threshold-sweep charts, confusion matrices, classification reports, summary statistics). No usernames, no verbatim user posts, no direct quotes. The paper's own Ethical Considerations section states this commitment explicitly.
- **`images/poster.jpg`** — the research poster. Aggregate content only (objectives, dataset description, feature list, model-accuracy summaries, one-shot evaluation). No usernames or raw posts.
- **`README.md`**, this file.

## Withheld (intentionally NOT published)

- **The relapse dataset** — raw Reddit posts, author usernames, timestamps, the DuckDB/parquet stores, and any per-author tables. This is re-identifiable data about individuals on a sensitive health topic and is not distributed.
- **The analysis notebooks** (`Jupyter_*.pdf` and their source) — these were written for the author's own analysis and contain **real Reddit usernames** (e.g. hardcoded in per-author SQL queries) and references to raw post text. They are not publication-safe as-is and are excluded.
- **The presentation deck** (`.pptx`) and the standalone abstract — redundant with the paper; omitted to keep the repo focused.

## Rationale

The scientific contribution — the labeling method, the engineered features, the models, and the results — is fully conveyed by the paper and poster without exposing any individual's data. Republishing usernames or post text tied to relapse disclosures would risk real harm to identifiable people, which the study's ethics stance (and this repo) explicitly avoid. Any future release of derived data would require proper anonymization and is out of scope here.
