
# ARQUE Benchmark Analysis

This directory contains the Jupyter Notebooks used to reproduce the rigorous 10-fold (and 5-fold) cross-validation results presented in the ARQUE paper.

## Features

* **Interactive Evaluation:** Full transparency of the pipeline, allowing step-by-step verification of data loading, feature extraction, and metric aggregation.
* **Dual Execution Engine:** The mathematical core supports both CPU (via Numba) and GPU (via CuPy) acceleration.
* **Rigorous "No-Leak" Protocol:** Ensures strict content separation to prevent data leakage during training.
* **Stratified Results:** Outputs detailed PLCC, SROCC, and RMSE metrics per distortion type (e.g., White Noise, JPEG, JP2K, Gaussian Blur).

## Requirements

To run these notebooks locally, install the standard dependencies:

`pip install jupyter numpy pandas scipy scikit-learn opencv-python numba`

*(Optional)* For maximum performance via GPU acceleration, ensure you have a CUDA-enabled device and install CuPy:

`pip install cupy-cuda11x` *(Adjust according to your local CUDA version)*

## Usage

You can view the pre-computed results, tables, and charts directly by clicking on the .ipynb files above. GitHub renders them natively.

To execute the code locally:

1. Ensure the databases are properly structured in the `../datasets/` directory (see the root instructions).
2. Start your Jupyter environment using the command: `jupyter notebook`
3. Open the desired notebook and run all cells.
