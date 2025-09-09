# Distance & Angle — Multi-Replicate MD Geometry Analysis (Colab-Ready)

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/davari-group/MD-Distance-Angle-Analysis/blob/main/Distance%26Angle.ipynb)
![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![MDAnalysis](https://img.shields.io/badge/MDAnalysis-2.x-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

> **One-line:** Compute and visualize **aromatic ring–H distances/angles**  across **multiple MD replicates**. Export publication-ready plots and tidy CSVs.

---

## Overview

This notebook analyzes MD trajectories to characterize:
- **Aromatic ring–H geometry** for residues **4, 10, 19, 20** vs **residue 22 (N/H)**:
  - **Distance** (ring centroid → H/N) and **angle** (to ring normal)
  - Filters events (default): **distance ≤ 5 Å** and **angle ≤ 60° or ≥ 120°**


It supports **three replicates** out-of-the-box and produces:
- `scatter.png` (distance–angle overlay),  
- `histogram.png` (distance distribution, % per replicate),  
- `histogram_g.png` (Gly O–H contact % by residue),  
- `Run1/2/3.csv` and `Run_All1/2/3.csv` (per-run and combined tables).

---
# Requirements for the IDP analysis pipeline
# Install with: pip install -r requirements.txt

numpy
MDAnalysis
pandas
matplotlib
seaborn
scipy
scikit-learn
requests
nglview
ipywidgets

# Optional (not required for core scripts but useful for notebooks)
jupyterlab
The full requirements list used are provided along with this repository in requirements_full.txt


---


You just need to upload the trajectories with respective gro file. You can use the E22G or WT version and comment the other when you are running the pipeline.
