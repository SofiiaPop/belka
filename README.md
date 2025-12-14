# BELKA: Molecule–Protein Binding Prediction

This repository contains our course project focused on predicting ligand–protein binding using different molecular representations and machine learning models.

The project is based on the [BELKA Kaggle competition dataset](https://www.kaggle.com/competitions/leash-BELKA) and explores classical ML approaches, graph neural networks and ensemble techniques.


## Problem Description
The goal is to predict whether a given small molecule binds to a specific protein.
This is a challenging task due to:
- very large dataset size,
- strong class imbalance,
- distribution shift between training and test data,
- complex molecular structures.

Evaluation metric: Average Precision (AP).


## Data
We use the BELKA dataset provided via Kaggle:
- Molecular structures represented as SMILES
- Target proteins
- Binary binding labels

Due to dataset size, experiments are conducted on representative balanced subsets.

> Raw data files are not included in this repository.


## Methods
We explored several approaches:

### Baselines
- ECFP fingerprints + Random Forest
- Logistic Regression / MLP on molecular encodings

### Molecular Representations
- ECFP (Morgan fingerprints)
- One-hot encodings
- Graph-based molecular representations (RDKit)

### Graph Neural Network
- Molecular graphs built using RDKit
- Node and edge features
- 5-fold cross-validation
- OOF evaluation

### Ensemble
- Rank-based and mean-based ensembling of best models
- Combination of tabular models and GNN predictions


## Experiments
Key experiments include:
- Comparison of different molecular encodings
- Cross-validation vs Kaggle leaderboard performance
- Error analysis (false positives / false negatives)
- Ensemble strategies


## Repository Structure
