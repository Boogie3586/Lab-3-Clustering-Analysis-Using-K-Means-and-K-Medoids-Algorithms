# MSCS_634_Lab_3 - Wine Dataset Clustering

## Overview
This lab explores clustering techniques using the Wine Dataset from the sklearn Python library. The goal is to apply both **K-Means** and **K-Medoids** clustering algorithms, analyze the resulting clusters, and compare their performance using quantitative metrics and visualizations. This lab demonstrates key concepts in clustering analysis, including data preprocessing, model implementation, performance evaluation, and visualization.

## Dataset
The Wine Dataset consists of **178 samples** of wines classified into **three classes**. Each sample has **13 chemical features**, including alcohol content, malic acid, ash, magnesium, flavanoids, and more. The dataset is commonly used for classification and clustering tasks.

- **Number of samples:** 178  
- **Number of features:** 13  
- **Number of classes:** 3  

## Lab Steps

### Step 1: Data Loading and Preparation
- Loaded the Wine Dataset from `sklearn.datasets`.
- Explored the dataset to examine features and class distribution.
- Standardized features using **z-score normalization** to ensure consistent scaling across all features.

### Step 2: K-Means Clustering
- Implemented **K-Means** clustering with **k = 3**.
- Trained the model and obtained cluster labels.
- Calculated performance metrics:
  - **Silhouette Score:** Measures cluster cohesion and separation.
  - **Adjusted Rand Index (ARI):** Compares clusters to actual class labels.

### Step 3: K-Medoids Clustering
- Implemented **K-Medoids** clustering with **k = 3**.
- Trained the model and obtained cluster labels.
- Calculated the same performance metrics as K-Means:
  - **Silhouette Score**
  - **Adjusted Rand Index (ARI)**

### Step 4: Visualization and Comparison
- Reduced data to 2D using **PCA** for visualization purposes.
- Created side-by-side scatter plots showing K-Means and K-Medoids clusters.
- Marked cluster centroids/medoids on the plots for clarity.
- Observed differences in cluster shapes and positioning.

## Results

| Algorithm   | Silhouette Score | Adjusted Rand Index (ARI) |
|------------|-----------------|---------------------------|
| K-Means    | 0.57            | 0.73                      |
| K-Medoids  | 0.58            | 0.75                      |

### Observations
- Both K-Means and K-Medoids were able to separate the wine classes effectively.
- **K-Medoids** showed slightly better-defined clusters, likely due to its robustness to outliers.
- K-Means assumes spherical clusters, while K-Medoids can handle irregular cluster shapes more effectively.
- K-Means is computationally faster for larger datasets, whereas K-Medoids provides better robustness in noisy datasets.

## Insights
- Standardizing features before clustering is critical to avoid bias from different scales.
- Visualization using PCA is useful for interpreting high-dimensional cluster structures.
- Choice of clustering algorithm depends on dataset characteristics:
  - Use K-Means for large datasets with mostly spherical clusters.
  - Use K-Medoids when data has outliers or irregular cluster shapes.

## Challenges
- Determining appropriate cluster evaluation metrics.
- Visualizing 13-dimensional data in 2D space while preserving structure.
- Ensuring reproducibility by setting random seeds.

## Files
- `Wine_Clustering_Lab.ipynb` - Jupyter Notebook containing all steps, code, and visualizations.
- `README.md` - This file, summarizing lab purpose, methodology, results, and observations.

## Author
**Carter Nelson**  
MSCS 634
