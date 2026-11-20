# SepHAR-Net

Code and reproducibility notebook for the paper:

**SepHAR-Net: A Lightweight Separable-Convolution Network for Efficient Human Activity Recognition**
Anika Rahman — Department of Computer Science and Engineering, Stamford University Bangladesh.

## Overview

SepHAR-Net is a compact (24,288-parameter) depthwise-separable convolutional–recurrent
network for human activity recognition from wearable inertial sensors. This repository
reproduces all experiments, tables, and figures in the paper, including:

- Leave-one-subject-out (LOSO) evaluation on **UCI HAR** (30 subjects) and **MotionSense**
  (24 subjects), with subject-level statistical testing.
- A fixed-split five-seed stability analysis.
- Model-efficiency metrics (parameters, storage, FLOPs).
- Figures 1–6.

## Contents

- `SepHAR-Net_Reproducibility.ipynb` — the full pipeline (data loading, models, evaluation, figures).
- `loso_results.json` — cached LOSO results on UCI HAR *(optional; lets you regenerate the figures
  without re-running the multi-hour evaluation)*.
- `loso_motionsense.json` — cached LOSO results on MotionSense.
- `requirements.txt` — Python dependencies.

## Datasets

- **UCI HAR** — UCI Machine Learning Repository, *Human Activity Recognition Using Smartphones*
  (doi:10.24432/C54S4K). Download `UCI HAR Dataset.zip` and upload it when prompted by the notebook.
- **MotionSense** — downloaded automatically by the notebook from the public repository.

## Running

Open `SepHAR-Net_Reproducibility.ipynb` in Google Colab (recommended; a GPU runtime is used) or in
Jupyter, and run the cells from top to bottom. The LOSO cells are computationally heavy (several hours
each) and are **resumable** — results are cached to JSON after every fold. To regenerate only the
figures, place the provided `loso_results.json` and `loso_motionsense.json` next to the notebook and
run Section 6.

## Requirements

Python 3 with TensorFlow/Keras, scikit-learn, SciPy, statsmodels, matplotlib, pandas, NumPy, and
Pillow (see `requirements.txt`).

## Citation

Manuscript under review at PLOS ONE; citation details will be added upon publication.
