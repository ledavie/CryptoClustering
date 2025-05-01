# CryptoClustering
Module 19 Challenge
CryptoClustering
Overview
In this challenge, I applied Python and unsupervised machine learning skills to analyze and cluster cryptocurrencies based on their short-term price fluctuations. The primary objective is to determine whether cryptocurrencies are more influenced by 24-hour or 7-day price changes using K-Means clustering and Principal Component Analysis (PCA).

Files Provided
crypto_market_data.csv – The dataset containing cryptocurrency market data.

Crypto_Clustering_starter_code.ipynb – Starter notebook to be renamed and completed.

Additional module files from the Module 19 Challenge.

Instructions
Repository Setup
Create a new repository named CryptoClustering.

Clone the repository to your local machine.

Add all files provided.

Rename Crypto_Clustering_starter_code.ipynb to Crypto_Clustering.ipynb.

Commit and push your changes to GitHub regularly.

Steps
1. Load and Explore the Data
Load crypto_market_data.csv into a Pandas DataFrame.

Generate summary statistics and visualizations to understand the data distribution.

2. Prepare the Data
Normalize the data using StandardScaler() from scikit-learn.

Create a new DataFrame with the scaled data.

Set the coin_id column as the index.

3. Determine the Optimal k-Value
Use the elbow method to find the optimal number of clusters (k):

Create a list of k values from 1 to 11.

Compute and store the inertia for each value.

Plot the inertia values to identify the "elbow" point.

Document the chosen k-value in the notebook.

4. Cluster with K-Means
Apply K-Means clustering with the optimal k.

Add cluster labels to the scaled DataFrame.

Visualize the clusters using hvPlot.scatter:

x-axis: price_change_percentage_24h

y-axis: price_change_percentage_7d

Use cluster labels for color.

Include coin_id in the hover_cols.

5. Principal Component Analysis (PCA)
Apply PCA to reduce features to 3 components.

Retrieve and analyze the explained variance.

Create a new DataFrame with the PCA results, using coin_id as the index.

6. Reevaluate Optimal k with PCA Data
Repeat the elbow method using the PCA-transformed data.

Document the new optimal k and compare it to the original.

7. Cluster with PCA Data
Perform K-Means clustering on the PCA-transformed data using the optimal k.

Add cluster labels to the PCA DataFrame.

Create a scatter plot with:

x-axis: PC1

y-axis: PC2

Cluster labels as color

coin_id in hover_cols

Key Questions
What is the best value for k before and after PCA?

Does using PCA affect the clustering results?

What is the impact of using fewer features when clustering?

Technologies
Python

Pandas

scikit-learn

hvPlot

Jupyter Notebook

Usage
To run the analysis:

Open Crypto_Clustering.ipynb in Jupyter Notebook.

Run each cell sequentially.

Observe outputs and visualizations to interpret the results.
