<div align="center">

<!-- Typing SVG Header -->
[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=28&duration=3000&pause=1500&color=39FF73&center=true&vCenter=true&multiline=true&repeat=true&width=750&height=80&lines=Hacking+histone+codes+in+plants+%F0%9F%8C%B1;From+raw+signal+to+biological+insight+%F0%9F%A7%AC)](https://biopelayo.github.io)

<br>

<img width="741" height="1024" alt="Pelayo González de Lena — Computational Biology" src="https://github.com/user-attachments/assets/0fabe2c6-8ccc-4ad9-bf0e-47f8974d11fa" />

<br>

# Pelayo González de Lena

**`Computational Biologist · Plant Epigenomicist · PhD Candidate`**

[![Website](https://img.shields.io/badge/biopelayo.github.io-0a0e17?style=for-the-badge&logo=github-pages&logoColor=39ff73)](https://biopelayo.github.io)
[![ORCID](https://img.shields.io/badge/ORCID-0000--0001--9409--1457-A6CE39?style=for-the-badge&logo=orcid&logoColor=white)](https://orcid.org/0000-0001-9409-1457)
[![Email](https://img.shields.io/badge/bio.pelayo@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:bio.pelayo@gmail.com)

</div>

---

## About me

I'm a computational biologist and bioinformatician working on **histone post-translational modifications (hPTMs) in plants**, with a special focus on **H3K79** methylation and acetylation in *Arabidopsis thaliana*.

Currently finishing my **PhD** at the **University of Oviedo** (FPI fellowship PRE2019-091395), building the **EpiProfile_PLANTS** ecosystem for reproducible plant histone proteomics. Previously at the **Spanish National Cancer Research Centre (CNIO)** in the Computational Cancer Genomics Group.

This account hosts my thesis work, analysis pipelines, teaching materials, and everything in between.

<br>

<div align="center">

### Tech stack

![MATLAB](https://img.shields.io/badge/MATLAB-0076A8?style=flat-square&logo=mathworks&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)
![Snakemake](https://img.shields.io/badge/Snakemake-5BB974?style=flat-square&logo=snakemake&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=flat-square&logo=latex&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)

![Bioconductor](https://img.shields.io/badge/Bioconductor-BioC-87b13f?style=flat-square)
![DESeq2](https://img.shields.io/badge/DESeq2-DE_analysis-276DC3?style=flat-square)
![Plotly](https://img.shields.io/badge/Plotly%20%2F%20Dash-3F4F75?style=flat-square&logo=plotly&logoColor=white)
![Minimap2](https://img.shields.io/badge/Minimap2-splice_aware-orange?style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)

</div>

---

## Current research focus

| Area | Description |
|:---|:---|
| **Plant epigenomics** | Chromatin regulation and histone PTM landscapes in *Arabidopsis*, *Marchantia*, *Chlamydomonas* |
| **H3K79 in plants** | Characterising H3K79me1/2/3 and H3K79ac across development and stress |
| **Histone proteomics** | Quantitative workflows for propionylation-based bottom-up MS |
| **Epitranscriptomics** | Nanopore direct RNA-seq and m6A modification detection |
| **Reproducible pipelines** | FAIR-compliant, containerised workflows from raw data to figures |
| **Teaching** | Making bioinformatics accessible to wet-lab biologists |

---

## The EpiProfile_PLANTS ecosystem

A central piece of my PhD: an end-to-end platform for plant histone proteomics, from vendor files to publication-ready figures.

```
WIFF/RAW ──▶ mzML ──▶ MS1/MS2 ──▶ EpiProfile_PLANTS ──▶ hDP/hPF/hPTM ──▶ Dashboard ──▶ Figures
   │            │          │              │                    │               │
   │      msconvert    xtract_xml    MATLAB core        3-tier model     Dash/Plotly
   │      (Docker)    (workflow)    (species bundles)   (audit-ready)    (7 tabs)
   ▼            ▼          ▼              ▼                    ▼               ▼
 PRIDE     centroided   text files    AT / MP / CR       QC artifacts    interactive
```

<table>
<tr>
<td width="33%">

### [`epiprofile-plants`](https://github.com/biopelayo/epiprofile-plants)

![MATLAB](https://img.shields.io/badge/MATLAB-100%25-0076A8?style=flat-square) ![License](https://img.shields.io/badge/GPL--3.0-blue?style=flat-square)

Core MATLAB code. Species-specific histone peptide catalogs and layouts for *Arabidopsis*, *Marchantia*, and *Chlamydomonas*. Three-tier data model: **hDP** (peptides) / **hPF** (peptideforms) / **hPTM** (site-level). RT reference system, T1-T4 audit provenance.

</td>
<td width="33%">

### [`epiprofile-plants-workflow`](https://github.com/biopelayo/epiprofile-plants-workflow)

![Python](https://img.shields.io/badge/Python-79.7%25-3776AB?style=flat-square) ![Shell](https://img.shields.io/badge/Shell-20.3%25-4EAA25?style=flat-square) ![License](https://img.shields.io/badge/GPL--2.0-blue?style=flat-square)

Docker + Snakemake preprocessing pipeline. PRIDE FTP download, msconvert to centroided mzML, MS1/MS2 extraction. Processed **220 raw files / 123 GB** across 3 datasets (PXD046034, PXD046788, PXD014739).

</td>
<td width="33%">

### [`epiprofile-dashboard`](https://github.com/biopelayo/epiprofile-dashboard)

![Python](https://img.shields.io/badge/Python-100%25-3776AB?style=flat-square) ![License](https://img.shields.io/badge/MIT-green?style=flat-square)

Interactive Dash/Plotly dashboard with **7 tabs**: Histone Ratios, Single PTMs, QC Dashboard, PSM Explorer, Sample Browser, Comparisons, Correlations. Heatmaps, PCA, dendrograms, mass accuracy QC.

</td>
</tr>
</table>

---

## K-CHOPORE

**Keen Comprehensive High-throughput Omics Pipeline Organizer** - a 9-stage Snakemake + Docker pipeline for **Oxford Nanopore direct RNA-seq** with emphasis on epitranscriptomics. Named after the Asturian *cachopo* - layers upon layers.

<div align="center">

```mermaid
graph LR
    A["1. Basecalling<br/>Dorado / Guppy"] --> B["2. Filtering<br/>NanoFilt"]
    B --> C["3. Read QC<br/>NanoPlot"]
    C --> D["4. Alignment<br/>Minimap2"]
    D --> E["5. Align QC<br/>samtools"]
    E --> F["6. Isoforms<br/>FLAIR / StringTie2"]
    F --> G["7. Epitranscriptomics<br/>ELIGOS2 / m6Anet"]
    G --> H["8. Diff. Expression<br/>DESeq2"]
    H --> I["9. Report<br/>MultiQC"]

    style A fill:#a78bfa,stroke:#7c3aed,color:#fff
    style B fill:#22d3ee,stroke:#06b6d4,color:#000
    style C fill:#22d3ee,stroke:#06b6d4,color:#000
    style D fill:#39ff73,stroke:#22c55e,color:#000
    style E fill:#22d3ee,stroke:#06b6d4,color:#000
    style F fill:#f59e0b,stroke:#d97706,color:#000
    style G fill:#f472b6,stroke:#ec4899,color:#000
    style H fill:#ef4444,stroke:#dc2626,color:#fff
    style I fill:#e2e8f0,stroke:#94a3b8,color:#000
```

</div>
<img width="1024" height="572" alt="image" src="https://github.com/user-attachments/assets/2dc48dcd-1bde-4de7-aa7c-651dc167b1bb" />

Currently applied to an ***Arabidopsis thaliana*** 2x2 factorial experiment (WT vs *anac017-1* mutant x Control vs Antimycin A):

| | Wild Type (WT) | *anac017-1* Mutant |
|:---|:---:|:---:|
| **Control** | 3 replicates | 3 replicates |
| **Antimycin A** | 3 replicates | 1 replicate |

**Results**: 20,958 isoforms quantified | 435 DEGs by genotype | 266 DEGs by treatment

[![K-CHOPORE](https://img.shields.io/badge/K--CHOPORE-anac017%20study-a78bfa?style=for-the-badge&logo=github)](https://github.com/biopelayo/kchopore-anac017-drs)

---

## PhD thesis: H3K79 in *Arabidopsis thaliana*

My thesis combines four chapters spanning methods, biology, and synthesis:

| Ch. | Topic | Approach |
|:---:|:---|:---|
| **1** | EpiProfile_PLANTS methods | Software validation, species-specific catalogs, QC framework |
| **2** | Arabidopsis rosette ontogeny | Developmental gradient (YNG / BOT / FLOR / SEN) histone PTM profiling |
| **3** | Re-analysis of public datasets | Genotoxic stress datasets from PRIDE (PXD010102, PXD046034, etc.) |
| **4** | H3K79 synthesis | Behaviour across development and stress-related contexts |

---

## Other projects

<table>
<tr>
<td width="50%">

### VIDIO

**Vision-Integrated Diagnostic Imaging Orchestrator**

Multi-modal biomedical image analysis for retinal imaging, histopathology (OpenSlide), radiology (DICOM/NIfTI), and spatial transcriptomics (H5AD). Built on Falcon WSGI, PyTorch/MONAI, OpenCV, with 5-stage pipeline and TCGA integration.

[![VIDIO](https://img.shields.io/badge/VIDIO-Repository-22d3ee?style=flat-square&logo=github)](https://github.com/biopelayo/VIDIO)

</td>
<td width="50%">

### CV Forge

**One CV, 31 styles, 2 languages**

A complete CV in a single self-contained HTML file: 31 visual themes, English and Spanish, three headline variants, and PDF export. No build step, no dependencies, no tracking. Open the file and it works.

[![cv-forge](https://img.shields.io/badge/cv--forge-Repository-f59e0b?style=flat-square&logo=github)](https://github.com/biopelayo/cv-forge)

</td>
</tr>
</table>

---

## Repository index

A map of what lives in this account, so you don't have to dig through the repository list.

### EpiProfile_PLANTS ecosystem

| Repo | What it is | Stack |
|:---|:---|:---|
| [`epiprofile-plants`](https://github.com/biopelayo/epiprofile-plants) | MATLAB core. Species bundles (AT / MP / CR), hDP-hPF-hPTM model | MATLAB |
| [`epiprofile-plants-workflow`](https://github.com/biopelayo/epiprofile-plants-workflow) | WIFF→mzML→MS1/MS2 preprocessing. Docker + Snakemake | Python |
| [`epiprofile-dashboard`](https://github.com/biopelayo/epiprofile-dashboard) | Interactive 7-tab dashboard for quantification output | Dash / Plotly |
| [`epiprofile-plants-at-h3h4`](https://github.com/biopelayo/epiprofile-plants-at-h3h4) | *Arabidopsis* H3/H4 peptide bundle | MATLAB |
| [`cap4-histone-ptms-at`](https://github.com/biopelayo/cap4-histone-ptms-at) | Reproducible `targets` pipeline for comparative hPTM analysis | R |
| [`histone-long-table-at`](https://github.com/biopelayo/histone-long-table-at) | Tidy long-format master table for *Arabidopsis* hPTMs | Python |

### Pipelines & analysis

| Repo | What it is | Stack |
|:---|:---|:---|
| [`kchopore-anac017-drs`](https://github.com/biopelayo/kchopore-anac017-drs) | K-CHOPORE pipeline applied to the *anac017-1* 2x2 factorial experiment | Snakemake |
| [`VIDIO`](https://github.com/biopelayo/VIDIO) | Multi-modal biomedical imaging orchestrator | Python |
| [`opencb-docker-stack`](https://github.com/biopelayo/opencb-docker-stack) | Docker Compose stack for OpenCB | Dockerfile |

### Web, tools & personal

| Repo | What it is | Stack |
|:---|:---|:---|
| [`biopelayo.github.io`](https://github.com/biopelayo/biopelayo.github.io) | Personal site | HTML |
| [`cv-forge`](https://github.com/biopelayo/cv-forge) | One-file CV: 31 styles, 2 languages, 3 headlines | HTML |
| [`asterov-dashboard`](https://github.com/biopelayo/asterov-dashboard) | Liga Asterov dashboard — San Claudio FC | JavaScript |
| [`paleotxomi`](https://github.com/biopelayo/paleotxomi) | Domingo González de Lena photographic archive + exhibition | TypeScript |
| [`awesome-awesomers`](https://github.com/biopelayo/awesome-awesomers) | Who curates the curators: awesomers on GitHub | Python |
| [`pelayo-x-claude`](https://github.com/biopelayo/pelayo-x-claude) | Public dossier of intensive Claude use in research | — |
| [`analisis-23-F`](https://github.com/biopelayo/analisis-23-F) | Analysis of the 23-F declassified documents | — |

---

## Reproducibility principles

Across all repositories I follow a consistent philosophy:

```text
raw_wiff/              # Vendor files, PXD accessions documented
mzML/                  # Converted with msconvert (Docker)
MS1_MS2/               # Extracted text files
EpiProfile_output/     # Quantification matrices
layouts/               # Species-specific peptide catalogs
phenodata/             # Sample metadata
R/                     # Downstream statistics
docs/                  # Documentation and manifests
```

- Every analysis links back to **explicit PXD accessions**
- Complete reproduction from **WIFF/RAW to figures** in a single command
- FAIR principles: findable, accessible, interoperable, reusable
- GPL-family licences with citable documentation

---

## Publications

| Year | Title | Venue |
|:---:|:---|:---|
| 2026 | [RNA Sequencing Platforms and Bioinformatics Tools](https://doi.org/10.1007/978-981-95-5183-5_2) | Book chapter |
| 2017 | [Clusterization in head and neck squamous carcinomas based on lncRNA expression](https://doi.org/10.1186/s13148-017-0334-6) | *Clinical Epigenetics* |

---

## Background & experience

```
University of Oviedo    ███████████████████████████░░░  PhD (FPI) · Plant epigenomics · 2020–present
CNIO                    ████████████████░░░░░░░░░░░░░  Computational Cancer Genomics · lncRNA / NGS
Teaching (IAAP & more)  ██████████████████████░░░░░░░  Linux, Python, R, Docker for biologists
GeoAI / ICM / FSP       ████████████░░░░░░░░░░░░░░░░░  Data analysis, geospatial AI, healthcare
```

---

## "Codigo Biologico"

A growing project to **teach bioinformatics and computational biology to biologists** from scratch:

- Step-by-step notebooks and slides with real biological data
- Recorded sessions and screencasts
- Reusable templates for academic and public administration courses
- Material linked from [biopelayo.github.io](https://biopelayo.github.io)

---

<div align="center">

### GitHub stats

<img src="https://github-readme-stats.vercel.app/api?username=biopelayo&show_icons=true&theme=radical&hide_border=true&bg_color=0a0e17&title_color=39ff73&icon_color=22d3ee&text_color=e2e8f0" height="170" alt="GitHub Stats" />
&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=biopelayo&layout=compact&theme=radical&hide_border=true&bg_color=0a0e17&title_color=39ff73&text_color=e2e8f0" height="170" alt="Top Languages" />

<br><br>

[![Streak](https://streak-stats.demolab.com/?user=biopelayo&theme=radical&hide_border=true&background=0a0e17&ring=39ff73&fire=f472b6&currStreakLabel=22d3ee)](https://github.com/biopelayo)

<br>

---

### Let's connect

If you work on **plant epigenomics**, **histone proteomics**, **reproducible omics workflows**, or are interested in **re-analysing PRIDE datasets related to chromatin**, feel free to open an issue or reach out.

**Suggestions, discussions, and pull requests are very welcome.**

[![Website](https://img.shields.io/badge/Website-biopelayo.github.io-39ff73?style=flat-square&logo=github-pages&logoColor=white)](https://biopelayo.github.io)
[![ORCID](https://img.shields.io/badge/ORCID-0000--0001--9409--1457-A6CE39?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0000-0001-9409-1457)
[![Email](https://img.shields.io/badge/Email-bio.pelayo@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:bio.pelayo@gmail.com)

<br>

<sub>Compilando... 62%</sub>

</div>
