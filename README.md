# How Many Clusters? Evaluating K in K-Means Using the Elbow Method and Silhouette Score

> A machine learning tutorial for the Machine Learning & Neural Networks course.

**Author:** Israel Ajayi  
**Course:** Machine Learning & Neural Networks  
**Submission format:** PDF Tutorial + Jupyter Notebook

---

## Overview

K-Means clustering is one of the most widely used unsupervised learning algorithms — but it requires you to specify the number of clusters **K** before it runs. This tutorial teaches two principled, evidence-based methods for choosing K:

1. **The Elbow Method** — plots within-cluster variance (inertia) against K and looks for the point of diminishing returns
2. **The Silhouette Score** — measures how well each point fits its own cluster versus neighbouring clusters (range: −1 to +1)

We demonstrate both methods on:
- A **synthetic dataset** (where the true K is known) to verify the methods work
- The **UCI Wine dataset** (13 chemical features, 178 samples) to show real-world application

---

## Repository Structure

```
kmeans-tutorial-repo/
│
├── README.md                   ← You are here
├── LICENSE                     ← MIT Licence
│
├── kmeans_tutorial.ipynb       ← Full Jupyter notebook (all code + figures)
└── kmeans_tutorial.pdf         ← PDF tutorial (<2000 words)
```

---

## Getting Started

### Prerequisites

You will need Python 3.8+ and the following packages:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### Running the Notebook

1. Clone this repository:
   ```bash
   git clone https://github.com/Easywiz/kmeans-tutorial.git
   cd kmeans-tutorial
   ```

2. Launch Jupyter:
   ```bash
   jupyter notebook kmeans_tutorial.ipynb
   ```

3. Run all cells from top to bottom (`Kernel → Restart & Run All`)

All figures will be generated automatically. No external data downloads are required — both datasets are loaded directly via scikit-learn.

---

## What the Notebook Covers

| Section | Description |
|---------|-------------|
| Setup & Imports | Libraries, colourblind-safe palette, reproducibility seed |
| K-Means Recap | Algorithm steps and inertia formula |
| Synthetic Dataset | 400-point, 4-cluster dataset with known ground truth |
| Elbow Method | Inertia vs K plot with annotated elbow |
| Silhouette Score | Average score plot + per-cluster silhouette diagrams |
| Feature Scaling | Why StandardScaler is essential before K-Means |
| Wine Dataset | Real-world evaluation on UCI Wine (13 features) |
| PCA Visualisation | 2D cluster projection for interpretability |
| When Methods Disagree | Demonstration with overlapping clusters |
| Summary Table | Side-by-side comparison of both methods |

---

## Datasets

| Dataset | Source | How it's loaded |
|---------|--------|-----------------|
| Synthetic blobs | Generated via `sklearn.datasets.make_blobs` | No download needed |
| UCI Wine | UCI ML Repository (built into scikit-learn) | `sklearn.datasets.load_wine()` |

---

## Accessibility

This tutorial was designed with accessibility in mind:

- **Colourblind-friendly** figures using seaborn's `colorblind` palette throughout
- **Alt-text** provided for every figure (printed in notebook output)
- **PDF** uses high-contrast text, clear section headings, and readable font sizes
- **Screen-reader friendly** PDF structure with logical reading order

---

## References

1. Rousseeuw, P.J. (1987). Silhouettes: a graphical aid to the interpretation and validation of cluster analysis. *Journal of Computational and Applied Mathematics*, 20, 53–65. https://doi.org/10.1016/0377-0427(87)90125-7

2. Arthur, D. & Vassilvitskii, S. (2007). k-means++: The advantages of careful seeding. *Proceedings of the 18th Annual ACM-SIAM Symposium on Discrete Algorithms*, 1027–1035.

3. Thorndike, R.L. (1953). Who belongs in the family? *Psychometrika*, 18(4), 267–276. https://doi.org/10.1007/BF02289263

4. Pedregosa, F. et al. (2011). Scikit-learn: Machine Learning in Python. *Journal of Machine Learning Research*, 12, 2825–2830. https://jmlr.org/papers/v12/pedregosa11a.html

5. Scikit-learn developers (2024). *Clustering*. https://scikit-learn.org/stable/modules/clustering.html

6. UCI Machine Learning Repository — Wine Dataset. https://archive.ics.uci.edu/ml/datasets/wine

---

## Licence

This project is licensed under the **MIT Licence** — see the [LICENSE](LICENSE) file for details.

You are free to use, adapt, and share this tutorial with attribution.
