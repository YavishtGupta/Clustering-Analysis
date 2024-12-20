# Clustering Analysis Results

This project aims to analyze clustering performance using various algorithms and preprocessing configurations. The algorithms were evaluated using multiple metrics to identify the best-performing configurations.

## Model Comparison

We experimented with multiple configurations, training clustering algorithms under different combinations of the following preprocessing conditions:

- **Preprocessing**: Enabled or Disabled (handling missing values, encoding, etc.)
- **Normalization**: Whether to normalize the data (Z-score normalization).
- **Transformation**: Applies feature transformation for better clustering separability.
- **PCA**: Reduces dimensions for clustering.
- **T+N**: Combines Transformation and Normalization.
- **T+N+PCA**: Combines Transformation, Normalization, and PCA.

### Configurations Compared
| Parameters         | c=3   | c=4   | c=5   | c=3 (Norm) | c=4 (Norm) | c=5 (Norm) | c=3 (Trans) | c=4 (Trans) | c=5 (Trans) | c=3 (PCA) | c=4 (PCA) | c=5 (PCA) | c=3 (T+N) | c=4 (T+N) | c=5 (T+N) | c=3 (T+N+PCA) | c=4 (T+N+PCA) | c=5 (T+N+PCA) |
|--------------------|-------|-------|-------|------------|------------|------------|-------------|-------------|-------------|-----------|-----------|-----------|-----------|-----------|-----------|---------------|---------------|---------------|

## Model Evaluation

Each clustering algorithm was evaluated using the following performance metrics:

- **Silhouette Score**: Measures how similar an object is to its own cluster compared to other clusters. Higher is better.
- **Calinski-Harabasz Index**: Evaluates the ratio of the sum of between-clusters dispersion and inter-cluster dispersion for all clusters. Higher is better.
- **Davies-Bouldin Index**: Measures the average similarity ratio of each cluster with its most similar cluster. Lower is better.

### Using K-Means Clustering
| Parameters         | c=3   | c=4   | c=5   | c=3 (Norm) | c=4 (Norm) | c=5 (Norm) | c=3 (Trans) | c=4 (Trans) | c=5 (Trans) | c=3 (PCA) | c=4 (PCA) | c=5 (PCA) | c=3 (T+N) | c=4 (T+N) | c=5 (T+N) | c=3 (T+N+PCA) | c=4 (T+N+PCA) | c=5 (T+N+PCA) |
|--------------------|-------|-------|-------|------------|------------|------------|-------------|-------------|-------------|-----------|-----------|-----------|-----------|-----------|-----------|---------------|---------------|---------------|
| **Silhouette**     | 0.5567| 0.5309| 0.5585| 0.1363     | 0.1506     | 0.1696     | 0.5561      | 0.5392      | 0.5613      | 0.5567    | 0.5549    | 0.5583    | 0.1303    | 0.1409    | 0.1912    | 0.0942        | 0.1460        | 0.1705        |
| **Calinski-Harabasz** | 6012.56| 6977.08| 9048.41| 164.71     | 190.33     | 195.12     | 5807.16     | 6752.47     | 8989.23     | 6012.56   | 6806.10   | 9054.65   | 171.27    | 196.11    | 207.57    | 144.52        | 184.86        | 206.36        |
| **Davies-Bouldin** | 0.5565| 0.5804| 0.5008| 2.3272     | 2.3197     | 1.6780     | 0.5612      | 0.5636      | 0.4988      | 0.5565    | 0.5056    | 0.5016    | 2.6034    | 2.4284    | 2.0878    | 2.8686        | 2.1637        | 2.0211        |

### Using Hierarchical Clustering
| Parameters         | c=3   | c=4   | c=5   | c=3 (Norm) | c=4 (Norm) | c=5 (Norm) | c=3 (Trans) | c=4 (Trans) | c=5 (Trans) | c=3 (PCA) | c=4 (PCA) | c=5 (PCA) | c=3 (T+N) | c=4 (T+N) | c=5 (T+N) | c=3 (T+N+PCA) | c=4 (T+N+PCA) | c=5 (T+N+PCA) |
|--------------------|-------|-------|-------|------------|------------|------------|-------------|-------------|-------------|-----------|-----------|-----------|-----------|-----------|-----------|---------------|---------------|---------------|
| **Silhouette**     | 0.5012| 0.5193| 0.5312| 0.1037     | 0.1498     | 0.1898     | 0.4587      | 0.4866      | 0.5204      | 0.5012    | 0.5193    | 0.5312    | 0.1036    | 0.1498    | 0.1895    | 0.1036        | 0.1498        | 0.1895        |
| **Calinski-Harabasz** | 4448.99| 6465.24| 7687.41| 188.73     | 198.05     | 211.92     | 4185.80     | 5483.69     | 7302.15     | 4448.99   | 6465.24   | 7687.41   | 188.74    | 198.07    | 211.92    | 188.74        | 198.07        | 211.92        |
| **Davies-Bouldin** | 0.5678| 0.5535| 0.5015| 2.5588     | 2.3750     | 2.1875     | 0.5562      | 0.5451      | 0.4788      | 0.5678    | 0.5535    | 0.5015    | 2.5595    | 2.3753    | 2.1875    | 2.5595        | 2.3753        | 2.1875        |

### Using Mean-Shift Clustering
| Parameters         | c=3   | c=4   | c=5   | c=3 (Norm) | c=4 (Norm) | c=5 (Norm) | c=3 (Trans) | c=4 (Trans) | c=5 (Trans) | c=3 (PCA) | c=4 (PCA) | c=5 (PCA) | c=3 (T+N) | c=4 (T+N) | c=5 (T+N) | c=3 (T+N+PCA) | c=4 (T+N+PCA) | c=5 (T+N+PCA) |
|--------------------|-------|-------|-------|------------|------------|------------|-------------|-------------|-------------|-----------|-----------|-----------|-----------|-----------|-----------|---------------|---------------|---------------|
| **Silhouette**     | 0.6167| 0.6167| 0.6167| 0.2990     | 0.2990     | 0.2990     | 0.6098      | 0.6098      | 0.6098      | 0.6167    | 0.6167    | 0.6167    | 0.2982    | 0.2982    | 0.2982    | 0.2982        | 0.2982        | 0.2982        |
| **Calinski-Harabasz** | 5227.16| 5227.16| 5227.16| 140.04     | 140.04     | 140.04     | 4876.76     | 4876.76     | 4876.76     | 5227.16   | 5227.16   | 5227.16   | 140.22    | 140.22    | 140.22    | 140.22        | 140.22        | 140.22        |
| **Davies-Bouldin** | 0.5092| 0.5092| 0.5092| 1.0656     | 1.0656     | 1.0656     | 0.5060      | 0.5060      | 0.5060      | 0.5092    | 0.5092    | 0.5092    | 1.0591    | 1.0591    | 1.0591    | 1.0591        | 1.0591        | 1.0591        |

## Best Performing Configuration
After comparing all models, the best-performing configuration was identified as follows:

### Best Algorithm: Mean-Shift Clustering
| Metric                  | Value   |
|-------------------------|---------|
| **Silhouette Score**    | 0.6167  |
| **Calinski-Harabasz**   | 5227.16 |
| **Davies-Bouldin Index**| 0.5092  |

## Conclusion
By comparing the clustering methods with different preprocessing strategies, the best-performing configuration was Mean-Shift Clustering with a Silhouette Score of 0.6167, indicating high clustering quality.
