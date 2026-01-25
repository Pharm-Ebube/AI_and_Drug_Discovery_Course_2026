# AI_and_Drug_Discovery_Course_2026

# Assignment 2: QSAR Data Curation Using ChEMBL

# Selected Target
**Target Name:** Replicase polyprotein 1ab (SARS-CoV-2 3CL-Pro protease)
**ChEMBL Target ID:** CHEMBL4523582
* **Number of Bioactivity Records:** 5,289 (Curated)

## Data Curation Workflow
1. **Data Retrieval:** Fetched 5,444 bioactivity records using the ChEMBL web service API.
2. **Bioactivity Filtering:** Filtered for IC50 measurements and removed entries with missing values.
3. **Preprocessing:** Standardized bioactivity units to nM.
    * Classified compounds into active, intermediate, and inactive categories.
4. **Storage:** Saved the curated dataset (5,289 records) as `bioactivity_preprocessed_data.csv`.
