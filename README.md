# Redesign to Mechanism: Interpretable AI Reveals Determinants of Protein Hydrate Binding

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)

## Overview
Natural antifreeze proteins (AFPs) demonstrate exquisite structure-function relationships, while in silico designs often struggle to achieve a balance between structural stability, expression efficiency, and functional activity. This study establishes a computational framework integrating deep learning, molecular dynamics simulations, and interpretable machine learning for the rational design of AFPs. The Chill+ algorithm showed that 83.4% of the designed peptides exhibited superior hydrate inhibition activity relative to wild-type Tenebrio molitor AFP (TmAFP). XGBoost and SHAP analysis revealed that spatially defined structural features more accurately predicted inhibitory activity than statistical sequence features. Asn29 stabilizes the hydrate lattice via bifunctional hydrogen bonding and hydrophobic guest mimicry, while Ser4-Ile17 mutations optimize hydrophilic water ordering and hydrophobic anchoring. Val mutations further revealed two functional regions within the hydrate-binding site, an ordered anchoring region and a dynamic perturbation region. This work establishes an interpretable, generalizable framework for engineering high-performance AFPs.
<img width="1047" height="1056" alt="截屏2026-05-22 16 36 10" src="https://github.com/user-attachments/assets/7a71275b-2dd0-4e58-8b41-fea04b33a155" />
## Data

**File:** `data/1ezgdata.csv`

This CSV file contains the dataset used for model training and evaluation.

| Column          | Description                                                       |
|-----------------|-------------------------------------------------------------------|
| `protein_name`  | Identifier for each protein variant (e.g., `1EZG`, `P1`–`P96`)   |
| `activity_score`| Experimentally measured antifreeze percentage of hydrate (0–1 scale)     |
| `sequence`      | Full amino acid sequence of the protein variant                   |

- **Wild-type:** `1EZG` — derived from PDB structure [1EZG](https://www.rcsb.org/structure/1EZG)
- **Variants:** 96+ designed mutants (`P1`–`P96`) and additional variants with `_C` / `_NC` suffixes (e.g., `P36_C`, `P46_NC`)
- **Total samples:** 121 protein sequences with corresponding percentage of hydrate
## Code

**File:** `code/TmAFP.ipynb`

A Jupyter Notebook implementing a complete machine learning pipeline for predicting TmAFP hydrate percentages.
