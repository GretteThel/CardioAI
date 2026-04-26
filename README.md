# CardioAI

CardioAI is a reproducible ECG classification workflow developed for PTB-XL in-domain evaluation and PTB Diagnostic inference-only external validation. The project includes standardized preprocessing, beat tokenization, CNN and hybrid CNN–Transformer modeling, evaluation, explainability, and a Streamlit-based research demo.

## Contents
- `notebooks/`: Colab/Jupyter notebooks used for training, evaluation, and figure generation
- `app/`: Streamlit prototype
- `configs/`: experiment configuration files
- `results/`: selected figures, tables, and sample outputs
- `docs/`: artefact manifest and reproduction notes

## Datasets
This repository does not redistribute PTB-XL or PTB Diagnostic data. Please obtain them from the official PhysioNet sources and place them in your local data directory.

## Reproducibility
1. Install dependencies from `requirements.txt`
2. Download PTB-XL and PTB Diagnostic from the official sources
3. Update dataset paths in the config files
4. Run preprocessing, tokenization, training, and evaluation notebooks in order

## Notes
This repository is for research and educational use only. It is not intended for clinical deployment.
