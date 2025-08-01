# Predicting Student Performance Using Synthetic Big Data and XGBoost

## Overview
This project predicts student academic performance (GPA categories) using a synthetically generated dataset scaled to **25 million records**. By leveraging XGBoost and big data techniques, we address challenges of privacy, data scarcity, and scalability in educational data mining. **DuckDB** was used to store the dataset in an accessible and query-efficient format, allowing us to process data directly within **Google Colab** without external database deployment.

---

## What Has Been Done
- **Synthetic Data Generation**: Created a 25M-record synthetic student dataset using a Gaussian Copula synthesizer.
- **Database Integration**: Normalized and loaded the data into **DuckDB** for fast, in-process SQL queries in Colab.
- **EDA & Preprocessing**:
  - Verified distributions and consistency of synthetic features.
  - Applied **PCA** on numeric features (90% variance retained) and **Chi-Squared** selection on one-hot encoded categorical features.
- **Model Training**:
  - Trained **XGBoost** on both original and synthetic datasets.
  - Tuned hyperparameters with **Optuna** on a stratified subset.
- **Evaluation**:
  - Reported accuracy, precision, recall, F1-score, MCC, and confusion matrices.
  - Compared synthetic-trained vs original-trained performance.
  - Performed qualitative checks using 10 handcrafted student profiles.
- **Visualization**: Feature importance plots, per-class performance metrics, and confusion matrices.

---

## Roadmap
- Expand visual and interactive model interpretation tools.
- Evaluate generalization across demographic segments or subgroups.
- Extend to additional ML models such as CatBoost or LightGBM.
- Explore scalability improvements using GPU-enabled synthesizers.
- Investigate transfer learning from synthetic to real-world domains.

---

## Topics Covered
- **Synthetic Data Generation**: Addressing privacy and data scarcity with high-fidelity synthetic records.
- **Scalable Modeling**: Using **XGBoost** with **DuckDB** to handle tens of millions of rows efficiently in Colab.
- **Privacy-Aware AI**: Preserving confidentiality while maintaining model performance.
- **Model Reliability**: Combining statistical metrics with domain-informed profile testing.

---

## Deliverables
1. **Google Colab Notebook**: End-to-end pipeline for synthesis, processing, modeling, and evaluation.
2. **Project Report (PDF)**: Methodology, findings, and visualizations.
3. **Synthetic Data Scripts**: Notebook(s) for generating and preparing synthetic data.
4. **README**: This document.

---

## Usage Instructions

```bash
git clone https://github.com/IssacL891/CSCI-620-Group-Project.git
cd CSCI-620-Group-Project
```

Then upload your notebook (e.g., `Final_Submission.ipynb`) to **Google Colab** and run all cells.

> ⚠️ **Warning**: Running the full pipeline may require **60 GB or more of RAM** in Colab or an equivalent environment, and initial compilation can take significant time.
