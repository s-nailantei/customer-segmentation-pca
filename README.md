. Customer Segmentation Using PCA + K-Means

> Unsupervised Machine Learning | Dimensionality Reduction | Clustering

. Project Overview
A credit card company wants to understand the behavioural patterns 
of its 8,950 customers to enable targeted marketing and risk management. 
Using PCA for dimensionality reduction and K-Means for clustering, 
we identify 5 distinct customer segments with actionable business insights.



. Dataset
- Source: [Kaggle — CC General Dataset](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata)
- Size: 8,950 customers × 17 behavioural features
- Features include: balance, purchases, cash advances, 
credit limit, payment behaviour, tenure



. Tech Stack
![Python](https://img.shields.io/badge/Python-3.x-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![Pandas](https://img.shields.io/badge/Pandas-Data-green)
![Seaborn](https://img.shields.io/badge/Seaborn-Viz-lightblue)



. Approach

| Step | Description |
|------|-------------|
| 1 | Load & explore data |
| 2 | Clean — median imputation for missing values |
| 3 | Scale — StandardScaler (mean=0, std=1) |
| 4 | PCA — reduce 17 features to 6 components (~80% variance) |
| 5 | Elbow method — determine optimal k |
| 6 | K-Means — k=5 clusters |
| 7 | Interpret & profile each segment |



. Key Visualisations

### Cumulative Explained Variance
Shows how many PCA components are needed to retain 80% of data variance.

### Elbow Plot
Used to determine the optimal number of clusters (k=5).

### Customer Segments — PC1 vs PC2
2D scatter plot of all 8,950 customers coloured by cluster.

. Cluster Heatmap
Mean feature values per cluster — the core interpretation visual.



. Customer Segments Discovered

| Cluster | Label | Size | Key Behaviour |
|---------|-------|------|---------------|
| 0 | Active High-Value Shoppers | 807 | High purchases, high frequency |
| 1 | Inactive Low Engagers | 3,905 | Minimal usage — churn risk |
| 2 | Cash Advance Dependent | 1,198 | Borrowers not spenders — credit risk |
| 3 | Installment Shoppers | 3,010 | Steady, budget-conscious |
| 4 | VIP Whales | 30 | 25x average purchases — premium customers |



. Business Recommendations

- **Cluster 1 — Inactive:** Launch re-engagement campaign with cashback incentives
- **Cluster 2 — Cash Advance:** Flag for credit risk review — near-zero full payment rate
- **Cluster 3 — Installment:** Target with installment plan promotions
- **Cluster 4 — VIPs:** Assign dedicated relationship managers + exclusive rewards
