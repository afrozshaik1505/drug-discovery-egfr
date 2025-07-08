
# 📄 Drug Discovery Project – Ligand-Based Screening Documentation

## 👤 Author
Afroz Shaik

## 📅 Date
July 7–8, 2025

## 📁 Notebook
`Drug_Discovery_Notebook.ipynb`

---

## 🎯 Project Goal
To develop a simple ligand-based drug screening workflow using ChEMBL bioactivity data for a specific protein target and classify compounds as active or inactive based on their IC₅₀ values.

---

## 🧪 Target Protein Used

- **Target Name:** Epidermal Growth Factor Receptor (EGFR)
- **ChEMBL Target ID:** `CHEMBL284`

This protein is a well-known cancer target. All ligand activity data in this project is related to this specific protein.

---

## 💊 Ligands Used – Explained

The ligand dataset was retrieved from ChEMBL for the target protein EGFR (CHEMBL284). Each ligand includes an IC₅₀ value and is classified as **active** (IC₅₀ < 1000 nM) or **inactive** (≥ 1000 nM).

### 🧬 A few example ligands from the dataset:

1. `"CC(=O)Oc1ccccc1C(=O)O"` – **Aspirin** (a general anti-inflammatory drug; not EGFR-specific, may appear due to wide screening)
2. `"CC1=CN(C(=O)NC1=O)CO"` – **Allopurinol-like compound** (used for gout; likely appears due to broad screening)
3. `"COC1=CC2=C(C=C1)N=C(N=C2NC3=CC=C(C=C3)F)OC"` – **Gefitinib**, a known and specific **EGFR inhibitor** used in cancer therapy

These molecules were represented using SMILES format and converted into chemical descriptors using RDKit.

> 📝 Note: The dataset contains many more ligands; these are just a few representative examples.

---

## ⚙️ Workflow Summary

1. Queried ligand activity data from ChEMBL for `CHEMBL284`
2. Filtered based on IC₅₀ values and labeled compounds as active/inactive
3. Converted SMILES strings into molecular descriptors using RDKit
4. Trained a machine learning model to predict ligand activity (classification)

---

## 🛠️ Libraries Used

- `chembl_webresource_client`
- `RDKit`
- `pandas`, `numpy`
- `scikit-learn`
- `matplotlib`, `seaborn`

---

## 📂 Project Files

- `Drug_Discovery_Notebook.ipynb` – Jupyter notebook with full code and workflow
- `results.tar.gz` – SwissDock output (to be used later for visualization)
- `README.md` – this documentation file

---

## ✅ Project Status

| Task                               | Done? |
|------------------------------------|-------|
| ChEMBL data retrieval               | ✅    |
| Ligand structure processing         | ✅    |
| Feature extraction and labeling     | ✅    |
| Classification model built          | ✅    |
| Docking submitted to SwissDock      | ✅    |
| Docking visualization (Mol*/PyMOL)  | ❌    |

---

## 🚀 Next Steps

- Extract and visualize docked ligand poses using Mol* Viewer or PyMOL
- Compare docked pose of Gefitinib with known EGFR binding site
- Perform docking with other inhibitors and compare scores

---
