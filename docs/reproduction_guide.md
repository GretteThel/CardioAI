# Reproduction Guide

## 1. Purpose

This guide describes the general steps required to reproduce the CardioAI workflow from the main research repository.

The workflow supports:

- PTB-XL in-domain preprocessing and evaluation
- beat-level tokenization
- CNN and hybrid CNN–Transformer experimentation
- multilabel and binary evaluation
- explainability analysis
- inference-only external validation on PTB Diagnostic

---

## 2. Recommended Environment

Recommended setup:

- Python 3.10+
- Google Colab or local Jupyter environment
- GPU recommended for model training and evaluation

The CardioAI workflow was primarily developed and executed in Google Colab. Users reproducing the workflow in a local Jupyter environment should ensure that package versions, file paths, and runtime settings are aligned with the repository configuration.

If using Google Colab, verify that:

- Google Drive is mounted correctly if files are stored there
- dataset paths are updated before execution
- package versions match the repository requirements

---

## 3. Install Dependencies

Install the required packages from:

```bash
pip install -r requirements.txt
````

If you are using Colab, you may need to restart the runtime after installing pinned versions.

---

## 4. Obtain the Datasets

Download the datasets from their official sources:

* PTB-XL
* PTB Diagnostic ECG Database

This repository does not redistribute the raw datasets.

After download, place the data in a local or cloud-accessible directory and update the dataset paths in the notebook or configuration files.

---

## 5. Configure Dataset Paths

Before running the workflow, update any dataset path variables to match your environment.

For cleaner reuse, environment-variable-based configuration is preferred, for example:

```python
import os
DATA_ROOT = os.environ.get("CARDIOAI_DATA_ROOT", "/path/to/datasets")
```

Avoid committing personal Drive paths or machine-specific local paths to the repository.

---

## 6. Recommended Workflow Order

Run the workflow in the following order:

1. Data loading and validation
2. Preprocessing and signal standardization
3. R-peak detection and beat tokenization
4. Patient-wise train/validation/test split setup
5. Model training
6. Evaluation and metric generation
7. Explainability analysis
8. Inference-only external validation on PTB Diagnostic
9. Export of selected figures and tables

If multiple notebooks are used, keep the execution order consistent with the project workflow.

---

## 7. Reproducibility Practices

For better reproducibility:

* use fixed random seeds where specified
* keep preprocessing settings consistent across PTB-XL and PTB Diagnostic
* separate raw data from generated artefacts
* store figures, tables, and outputs in structured folders
* avoid mixing temporary experiment files with final artefact files

If a notebook writes outputs, ensure that output directories exist before running.

---

## 8. Explainability and Evaluation Notes

The workflow may include explainability analysis such as:

* Integrated Gradients
* GradientSHAP
* related attribution outputs used for model auditing

Evaluation outputs may include:

* accuracy
* precision
* recall
* specificity
* F1-score
* AUROC
* AUPRC
* selected bootstrap confidence intervals
* confusion matrices and supporting plots

---

## 9. External Validation Scope

The external validation component is designed as an inference-only transfer setting using PTB Diagnostic.

This means:

* no retraining is performed on PTB Diagnostic
* preprocessing and input formatting should remain aligned with the PTB-XL-trained workflow
* results should be interpreted within the defined scope of the project, not as broad clinical generalization claims

---

## 10. Streamlit Demo

The Streamlit-based research demo is maintained in a separate CardioAI_streamlit repository.

That repository is distinct from the main CardioAI workflow repository and should be treated as a related demonstration artefact rather than the core experimental pipeline.

---

## 11. Troubleshooting

Common issues include:

* incorrect dataset paths
* missing files after Drive remounting
* package version mismatches
* runtime restart requirements after installation
* missing output directories
* notebook cells executed out of order

If results look inconsistent, first verify:

* dataset path correctness
* package versions
* seed settings
* workflow order
* preprocessing consistency

---

## 12. Final Note

This repository is intended for:

* research transparency
* academic reproducibility
* educational use

It is not intended for clinical deployment or medical decision-making.
