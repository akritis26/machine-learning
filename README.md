# Student Performance ML Labs

This repository adapts a 14-experiment machine-learning notebook sequence to the supplied student performance dataset.

## Dataset

`data/student_data.csv` contains 395 records and 33 fields, including demographic, family, school, study-habit, and grade information. The notebooks use `G3` (final grade, 0–20) as the regression target. Classification notebooks define pass as `G3 >= 10`. The dataset contains student demographic and lifestyle fields; review your institution's privacy and sharing requirements before publishing it.

The notebook sequence follows the structure of [Aayush217's Chronos notebook project](https://github.com/Aayush217/chronos---Turbofan-Predictive-Maintenance-RUL-Prognostics), with data loading, targets, preprocessing, features, and evaluations adapted for student performance. These are adapted experiments, not a claim that the original notebooks were validated on this dataset.

## Notebooks

1. `01_data_exploration.ipynb` — dataset structure and quality
2. `02_data_preprocessing.ipynb` — missingness, scaling, and encoding
3. `03_eda.ipynb` — distributions and relationships
4. `04_linear_regression.ipynb` — predict final grade
5. `05_logistic_regression.ipynb` — pass/fail classification
6. `06_decision_tree.ipynb` — depth comparison and tree visualization
7. `07_random_forest.ipynb` — tree ensemble and feature importance
8. `08_svm.ipynb` — kernel comparison
9. `09_knn.ipynb` — neighbor-count comparison
10. `10_model_evaluation_and_tuning.ipynb` — cross-validation and tuning
11. `11_kmeans_clustering.ipynb` — student profile clustering
12. `12_dbscan_clustering.ipynb` — density-based clustering
13. `13_pca.ipynb` — unsupervised dimensionality reduction
14. `14_lda.ipynb` — supervised dimensionality reduction

## Run

The dataset file is intentionally excluded from version control. Put your local copy at `data/student_data.csv`, install the packages in `requirements.txt`, then launch Jupyter from this repository root and open a notebook. The notebooks locate the CSV whether the working directory is the repository root or `notebooks/`.

```bash
python -m pip install -r requirements.txt
jupyter notebook
```

## Interpretation notes

- The classification threshold is an explicit lab choice, not an official measure of student success.
- Including `G1` and `G2` makes this a prediction of final grade after earlier grades are available. For an earlier intervention setting, remove them and rerun the experiments.
- The dataset has only 395 rows. Scores may vary with the split and should not be treated as evidence for decisions about individual students.
- Clustering is exploratory; cluster IDs do not represent objective student types.
