# ARQUE: Anisotropic Richness Quality Estimation for NR-IQA
Official repository for the ARQUE NR-IQA framework.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

Official repository for the paper: **"ARQUE: A Hybrid Multi-Expert Framework for No-Reference Image Quality Assessment Using Curvature Analysis", 2026**.

ARQUE is a No-Reference Image Quality Assessment (NR-IQA) framework that shifts the paradigm from Generalist Statistics to Specialist Physics. By adopting a Mixture of Experts (MoE) architecture, ARQUE employs specific filters calibrated to the physical curvature of artifacts, proving highly robust against "Data Leakage" (content overlap) in training datasets.

## 📄 Abstract

This work introduces ARQUE (Anisotropic Richness Quality Estimation), a No-Reference Image Quality Assessment (NR-IQA) framework based on a "Mixture of Experts" (MoE) architecture. The method relies on the Anisotropic Texture Richness (ATR) metric, which derives structural integrity measures from bi-directional curvature maps. Unlike conventional approaches that frequently benefit from global statistics and content overlap, the proposed system implements a physically grounded two-stage hybrid model. A probabilistic classifier first identifies the distortion type, followed by a weighted fusion of specialist Support Vector Regressors (SVRs) operating on a 21-dimensional feature space. Experimental validation employing a rigorous 10-fold cross-validation protocol on the LIVE, CSIQ, and TID2013 datasets indicates the stability of the proposed method. In the content-independent "Standard" scenario, ARQUE yields a Pearson Linear Correlation Coefficient (PLCC) of 0.901 on LIVE and 0.868 on TID2013, surpassing the optimized BRISQUE baseline (0.708 and 0.821, respectively). Moreover, while the baseline performance declines by approximately 25% when content overlap is removed, ARQUE exhibits stability with a variation of less than 3%, suggesting a reduced dependency on data leakage compared to statistical approaches.

## 📂 Repository Structure

*   `datasets/`: Instructions for downloading and structuring the LIVE, CSIQ, and TID2013 datasets (no images are hosted here due to licensing).
*   `benchmark/`: Source code to reproduce the rigorous "Standard No-Leak" cross-validation analysis against the BRISQUE baseline.
*   `app/`: Command-line interface (CLI) to run ARQUE on your own images and obtain quality scores and distortion probabilities using pre-trained weights. *(Coming soon)*

## ⚙️ Installation

1. Clone this repository:
   ```bash
   git clone [https://github.com/](https://github.com/)[seu-usuario]/ARQUE-IQA.git
   cd ARQUE-IQA
