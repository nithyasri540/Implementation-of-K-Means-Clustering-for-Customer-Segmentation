# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required libraries and load the Mall Customers dataset.
2.Check the dataset for information and missing values.
3.Use the K-means clustering algorithm and apply the Elbow Method to find the optimal number of clusters.
4.Train the K-Means model with 5 clusters and predict the cluster values for each customer.
5.Visualize the clusters using a scatter plot of Annual Income versus Spending Score.
  

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: S.NITHYASRI
RegisterNumber: 25018590
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("C:/users/acer/Downloads/mall_Customers.csv")

print(data.head())

print(data.info())

data.isnull().sum()

from sklearn.cluster import KMeans
wcss = []

for i in range(1,11):
    kmeans = KMeans(n_clusters = i,init = "k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)
plt.xlabel("No of Cluster")
plt.ylabel("wcss")
plt.title("Elbow Method")
plt.figure()

km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])

KMeans(n_clusters=5)

y_pred = km.predict(data.iloc[:,3:])
print("Predicted values: \n",y_pred)

data["cluster"]=y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")
plt.legend()
plt.title("Customer Segments")
plt.show()
*/
```

## Output:
<img width="784" height="400" alt="Screenshot 2026-02-25 110921" src="https://github.com/user-attachments/assets/84c65b6c-4382-453d-b7e6-725c8adaabe4" />
<img width="797" height="163" alt="Screenshot 2026-02-25 111326" src="https://github.com/user-attachments/assets/207b4ddc-05e5-4fff-985a-d32b62d6cf03" />
<img width="1042" height="772" alt="image" src="https://github.com/user-attachments/assets/50d02d9d-0bd9-4f97-80d2-79e45c701968" />
<img width="1066" height="780" alt="image" src="https://github.com/user-attachments/assets/b153761b-af3c-42bb-af08-d274ce81f817" />





## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
