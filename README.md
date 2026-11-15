# Customer Segmentation Using K-Means and Gaussian Mixture Models

## Overview

This project explores customer segmentation using two unsupervised machine learning approaches: **K-Means Clustering** and **Gaussian Mixture Models (GMM)** trained using the Expectation-Maximization (EM) algorithm.

The objective is to group customers based on their annual income and spending behavior, visualize the resulting clusters, and compare the performance of both algorithms using standard clustering evaluation metrics.

## Technologies Used

- Python
- Pandas
- Matplotlib
- Scikit-learn
- K-Means Clustering
- Gaussian Mixture Models (EM)

## Dataset

The analysis uses customer information containing the following features:

- **Annual Income (k$):** Customer annual income in thousands of dollars.
- **Spending Score (1–100):** A score representing customer spending behavior.

These two features are used for clustering.

## Methodology

**1. Data Loading:** Load the customer dataset using Pandas.

**2. Feature Selection:** Select Annual Income and Spending Score as the clustering variables.

**3. Feature Scaling:** Apply StandardScaler to normalize the features.

**4. K-Means Clustering:** Segment customers into five clusters using K-Means.

**5. Gaussian Mixture Models:** Apply GMM with five components, using the EM algorithm for model estimation.

**6. Model Evaluation:** Compare the resulting clusters using Silhouette Score and Davies-Bouldin Index.

**7. Cluster Agreement:** Calculate the Adjusted Rand Index (ARI) to measure agreement between the two clustering assignments.

**8. Visualization:** Generate side-by-side scatter plots of the clustering results.

## Evaluation Metrics

| Metric | Interpretation |
|---|---|
| Silhouette Score | Higher values generally indicate better-separated clusters. |
| Davies-Bouldin Index | Lower values generally indicate better clustering. |
| Adjusted Rand Index | Measures agreement between two clustering assignments, adjusted for chance. |

## Clustering Visualization

![K-Means vs GMM Clustering](results/clusters.png)

The visualization compares customer segmentation produced by K-Means and GMM using annual income and spending score.

## How to Run

Clone the repository and install the required dependencies.

1. Clone the repository.
2. Install dependencies using `pip install -r requirements.txt`.
3. Ensure the Google Drive dataset URL in the script is accessible.
4. Run `python customer_segmentation.py`.

The program will display clustering evaluation metrics and generate a visualization.

## Limitations

- The number of clusters is fixed at five rather than optimized experimentally.
- Only two customer features are considered.
- Evaluation metrics provide internal clustering quality measures, not ground-truth classification accuracy.
- The dataset must remain accessible through its external download URL.

## Future Improvements

- Use the Elbow Method and Silhouette Analysis to explore optimal cluster numbers.
- Compare clustering performance for multiple values of K.
- Apply additional clustering techniques such as DBSCAN.
- Explore customer characteristics within individual clusters.
- Analyze GMM membership probabilities for uncertain assignments.

## Conclusion

This project demonstrates how K-Means and GMM can be applied to customer segmentation and compared using clustering metrics and visual analysis. It provides a foundation for exploring unsupervised machine learning techniques in customer analytics.
