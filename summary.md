# Bio-BERT & ESM-2 Protein Language Model (PLM) Featurizer & Screening Pipeline

A comprehensive Jupyter Notebook pipeline for protein target retrieval, embedding generation using transformer-based Protein Language Models (ESM-2 / Bio-BERT), chemical dataset ingestion, Tanimoto novelty filtering, and pharmacokinetic (SwissADME-style) profiling.

## 🚀 Key Pipeline Steps

1. **Target Protein Acquisition**: Automatically fetches sequences and metadata from **PDB** or **UniProt** based on user-defined gene symbols, PDB IDs, or raw sequences.
2. **Protein Language Modeling**: Loads lightweight pretrained transformer models (`facebook/esm2_t6_8M_UR50D`) to encode and process protein representations.
3. **Chemical Dataset Ingestion**: Dynamically pulls real-world chemical datasets (e.g., Delaney dataset) and maps candidate ligands to target receptors.
4. **Novelty Filtering**: Uses **RDKit** Morgan fingerprints and Tanimoto similarity metrics to filter out analogs against a user-defined reference drug.
5. **Publication-Grade Visualizations**: Generates high-resolution ranking charts and target-ligand binding confidence heatmaps (`matplotlib` & `seaborn`).
6. **Pharmacokinetic Profiler (SwissADME-style)**: Computes molecular weight, logP, Lipinski's Rule of Five violations, ESOL aqueous solubility (LogS), gastrointestinal (GI) absorption, and blood-brain barrier (BBB) permeation heuristics.

---

## 🛠️ Prerequisites & Installation

Ensure you have Python 3.8+ installed. Clone the repository and install the required dependencies:

```bash
# Clone the repository
git clone [https://github.com/your-username/bio-bert-plm-featurizer.git](https://github.com/your-username/bio-bert-plm-featurizer.git)
cd bio-bert-plm-featurizer

# Install required packages
pip install -r requirements.txt
