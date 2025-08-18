# Distance & Angle — MD Replicate Geometry Analyzer (Colab-Ready)

This project provides a **Google Colab–friendly workflow** to quantify **aromatic ring–H geometries** and **short O–H contacts** across **multiple MD replicates**. It is built on **MDAnalysis**, **NumPy/Pandas**, and **Matplotlib**.

**What it does**
- Loads **3 MD replicates** (example: `E22G/MD.gro` with `E22G/3uMD*_noPBC.xtc`).
- For aromatic residues **4, 10, 19, 20**, computes per-frame:
  - Distance from **ring centroid → residue 22 (N/H)**
  - Angle between **centroid→H vector** and the **ring normal**
- Filters events (example thresholds in notebook): **distance ≤ 5 Å** and **angle ≤ 60° or ≥ 120°**.
- Aggregates results per run and **exports CSVs** (`Run1/2/3.csv`, `Run_All1/2/3.csv`).
- Tallies **Gly O–H contacts** (residues 9, 22, 25, 29, 33, 37, 38) using **2.61 Å** cutoff and
  renders a per-replicate **bar chart**.

**Outputs**
- `scatter.png` — Distance vs angle (per replicate overlay)
- `histogram.png` — Binned distance distribution for ring-H events
- `histogram_g.png` — Gly O–H contact occurrence (%) by residue
- `Run*.csv`, `Run_All*.csv` — Clean tables for stats/ML
