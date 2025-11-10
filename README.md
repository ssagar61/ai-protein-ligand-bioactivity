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

This project demonstrates the synergistic integration of **Molecular Dynamics simulations** and **Graph Neural Network modeling** for the prediction of bioactivity metrics such as binding affinity and cytotoxicity.  
The study uses **noscapine-based ionic liquids (NOS–ILs)** bound to **human serum albumin (HSA)** as a model system to show how physics-driven features from MD trajectories can feed into AI models to uncover structure–activity relationships.

**Key objectives:**
- Combine **MD-derived global and local descriptors** (RMSD, Rg, SASA, H-bonds, π–cation distance, helix tilt) with **AI models**.
- Capture **conformational heterogeneity** using PCA, FEL, clustering, and t-SNE.
- Develop **GNN-based models** for quantitative bioactivity prediction.
- Provide an **open and reproducible pipeline** for multi-scale biophysical–AI integration.

---

## ⚙️ Workflow Summary

```mermaid
graph LR
A[System Setup & MD Simulation] --> B[Feature Extraction (RMSD, Rg, SASA, etc.)]
B --> C[PCA, FEL, Clustering, t-SNE]
C --> D[Representative Structure Extraction]
D --> E[Feature Integration (global_md_with_sasa.csv)]
E --> F[GNN Model Training & Evaluation]
F --> G[Bioactivity Prediction & Interpretation]
```

