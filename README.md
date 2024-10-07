# CryptoClustering
Module 19 Challenge

In this challenge, I used Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

To prepare the data, I used the StandardScaler module from scikit-learn to normalize the data from the CSV file, then created a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

To find the best value for k using the scaled DataFrame, I used the elbow method using the following steps:

Created a list with the number of k values from 1 to 11.
Created an empty list to store the inertia values.
Created a for loop to compute the inertia with each possible value of k.
Created a dictionary with the data to plot the elbow curve.
Plotted a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
Using these steps, I was able to find the best value for k, then clustered the crypto currencies with K-means using the scaled DataFrame:

Initialized the K-means model with the best value for k.
Fit the K-means model using the scaled DataFrame.
Predicted the clusters to group the cryptocurrencies using the scaled DataFrame.
Created a copy of the scaled DataFrame and add a new column with the predicted clusters.
Created a scatter plot using hvPlot as follows:
Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
Colored the graph points with the labels found using K-means.
Added the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
Using the original scaled DataFrame, I performed a PCA and reduced the features to three principal components. Next I retrieved the explained variance to determine how much information can be attributed to each principal component, then created a new DataFrame with the scaled PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

Next, I used the elbow method on the scaled PCA DataFrame to find the best value for k using the following steps:

Created a list with the number of k-values from 1 to 11.
Created an empty list to store the inertia values.
Created a for loop to compute the inertia with each possible value of k.
Created a dictionary with the data to plot the Elbow curve.
Plotted a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
Lastly, I used the following steps to cluster the cryptocurrencies for the best value for k on the PCA DataFrame:

Initialized the K-means model with the best value for k.
Fit the K-means model using the scaled PCA DataFrame.
Predicted the clusters to group the cryptocurrencies using the scaled PCA DataFrame.
Created a copy of the scaled PCA DataFrame and add a new column to store the predicted clusters.
Created a scatter plot using hvPlot as follows:
Set the x-axis as "PC1" and the y-axis as "PC2".
Colored the graph points with the labels found using K-means.
Added the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
Resources used for this project included: Referred to ChatGPT on two occasions.
