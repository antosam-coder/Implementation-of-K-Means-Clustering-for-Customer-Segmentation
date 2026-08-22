# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load the customer dataset and select relevant features such as income and spending score.
2. Choose the number of clusters (K) and initialize the cluster centroids.
3. Assign customers to the nearest centroid and update the centroids repeatedly.
4. Repeat until convergence and analyze the resulting customer segments.


## Program:
```
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
data = pd.read_csv("Mall_Customer.csv")
X = data.iloc[:, [3, 4]].values
kmeans = KMeans(n_clusters=5, random_state=0)
y_kmeans = kmeans.fit_predict(X)
plt.scatter(X[:, 0], X[:, 1], c=y_kmeans, s=100)
plt.scatter(kmeans.cluster_centers_[:, 0],
            kmeans.cluster_centers_[:, 1],
            s=200,
            marker='X')
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")
+plt.show()
```

Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Anto Sam A
RegisterNumber: 212225060019


## Output:
<img width="953" height="558" alt="image" src="https://github.com/user-attachments/assets/02b44b20-4582-4a61-9f20-158624e170d0" />



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
