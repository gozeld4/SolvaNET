# SolvaNET
## This is the final project for ML4MolEng Spring 2024

This project involves applying supervised machine learning to predict solvation free energies and partition coefficients of solute-solvent pairs, utilizing data from the Solv@TUM database.

## Project Overview

The goal is to develop machine learning models that predict partition coefficients (logK) from molecular features. The dataset contains solvent and solute information in SMILES format, and molecular properties like molecular weight, dipole moment, and polarizability are provided for feature engineering.

### Key Objectives:
1. **Data Preprocessing**:
   - Load and preprocess solute and solvent data, handle missing values, and build feature sets by combining molecular descriptors.
   - Extract additional features using RDKit and Morgan Fingerprints to enhance molecular representation.
2. **Modeling Approaches**:
   - Baseline models using **Linear Regression** and **MLP Regression** to predict logK.
   - Advanced machine learning models (e.g., Random Forests, Gradient Boosted Trees, Neural Networks) to improve prediction performance.
3. **Model Evaluation**: Use **5-fold cross-validation** and Kaggle competition metrics to evaluate model performance using R² score.

## Dataset

The dataset consists of:
- **solvation_train.csv**: Contains training data with solvent SMILES, solute SMILES, partition coefficients (logK), and solvation free energies (ΔG).
- **solvation_test.csv**: Contains test data for solute-solvent pairs.
- **mol_prop.csv**: Provides molecular properties (molecular weight, dipole moment, polarizability) for feature generation.

## Solution Structure

SolvaNET.ipynb/: The jupyter notebook that includes all code.
README.md/: This file.

## Conclusion

The best performing model was gradient boosting model that includes RDkit and Morgan finerprint data

## References

1. **Kroger et al.** Prediction of solvation free energies of ionic solutes in neutral solvents. *The Journal of Physical Chemistry A* (2020).
2. **Subramanian et al.** Multisolvent models for solvation free energy predictions using 3D-RISM hydration thermodynamic descriptors. *Journal of Chemical Information and Modeling* (2020).
3. **Hille et al.** Generalized molecular solvation in non-aqueous solutions. *The Journal of Chemical Physics* (2019).
4. **Lim & Jung**. Delfos: deep learning model for prediction of solvation free energies. *Chemical Science* (2019).



---

