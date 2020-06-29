# Cryptocurrencies

## Resources
* Data Source: crypto_data.csv
* Software: Python 3.7.6, Jupyter Notebook
* Libraries: Pandas, Plotly Express, Hvplot, Sklearn

## Data Preprocessing
Start by loading the data in a Pandas DataFrame 
named “crypto_df.” Continue with the following data preprocessing tasks:

1. Remove all cryptocurrencies that aren’t trading.
2. Remove all cryptocurrencies that don’t have an algorithm defined.
3. Remove the IsTrading column.
4. Remove all cryptocurrencies with at least one null value.
5. Remove all cryptocurrencies without coins mined.
6. Store the names of all cryptocurrencies on a DataFramed named coins_name, and use the crypto_df.index as the index for this new DataFrame.
7. Remove the CoinName column.
8. Create dummies variables for all of the text features, and store the resulting data on a DataFrame named X.
9. Use the StandardScaler from sklearn (Links to an external site.) to standardize all of the data from the X DataFrame.
 Remember, this is important prior to using PCA and K-means algorithms.

 ## Reducing Data Dimensions Using PCA
Use the PCA algorithm from sklearn (Links to an external site.) to reduce the 
dimensions of the X DataFrame down to three principal components.

Once you have reduced the data dimensions, create a DataFrame named “pcs_df” 
that includes the following columns: PC 1, PC 2, and PC 3. Use the crypto_df.index as the index for this new DataFrame.

## Clustering Cryptocurrencies Using K-means
You’ll use the KMeans algorithm from sklearn (Links to an external site.) to cluster the cryptocurrencies using the PCA data.

Complete the following tasks:

1. Create an elbow curve to find the best value for K, and use the pcs_df DataFrame.
2. Once you define the best value for K, run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data. Use the pcs_df to run the K-means algorithm.
3. Create a new DataFrame named “clustered_df,” that includes the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class.


## Visualizing Results

You’ll create data visualizations to present the final results.

Complete the following tasks:

1. Create a 3D scatter plot using Plotly Express to plot the clusters using the clustered_df DataFrame. You should include the following parameters on the plot: hover_name="CoinName" and hover_data=["Algorithm"] to show this additional info on each data point.
2. Use hvplot.table to create a data table with all the current tradable cryptocurrencies. The table should have the following columns: CoinName, Algorithm, ProofType, TotalCoinSupply, TotalCoinsMined, and Class.
3. Create a scatter plot using hvplot.scatter to present the clustered data about cryptocurrencies having x="TotalCoinsMined" and y="TotalCoinSupply" to contrast the number of available coins versus the total number of mined coins. Use the hover_cols=["CoinName"] 
parameter to include the cryptocurrency name on each data point.

## Usage
Note: Please ensure you have all the required and updated softwares on your computer.

Download the following files into the same folder for the project.

Resource/crypto_data.csv
Cryptocurrency.ipynb
In your Anaconda prompt, activate your development environment and navigate to the folder holding the above files and run Jupyter Notebook. For this specific project, Jupyter Notebook will render the plots. If you want to run the visualizations in Jupyter Lab, you will need to install a few things first. You can check out what is needed at https://plotly.com/python/getting-started/#jupyterlab-support-python-35.

You can now run all the cells to see their outputs. If you want to test out the results, you can change the parameters.