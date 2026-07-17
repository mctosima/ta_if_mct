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

## 📖 Table of Contents

- [About](#-about)
- [Repository Structure](#-repository-structure)
- [Getting Started](#-getting-started)
- [Reproducing Experiments](#-reproducing-experiments)
- [Thesis Build](#-thesis-build)
- [Review Process](#-review-process)
- [Citation](#-citation)

---

## 🔍 About

This repository contains the code, data, and LaTeX source for my undergraduate thesis
at **[Institution Name]**.

**Research Question:** [Your main research question]

**Methodology:** [Brief description]

**Key Findings:** [Brief summary]

---

## 📁 Repository Structure

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

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- LaTeX distribution ([TeX Live](https://tug.org/texlive/) or [MiKTeX](https://miktex.org/))

### Installation

```bash
git clone https://github.com/USER/ta_if_mct.git
cd ta_if_mct
python -m venv .venv
source .venv/bin/activate
pip install -r src/requirements.txt
```

---

## 🔄 Reproducing Experiments

<!-- TODO: Replace with actual commands -->

```bash
cd code
python main.py
```

---

## 📄 Thesis Build

```bash
cd thesis
latexmk -pdf main.tex
```

---

## 👀 Review Process

This repository is supervised. Reviews happen on a regular schedule:

1. Supervisor reviews the latest commit
2. Findings are recorded in `reviews/YYYY-MM-DD_review_NN.md`
3. Each finding is assigned severity: 🔴 Blocker / 🟡 Needs Attention / 🟢 Minor
4. 🔴 items must be resolved before the next review

AI agents assist review via the protocol documented in [AGENTS.md](AGENTS.md).

---

## 📚 Citation

```bibtex
@thesis{yourname2025ta,
  title     = {Your Thesis Title},
  author    = {Your Name},
  year      = {2025},
  school    = {Your Institution},
  type      = {Undergraduate Thesis},
  url       = {https://github.com/USER/ta_if_mct}
}
```

---

## 📝 License

<!-- Choose and add a LICENSE file -->

---

---

## 🇮🇩 Tentang

Repositori ini berisi kode, data, dan sumber LaTeX untuk Tugas Akhir (S1) di
**[Nama Institusi]**.

**Pertanyaan Penelitian:** [Pertanyaan penelitian utama Anda]

**Metodologi:** [Deskripsi singkat]

**Temuan Utama:** [Ringkasan singkat]

---

## 📁 Struktur Repositori

```
ta_if_mct/
├── AGENTS.md                 ← Instruksi untuk AI agent (review otomatis)
├── README.md                 ← File ini
├── CHANGELOG.md              ← Riwayat versi
│
├── reviews/                  ← Catatan sesi review dosen pembimbing
│
├── thesis/                   ← Sumber LaTeX tesis
├── code/                     ← Entry point kode utama
├── src/                      ← Modul kode sumber
├── results/                  ← Output: gambar, tabel, log eksperimen
├── references/               ← Daftar pustaka & catatan bacaan
└── docs/                     ← Catatan metodologi & dokumen pendukung
```

---

## 🚀 Memulai

### Prasyarat

- Python 3.10+
- Distribusi LaTeX ([TeX Live](https://tug.org/texlive/) atau [MiKTeX](https://miktex.org/))

### Instalasi

```bash
git clone https://github.com/USER/ta_if_mct.git
cd ta_if_mct
python -m venv .venv
source .venv/bin/activate
pip install -r src/requirements.txt
```

---

## 🔄 Mereproduksi Eksperimen

```bash
cd code
python main.py
```

---

## 📄 Membangun Tesis

```bash
cd thesis
latexmk -pdf main.tex
```

---

## 👀 Proses Review

Repositori ini diawasi oleh dosen pembimbing. Review dilakukan secara berkala:

1. Pembimbing me-review commit terbaru
2. Temuan dicatat di `reviews/YYYY-MM-DD_review_NN.md`
3. Setiap temuan diberi tingkat keparahan: 🔴 Penghalang / 🟡 Perlu Perhatian / 🟢 Minor
4. Item 🔴 harus diselesaikan sebelum review berikutnya

AI agent membantu review melalui protokol yang terdokumentasi di [AGENTS.md](AGENTS.md).

---

## 📚 Sitasi

```bibtex
@thesis{yourname2025ta,
  title     = {Judul Tesis Anda},
  author    = {Nama Anda},
  year      = {2025},
  school    = {Institusi Anda},
  type      = {Tugas Akhir},
  url       = {https://github.com/USER/ta_if_mct}
}
```
