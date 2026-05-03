# AIDA AIRR Analysis Code

This repository contains the analysis code for the manuscript:

> **Population-scale single-cell profiling of T- and B-cell receptor repertoires across six Asian populations**

The notebooks reproduce all main figures (Figure 1–6) of the paper 

---

## Repository structure

```
AIDA_AIRR_code/
├── notebooks/
│   ├── Figure1_demographic_landscape.ipynb
│   ├── Figure2_TCR_clonality_public_clones.ipynb
│   ├── Figure3_TCR_VDJ_space.ipynb
│   ├── Figure4_BCR_demographic_clonality_SHM_isotype.ipynb
│   ├── Figure5_BCR_VDJ_space.ipynb
│   └── Figure6_integrated_immune_phenotypes.ipynb
├── requirements.txt
└── README.md
```

---

## Figure ↔ notebook mapping

| Notebook | Figure panels | Content |
|---|---|---|
| `Figure1_demographic_landscape.ipynb` | Fig. 1B–I | T- and B-cell UMAPs, subset abundance vs. age/sex/ethnicity, ridge regression of demographic predictors |
| `Figure2_TCR_clonality_public_clones.ipynb` | Fig. 2A–G | TCR clonality (Gini, Shannon), rarefied Gini per subset, public-clone analysis, VDJdb annotation |
| `Figure3_TCR_VDJ_space.ipynb` | Fig. 3A–G | TCR V(D)J pseudobulk metacells (`dandelion` + `milopy`), V/J usage, motif logos, demographic associations |
| `Figure4_BCR_demographic_clonality_SHM_isotype.ipynb` | Fig. 4A–H | B-cell clonality, somatic hypermutation, isotype proportions, demographic associations |
| `Figure5_BCR_VDJ_space.ipynb` | Fig. 5A–G | BCR V(D)J pseudobulk metacells, isotype-resolved V/J usage, isotype × VDJ coupling |
| `Figure6_integrated_immune_phenotypes.ipynb` | Fig. 6A–F | Per-donor integrated TCR + BCR feature matrix, K-means immune phenotypes, ForceAtlas2 layout, demographic enrichment |

---

## Environment

A Python ≥ 3.9 environment is required. Install dependencies with:

```bash
pip install -r requirements.txt
```

Two key packages are not on PyPI and require manual install:

- **`dandelion`** — V(D)J analysis: <https://github.com/zktuong/dandelion>
- **`sceleto2`** — in-house clonality / repertoire utilities used in this study; available on request.

GPU is not required. Memory: ≥ 256 GB recommended for the full T-cell object.


```bash
jupyter lab notebooks/
```

Random seeds are fixed where applicable (bootstrap iterations, K-means initialisation, leiden clustering). Minor numerical differences across machines may occur for stochastic methods (UMAP, ForceAtlas2).

---

## Contact

For questions about the code, please open a GitHub issue. For questions about the data or the study, contact the first author.
