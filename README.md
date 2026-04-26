# CardioAI

CardioAI is a reproducible ECG classification workflow developed for **PTB-XL** in-domain evaluation and **PTB Diagnostic** inference-only external validation. The project integrates standardized preprocessing, beat tokenization, controlled comparison between a CNN-only baseline and a hybrid CNN–Transformer, evaluation, explainability analysis, and thesis artefact materials.

This repository contains the **core research workflow** used in the CardioAI study. It is intended for **research transparency, reproducibility, and educational demonstration**.

---

## Overview

The CardioAI workflow was designed to support:

- standardized ECG preprocessing
- beat-level tokenization
- patient-wise train/validation/test evaluation on PTB-XL
- inference-only cross-dataset transfer to PTB Diagnostic
- explainability and model-auditing analysis
- organized export of selected figures, tables, and artefact materials

Within the implemented thesis scope, the workflow supports:

- **binary normal-vs-abnormal classification** on PTB-XL
- **multilabel / five-superclass classification** on PTB-XL
- **external MI-vs-healthy inference-only evaluation** on PTB Diagnostic
- **explainability analysis** using methods such as Integrated Gradients and GradientSHAP

---

## Repository Structure

```text
CardioAI/
├── README.md
├── .gitignore
├── requirements.txt
├── notebooks/
│   └── CardioAI_workflow.ipynb
├── configs/
├── results/
│   ├── figures/
│   └── tables/
├── docs/
│   ├── artefact_manifest.md
│   └── reproduction_guide.md
└── appendix_assets/
````

### Main contents

* **`notebooks/`**
  Colab/Jupyter notebooks used for preprocessing, tokenization, training, evaluation, and figure generation.

* **`configs/`**
  Configuration files for experiment settings, paths, and reproducibility-related parameters.

* **`results/`**
  Selected output figures, tables, and sample artefacts used in the thesis and supporting analysis.

* **`docs/`**
  Artefact documentation, including the artefact manifest and reproduction notes.

* **`appendix_assets/`**
  Thesis-ready figures and supplementary artefact materials.

---

## Related Repository

The **Streamlit-based research demo** is maintained in a separate repository.

That separate repository contains the user-facing prototype for:

* ECG viewing
* prediction display
* explanation visualization

This repository focuses on the **core research pipeline**, while the Streamlit repository is kept separate to preserve a clear distinction between:

* the **experimental/reproducibility workflow**, and
* the **demonstration-oriented application**

---

## Datasets

This repository **does not redistribute** PTB-XL or PTB Diagnostic ECG data.

Please obtain the datasets from their **official sources** and place them in your local or cloud data directory before running the notebooks.

### Datasets used

* **PTB-XL** — primary development dataset for in-domain training and evaluation
* **PTB Diagnostic ECG Database** — independent cohort used for inference-only external validation

---

## Reproducibility

### Recommended environment

* Python 3.10+
* Google Colab or local Jupyter environment
* GPU recommended for model training and evaluation

### General workflow

1. Install dependencies from `requirements.txt`
2. Download PTB-XL and PTB Diagnostic from the official sources
3. Update dataset paths in the notebook or configuration files
4. Run preprocessing and signal standardization
5. Run beat extraction / tokenization
6. Run training and evaluation
7. Run explainability analysis
8. Run inference-only external validation on PTB Diagnostic
9. Export selected figures and tables

### Notes on reproducibility

* Fixed random seeds should be used where specified in the notebook/configuration
* Preprocessing settings should remain consistent across PTB-XL and PTB Diagnostic
* Raw data should be kept separate from generated artefacts
* Large intermediate caches and temporary files are intentionally excluded from the repository

---

## Included in this Repository

* preprocessing and tokenization workflow notebooks
* training and evaluation notebooks
* experiment configuration files
* selected figures and tables used in the thesis
* supporting artefact documentation
* thesis pipeline and appendix materials

---

## Not Included

* raw PTB-XL or PTB Diagnostic data
* large cached artefacts
* private credentials, tokens, or access keys
* full deployment assets for the separate Streamlit app repository

---

## Intended Use

This repository is provided for:

* research reproducibility
* academic documentation
* educational demonstration

It is **not intended for clinical deployment or medical decision-making**.

---

## Citation / Project Context

If this repository is used in connection with the CardioAI thesis or related academic work, please cite or reference the associated thesis/report as appropriate.

---

## Disclaimer

CardioAI is a **research and educational project**. The models, analyses, and outputs in this repository are not validated for clinical use and must not be used as a substitute for professional medical interpretation.

