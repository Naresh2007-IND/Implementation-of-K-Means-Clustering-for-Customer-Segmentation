# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries, load the mall customer dataset, and check for missing values and dataset information.
2. Apply the K-Means clustering algorithm with different cluster values to calculate WCSS and use the Elbow Method to find the optimal number of clusters.
3. Train the K-Means model with 5 clusters, predict customer groups, and store the cluster labels in the dataset.
4. Separate the customers based on clusters and visualize the customer segments using a scatter plot of Annual Income vs Spending Score.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Naresh J<br>
RegisterNumber:  212225230195 <br>
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers (1).csv")
data.head()
data.info()
data.isnull()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss= [] 
for i in range(1,11):
kmeans=KMeans(n_clusters = i,init = "k-means++")
kmeans.fit(data.iloc[:,3:])
wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No. of clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])
y_pred=km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
1/4
https://github.com/Guhanandan/Implementation-of-K-Means-Clustering-for-Customer-Segmentation
11/24/24, 6:00 PM
Guhanandan/Implementation-of-K-Means-Clustering-for-Customer-Segmentation
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="black",label="clu
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="cyan",label="clust
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="yellow",label="cl
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="blue",label="clust
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="green",label="clu
plt.legend()
plt.title("Customer Segments")
*/
```

## Output:
![K Means Clustering for Customer Segmentation](sam.png)<img width="764" height="1079" alt="Screenshot 2026-05-16 160610" src="https://github.com/user-attachments/assets/b2d58f13-be11-47ae-b4d8-680ca5a77a6f" />
<img width="551" height="322" alt="Screenshot 2026-05-16 161117" src="https://github.com/user-attachments/assets/5cb1219e-1ae1-405b-ac69-abf5dc69a5da" />



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
