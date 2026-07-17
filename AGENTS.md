# AGENTS.md — TA IF MCT

## Repository Purpose
This is an undergraduate thesis (Tugas Akhir) repository supervised by [Supervisor Name].
The supervisor conducts periodic reviews of all student work using AI-assisted review sessions.

## Repository Structure

```
ta_if_mct/
├── AGENTS.md                 ← AI agent instructions (this file)
├── README.md                 ← Bilingual project overview (EN + ID)
├── CHANGELOG.md              ← Version history per Keep a Changelog
├── LOGBOOK.md                ← Student research logbook (daily notes)
│
├── reviews/                  ← Supervisor review sessions
│   ├── TEMPLATE.md           ← Reusable review template
│   └── YYYY-MM-DD_review_NN.md
│
├── thesis/                   ← LaTeX thesis (student)
│   ├── reference.bib         ← BibTeX bibliography
│   ├── main.tex              ← Master LaTeX document
│   ├── chapters/             ← Chapter .tex files
│   └── figures/              ← Thesis figures
│
├── code/                     ← Main entry points (student)
│   └── main.py               ← Primary code entry point
│
├── src/                      ← Source code modules (student)
│   ├── data/raw/             ← Raw datasets — never modify
│   ├── data/processed/       ← Cleaned/transformed data
│   ├── models/               ← Model implementations
│   ├── notebooks/            ← Jupyter notebooks
│   ├── scripts/              ← Training, evaluation, preprocessing
│   ├── configs/              ← YAML experiment configs
│   └── requirements.txt      ← Python dependencies
│
├── results/                  ← Generated outputs (student)
│   ├── figures/              ← Publication-ready figures
│   ├── tables/               ← LaTeX table .tex files
│   └── EXPERIMENT_LOG.md     ← All experimental runs
│
├── references/               ← Paper references & literature
│   ├── reading_notes.md      ← Annotated bibliography
│   └── (paper PDFs optional)
│
└── docs/                     ← Supporting documentation
    └── methodology_notes.md  ← Protocol, assumptions, constraints
```

## File Ownership

| Directory | Owner | Purpose |
|-----------|-------|---------|
| `thesis/` | Student | LaTeX thesis source |
| `code/` | Student | Main code entry points |
| `src/` | Student | Source code modules |
| `results/` | Student | Generated outputs |
| `references/` | Student | Bibliography & reading notes |
| `docs/` | Student | Supporting documentation |
| `reviews/` | Supervisor | Review sessions & feedback |
| `LOGBOOK.md` | Student | Daily research logbook |
| `AGENTS.md` | Supervisor | AI agent instructions |

## AI Agent Constraints

- **READ-ONLY** on student work: `thesis/`, `code/`, `src/`, `results/`, `references/`, `docs/`, `LOGBOOK.md`
- **MAY create or update** files ONLY in `reviews/`
- **MUST NOT** modify any file outside `reviews/` without explicit supervisor instruction
- **MUST NOT** commit changes — the supervisor commits after reviewing AI-generated review files

## Supervisor Review Protocol

- Reviews are stored in `reviews/` as dated markdown files
- File naming: `YYYY-MM-DD_review_NN.md`
- Each review references a specific git commit hash
- Severity levels:
  - 🔴 **Blocker** — critical issue; must be resolved before next review
  - 🟡 **Needs Attention** — significant concern; address before submission
  - 🟢 **Minor / Suggestion** — nice to have; at student's discretion
- Action items are binding — 🔴 items block progress

## AI Agent Review Guidelines

When the supervisor asks an AI agent to review this repository, follow this protocol:

### Phase 1 — Orientation
1. Read `reviews/TEMPLATE.md` for the review format
2. Read the latest review file in `reviews/` to understand current state
3. Run `git log --oneline -20` for recent commit activity
4. Read `CHANGELOG.md` for version context
5. Read `LOGBOOK.md` for student's recent notes

### Phase 2 — Thesis Review
1. Read `thesis/main.tex` and all files in `thesis/chapters/`
2. Check for:
   - Argument coherence across chapters
   - All `\cite{}` keys exist in `thesis/reference.bib`
   - All `\label{}` have corresponding `\ref{}` — no orphan labels
   - Figures and tables are referenced in the text
   - Acronyms are defined at first use
3. Check spelling and grammar for the primary thesis language

### Phase 3 — Code Review (if `code/` or `src/` has content)
1. Read all `.py` files and notebooks
2. Check for: function docstrings, config-driven experiments, error handling, hardcoded values
3. Verify `src/requirements.txt` matches actual imports
4. Check `src/configs/` YAMLs are loaded by corresponding scripts

### Phase 4 — Results Audit
1. Read `results/EXPERIMENT_LOG.md`
2. Cross-reference: claims in thesis vs logged experiment results
3. Verify figures in `results/figures/` are referenced in thesis
4. Flag unreported experiments or runs missing from the log

### Phase 5 — Structure Compliance
1. Verify `src/data/raw/` exists and is not being modified by pipeline scripts
2. Check `.gitignore` covers LaTeX auxiliary outputs
3. Verify `CHANGELOG.md` is updated for recent changes
4. Check no large binary blobs are tracked outside Git LFS

### Phase 6 — Generate Review
1. Create `reviews/YYYY-MM-DD_review_NN.md` (increment NN from latest)
2. Use `reviews/TEMPLATE.md` structure
3. Reference specific file paths and line numbers for every finding
4. Assign severity to each finding: 🔴 🟡 🟢
5. End with numbered, deadline-targeted action items
6. Include AI Agent Notes section summarizing: scope checked, key findings, limitations

### Commands to Run (read-only)

```bash
# Phase 1
git log --oneline -20
ls -la src/data/raw/

# Phase 2 (for LaTeX diagnostics)
grep -r '\\\\label{' thesis/ | wc -l
grep -r '\\\\ref{' thesis/ | wc -l

# Phase 5
git ls-files -z | xargs -0 -n1 -I{} sh -c 'test -f "{}" && wc -c < "{}"' | awk '$1 > 52428800 {print "LARGE FILE: " FILENAME}' 2>/dev/null || echo "No files over 50MB"
```
