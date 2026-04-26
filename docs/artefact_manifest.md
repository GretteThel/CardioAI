# Artefact Manifest

## Project

**CardioAI** is a reproducible ECG classification workflow developed for PTB-XL in-domain evaluation and PTB Diagnostic inference-only external validation.

This artefact accompanies the CardioAI thesis/project and documents the materials included in the main research repository.

---

## Included in this Repository

The main CardioAI repository contains the **core research workflow** and supporting artefact materials, including:

- Colab/Jupyter notebooks for:
  - preprocessing
  - signal standardization
  - beat extraction / tokenization
  - training
  - evaluation
  - figure generation
- configuration files for reproducibility and experiment setup
- selected figures and tables used in the thesis
- thesis-ready appendix assets
- documentation supporting research transparency and reproduction

---

## Repository Scope

This repository is intended to represent the **experimental and reproducibility-oriented component** of the CardioAI project.

It covers:

- PTB-XL in-domain workflow
- inference-only external validation on PTB Diagnostic
- explainability-related analysis
- selected saved outputs relevant to the report

It does **not** function as a clinical system or production medical tool.

---

## Related Repository

The **Streamlit-based research demonstration app** is maintained in a **separate repository**.

That separate repository contains the user-facing prototype for:

- ECG viewing
- prediction display
- explanation visualization

The separation is intentional so that:

- the **main CardioAI repository** remains focused on the research workflow and artefact documentation
- the **Streamlit repository** remains focused on the demonstration interface and app-specific deployment structure

---

## Not Included

The following items are intentionally excluded from this repository:

- raw PTB-XL dataset files
- raw PTB Diagnostic dataset files
- large intermediate caches
- large temporary artefacts
- private credentials, API keys, or access tokens
- sensitive local/cloud storage paths
- full deployment materials for the separate Streamlit application

---

## Data Access

Users must obtain PTB-XL and PTB Diagnostic data directly from their **official sources** and place them in an appropriate local or cloud data directory before running the workflow.

This repository does not redistribute dataset contents.

---

## Reproducibility Notes

Reproducibility depends on:

- correct dataset acquisition from the official sources
- matching Python package versions
- consistent preprocessing settings
- stable path configuration
- use of the notebooks/configuration files in the intended workflow order

Refer to `docs/reproduction_guide.md` for step-by-step reproduction guidance.

---

## Intended Use

This artefact is provided for:

- academic documentation
- research transparency
- reproducibility support
- educational demonstration

It is **not intended for clinical decision-making or deployment**.
