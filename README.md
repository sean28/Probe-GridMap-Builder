# 🧪 Probe GridMap Builder

This is a web-based tool for analyzing molecular dynamics trajectories (.trr or .nc) using AmberTools' `cpptraj` and generating grid-based spatial distribution maps for probe atoms. Output includes processed PDBs and clustering results, provided in a downloadable ZIP package.  👉 [Live Demo](https://sean28.github.io/MixMD/probe_gridmap_ui.html)


## ✅ Features

- Upload `.trr` or `.nc` trajectory files
- Grid map generation via `cpptraj`
- Cluster analysis and PDB annotation via `cluster.py`
- Automatic packaging of results (PDB + summary)

## 📦 Conda Environment Setup

This project is designed to run inside a Conda environment with **AmberTools** and **Flask**.

You can create the environment with the following steps:

```bash
# 1. Create a new environment
conda create -n amber python=3.12

# 2. Activate the environment
conda activate amber

# 3. Install required packages
conda install -c conda-forge ambertools flask pandas matplotlib scikit-learn parmed

# 4. Install additional pip packages
pip install pytraj amberutils sander pdb4amber packmol-memgen

```
## 🚀 Run the Server

```
conda activate amber
python probe-gridmap.py

```
open the http://127.0.0.1:8082 

## 📝 Usage

1. Upload your .trr or .nc trajectory file via the web interface.
2. Upload the corresponding .pdb file and choose probe atoms.
3. Submit the job, and download the result ZIP containing:
	•	nonortho.pdb
	•	nonortho_mark.pdb
	•	cluster_summary.txt
