# MSPE49600 Project 04

Repository for MSPE49600 Project 04

## Overview

This project uses ANSYS Fluent and Gaussian Process Regression to evaluate the aerodynamic performance of a NACA 0015 airfoil over a range of wing angles. CFD simulations were automated through ANSYS Workbench and Python. The resulting drag and lift forces were used to train Gaussian Process models, evaluate prediction accuracy, and recommend a wing angle for future simulations. The objective was to identify wing angles that provide favorable aerodynamic efficiency measured using the drag-to-downforce ratio.

## Files Included

- run_airfoil_sweep.py
- cvanvoor_pr04_notebook.ipynb
- cvanvoor_pr04_cfd.csv
- README.md

## Python Packages

The notebook and scripts use:

- pandas
- numpy
- matplotlib
- scipy
- scikit-learn
- ansys-workbench-core

## Reproducing the Analysis

1. Open `cvanvoor_pr04_notebook.ipynb`.
2. Ensure the required Python packages are installed.
3. Place `cvanvoor_pr04_cfd.csv` in the same directory as the notebook.
4. Run the notebook cells from top to bottom.
5. The notebook will:
   - Load the CFD results
   - Build Gaussian Process models for drag and lift
   - Evaluate model accuracy
   - Generate prediction and variance plots
   - Produce the engineering recommendation

## Engineering Recommendation

The Gaussian Process models identified an angle of approximately 4.815° as having the lowest predicted drag-to-downforce ratio. A follow-up CFD simulation near 2° is recommended because the predictive variance is highest in that region, indicating greater model uncertainty. Additional CFD data near 2° would improve model confidence and help validate the surrogate model predictions. 

- This repository contains the final notebook, CFD dataset, and automation script used for Project 04.
