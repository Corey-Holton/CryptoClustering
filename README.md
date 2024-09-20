# Cryptocurrency Market Data Clustering and PCA Analysis

This project aims to cluster cryptocurrencies based on various price change percentages over different time periods. It uses K-Means clustering and Principal Component Analysis (PCA) to explore patterns in the data.

## Project Structure

### 1. **Data Preparation**
   - The data is loaded from `crypto_market_data.csv`, and the index is set to `coin_id`.
   - Columns used: Various price change percentages over different time periods such as 24 hours, 7 days, 30 days, etc.
   - The data is normalized using `StandardScaler` from `scikit-learn`.

### 2. **K-Means Clustering**
   - **Objective**: Cluster the cryptocurrencies using K-Means to group them based on their price change patterns.
   - The optimal number of clusters (`k`) is determined using the Elbow method. The elbow plot is generated to visually identify the ideal value of `k` (which is 4 for this dataset).
   - Clustering is performed both on the original scaled data and on the PCA-reduced data.

### 3. **Principal Component Analysis (PCA)**
   - **Objective**: Reduce the dimensionality of the data while retaining most of the variance.
   - PCA reduces the data into 3 principal components, which explain approximately 89.50% of the variance.
   - The weights of each feature on the principal components are also analyzed to understand which features contribute the most to each component.

### 4. **Visualization**
   - Scatter plots are generated to visualize clusters based on both the original data and the PCA-transformed data.
   - The PCA-based scatter plot shows how cryptocurrencies are grouped in a lower-dimensional space.

## Project Workflow

1. **Data Loading and Preprocessing**:
   - `crypto_market_data.csv` is loaded, and the features are normalized using `StandardScaler`.

2. **Clustering using K-Means**:
   - The Elbow method is used to find the optimal number of clusters (`k`), which is 4.
   - Clusters are predicted using the K-Means model, and cryptocurrencies are assigned to clusters.

3. **Dimensionality Reduction with PCA**:
   - PCA is applied to reduce the dataset to 3 principal components.
   - The clusters are then predicted using PCA data, and the results are visualized using scatter plots.

4. **Feature Importance**:
   - The contributions of each original feature to the principal components are calculated to determine the importance of each feature in the PCA model.

## Results
- **Best k-value**: 4 (consistent across original and PCA-transformed data).
- **Total Explained Variance by PCA**: 89.50%.
- **Cluster Visualization**: Visualizations show distinct clusters for cryptocurrencies based on price change percentages.

## Usage

To run the analysis:
1. Ensure the required dependencies are installed:
   ```bash
   pip install pandas scikit-learn hvplot
2. Place the `crypto_market_data.csv` file in the `Resources` folder.
3. Run the script to generate the clustering analysis and visualizations.

## Dependecies
   - Python 3.x
   - Pandas
   - Scikit-learn
   - Hvplot

## References
Classwork was the main sorce of finding code for this project. Chat GPT was used to assist with the readme file. Homework was reviewed by TA's but no significant changes were made based on their reviews.
