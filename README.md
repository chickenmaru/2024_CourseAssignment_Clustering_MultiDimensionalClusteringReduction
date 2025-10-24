# 2024_CourseAssignment_Clustering_MultiDimensionalClusteringReduction

# Overview


# Flow

## 1.Flowchat 1: 
### (1) Open four_cols.csv and use the Data Table to describe the dataset content.
| Attribute Name | Attribute Meaning | Distribution |
| :--- | :--- | :--- |
| `income` | Customer Income | <img width="2329" height="329" alt="image" src="https://github.com/user-attachments/assets/4d02ece4-1308-4105-ae8e-611b7950ea39" /> |
| `age` | Customer Age | <img width="2335" height="335" alt="image" src="https://github.com/user-attachments/assets/c6d644a4-f9e5-43b0-a64f-975ccc145ebd" />|
| `days_since_purchase` | Days Since Last Purchase | <img width="2294" height="316" alt="image" src="https://github.com/user-attachments/assets/6a3779e5-4fdf-4c59-b824-cc60ae225b2b" />|
| `annual_spend` | Customer's Annual Spending Amount | <img width="2384" height="343" alt="image" src="https://github.com/user-attachments/assets/f744db5e-fcdf-441c-a0e9-b99d9145cead" />|

### (2) Use PCA to reduce the data to 2 dimensions, then plot in a Scatter Plot using the new dimensional space. Explain whether the plotting results can clearly show 3 clusters. (10%)
After using PCA to reduce the four-dimensional data to two dimensions, the generated scatter plot is as follows, where it can be clearly observed that the data mainly forms three clusters.

<img width="764" height="638" alt="image" src="https://github.com/user-attachments/assets/08694e97-b083-41e2-bb55-c91f2ed3aaf2" />

## 2.Flowchat 2:
### (1) Use k-Means with k=3, initialized with KMeans++, to cluster four_cols.csv, then reduce the data to 2 dimensions via PCA, and finally plot the clustered scatter plot using Scatter Plot (use different colors and shapes to represent data from different clusters).

<img width="764" height="514" alt="image" src="https://github.com/user-attachments/assets/3305b8bf-e963-4b7c-9061-9ea2080a1933" />

### (2) Similar to the above, change k=4 and k=5 respectively, and plot the clustered scatter plots. (10%)
The figure below is the scatter plot for k=4.

<img width="865" height="583" alt="image" src="https://github.com/user-attachments/assets/5c48dc5d-2b85-4660-924a-8f5d88d2f84e" />

The figure below is the scatter plot for k=5.
<img width="865" height="583" alt="image" src="https://github.com/user-attachments/assets/05fd415f-5f29-4d10-80ab-8c92b5d7f465" />


