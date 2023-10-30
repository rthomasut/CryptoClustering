# CryptoClustering Challenge

In this challenge, you'll use Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes. This README will guide you through the process.

## Before You Begin

1. Create a new repository for this project called CryptoClustering.
2. Clone the new repository to your computer.
3. Push your changes to GitHub.

## Instructions

1. Rename the `Crypto_Clustering_starter_code.ipynb` file as `Crypto_Clustering.ipynb`.
2. Load the `crypto_market_data.csv` into a DataFrame.
3. Get the summary statistics and plot the data to see what the data looks like before proceeding.

### Prepare the Data

1. Use the `StandardScaler()` module from scikit-learn to normalize the data from the CSV file.
2. Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

### Find the Best Value for k Using the Original Scaled DataFrame

1. Use the elbow method to find the best value for k.
2. Create a list with the number of k values from 1 to 11.
3. Create an empty list to store the inertia values.
4. Create a for loop to compute the inertia with each possible value of k.
5. Create a dictionary with the data to plot the elbow curve.
6. Plot a line chart with all the inertia values computed with different values of k to visually identify the optimal value for k.

### Cluster Cryptocurrencies with K-means Using the Original Scaled Data

1. Initialize the K-means model with the best value for k.
2. Fit the K-means model using the original scaled DataFrame.
3. Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
4. Create a copy of the original data and add a new column with the predicted clusters.
5. Create a scatter plot using hvPlot with the x-axis as "PC1" and the y-axis as "PC2". Color the graph points with the labels found using K-means. Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

### Optimize Clusters with Principal Component Analysis

1. Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
2. Retrieve the explained variance to determine how much information can be attributed to each principal component.

### Find the Best Value for k Using the PCA Data

1. Use the elbow method on the PCA data to find the best value for k.
2. Create a list with the number of k-values from 1 to 11.
3. Create an empty list to store the inertia values.
4. Create a for loop to compute the inertia with each possible value of k.
5. Create a dictionary with the data to plot the elbow curve.
6. Plot a line chart with all the inertia values computed with different values of k to visually identify the optimal value for k.

### Cluster Cryptocurrencies with K-means Using the PCA Data

1. Initialize the K-means model with the best value for k.
2. Fit the K-means model using the PCA data.
3. Predict the clusters to group the cryptocurrencies using the PCA data.
4. Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
5. Create a scatter plot using hvPlot with the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d". Color the graph points with the labels found using K-means. Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency that each data point represents.

### Visualize and Compare the Results

1. Create a composite plot using hvPlot to compare the elbow curve created from the original data with the one created from the PCA data.
2. Create a composite plot to compare the cryptocurrency clusters that resulted from using the original data with those that resulted from the PCA data.

### Coding Conventions and Formatting

- Place imports at the top of the file.
- Name functions and variables with lowercase characters and underscores.
- Follow DRY (Don't Repeat Yourself) principles.
- Use concise logic and creative engineering where possible.

### Deployment and Submission

- Submit a link to a GitHub repository that's cloned to your local machine.
- Use the command line to add your files to the repository.
- Include appropriate commit messages in your files.

### Code Comments

- Be well commented with concise, relevant notes that other developers can understand.

---

Follow these instructions to complete the CryptoClustering challenge and meet the requirements for each section. Good luck!
