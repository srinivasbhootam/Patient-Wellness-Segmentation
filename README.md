# Patient-Wellness-Segmentation


## 📘 Project Overview

**Patient-Wellness-Segmentation** leverages unsupervised machine learning to identify distinct groups of patients based on five lifestyle indicators: exercise, healthy meals, sleep, stress, and BMI. By integrating K‑Means and Ward’s hierarchical clustering with PCA for dimensionality reduction, this project delivers actionable wellness segments for personalized care.

## 🔍 Analysis & Results

1. **Data Preprocessing**
   - Handled <2% missing values via imputation using column means.
   - Standardized each indicator to zero mean and unit variance to ensure comparability.

2. **Exploratory Data Analysis**
   - **Correlation Heatmap:** Identified moderate negative correlations between stress & sleep and between exercise & BMI, confirming distinct dimensions of wellness.
   - **Distribution Plots:** Verified that all five indicators form roughly symmetric bell curves with no extreme outliers, supporting reliable clustering.

3. **Clustering Execution**
   - Applied the **Elbow Method** (Figure 7) and **Ward’s Dendrogram** (Figure 8), both indicating four optimal clusters.
   - Executed K‑Means and hierarchical clustering on the full five-dimensional data.

4. **Dimensionality Reduction (PCA)**
   - Reduced to two principal components capturing 45.8% of total variance (PC1 = 23.7%, PC2 = 22.1%).
   - Enabled 2D visualization of cluster separation and interpretability of component loadings.

## 📊 Model Comparison

| Method                           | Silhouette Score | WCSS (Within-Cluster Sum of Squares) |
|----------------------------------|------------------|---------------------------------------|
| K‑Means (5 variables)            | 0.168            | 190.42                                |
| Hierarchical (5 variables)       | 0.114            | 215.37                                |
| K‑Means (PCA-reduced, 2 comps)   | 0.152            | 205.88                                |

- **Best Performance:** K‑Means on full data achieved the highest silhouette score, indicating superior cluster separation.
- **PCA Trade‑off:** Two-component solution retains most structure with only a slight drop in silhouette, facilitating simpler visualization.

## 🎯 Cluster Profiles & Recommendations

| Cluster | Profile Highlights                                           | Tailored Intervention                          |
|---------|---------------------------------------------------------------|-----------------------------------------------|
| A       | High exercise, healthy meals, good sleep, low stress, normal BMI  | Encourage peer mentoring and reward sharing  |
| B       | Low activity, poor diet, short sleep, high stress, high BMI       | Provide beginner workouts and meal plans     |
| C       | Moderate levels across all metrics                               | Offer periodic check‑ins and self‑tracking    |
| D       | Average activity, average sleep, very high stress                | Supply guided relaxation modules and sleep tips |

- **High‑Risk (Cluster B):** Focus on simple meal and exercise programs.  
- **Stress‑Dominant (Cluster D):** Introduce mindfulness and sleep hygiene sessions.  
- **Well‑Balanced (Cluster A & C):** Engage as peer coaches or maintain self‑monitoring tools.

---

## Contact

**Srinivas** – srinivas.bhootam@gmail,com

Thank you for exploring **Patient-Wellness-Segmentation**! Your feedback and contributions are welcome.
