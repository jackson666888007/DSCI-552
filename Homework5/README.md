# DSCI 552 - Homework 5

This homework covers decision trees and regression models.

## Files

- `HW5.ipynb`: Code, plots, results, and answers.
- `data/`: Data files used by the notebook.
- `requirements.txt`: Python packages needed to run the code.

## Part 1: Decision Trees

I use the Acute Inflammations data to build a decision tree.
I combine the two labels into four classes.

I plot the tree, write IF-THEN rules, and use cost-complexity
pruning to make the tree smaller.

The smaller tree is easier to read, but it makes more errors
on the training data.

## Part 2: Regression

I use the Communities and Crime data.
The first 1,495 rows are used for training.
The remaining 499 rows are used for testing.

I remove the nonpredictive columns and fill missing values
with training medians.

I study correlations and the coefficient of variation.
Then I compare OLS, Ridge, LASSO, PCR, and XGBoost.

I use five-fold cross-validation to choose model settings.
Data preparation is fitted inside each training fold.

XGBoost has the lowest test MSE in this comparison.
Ridge has the lowest test MSE among the linear models.

## How to Run

1. Open a terminal in the `Homework5` folder.
2. Use a Python environment with the required packages.
3. Run `python -m pip install -r requirements.txt`.
4. Run `python -m notebook`.
5. Open `HW5.ipynb`.
6. Choose Restart Kernel and Run All Cells.

Keep the data files in the `data` folder.

## Data Sources

- [Acute Inflammations](https://archive.ics.uci.edu/dataset/184/acute+inflammations)
- [Communities and Crime](https://archive.ics.uci.edu/dataset/183/communities+and+crime)
