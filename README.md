# AI and Drug Discovery Course 2026: QSAR Modeling for SARS-CoV-2 MPRO
**Target Name:** Replicase polyprotein 1ab (SARS-CoV-2 3CL-Pro protease)  
**ChEMBL ID:** [CHEMBL4523582](https://www.ebi.ac.uk/chembl/target_report_card/CHEMBL4523582/)

---

## 🧬 Project Overview
This repository documents a systematic Quantitative Structure-Activity Relationship (QSAR) study. The objective is to characterize the chemical space of known inhibitors of the SARS-CoV-2 main protease (MPRO) and prepare a high-quality feature set for predictive machine learning modeling.



---

## 🛠️ Implementation Phases

### Phase 1: Data Collection & Curation
* **Source:** ChEMBL Database.
* **Retrieval:** Fetched 5,444 bioactivity records using the ChEMBL web service API.
* **Cleaning:** Standardized $IC_{50}$ measurements to nM, removed missing values, and converted values to $pIC_{50}$.
* **Classification:** Compounds categorized into **Active** ($pIC_{50} \geq 6$), **Intermediate**, and **Inactive** ($pIC_{50} < 6$).
* **Output:** A curated set of 2,994 molecules (excluding intermediates).

### Phase 2: Exploratory Data Analysis (EDA)
* **Lipinski Descriptors:** Calculated Molecular Weight (MW), LogP, Hydrogen Bond Donors (HBD), and Hydrogen Bond Acceptors (HBA).
* **Statistical Analysis:** A Mann-Whitney U test was performed to compare active and inactive classes.
* **Key Findings:** All four Lipinski descriptors were found to be **statistically significant ($p < 0.05$)**. 
* **Insight:** Active inhibitors generally possess higher lipophilicity and larger molecular size, critical for effective binding within the MPRO catalytic site.



### Phase 3: Molecular Descriptor & Fingerprint Calculation
* **Tool:** PaDEL-Descriptor (via the `padelpy` wrapper).
* **Fingerprint Type:** **PubChem Fingerprints** (881 bits).
* **Rationale:** PubChem fingerprints provide a standardized binary representation of 881 specific structural fragments. This allows for high-resolution structural mapping, essential for training robust machine learning algorithms.



---

## 📂 Repository Structure
* **`notebooks/`**: Contains curation, EDA, and fingerprint calculation notebooks.
* **`data/`**: Preprocessed datasets and generated fingerprints (`df_lipinski.csv`, `pubchem_fingerprints.csv`).
* **`results/`**: Statistical summaries, visualization plots, and the Summary Report PDF.

---

> "The heart of the discerning acquires knowledge, for the ears of the wise seek it out." — **Proverbs 18:15**
