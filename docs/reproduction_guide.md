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

If using Google Colab, verify that:

- Google Drive is mounted correctly if files are stored there
- dataset paths are updated before execution
- package versions match the repository requirements

---

## 3. Install Dependencies

Install the required packages from:

```bash
pip install -r requirements.txt
