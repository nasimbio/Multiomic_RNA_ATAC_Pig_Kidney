# 🧬 10x Multiomic RNA + ATAC Profiling — Pig Kidney (Single-Nuclei)

This project applies 10x Genomics Multiome (Gene Expression + ATAC) technology to profile RNA and chromatin accessibility from two pig kidney samples at the single-nucleus level. The pipeline involves joint modality analysis and cluster annotation using canonical pig kidney markers.

---

## 📘 Project Overview

Multiomic single-nuclei data from two pig kidney samples (P0906 and P0909) were processed to explore gene expression and chromatin accessibility using the WNN (Weighted Nearest Neighbor) approach. This project aims to:

- Perform modality-specific QC and filtering on RNA and ATAC data
- Apply WNN-based multimodal integration to define biologically meaningful clusters
- Annotate cell types based on known kidney-specific markers from literature

---

## 📊 Analysis Tasks

### ** Task 1: Data Processing and Quality Control**

- Read 10x HDF5 files and extract RNA and ATAC matrices per sample
- Create Seurat objects with both RNA and ATAC assays
- Generate violin plots and calculate median QC metrics
- Filter low-quality cells based on custom thresholds
- Visualize post-filtering QC distributions


---

### **Task 2: WNN Integration and Cell Type Annotation**

  - Apply SCTransform for RNA and TF-IDF + SVD for ATAC modality
  - Perform dimensionality reduction (UMAP) for each modality separately
  - Run FindMultiModalNeighbors to integrate RNA and ATAC
  - Generate WNN-based UMAP and cluster cells
  - Annotate clusters based on canonical pig kidney markers

---

# 💡 Notes

- This dataset includes pig samples, required custom gene references and marker sets. 
- Raw data is not publicly available due to client ownership and confidentiality.
- Some example outputs plots are organized by task in the `output/` folder.
- This project is designed for both reproducibility and clarity.

---

## 📬 Contact

*Author:* Nasim Rahmatpour 
*Email:* nasimrahmatpour1@gmail.com 
*GitHub:* (https://github.com/nasimbio)

