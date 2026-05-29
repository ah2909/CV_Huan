# GitHub Actions Workflow

[`latex.yml`](latex.yml) builds the resume and publishes it as a GitHub Release.

## What it does

1. **Build** — compiles `main.tex` with XeLaTeX (`latexmk -xelatex -shell-escape`) on every push, pull request, and manual dispatch.
2. **Rename** — copies the output to `Cao_Anh_Huan_Resume.pdf`.
3. **Upload artifacts** — the PDF and build logs (`main.log`, `main.aux`).
4. **Release** (push only) — creates a release tagged `build-{run_number}` with a changelog generated from commit history and the PDF attached.

## Required packages

Installed at runtime via `tlmgr` in the `pre_compile` step: `fontawesome5`, `fontspec`, `lm`, `babel-english`.

## Triggers

- `push` — build + release
- `pull_request` — build only
- `workflow_dispatch` — manual build

## Download

Latest PDF: [Releases](https://github.com/HThanh-how/CV_Huan/releases/latest).
