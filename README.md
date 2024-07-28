# CryptoClustering

## Cryptocurrency Clustering Project

This project focuses on clustering cryptocurrencies using K-means clustering and Principal Component Analysis (PCA). The steps include data normalization, finding the optimal number of clusters (k) using the elbow method, clustering with K-means, and optimizing clusters with PCA. Visualizations are created to analyze the clustering results.

### File Structure

```
CryptoClustering/
├── Resources/
│   └── crypto_market_data.csv        # CSV file containing the cryptocurrency data
├── Crypto_Clustering.ipynb           # Jupyter Notebook with the analysis and visualizations
└── README.md                         # This README file

```

### What do you need?

- Python 3.7+
- pandas
- scikit-learn
- hvPlot
- Jupyter Notebook

### How to use the code?

1. Clone this repository to your local machine.
2. Install the required libraries using pip install
3. Open the Jupyter Notebook `Crypto_Clustering.ipynb` to view and run the analysis.

### Steps and Features

#### Prepare the Data

- Normalize the Data:
  - Use StandardScaler from scikit-learn to normalize the data from the CSV file.
  - Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame.

#### Find the Best Value for k Using the Original Scaled DataFrame

- Elbow Method:
  - Create a list with k values from 1 to 11.
  - Compute inertia for each k and store the values.
  - Plot the elbow curve to visually identify the optimal k.
  - Question: What is the best value for k?

#### Cluster Cryptocurrencies with K-means Using the Original Scaled Data

- K-means Clustering:
  - Initialize and fit the K-means model with the best value for k.
  - Predict the clusters using the scaled DataFrame.
  - Add a new column with the predicted clusters to the original DataFrame.
  - Create a scatter plot using hvPlot.

#### Optimize Clusters with Principal Component Analysis

- PCA:
  - Perform PCA on the original scaled DataFrame and reduce to three principal components.
  - Retrieve explained variance and determine the total explained variance.
  - Create a new DataFrame with PCA data and set the "coin_id" index.

#### Find the Best Value for k Using the PCA Data

- Elbow Method on PCA Data:
  - Repeat the elbow method steps using PCA data to find the best k.
  - Questions:
    - What is the best value for k using PCA data?
    - Does it differ from the original data?

#### Cluster Cryptocurrencies with K-means Using the PCA Data

- K-means Clustering on PCA Data:
  - Initialize and fit the K-means model with the best value for k using PCA data.
  - Predict the clusters using the PCA DataFrame.
  - Create a scatter plot using hvPlot.
  - Question: What is the impact of using fewer features to cluster the data using K-means?

### Conclusion

This project provides a comprehensive approach to clustering cryptocurrencies using K-means and PCA, offering insights into the optimal number of clusters and the impact of dimensionality reduction on clustering performance.
