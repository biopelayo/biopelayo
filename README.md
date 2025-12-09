# 🧬 Pelayo González de Lena — Computational Biology & Plant Chromatin

Hi, I’m **Pelayo González de Lena** (`@biopelayo`) — a computational biologist / bioinformatician working on **histone post-translational modifications (hPTMs) in plants**, with a special focus on **H3K79** in *Arabidopsis thaliana*.

This account is the hub for my **PhD thesis**, the **EpiProfile_PLANTS** ecosystem, and several workflows and teaching materials around reproducible omics.

---

## 🔍 What I work on right now

- **Plant epigenomics & chromatin regulation**
- **Histone proteomics and quantitative hPTMs**, especially H3K79me1/2/3 and H3K79ac  
- **End-to-end, reproducible workflows** for:
  `WIFF / RAW → mzML → MS1/MS2 → EpiProfile_PLANTS → hPTM matrices → figures`
- **FAIR data practices** for PRIDE / ProteomeXchange datasets
- **Training biologists in bioinformatics** (Linux, R/Bioconductor, Python, workflows)

I currently hold an **FPI fellowship (PRE2019-091395)** at the **University of Oviedo**, where my PhD thesis centres on H3K79 in *Arabidopsis* within the broader context of plant epiproteomics and chromatin regulation.

---

## 📚 PhD thesis: H3K79 in *Arabidopsis thaliana*

My thesis combines:

1. A **software / methods chapter** on _EpiProfile_PLANTS_ for plant datasets.  
2. An **ontogeny study of the Arabidopsis rosette** (leaf developmental gradient, BGSR: YNG/BOT/FLOR/SEN).  
3. A **re-analysis of public datasets** (e.g. genotoxic stress in *Arabidopsis*).  
4. A **synthesis of H3K79 behaviour** across development and stress-related contexts.

**Main repository**

- 📘 **Thesis – `thesis-h3k79-arabidopsis`**  
  → thesis text (LaTeX/Quarto), figures, analysis notebooks, and manifests documenting which PRIDE datasets and which versions of EpiProfile_PLANTS / workflows are used in each chapter.

---

## 🧪 EpiProfile_PLANTS ecosystem

A central piece of my work is **EpiProfile_PLANTS**, an extension of **EpiProfile 2.0** tailored to plant histone proteomics and modern, automated workflows.

### 1️⃣ Core MATLAB code — `epiprofile-plants`

- MATLAB codebase for **plant-specific EpiProfile**:
  - Histone peptide catalogues and layouts for:
    - *Arabidopsis thaliana* (AT)  
    - *Marchantia polymorpha* (MP)  
    - *Chlamydomonas reinhardtii* (CR)
  - Species-specific panels for H3, H4, H2A, etc.
  - Separation between:
    - Files reused verbatim from EpiProfile 2.0  
    - Files adapted for plants  
    - New functions developed for EpiProfile_PLANTS
  - Utilities for QC, chromatogram inspection and isotopic profile visualisation.

### 2️⃣ Workflow WIFF→mzML→MS1/MS2→EpiProfile — `epiprofile-plants-workflow`

- Docker + Snakemake workflow to:
  1. Organise PRIDE/ProteomeXchange datasets in a standard layout.
  2. Convert vendor files (e.g. SCIEX WIFF/WIFFSCAN) to `mzML` via **msconvert** in Docker.
  3. Extract `MS1` / `MS2` text files required by EpiProfile.
  4. Run EpiProfile_PLANTS with species-specific layouts.
  5. Produce analysis-ready hPTM matrices for downstream R/Python analysis.

Typical use cases include:

- Re-analysing PXD datasets (e.g. **PXD010102**, **PXD046034**) under a unified workflow.  
- Internal ontogeny datasets for *Arabidopsis* rosettes (BGSR).  
- Small demonstration sets (e.g. **ONTOGENY_DEMO** as a fully documented mini-dataset).

---

## 🧰 Other pipelines and side projects

Some related / satellite projects:

- 🥩 **K-CHOPORE (`k-chopore`)**  
  A bioinformatics pipeline for RNA modification and transcriptomics analysis, adapted (or being adapted) to **plant species**. Inspired by the Asturian *cachopo*.

- 🧪 **Pre-QC for histone proteomics (`preqc-histones-py`, in progress)**  
  Python modules for:
  - Dataset inventory and basic metadata checks  
  - Enforcing a standard directory structure for histone proteomics  
  - Pre-EpiProfile sanity checks (file completeness, NA/zero structure, etc.)

- 🌐 **Personal website (`biopelayo.github.io`)**  
  A hub for:
  - Short bio and CV highlights  
  - Research projects in plant epigenomics and epiproteomics  
  - Blog-style notes, slides and teaching material  
  - Documentation and visual material linked to EpiProfile_PLANTS

---

## 🧱 Data, layout and reproducibility principles

Across my repositories you will find:

- **Explicit lists of PXD accessions** used in each analysis.  
- Scripts/notebooks to:
  - Download and verify raw data  
  - Organise it into **standard directory trees**, typically:

    ```text
    raw_wiff/
    mzML/
    MS1_MS2/
    EpiProfile_output/
    layouts/
    phenodata/
    R/
    docs/
    ```

- A strong emphasis on:
  - Reproducing complete analyses from **WIFF/RAW to figures**  
  - Reusing individual components (conversion, EpiProfile_PLANTS, downstream statistics)  
  - Aligning everything with **FAIR principles** (findable, accessible, interoperable, reusable)

Where possible, I release code and workflows under **copyleft licences** (GPL family) and accompany them with documentation that can be cited in manuscripts and theses.

---

## 🧭 Background & experience (beyond the PhD)

Before and alongside the PhD, I have worked across academia, research institutes and training:

- 🧬 **Computational biology & omics**
  - Experience in **NGS / transcriptomics / lncRNA** pipelines  
  - Work with tools such as **VEp**, FEELnc and custom analysis scripts (some early work via forks on this account).

- 🏥 **Research and data roles**
  - Collaborations and positions spanning:
    - **CNIO** (National Cancer Research Centre, Spain)  
    - **GeoAI-related work** (geospatial / AI-driven analysis)  
    - **ICM Lugo** (research / healthcare context)  
    - Regional public health and research environments (e.g. FSP-linked initiatives)

- 🏫 **Teaching & training**
  - Courses and workshops with:
    - **Instituto Asturiano de Administración Pública (IAAP)**  
    - **University of Oviedo** and local institutions  
    - **City Council of Oviedo**  
    - Training companies such as **FORMACAL** and **ARTEAULA**
  - Main topics:
    - Linux / WSL2 / Docker for scientific computing  
    - Introductory **Python** and **R/Bioconductor** for omics  
    - Small, self-contained projects that connect code with real biological questions

These experiences shape how I design workflows: **practical, documented, and teachable**.

---

## 🎓 Teaching, outreach & “Código Biológico”

A medium-term goal is to consolidate a broader project tentatively called **“Código Biológico”**:

- A space to **teach bioinformatics and computational biology to biologists** from scratch.  
- Material will likely include:
  - Step-by-step notebooks and slides  
  - Recorded sessions or screencasts  
  - Real biological examples (not toy datasets)  
  - Reusable templates for courses in public administration and academic settings

Some of this material will live in this GitHub account and be linked from my personal website.

---

## 📫 Contact & online presence

- 🌐 Personal website: **https://biopelayo.github.io**  
- ✉️ Email: **bio.pelayo@gmail.com**  
- 🆔 ORCID: **https://orcid.org/0000-0001-9409-1457**  
- 💼 LinkedIn / X / others: to be added as the ecosystem stabilises

If you are interested in:

- Plant epigenomics and histone proteomics  
- Reproducible workflows for omics data  
- Collaborating on the re-analysis of PRIDE datasets related to chromatin

…feel free to open an Issue on any relevant repository or contact me by email.  
**Suggestions, discussions and pull requests are very welcome.**
