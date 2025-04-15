# Interactive Cascade Learning for User-Aware Personalization

This repository accompanies the research paper **"Efficient Interactive Cascade Learning for User-Aware Personalization in Edge Activity Recognition"**. The project introduces a personalized cascade strategy for activity recognition based on user interaction and confidence-aware model execution, applied in resource-constrained, edge-intelligent environments.

## Overview

The Python script provided in this repository implements the interactive cascade evaluation described in the paper. It simulates a leave-one-subject-out (LOSO) evaluation using the OHM dataset and supports stratified sampling, configurable confidence thresholds, and retraining using user-labeled instances.

## Files

- `Interactive_Model_Cascade_Experiment.ipynb`: Notebook containing the core implementation for the evaluation of the interactive cascade pipeline.

## Features

- Three-stage model cascade with confidence-based thresholds.
- Interactive labeling simulation based on prediction uncertainty.
- Support for different levels of user involvement (low, medium, high).
- Comparison of generic vs. personalized models.
- Aggregation and export of results across multiple algorithms and repetitions.

## Dataset

The system was evaluated on the **OHM (Office Hydration Monitoring)** dataset (**Repository link**: [https://zenodo.org/records/4681206](https://zenodo.org/records/4681206)):
- 10 users × 100 labeled sequences each.
- Sensor data (accelerometer + gyroscope) from bottle gestures.
- Split into 60% for simulated interaction and 40% for evaluation.

## Evaluation Protocol

- **Cross-validation**: Leave-One-Subject-Out (LOSO)
- **Resampling**: 100 repetitions with stratified sampling to preserve class balance.
- **Metrics**: Accuracy before and after personalization under both interactive (`M1+M2`) and non-interactive (`All M3`) cascade settings.


## Usage

Clone the repository, install the dependencies, and launch the notebook:

```bash
git clone https://github.com/OihaneGomez/Interactive_Model_Cascade
cd Interactive_Model_Cascade
pip install -r requirements.txt
jupyter notebook Interactive_Model_Cascade_Experiment.ipynb

