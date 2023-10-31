# CryptoClustering Challenge

## Introduction

In the CryptoClustering challenge, we used Python and unsupervised learning techniques to predict how cryptocurrencies are affected by 24-hour and 7-day price changes. This README provides an overview of the steps involved in the challenge and the results obtained.

## Table of Contents

- [Before You Begin](#before-you-begin)
- [Prepare the Data](#prepare-the-data)
- [Find the Best Value for k Using the Original Scaled DataFrame](#find-the-best-value-for-k-using-the-original-scaled-data)
- [Cluster Cryptocurrencies with K-means Using the Original Scaled Data](#cluster-cryptocurrencies-with-k-means-using-the-original-scaled-data)
- [Optimize Clusters with Principal Component Analysis](#optimize-clusters-with-principal-component-analysis)
- [Find the Best Value for k Using the PCA Data](#find-the-best-value-for-k-using-the-pca-data)
- [Cluster Cryptocurrencies with K-means Using the PCA Data](#cluster-cryptocurrencies-with-k-means-using-the-pca-data)
- [Visualize and Compare the Results](#visualize-and-compare-the-results)

## Before You Begin

- Created a new repository called CryptoClustering.
- Cloned the repository to the local computer.
- Pushed changes to GitHub.

## Prepare the Data

- Loaded the `crypto_market_data.csv` into a DataFrame.
- Normalized the data using the `StandardScaler()` module from scikit-learn.
- Created a DataFrame with the scaled data, setting "coin_id" as the index.

![Initial Data View](/images/initialdataview.png)

## Find the Best Value for k Using the Original Scaled DataFrame

- Used the elbow method to find the best value for k.
- Created a list of k values from 1 to 11.
- Computed inertia for each k and plotted an elbow curve to identify the optimal k.

![Elbow Curve](/images/elbow_curve.png)

## Cluster Cryptocurrencies with K-means Using the Original Scaled Data

- Initialized the K-means model with the best value for k.
- Fitted the K-means model using the original scaled DataFrame.
- Predicted clusters and added a new column with predicted cluster labels.
- Created a scatter plot to visualize the clusters.

![Original Data Clusters](/images/original_data_clusters.png)

## Optimize Clusters with Principal Component Analysis

- Performed PCA on the original scaled DataFrame to reduce features to three principal components.
- Determined the explained variance for each principal component.

## Find the Best Value for k Using the PCA Data

- Applied the elbow method to the PCA data to find the best value for k.
- Plotted an elbow curve to visualize the optimal k.

![PCA Elbow Curve](/images/pca_elbow_curve.png)

## Cluster Cryptocurrencies with K-means Using the PCA Data

- Initialized the K-means model with the best value for k.
- Fitted the K-means model using the PCA data.
- Predicted clusters and added a new column with predicted cluster labels.
- Created a scatter plot to visualize the clusters using PCA data.

![PCA Data Clusters](/images/pca_data_clusters.png)

## Visualize and Compare the Results

- Created composite plots to compare the elbow curves and cluster results obtained from the original data and PCA data.

![Original vs. PCA Elbow Curves](/images/original_vs_pca_elbow.png)
![Original vs. PCA Clusters](/images/original_vs_pca_clusters.png)

## Conclusion

The CryptoClustering challenge involved preprocessing data, determining optimal cluster numbers, and using K-means clustering to group cryptocurrencies. The results were compared between original and PCA data, providing insights into the impact of feature reduction on clustering.

Feel free to explore the code in the [Crypto_Clustering.ipynb](Crypto_Clustering.ipynb) Jupyter Notebook for detailed implementation.

For images and more details, refer to the `images` directory in this repository.

Tags: #clustering #k-means #PCA #cryptocurrencies #data-analysis #machine-learning
