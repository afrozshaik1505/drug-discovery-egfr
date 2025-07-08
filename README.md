# drug-discovery-egfr
A beginner-friendly ligand-based drug discovery project using ChEMBL data for EGFR. Includes data extraction, molecular descriptor generation, and activity prediction using machine learning. Notebook runnable on Google Colab.
## 🔗 Open in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/afrozshaik1505/drug-discovery-egfr/blob/main/Drug_Discovery_Notebook.ipynb)

📄 Drug Discovery Project – Ligand-Based Screening Documentation
👤 Author
Afroz Shaik

📁 Notebook
Drug_Discovery_Notebook.ipynb

🎯 Project Goal
To develop a simple ligand-based drug screening workflow using ChEMBL bioactivity data for a specific protein target and classify compounds as active or inactive based on their IC₅₀ values.

🧪 Target Protein Used
Target Name: Epidermal Growth Factor Receptor (EGFR)

ChEMBL Target ID: CHEMBL284

This protein is a well-known cancer target. All ligand activity data in this project is related to this specific protein.

💊 Ligands Used – Explained
The ligand dataset was retrieved from ChEMBL for the target protein EGFR (CHEMBL284). Each ligand includes an IC₅₀ value and is classified as active (IC₅₀ < 1000 nM) or inactive (≥ 1000 nM).

🧬 A few example ligands from the dataset:
"CC(=O)Oc1ccccc1C(=O)O" – Aspirin
(a general anti-inflammatory drug; not EGFR-specific, may appear due to wide screening)

"CC1=CN(C(=O)NC1=O)CO" – Allopurinol-like compound
(used for gout; likely appears due to broad screening)

"COC1=CC2=C(C=C1)N=C(N=C2NC3=CC=C(C=C3)F)OC" – Gefitinib
(a known and specific EGFR inhibitor used in cancer therapy)

📝 Note: The dataset contains many more ligands; these are just a few representative examples.

⚙️ Workflow Summary
Queried ligand activity data from ChEMBL for CHEMBL284

Filtered based on IC₅₀ values and labeled compounds as active/inactive

Converted SMILES strings into molecular descriptors using RDKit

Trained a machine learning model to predict ligand activity (classification)

🛠️ Libraries Used
chembl_webresource_client

RDKit

pandas, numpy

scikit-learn

matplotlib, seaborn

📂 Project Files
Drug_Discovery_Notebook.ipynb – Jupyter notebook with full code and workflow

results.tar.gz – SwissDock output (to be used later for visualization)

README.md – This documentation file

✅ Project Status
Task	                          Done?
ChEMBL data retrieval	          ✅
Ligand structure processing	    ✅
Feature extraction and labeling	✅
Classification model built	    ✅
Docking submitted to SwissDock	✅
