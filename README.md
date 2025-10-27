# 📘 Overview


# ⚙️ Flow

## 1.Flowchart 1: 
### (1) Open four_cols.csv and use the Data Table to describe the dataset content.
| Attribute Name | Attribute Meaning | Distribution |
| :--- | :--- | :--- |
| `income` | Customer Income | <img width="2329" height="329" alt="image" src="https://github.com/user-attachments/assets/4d02ece4-1308-4105-ae8e-611b7950ea39" /> |
| `age` | Customer Age | <img width="2335" height="335" alt="image" src="https://github.com/user-attachments/assets/c6d644a4-f9e5-43b0-a64f-975ccc145ebd" />|
| `days_since_purchase` | Days Since Last Purchase | <img width="2294" height="316" alt="image" src="https://github.com/user-attachments/assets/6a3779e5-4fdf-4c59-b824-cc60ae225b2b" />|
| `annual_spend` | Customer's Annual Spending Amount | <img width="2384" height="343" alt="image" src="https://github.com/user-attachments/assets/f744db5e-fcdf-441c-a0e9-b99d9145cead" />|

### (2) Use PCA to reduce the data to 2 dimensions, then plot in a Scatter Plot using the new dimensional space. Explain whether the plotting results can clearly show 3 clusters.
After using PCA to reduce the four-dimensional data to two dimensions, the generated scatter plot is as follows, where it can be clearly observed that the data mainly forms three clusters.

<img width="764" height="638" alt="image" src="https://github.com/user-attachments/assets/08694e97-b083-41e2-bb55-c91f2ed3aaf2" />

## 2.Flowchart 2:
### (1) Use k-Means with k=3, initialized with KMeans++, to cluster four_cols.csv, then reduce the data to 2 dimensions via PCA, and finally plot the clustered scatter plot using Scatter Plot (use different colors and shapes to represent data from different clusters).

<img width="764" height="514" alt="image" src="https://github.com/user-attachments/assets/3305b8bf-e963-4b7c-9061-9ea2080a1933" />

### (2) Similar to the above, change k=4 and k=5 respectively, and plot the clustered scatter plots.
The figure below is the scatter plot for k=4.

<img width="865" height="583" alt="image" src="https://github.com/user-attachments/assets/5c48dc5d-2b85-4660-924a-8f5d88d2f84e" />

The figure below is the scatter plot for k=5.
<img width="865" height="583" alt="image" src="https://github.com/user-attachments/assets/05fd415f-5f29-4d10-80ab-8c92b5d7f465" />

## 3.Flowchart 3:
### (1) Use the silhouette score evaluation method to select the optimal k value for k-Means, and explain whether the optimal k value differs from the number of clusters visualized in Flowchart 1. 
Using the silhouette score to evaluate the optimal k value, it is found that k=5 yields the highest silhouette score, which differs from the number of clusters observed in the visualization of Flowchart 1. The comparison chart generated from both visualizations is as follows.
| Flowchart 1 visualization cluster |Evaluating the Optimal k Value Using Silhouette Score |
| :--- | :--- |
|<img width="383" height="320" alt="image" src="https://github.com/user-attachments/assets/5b5ec976-c1d6-433a-b3d1-6426c52e8ea0" /> | <img width="379" height="319" alt="image" src="https://github.com/user-attachments/assets/bf5eac03-35d6-4877-a6c0-8228ca7f5c75" />|

### (2)Please use Box Plot analysis to examine the characteristics of each cluster under the optimal k value clustering. 
Under the condition of dividing into 5 clusters, the distribution of each cluster's respective attributes is as follows.

|income |age|
| :--- | :--- |
|<img width="1429" height="919" alt="image" src="https://github.com/user-attachments/assets/d2de9893-25b8-4b8f-884c-59b3528b7473" />|<img width="1342" height="929" alt="image" src="https://github.com/user-attachments/assets/25de0593-e124-43e9-b2fc-c9791d2c75be" />|
|days_since_purchase|annual_spend|
|<img width="1376" height="931" alt="image" src="https://github.com/user-attachments/assets/857dc36b-be5a-48d9-b29b-0e87760b3cb4" />|<img width="1532" height="943" alt="image" src="https://github.com/user-attachments/assets/fe4c1c56-0e88-411b-bf31-903841b8a5c9" />|
