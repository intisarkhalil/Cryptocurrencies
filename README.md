# Cryptocurrencies.
- Machine Learning
- Unsupervised Learning.
- Python
- Jupyter Notebook
## Project overview
In this project we used the   unsupervised learning is used for, how to process data, how to cluster, how to reduce  dimensions, and how to reduce the principal components using PCA. We used the   all these skills to create an analysis for our clients who are preparing to get into the cryptocurrency market.
Accountability Accounting, a prominent investment bank,  it is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however,  lost in the vast universe of cryptocurrencies. So, they’ve asked us to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.
The data we are working on is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what we are looking for, we  decided to use unsupervised learning. To group the cryptocurrencies, we decided on a clustering algorithm.  we used data visualizations to share  findings.

## Challenges
### Preprocessing the Data for PCA:
  The following five preprocessing steps have been performed on the crypto_df DataFrame:
 
```
All cryptocurrencies that are not being traded are removed
The IsTrading column is dropped 
All the rows that have at least one null value are removed
All the rows that do not have coins being mined are removed 
The CoinName column is dropped 
A new DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame 
The get_dummies() method is used to create variables for the text features, which are then stored in a new DataFrame,
The features from the X DataFrame have been standardized using the StandardScaler fit_transform() function 
```
### Reducing Data Dimensions Using PCA.

```
The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components.
The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame.
```

### Clustering Cryptocurrencies Using K-means.
The K-means algorithm is used to cluster the cryptocurrencies using the PCA data, where the following steps have been completed:

```
An elbow curve is created using hvPlot to find the best value for K
Predictions are made on the K clusters of the cryptocurrencies’ data 
A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class.
```
### Visualizing Cryptocurrencies Results
```
The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover.
A table with tradable cryptocurrencies is created using the hvplot.table() function.
The total number of tradable cryptocurrencies is printed.
A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns.
A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point.
```
