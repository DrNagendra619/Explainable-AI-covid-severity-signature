# Explainable-AI-covid-severity-signature
Explainable_AI_for_Precision_Medicine_Discovery_Benchmarking_and_Mechanistic_Validation_of_a_Parsimonious_3_Gene_Signature_for_COVID_19_Severity
# Explainable AI for Precision Medicine: COVID-19 Severity Signature

![GitHub license](https://img.shields.io/badge/License-MIT-blue.svg)
![Python Version](https://img.shields.io/badge/Python-3.8%2B-green.svg)
![AI Framework](https://img.shields.io/badge/XAI-Feyn%20QLattice-orange.svg)

## 📝 Project Overview
**Title:** Explainable AI for Precision Medicine: Discovery, Benchmarking, and Mechanistic Validation of a Parsimonious 3-Gene Signature for COVID-19 Severity

This project utilizes **Explainable AI (Symbolic Regression)** to move beyond "black-box" machine learning. By analyzing high-dimensional RNA-Seq data, we identify a transparent mathematical model using only **three genes** (`GZMH`, `LCN2`, `IL1R2`) that predicts COVID-19 severity with high accuracy. 

Unlike standard deep learning models that require hundreds of variables, this parsimonious approach offers a direct path to clinical translation via targeted PCR assays.

---

## 🧬 Scientific Discovery: The 3-Gene Signature
Through an evolutionary process on the **Abzu QLattice**, the following biomarkers were identified as the most critical drivers of severity:

1.  **GZMH (Granzyme H):** Key in cytotoxic T-cell response.
2.  **LCN2 (Lipocalin 2):** Associated with neutrophil activation and inflammation.
3.  **IL1R2 (Interleukin 1 Receptor Type 2):** A decoy receptor that regulates IL-1 inflammation.

### The Mathematical Formula
The AI evolved the following explicit equation for clinical prediction:
$$\text{Severity} = \text{logreg}(-0.016 \cdot \text{GZMH} - 1.29 \cdot (0.001 \cdot \text{IL1R2} - 1.47) \cdot (0.0019 \cdot \text{LCN2} - 2.27) + 3.52)$$

---

## 🚀 Performance Benchmarking
Our 3-gene model was benchmarked against an **ExtraTreesClassifier** (using 219 genes). The results demonstrate that complexity does not always equal better performance:

| Metric | 3-Gene XAI Model | ExtraTrees (219 Genes) |
| :--- | :--- | :--- |
| **AUC Score** | **0.846** | 0.821 |
| **Specificity** | **93.3%** | 88.0% |
| **Interpretability** | **High (Equation)** | Low (Black-box) |

---

## 🛠️ Methodology & Tech Stack

### Data Source
* **Dataset:** [GSE157103](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE157103) (NCBI GEO)
* **Samples:** 126 Patient Profiles (Harmonized RNA-Seq)

### Analysis Pipeline
1. **Live Ingestion:** Data is streamed directly from NCBI using `GEOparse`.
2. **Unsupervised Learning:** 3D PCA visualization of the transcriptomic landscape.
3. **Symbolic Regression:** Using the `Feyn` library to evolve high-performing, simple mathematical structures.
4. **Validation:** Mechanistic validation and performance testing on unseen data.



---

## 📦 Installation & Setup

### Prerequisites
* Python 3.8+
* A Feyn QLattice instance (Available at [abzu.ai](https://abzu.ai))

### Dependencies
```bash
pip install feyn GEOparse plotly scikit-learn pandas numpy openpyxl
