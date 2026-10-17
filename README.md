# ML_clustering

A Python notebook exploring customer segmentation with scikit-learn's K-means clustering. Using the included `Mall_Customers.csv`, it groups customers by age, annual income, spending score, and encoded gender, then compares clustering before and after principal component analysis (PCA).

## Features

- An 80/20 train/test split, descriptive statistics, and numeric feature standardization.
- Cluster-count exploration using elbow plots and silhouette scores.
- Two-component PCA with cluster and centroid visualization.
- CSV export of test-set features and cluster assignments.

## Installation and Usage

With Python 3 installed, run the following from the project directory:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install notebook pandas numpy scikit-learn matplotlib
python -m notebook mall.ipynb
```

In Jupyter, select the environment's Python kernel and run the cells from top to bottom. Keep `Mall_Customers.csv` beside the notebook; no separate dataset download is required.

The final models use six clusters on the standardized features and three on the PCA-transformed features. Running the notebook overwrites `predicts.csv` with standardized test-set features, encoded gender, and the `Cluster` and `PCA_Cluster` assignments. Cluster numbers identify groups, not known customer categories.

The accompanying [project brief](ML_Project_final.pdf) provides assignment context.
