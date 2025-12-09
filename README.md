# biopelayo – Computational Biology & Plant Chromatin

Welcome to the GitHub space of **Pelayo González de Lena** (@biopelayo).

This account serves as the **entry point** to a set of repositories built
around my doctoral work on **histone post-translational modifications (hPTMs) in plants**,  
with a particular focus on the detection and quantification of **H3K79** in *Arabidopsis thaliana*.

---

## 1. Profile

I am a **computational biologist / bioinformatician** and **FPI fellow (PRE2019-091395)**
at the University of Oviedo.

My work sits at the interface between:

- **Plant epigenomics** and chromatin regulation.
- **Histone proteomics** and quantitative analysis of hPTMs.
- **Reproducible software development** for large-scale omics.
- **FAIR data management** for public repositories (PRIDE / ProteomeXchange).

I routinely work with **Linux, WSL2, Docker, R, Python and MATLAB**, and I am interested in
turning “one-off” analysis scripts into **well-documented, reusable workflows**.

---

## 2. Research focus

Current interests include:

- Proteomic readout of the **“histone code”** in plants, with emphasis on **H3K79me1/2/3 and H3K79ac**.
- End-to-end pipelines for hPTMs:

  > `WIFF / RAW → mzML → MS1 / MS2 → EpiProfile_PLANTS → hPTM matrices → figures`

- Systematic re-analysis of **public datasets (PRIDE / ProteomeXchange)** under a common,
  documented workflow.
- **Training and materials for biologists** entering bioinformatics:
  courses, hands-on sessions, and written material (Quarto, notebooks, slides).

---

## 3. Doctoral thesis: H3K79 in *Arabidopsis thaliana*

My PhD thesis focuses on **plant histone epiproteomics**, combining:

- A software and methods chapter on **EpiProfile_PLANTS** for plant datasets.
- An ontogeny study of the **Arabidopsis rosette** (leaf developmental gradient).
- A reproducible re-analysis of selected public datasets (e.g. genotoxic stress in *Arabidopsis*).
- A synthesis of how **H3K79** behaves across development and stress conditions.

Main repository:

- **Doctoral thesis – `thesis-h3k79-arabidopsis`**  
  <https://github.com/biopelayo/thesis-h3k79-arabidopsis>

Expected contents:

- Thesis text (LaTeX / Quarto), following the UNIOVI structure.
- Figures, diagrams and iconography of the WIFF→Biology workflow.
- Manifests describing which **PXD** accessions are used, and how.
- Supplementary material:
  - hPTM matrices and summary tables.
  - R/Python scripts and notebooks for QC and downstream analysis.

---

## 4. EpiProfile_PLANTS ecosystem

A central component of my work is **EpiProfile_PLANTS**, an adaptation and extension
of **EpiProfile 2.0** tailored to plant data and modern workflows.

### 4.1 Core MATLAB code – `epiprofile-plants`

- **EpiProfile_PLANTS (MATLAB) – `epiprofile-plants`**  
  <https://github.com/biopelayo/epiprofile-plants>

Key elements:

- Histone peptide catalogs for:
  - *Arabidopsis thaliana* (AT)
  - *Marchantia polymorpha* (MP)
  - *Chlamydomonas reinhardtii* (CR)
- Species-specific panels for H3, H4, H2A, etc., and corresponding layouts.
- A documented separation between:
  - Functions reused verbatim from EpiProfile 2.0.
  - Functions modified for plant workflows.
  - New functions developed for EpiProfile_PLANTS.
- Utilities for:
  - QC and chromatogram inspection.
  - Isotopic profile visualization.
  - Auditing runs and panels.

### 4.2 Workflow WIFF→mzML→MS1/MS2→EpiProfile – `epiprofile-plants-workflow`

- **Workflow – `epiprofile-plants-workflow`**  
  <https://github.com/biopelayo/epiprofile-plants-workflow>

This repository is designed as an **end-to-end, reproducible pipeline**:

1. **Dataset inventory and download** from PRIDE (R packages such as `rpx`, etc.).
2. **Conversion** `WIFF / RAW → mzML` using `msconvert` (Docker / WSL2).
3. **Extraction** of MS1 / MS2 and preparation of inputs for EpiProfile_PLANTS.
4. **Batch execution** of EpiProfile_PLANTS.
5. Generation of outputs ready for:
   - QC and statistics in **R**.
   - Integration into reports, Shiny dashboards or notebooks.

The goal is that every step—from raw vendor files to the final hPTM matrices—is
**transparent, version-controlled and shareable**.

---

## 5. Other pipelines and related projects

Some related or satellite projects include:

- **K-CHOPORE – `k-chopore` (fork)**  
  <https://github.com/biopelayo/k-chopore>  
  Pipeline for **RNA modification and transcriptomics** analysis, adapted or being
  adapted to plant species.

- **Pre-QC for histone proteomics – `preqc-histones-py`** *(in development)*  
  Python modules for:
  - Dataset inventory and basic metadata.
  - Standard directory structures (e.g. `raw_wiff/`, `mzML/`, `MS1_MS2/`, `EpiProfile_output/`, `phenodata/`).
  - Pre-EpiProfile QC and sanity checks.

- **Dashboards and Shiny apps** *(planned)*  
  Interactive QC, heatmaps of hPTMs, and exploratory views for evolutionary
  comparisons (e.g. conserved H3/H4 peptides across species).

---

## 6. Public data, FAIR principles and reproducibility

A substantial part of this work builds on **public ProteomeXchange / PRIDE datasets**,
both my own and third-party.

Across the repositories you will find:

- Explicit lists of **PXD accessions** used in each analysis.
- Scripts and notebooks to:
  - Download raw data.
  - Check integrity and size.
  - Organize files into consistent directory trees.
- Standardized layouts such as:

  ```text
  raw_wiff/
  mzML/
  MS1_MS2/
  EpiProfile_output/
  layouts/
  phenodata/
  R/
  docs/
