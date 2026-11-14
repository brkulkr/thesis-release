# Data-Efficient Deep Learning Inference for Sensing Systems

PhD thesis of Berk Ulker (Eindhoven University of Technology). This repository holds
what is released for review: the shared to-do list and the thesis document package
(LaTeX sources, bibliography, figures). Result reports will be added here as they are
released. Code and experiments live elsewhere.

## Contents

| Path | What |
|---|---|
| `TODO.md` | Shared to-do list. **Editable**: tick or add tasks here. |
| `main.tex`, `chapters/`, `frontmatter/`, `backmatter/` | Thesis sources |
| `bib/`, `figures/` | Bibliography and figures |
| `RELEASES.md` | One line per document release |

## Structure

| Ch | Title | Based on |
|---|---|---|
| 1 | Introduction | – |
| 2 | Background and cost framework | – |
| 3 | How: framework and platform choice | SCOPES 2020 |
| 4 | Where: prior object locations in video | ICIAP 2022 |
| 5 | Which: attribution-based band selection | GISTAM 2026 |
| 6 | When: retrieval-efficient acquisition selection | IEEE JSTARS paper (in preparation) |
| 7 | Which + when: joint spectral–temporal reduction | new |
| 8 | Conclusion | – |

## Build

`latexmk -pdf main.tex` (or `make`), or upload the folder to Overleaf (pdfLaTeX, biber).

## How to contribute

- **To-do list:** edit `TODO.md` directly on GitHub and commit. Changes are merged into
  Berk's list at the next sync. Instructions are at the top of the file.
- **Comments on the text:** open an issue, or comment on a release commit.
- Please edit only `TODO.md`. Every other file is replaced at each release, so edits
  there would be lost.
