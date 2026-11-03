# DSCI 552 - Homework 7

## Files

- HW7.ipynb: Code, results, plots, and written answers.
- requirements.txt: Package versions used for this homework.
- data/Frogs_MFCCs.csv: The dataset used in the notebook.
- data/Readme.txt: The original dataset notes.

## Data

I use the Anuran Calls (MFCCs) dataset from the course data ZIP.

The dataset has 7195 samples and 22 MFCC features. The target columns are Family, Genus, and Species. RecordID is not used as a feature.

Extract the course ZIP and place Frogs_MFCCs.csv in the data folder.

Source:
https://archive.ics.uci.edu/ml/datasets/Anuran+Calls+%28MFCCs%29

## How to Run

I used Python 3.13.

Open a terminal in the Homework7 folder. Use a Python environment and install the packages:

```bash
python -m pip install -r requirements.txt
```

Start JupyterLab:

```bash
python -m jupyterlab
```

Open HW7.ipynb. Restart the kernel and run all cells in order.

Cross-validation and the 50 clustering runs may take several minutes.

## Methods

Question 1 compares an RBF SVM, an L1 linear SVM, and an L1 linear SVM with SMOTE.

The models use a random 70% training and 30% test split, stratified by Species. Parameters are selected using 10-fold cross-validation. Scaling and SMOTE are fitted inside the training folds.

Question 2 uses all samples for K-means clustering. The CH score selects k in each of 50 runs. Cluster labels come from the majority Family, Genus, and Species in each cluster.

Question 3 answers ISLR 12.6.2 and shows the hierarchical clustering dendrograms.

## Evaluation

I report Exact Match, Hamming Distance, Hamming Loss, and Hamming Score. I define Hamming Score as 1 minus Hamming Loss.

I also report Sample Jaccard, Macro Recall, and Macro F1 for the classification results.
