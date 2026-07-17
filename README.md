<div align="center">

  <h1>TA IF MCT</h1>

  <p>
    <strong>Undergraduate Thesis — [Your Full Thesis Title Here]</strong>
  </p>

  <!-- Badges -->
  <p>
    <img src="https://img.shields.io/badge/status-in%20progress-yellow" alt="status" />
    <img src="https://img.shields.io/badge/thesis-LaTeX-green" alt="LaTeX" />
    <img src="https://img.shields.io/badge/python-3.10+-3776AB?logo=python&logoColor=white" alt="Python" />
    <img src="https://img.shields.io/github/last-commit/USER/ta_if_mct" alt="last commit" />
  </p>

  <!-- Quick links -->
  <h4>
    <a href="https://github.com/USER/ta_if_mct/tree/main/thesis">📄 Thesis</a>
  <span> · </span>
    <a href="https://github.com/USER/ta_if_mct/tree/main/code">💻 Code</a>
  <span> · </span>
    <a href="https://github.com/USER/ta_if_mct/blob/main/results/EXPERIMENT_LOG.md">📊 Experiments</a>
  <span> · </span>
    <a href="https://github.com/USER/ta_if_mct/blob/main/CHANGELOG.md">📋 Changelog</a>
  </h4>

</div>

<br />

---

> **⚠️ IMPORTANT — Before you start working, make sure you have done all three:**
>
> 1. **Set your repository to Private.**
>    Go to **Settings → Danger Zone → Change repository visibility → Make private**.
>    Your thesis code and data must not be publicly visible.
>
> 2. **Transfer ownership to the MCT organization.**
>    Go to **Settings → Danger Zone → Transfer ownership** and transfer to the `mctosima` organization.
>    Your repo must live under MCT for supervision and archival.
>
> 3. **Use the correct repository name format.**
>    ```
>    github.com/[your-username]/ta_if_{your-call-name}_{your-student-id}
>    ```
>    Examples:
>    - `github.com/johndoe/ta_if_john_12345678`
>    - `github.com/janedoe/ta_if_jane_23456789`
>    - `github.com/budi/ta_if_budi_34567890`
>
>    Replace `{your-call-name}` with your first name or nickname, and `{your-student-id}` with your student ID number. Do **not** use spaces or special characters.

---

## Table of Contents

- [About](#about)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Reproducing Experiments](#reproducing-experiments)
- [Thesis Build](#thesis-build)
- [Review Process](#review-process)
- [Citation](#citation)

---

## About

This repository contains the code, data, and LaTeX source for my undergraduate thesis
at **[Institution Name]**.

**Research Question:** [Your main research question]

**Methodology:** [Brief description]

**Key Findings:** [Brief summary]

---

## Repository Structure

```
ta_if_mct/
├── AGENTS.md                 ← AI agent instructions (for automated review)
├── README.md                 ← This file
├── CHANGELOG.md              ← Version history
│
├── reviews/                  ← Supervisor review sessions
│
├── thesis/                   ← LaTeX thesis source
├── code/                     ← Main code entry points
├── src/                      ← Source code modules
├── results/                  ← Generated figures, tables, experiment log
├── references/               ← Bibliography & reading notes
└── docs/                     ← Methodology notes & supporting docs
```

---

## Getting Started

### Prerequisites

- Python 3.10+
- LaTeX distribution ([TeX Live](https://tug.org/texlive/) or [MiKTeX](https://miktex.org/))

### Installation

```bash
git clone https://github.com/[your-username]/ta_if_{call_name}_{student_id}.git
cd ta_if_{call_name}_{student_id}
python -m venv .venv
source .venv/bin/activate
pip install -r src/requirements.txt
```

---

## Reproducing Experiments

<!-- TODO: Replace with actual commands -->

```bash
cd code
python main.py
```

---

## Thesis Build

```bash
cd thesis
latexmk -pdf main.tex
```

---

## Review Process

This repository is supervised. Reviews happen on a regular schedule:

1. Supervisor reviews the latest commit
2. Findings are recorded in `reviews/YYYY-MM-DD_review_NN.md`
3. Each finding is assigned severity: 🔴 Blocker / 🟡 Needs Attention / 🟢 Minor
4. 🔴 items must be resolved before the next review

AI agents assist review via the protocol documented in [AGENTS.md](AGENTS.md).

---

## Citation

```bibtex
@thesis{yourname2025ta,
  title     = {Your Thesis Title},
  author    = {Your Name},
  year      = {2025},
  school    = {Your Institution},
  type      = {Undergraduate Thesis},
  url       = {https://github.com/[your-username]/ta_if_{call_name}_{student_id}}
}
```

---

## License

<!-- Choose and add a LICENSE file -->
