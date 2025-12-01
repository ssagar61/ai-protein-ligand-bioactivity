# 🧠 AI-Assisted Prediction of Bioactivity and Protein–Ligand Interactions

This repository contains the datasets, scripts, and trained models developed for the study:  
**“AI-Assisted Prediction of Bioactivity and Protein–Ligand Interactions”**  
which integrates **classical Molecular Dynamics (MD)** simulations with **Graph Neural Network (GNN)**-based machine learning to predict protein–ligand bioactivity with mechanistic interpretability.

---

## 📑 Table of Contents

1. [Overview](#overview)  
2. [Workflow Summary](#workflow-summary)  
3. [Repository Structure](#repository-structure)  
4. [Installation](#installation)  
5. [Data Preparation](#data-preparation)  
6. [Running the Analysis](#running-the-analysis)  
7. [AI/ML Modeling](#aiml-modeling)  
8. [Results and Outputs](#results-and-outputs)  
9. [Citing This Work](#citing-this-work)  
10. [License](#license)
11. [Contact](#contact)

---

## 🧩 Overview

This project demonstrates a **hybrid MD + AI workflow** that unifies:

- **Molecular Dynamics simulations**  
- **Physics-informed descriptors**  
- **Machine Learning models (RF/XGBoost/MLP)**  
- **Graph Neural Networks (GCN/GAT/GIN)**  
- **Dimensionality reduction (PCA, t-SNE)**  
- **Free energy landscape (FEL) analysis**  
- **Explainable AI (SHAP + GNN saliency)**  

The study uses **noscapine-based ionic liquids (NOS–ILs)** bound to **human serum albumin (HSA)** as a model system to demonstrate how MD-derived structural features improve AI-driven prediction of:

- Binding affinity  
- Cytotoxicity (logIC₅₀)  
- Mechanistic interaction fingerprints  

**Key Objectives:**

- Extract both **global** and **local** MD descriptors (RMSD, Rg, SASA, Trp-214 exposure, π–cation interactions, hydrogen bonds).  
- Identify **conformational states** via PCA, FEL, and clustering.  
- Train **GNN models** on molecular graphs enhanced with MD features.  
- Build **tabular ML models** using merged descriptors + SHAP explainability.  
- Provide a **fully reproducible pipeline** for MD-to-AI bioactivity prediction.

---

## ⚙️ Workflow Summary

```mermaid
graph LR;
A[System Setup & MD Simulation] --> B["Feature Extraction (RMSD / Rg / SASA / π–cation / Trp-214 SASA)"];
B --> C[PCA & FEL & Clustering & t-SNE];
C --> D[Representative Structure Extraction];
D --> E[Feature Integration → final_features.csv];
E --> F1[Tabular ML (RF/XGB/MLP)];
E --> F2[GNN Model Training (GCN/GAT/GIN)];
F1 --> G[Explainability (SHAP)];
F2 --> H[GNN Saliency / Attention];
G --> I[Bioactivity Prediction & Mechanistic Interpretation];
H --> I;

```

