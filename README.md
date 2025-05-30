# Wine Unsupervised Learning Analysis

## Overview
In this project, I explored a curated dataset of 178 fine wines using unsupervised methods—PCA, t-SNE, MDS—and clustering algorithms (k-Means, DBSCAN) to uncover natural groupings without any labels. By comparing global versus local embeddings and different clustering paradigms, I revealed both broad categories and nuanced subtypes in the wine space.

## Features
- **Dimensionality Reduction:**  
  - **PCA:** Found 5 components with eigenvalues >1; first two explain 99.98% of variance  
  - **t-SNE:** Analyzed KL-divergence vs. perplexity (5–150) and visualized 2D embedding at perplexity 20  
  - **MDS:** Generated a 2D embedding (stress ≈19573) to preserve global distances  
- **Clustering Methods:**  
  - **k-Means + PCA:** Used silhouette analysis to select k=2, yielding a total within-cluster sum of 4,540,738.7  
  - **DBSCAN + PCA:** Tuned ε and MinPts to identify core clusters and outlier wines  
- **Comparative Insights:** Contrasted how each reduction and clustering method emphasizes global structure versus local nuances.

## Tech & Tools
- **Language:** Python 3  
- **Data Handling:** pandas, NumPy  
- **Dimensionality Reduction & Clustering:** scikit-learn (PCA, TSNE, MDS, KMeans, DBSCAN), scikit-learn’s silhouette_score  
- **Visualization:** Matplotlib, Seaborn  
- **Environment:** Jupyter Notebook (`analysis.ipynb`)  
- **Version Control:** Git & GitHub  

## Results & Key Takeaways
- **PCA:** Identified 5 significant components; PC1 & PC2 capture virtually all variance (99.98%), indicating a strong underlying chemical gradient.  
- **t-SNE:** KL-divergence plateaus around perplexity 60; at perplexity 20, clear clusters emerge along a curved manifold.  
- **MDS:** High stress reveals that global relationships compress to a continuum, contrasting t-SNE’s local cluster emphasis.  
- **k-Means:** Silhouette method picked k=2, splitting wines into two broad groups (sum of squared distances = 4.54M).  
- **DBSCAN:** Detected multiple irregular clusters and noise points—highlighting unique outlier wines beyond k-Means’ scope.

## Skills Gained
Unsupervised Techniques, Cluster Validation, Density-Based Clustering, Visualization, and Analytical Interpretation. 

## Quick Start

```bash
git clone https://github.com/yourusername/wine-unsupervised-learning.git
cd wine-unsupervised-learning
pip install -r requirements.txt
jupyter lab analysis.ipynb
