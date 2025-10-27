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

| Cluster | Income | Age | Days Since Purchase | Annual Spend |
| :--- | :--- | :--- | :--- | :--- |
| C1 | Similar to C4 and C5 distributions, most data falls around 43,000. | Similar to C3 and C5 distributions, most data falls around 50. | Similar to C2 distribution, most data falls around 300. | Similar to C3 and C5 distributions, most data falls around 5,500. |
| C2 | Similar to C3 distribution, most data falls around 115,000, but with more severe outliers. | Similar to C4 distribution, most data falls around 30. | Similar to C1 distribution, most data falls around 300. | Similar to C4 distribution, most data falls around 2,500. |
| C3 | Similar to C3 distribution, most data falls around 115,000. | Similar to C1 and C5 distributions, most data falls around 50. | Similar to C4 and C5 distributions, most data falls around 500. | Similar to C1 and C5 distributions, most data falls around 5,500. |
| C4 | Similar to C1 and C5 distributions, most data falls around 43,000. | Similar to C2 distribution, most data falls around 30. | Similar to C3 and C5 distributions, most data falls around 500. | Similar to C2 distribution, most data falls around 2,500. |
| C5 | Similar to C1 and C4 distributions, most data falls around 43,000. | Similar to C1 and C3 distributions, most data falls around 50. | Similar to C3 and C4 distributions, most data falls around 500. | Similar to C1 and C3 distributions, most data falls around 5,500. |

Finally, based on the above data, we can simply infer the customer characteristics of each cluster as follows: (Due to the obvious outliers in the attribute data, the following inferences do not represent that all customers in the cluster possess the cluster characteristics)
C1: Middle income, frequently purchases the company's products, and has a high purchase amount—middle-aged individuals.
C2: High income, frequently purchases the company's products, but has a low purchase amount—young individuals.
C3: High income, occasionally purchases the company's products, but has a high purchase amount—middle-aged individuals.
C4: Middle income, occasionally purchases the company's products, and has a low purchase amount—young individuals.
C5: Middle income, occasionally purchases the company's products, but has a high purchase amount—middle-aged individuals.

### (3) Please analyze, if you are the marketing department supervisor, when formulating marketing strategies, whether k=3 or the optimal k value is more practical.
K=3 is more practical. If customers are divided into more clusters, more differentiated marketing is required, which increases marketing costs. If dividing into more clusters cannot effectively distinguish differences between clusters, then when performing customer classification, it is preferable to divide into fewer clusters. Under the optimal k value (k=5), there are three clusters of customers whose characteristics are not significantly different from each other, and no obvious differences can be observed, so treating them as the same cluster can effectively reduce marketing costs.

## 4.Flowchart 4:
### (1) For Top N=3, use Hierarchical Clustering with the silhouette score evaluation method to identify the best linkage method (25%), and organize the experimental results in a Data Table. 
The following figure lists the clustering results for different linkages.
|Single |Average|Weighted|
| :--- | :--- | :--- |
|<img width="233" height="177" alt="image" src="https://github.com/user-attachments/assets/70db7a63-b28c-401b-99d7-367595dbecc5" /> |<img width="240" height="177" alt="image" src="https://github.com/user-attachments/assets/06199cff-ccf5-42a5-aa14-f57f91f617d7" /> |<img width="219" height="163" alt="image" src="https://github.com/user-attachments/assets/de2665f3-2de3-482f-9eb0-5ac12aa37943" /> |
| Complete | Ward | |
|<img width="237" height="178" alt="image" src="https://github.com/user-attachments/assets/4cbf7f42-dbd6-4331-9bdb-d04e36bd43a1" /> |<img width="244" height="183" alt="image" src="https://github.com/user-attachments/assets/7ecb3513-68a7-45d8-96fd-1850b0b45a06" /> | |

The following table shows the silhouette score values for each cluster under different linkage methods.
 | Linkage type | C1    | C2    | C3    |
| :--- | :--- | :--- | :--- |
| Single       | 0     | 0     | -0.446 |
| Average      | -0.524| 0.512 | 0.616  |
| Weighted     | -0.556| 0.498 | 0.605  |
| Complete     | -0.313| 0.569 | -0.244 |
| Ward         | -0.524| 0.512 | 0.606  |

After comparison, it is found that under the TOP N=3 condition, the sum of the scores for Average linkage and Ward linkage is the highest. Additionally, upon observing the MDS, the clustering situation is more distinct compared to the other three methods. Therefore, Average linkage and Ward linkage are the best linkage methods.


## 5.Flowchart 5:
### (1) Use paint data to create the following four clusters. 
The data produced using paint data is as follows, along with the figure below.

<img width="749" height="1044" alt="image" src="https://github.com/user-attachments/assets/021414f2-c524-4f6f-9b95-13ab80eb44f1" />

### (2) Please perform the following three operations on the results of the above figure respectively:
#### 2-1. Use DBSCAN to divide into four clusters, and explain the parameter values used. 
In DBSCAN, the parameter values used are as follows.

| Parameter Name          | Parameter Meaning  | Actual Set Value |
| :---                     | :---                                                                               | :---              |
| `Core point neighbor`   | In a circle centered at point X with radius Neighborhood distance, if the number of data points inside is greater than Core point neighbor, then X is considered a core point. | 4                |
| `Neighborhood distance` | Circle radius; the smaller the radius, the fewer core points in the dataset, which may result in more clusters. | 0.234            |

The initial default for the Neighborhood distance is positioned on the axis point of the core point count. Taking the following figure as an example, it will first search for the Neighborhood distance when the core point count is 100 (i.e., setting this dataset to have 100 core points).

<img width="735" height="517" alt="image" src="https://github.com/user-attachments/assets/411a40f5-5424-4940-b218-da6193a73a8e" />

Furthermore, for subsequent fine-tuning, one can simultaneously open the DBSCAN and Scatter plot pages, adjusting the baseline while monitoring whether the number of noise points in the Scatter plot decreases. The final experimental results also indicate that, with the core point neighbor set to 4 and the neighborhood distance set to 0.234, the clustering results exhibit the fewest noise points and are similar to the initial clustering data, as shown in the following figure.

<img width="729" height="327" alt="image" src="https://github.com/user-attachments/assets/91fcaf9e-28d2-4de3-b759-71d5516eee37" />

#### 2-2.Try different linkage methods of Hierarchical Clustering, and explain whether similar four clusters to the above figure can be found. 

After plotting the different linkages using scatter plots, it can be found that the result from using single linkage is the closest to the clustering result of the original figure.



