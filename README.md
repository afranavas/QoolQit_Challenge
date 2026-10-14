# QoolQit Challenge: Quantum Reservoir Computing for Molecular Property Prediction

## Overview

This project investigates the reproduction and validation of quantum reservoir computing (QRC) experiments for molecular property prediction using **QoolQit**.

The work focuses on Activity 4 (ACT4) from the Merck Molecular Activity Challenge dataset, using a 200-record subset. Saved quantum reservoir embeddings are compared against reference embeddings to evaluate numerical agreement and investigate differences between the two outputs.

## Objectives

- Explore quantum reservoir computing for molecular property prediction.
- Work with QoolQit-generated molecular embeddings.
- Compare generated embeddings with reference outputs.
- Evaluate numerical differences using error metrics and correlation analysis.
- Document the experimental workflow and reproducibility limitations.

## Repository Structure

```text
QoolQit_Challenge/
├── README.md
├── requirements.txt
├── submission/
│   ├── QoolQit_Molecular_QRC_Reproduction.ipynb
│   └── QoolQit_Challenge_Two_Slides.pdf
├── qoolqit/
│   └── batch_embeddings_act4_sub1_v3/
│       ├── train_embeddings.csv
│       ├── test_embeddings.csv
│       ├── train_embeddings.npy
│       ├── test_embeddings.npy
│       ├── train_ids.csv
│       └── test_ids.csv
├── reference_data/
│   ├── merck_train_embeddings_recs200rec_sub1act4v3.csv
│   └── merck_test_embeddings_recs200rec_sub1act4v3.csv
├── classical_benchmark.py
└── classical_benchmark_results.csv
```

*The structure above describes the intended submission layout. Include the optional classical benchmark files only if they are part of the final experiment.*

## Experimental Configuration

| Parameter | Configuration |
|---|---|
| Framework | QoolQit |
| Method | Quantum Reservoir Computing |
| Dataset | Merck Molecular Activity Challenge |
| Molecular activity task | Activity 4 (ACT4) |
| Subset size | 200 records |
| Split | 160 training records, 40 test records |
| Subset version | Subsample 1, version 3 |
| Embedding dimension | 1,710 features per record |

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/afranavas/QoolQit_Challenge.git
cd QoolQit_Challenge
```

### 2. Create a Python environment

```bash
python3 -m venv .venv
source .venv/bin/activate
```

On Windows, activate the environment using:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Run the notebook

Open `submission/QoolQit_Molecular_QRC_Reproduction.ipynb` in Jupyter Notebook, JupyterLab, or an appropriate notebook environment.

Ensure that all input files are present in the repository and that the paths used in the notebook match the directory structure above.

## Evaluation and Validation

The validation workflow compares the saved QoolQit embeddings with the corresponding reference embeddings for the training and test splits.

The analysis includes:

- Shape and dimensionality checks.
- Numerical consistency checks between saved CSV and NumPy outputs.
- Mean absolute error (MAE).
- Root mean squared error (RMSE).
- Maximum absolute difference.
- Pearson correlation coefficient.

These metrics help quantify agreement between the generated and reference embeddings.

## Reproducibility Notes

The current work should be treated as an experimental reproduction and validation effort. Numerical agreement with the reference embeddings has **not yet been established**.

The repository includes saved outputs to support analysis without requiring every quantum reservoir simulation to be rerun. A complete reproduction from the original inputs requires the appropriate source data, compatible dependencies, documented configuration, and any necessary simulation steps.

Results should be interpreted as comparisons between the available outputs, not as evidence of quantum advantage.

## Limitations

- Numerical differences between generated and reference embeddings require further investigation.
- Reproducing the full simulation may require additional computational resources and time.
- Results from one molecular activity task and one data subset do not establish general performance across molecular property prediction tasks.

## References

- Beaulieu et al., *Robust Quantum Reservoir Computing for Molecular Property Prediction*, arXiv:2412.06758.
- QoolQit repository: https://github.com/QuEraComputing/robust-qrc-molecular-prediction

## Author

**Afra Navas**
**Qclairvoyance Quantum Labs**

QoolQit Challenge — Quantum Reservoir Computing for Molecular Property Prediction
