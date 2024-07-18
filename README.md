# Customer_Segment_Analysis

# Customer Segmentation Analysis

This project involves analyzing a dataset of annual spending by customers across various product categories to uncover patterns and segment customers. The goal is to understand the different types of customers a wholesale distributor serves, providing insights to optimize their delivery services.

The dataset can be found on the [ML Repository](https://archive.ics.uci.edu/ml/datasets/Wholesale+customers). The analysis excludes the 'Channel' and 'Region' features, focusing on six product categories.

---

## Data Exploration
The dataset includes the following product categories:
- Fresh
- Milk
- Grocery
- Frozen
- Detergents_Paper
- Delicatessen

### Sample Percentile Analysis
#### Customer Index: 25 (Index 0)
- **High Spending:** Fresh, Detergents_Paper
- **Medium Spending:** Milk, Grocery
- **Low Spending:** Frozen, Delicatessen
  - **Conclusion:** Likely a small retail store.

#### Customer Index: 50 (Index 1)
- **High Spending:** Frozen, Delicatessen
- **Medium Spending:** Fresh, Detergents_Paper
- **Low Spending:** Milk, Grocery
  - **Conclusion:** Likely a restaurant.

#### Customer Index: 75 (Index 2)
- **High Spending:** Frozen, Fresh
- **Medium Spending:** Delicatessen
- **Low Spending:** Milk, Grocery, Detergents_Paper
  - **Conclusion:** Possibly a supplier with a small restaurant business or a supermarket with an attached small restaurant.

### Feature Distribution
![Feature Distribution]()

---

## Data Preprocessing

### Feature Scaling
Scaling is applied to normalize the data distribution.
#### Before Normalization
![Before Normalization]()
#### After Normalization
![After Normalization]()

---

## Feature Transformation

### PCA Implementation
Principal Component Analysis (PCA) is used to reduce dimensionality.
![PCA Implementation](g)

### Dimensionality Reduction
![Dimensionality Reduction]()

### Biplot Visualization
A biplot visualizes data points in terms of principal components, showing the relationship between components and original features.
![Biplot]()

---

## Clustering

The Gaussian Mixture Model (GMM) algorithm is chosen for its soft classification capability, enhanced by the PCA dimensionality reduction.

### GMM Clustering Visualization
![GMM Clustering]()

---

## Visualizing Underlying Distributions
![Underlying Distributions]()

### Final Conclusion
- The GMM clustering effectively identified key customer segments, though some anomalies remain, such as retailers within the hotel/restaurant/cafe cluster.
- The actual data shows strong correlation with predicted clusters, validating the segmentation approach.
- Predicted classifications were largely accurate: Cluster 0 likely represents restaurants/cafes, and Cluster 1 represents bulk distributors or supermarkets.

This analysis equips the wholesale distributor with actionable insights to better tailor their services to meet customer needs.
