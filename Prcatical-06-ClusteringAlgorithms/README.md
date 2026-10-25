# Customer Segmentation Using Clustering Algorithms

## Aim
To implement clustering algorithms on a synthetic customer dataset to identify meaningful groups and evaluate clustering quality using Silhouette Score, Davies–Bouldin Index, and visualization.

## Objectives
- Generate a synthetic customer dataset using Python.
- Implement K-Means, Agglomerative Clustering, and DBSCAN.
- Group customers based on annual income and spending score.
- Evaluate clustering performance using appropriate metrics.
- Visualize and compare the clustering results.

## Technologies Used
- **Python** – Programming language.
- **NumPy** – Numerical operations and data generation.
- **Pandas** – Dataset creation and data manipulation.
- **Matplotlib** – Data visualization.
- **Scikit-learn** – Clustering algorithms, preprocessing, and evaluation metrics.
- **Google Colab / Jupyter Notebook** – Code execution environment.

## Dataset Description
A synthetic dataset of 300 customers is generated using Scikit-learn's `make_blobs()` function.

**Features used for clustering:** Annual_Income and Spending_Score.

The dataset is generated programmatically, so downloading an external dataset is not required.

## Clustering Algorithms

### 1. K-Means Clustering
Divides customers into a predefined number of clusters using cluster centroids. In this practical, five clusters are created.

### 2. Agglomerative Clustering
A hierarchical clustering algorithm that starts with individual data points and repeatedly merges similar clusters until five clusters remain.

### 3. DBSCAN
A density-based clustering algorithm that identifies dense groups of customers and detects noise points or outliers. The number of clusters is not specified beforehand.

## Methodology
1. Generate the synthetic customer dataset.
2. Select annual income and spending score.
3. Standardize the selected features using `StandardScaler`.
4. Apply K-Means, Agglomerative Clustering, and DBSCAN.
5. Evaluate the results using clustering metrics.
6. Visualize the clusters using scatter plots.
7. Save the final results to a CSV file.

## Evaluation Metrics

- **Silhouette Score:** Measures how well-separated the clusters are. A higher score generally indicates better clustering.
- **Davies–Bouldin Index:** Measures cluster compactness and similarity. A lower score generally indicates better clustering.
- **Scatter Plot Visualization:** Helps inspect the distribution and separation of customer groups.

## Results and Observations
- K-Means divides customers into five clusters.
- Agglomerative Clustering forms five groups by merging similar data points.
- DBSCAN identifies groups based on density and may classify isolated points as noise.
- Scatter plots help compare the customer groups identified by the three algorithms.
- The best-performing algorithm should be determined by comparing the actual evaluation scores and the usefulness of the clusters.

## Output
The practical generates:
- A synthetic customer dataset.
- Cluster labels for all three algorithms.
- Silhouette Score and Davies–Bouldin Index comparisons.
- Scatter plots of the clustering results.
- `Customer_Segmentation_Results.csv` containing the dataset and cluster labels.

## How to Run
1. Clone or download this GitHub repository.
2. Open the Python notebook or script in Google Colab or Jupyter Notebook.
3. Install the required libraries if they are not already available:
   pip install numpy pandas matplotlib scikit-learn
4. Execute the code cells in sequence.
5. View the clustering graphs, evaluation metrics, and saved CSV file.

## Applications
- Customer segmentation.
- Targeted marketing and personalized offers.
- Customer behavior analysis.
- Market research.
- Identification of unusual customer patterns.

## Conclusion
K-Means, Agglomerative Clustering, and DBSCAN were implemented on a synthetic customer dataset. Their results were visualized and evaluated using clustering metrics. This practical demonstrates how unsupervised learning can identify meaningful customer groups and support data-driven business decisions.



