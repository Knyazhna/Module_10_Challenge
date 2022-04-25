# Crypto Clustering
In this challange we’ll combine our financial Python programming skills with the new unsupervised learning skills that we acquired.

---
## Technologies

Crypto Clustering project leverages python 3.7 with the following packages:

  [Pandas](https://github.com/pandas-dev/pandas "Pandas") 
  
 --- 
  ## Installation Guide

First install the following libraries and dependencies.

```
# conda
conda install pandas
```
  [Hvplot](https://hvplot.holoviz.org/user_guide/Plotting.html "Hvplot") 
   
  [scikit-learn](https://scikit-learn.org/stable/user_guide.html "Scikit-learn") 

```
import pandas as pd
import hvplot.pandas
from path import Path
from sklearn.cluster import KMeans
from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler
```

---
## Usage

**Import and Prepare Data**

Import and prepare the data. Plot the data to see what's in the DataFrame.

![](Images/Market_data_plot.png)

**Best Value for k Using the Original Data**

Code the elbow method algorithm to find the best value for k and plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

![](Images/Elbow_curve.png)

**Cluster Cryptocurrencies with K-means Using the Original Data**

Initialize, Fit the K-means model, Predict the clusters to group the cryptocurrencies using the original data. Use hvPlot, create a scatter plot.

![](Images/Cluster_plot.png)

**Optimize Clusters with Principal Component Analysis**

Create and use a PCA model to reduce to 3 principal components.

Answer the following question: What is the total explained variance of the three principal components?

```
pca.explained_variance_ratio_.sum()
```

```
df_crypto_pca_data = pd.DataFrame(crypto_pca_data, columns=["PC1", "PC2", "PC3"])
```

**Best Value for k Using the PCA Data**

Code the elbow method algorithm and use the PCA data. Plot a chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

![](Images/PCA_elbow.png)

**Cluster Cryptocurrencies with K-means Using the PCA Data**

Initialize the K-means model with four clusters by using the best value for k. Fit the K-means model by using the PCA data. Predict the clusters to group the cryptocurrencies by using the PCA data. Finally, create the PCA scatter plot.

![](Images/PCA_cluster_plot.png)

**Visualize and Compare the Results**

Create a composite plot using hvPlot and the plus (+) operator to compare the elbow curve that you created to find the best value for k with the original data and the PCA data.
```
elbow_plot + elbow_pca_plot
```
Create a composite plot using hvPlot and the plus (+) operator to compare the cryptocurrencies clusters using the original data and the PCA data.
```
crypto_clusters + pca_clusters
```


---
## Contributors

* Brought to you by Olga Koryachek.
* Email: olgakoryachek@live.com
* [LinkedIn](https://www.linkedin.com/in/olga-koryachek-a74b1877/?msgOverlay=true "LinkedIn")

---
## License

Licensed under the [MIT License](https://choosealicense.com/licenses/mit/)
