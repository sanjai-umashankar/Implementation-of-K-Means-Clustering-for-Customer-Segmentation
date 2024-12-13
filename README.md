# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 1.Import pandas and matplotlib.pyplot

2.Read the dataset and transform it

3.Import KMeans and fit the data in the model

4.Plot the Cluster graph
 

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: SANJAI U
RegisterNumber:  24004616
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("C:/Users/LENOVO/Downloads/Mall_Customers.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss = [] #Within-Cluster Sum of Square
#It is the sum of squared distance between each point & the centroid in a cluster.

for i in range(1,11):
    kmeans = KMeans(n_clusters = i,init = "k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])

y_pred = km.predict(data.iloc[:,3:])
y_pred

data["cluster"] = y_pred
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
*/
```

## Output:
![image](https://github.com/user-attachments/assets/42cc5d09-087a-4c72-8a4b-c1b3ebe7300d)

![image](https://github.com/user-attachments/assets/5df5a036-5a18-4e57-bbc2-19e0a9bf2741)

![image](https://github.com/user-attachments/assets/b659eb7f-28e8-4bdf-8b16-324ab794ac03)

![image](https://github.com/user-attachments/assets/c90488ac-7f58-4be8-98c6-8ad93162811d)

![image](https://github.com/user-attachments/assets/931bbc69-0a50-47a1-8fd1-0b7568c6282f)

![image](https://github.com/user-attachments/assets/4dfeac4f-d0d1-4bab-8776-b534448a1be7)

![image](https://github.com/user-attachments/assets/64005df5-d078-4ecd-8228-feada7586600)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
