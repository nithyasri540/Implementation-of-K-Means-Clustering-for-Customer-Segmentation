# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and load the Mall Customers dataset.
2.Check the dataset for information and missing values. 
3. Use the K-means clustering algorithm and apply the Elbow Method to find the optimal number of clusters.
4. Visualize the clusters using a scatter plot of Annual Income versus Spending Score.

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
<img width="783" height="400" alt="image" src="https://github.com/user-attachments/assets/11a1e2df-f94a-4a35-8934-cc41723a6c5e" />
<img width="797" height="162" alt="image" src="https://github.com/user-attachments/assets/a074bdee-de96-45bb-8456-0f783c5d513c" />

![WhatsApp Image 2026-02-25 at 11 08 23 AM](https://github.com/user-attachments/assets/ec1ee3eb-cf2c-43a3-8370-7e5ea089bd6b)
![WhatsApp Image 2026-02-25 at 11 08 23 AM (1)](https://github.com/user-attachments/assets/a48f4136-d06c-4730-8097-c2a816183ed2)





## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
