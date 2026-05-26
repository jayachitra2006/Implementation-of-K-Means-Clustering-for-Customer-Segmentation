# ML-EXP-11
# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary packages using import statement.
2. Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().
3. Import KMeans and use for loop to cluster the data and Predict the cluster and plot data graphs.
4. Print the outputs and end the program.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: JAYACHITRA J
RegisterNumber:  212224040312
*/
```
```
import pandas as pd 
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")
display(data.head())
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []
for i in range(1,11):
    Kmeans=KMeans (n_clusters = i, init ="k-means++")
    Kmeans.fit(d.iloc[:,3:])
    wcss.append(Kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("no of cluster")
plt.ylabel("wcss")
plt.title("Elbow Metthod")
km=KMeans(n_clusters=5)
km.fit(d.iloc[:,3:])
y_pred = km.predict(d.iloc[:,3:])
y_pred
d["clusters"]=y_pred
df0=d[d["clusters"]==0]
df1=d[d["clusters"]==1]
df2=d[d["clusters"]==2]
df3=d[d["clusters"]==3]
df4=d[d["clusters"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="clusters0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="pink",label="clusters1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="green",label="clusters2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="blue",label="clusters3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="black",label="clusters4")
plt.legend()
plt.title("Customer Segments")

```


## Output:

<img width="746" height="440" alt="image" src="https://github.com/user-attachments/assets/88ccc71d-885b-43cc-a338-133194a6d585" />

<img width="366" height="393" alt="image" src="https://github.com/user-attachments/assets/27f0a45d-4c4f-4456-9429-88e184cd59ba" />


<img width="842" height="716" alt="image" src="https://github.com/user-attachments/assets/1e3d624b-8a4e-417e-acd7-490896255005" />


<img width="796" height="534" alt="image" src="https://github.com/user-attachments/assets/6e13ed9a-1658-45d9-8c6b-c2ed8890cfd0" />





## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
