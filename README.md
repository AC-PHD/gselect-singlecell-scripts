# gSELECT – Supplementary Single-Cell Scripts

This repository contains Jupyter notebooks and utility scripts supporting additional analyses for the gSELECT publication. The focus is on logistic regression, Wilcoxon-based DEG analysis, UMAP visualization, and data preparation workflows in single-cell transcriptomics.

---

## Files Overview

###  `hdf5_to_h5ad.ipynb`
Converts raw HDF5-based input (e.g., `.h5` from Cell Ranger) into `.h5ad` format for downstream Scanpy processing.

###  `mtx_to_h5ad.ipynb`
Reads a 10X-style directory with `matrix.mtx.gz`, `barcodes.tsv.gz`, and `features.tsv.gz`, and builds an `.h5ad` file (AnnData) with basic QC.

---

###  `UMAP&Wilcoxn&LogReg&Violin.ipynb`
Performs:
- UMAP projection on full dataset
- Wilcoxon and Logistic Regression DEG analysis
- Violin plots of top marker genes

→ Grouping variable (e.g. `donor_sex_label`) and plotting can be customized inside the notebook.

---

###  `UMAP_allgenes.ipynb`
Visualizes the UMAP projection of all genes without filtering. Useful for exploring transcriptomic landscapes before applying feature selection.

---

###  `csv_UMAP_Wilcoxn_LogReg_Violin.ipynb`
End-to-end pipeline using CSV input (e.g., gene expression matrix with metadata labels).
- Computes UMAP
- Runs Wilcoxon & LogReg DEG
- Generates violin plots

→ Suitable for csv format (outside of `.h5ad`).

---

##  Requirements

All notebooks are written in Python ≥3.8 and use:

- `scanpy`
- `numpy`, `pandas`
- `matplotlib`, `seaborn`

Use a virtual environment or conda environment to ensure reproducibility.

---

##  Related Publication

> This code complements the manuscript on gSELECT, a flexible gene selection framework for pre-analysis in single-cell datasets.
> https://github.com/CaliskanDeniz/gSELECT

---

##  How to Cite

If you use these scripts, please cite the main gSELECT paper (link pending).
