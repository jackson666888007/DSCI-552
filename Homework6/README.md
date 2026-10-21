# DSCI 552 - Homework 6

## Files

- HW6.ipynb: Code, results, plots, and written answers.
- requirements.txt: Package versions used for this homework.

## Data

Extract the course data ZIP file. Put these two files in the data folder:

- data/aps_failure_training_set.csv
- data/aps_failure_test_set.csv

Keep the original CSV files, including their header lines.

## How to Run

This notebook was tested with Python 3.13.

Open a terminal in the Homework6 folder. Use a Python environment and install the packages:

```bash
python -m pip install -r requirements.txt
```

Start JupyterLab:

```bash
python -m jupyterlab
```

Open HW6.ipynb. Restart the kernel and run all cells in order.
Cross-validation may take several minutes.

## Methods

The notebook uses median imputation and keeps all 170 features for the models.
It compares Random Forest, a weighted Random Forest, and XGBoost models.
It also tests SMOTE.

For cross-validation, imputation, scaling, and SMOTE are fitted inside each training fold.
The test set is used for the final evaluation.

## XGBoost Implementation Note

The gblinear model is one global linear model.
The gbtree model uses boosted trees with a binary logistic objective.
Its reg_alpha parameter controls L1 regularization on leaf weights.
The selected SMOTE tree model has reg_alpha = 0, so its final fit has no L1 penalty.

Neither model fits a separate logistic regression at each node.
The model tree wording in the assignment needs clarification.

## Written Questions

The notebook also includes answers about Lasso, Ridge, tree predictions,
and the maximal margin classifier.
