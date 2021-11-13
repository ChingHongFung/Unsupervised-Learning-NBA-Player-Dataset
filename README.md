# Unsupervised Learning: NBA PLayer Dataset

## Project Aim

This is a project looking at a nba player dataset. The objective is to test the performance of different clustering algorithms in grouping NBA players into clusters. It is especially fun as I could combine my ML skills with a personal interest to generate some interesting insights. Data is available via https://www.kaggle.com/drgilermo/nba-players-stats

A supervised learning approach is used where I tested the KMeans, Hierarchical and Mean-shift algorithms using Scikit-Learn and SciPy. More descriptions could be found in the Jupyter Notebook document.

### Technologies and Algorithms
* Python 3.8
* Scikit-Learn
* SciPy
* Plotly
* KMeans Clustering
* Hierarchical Clustering
* Mean-shift Clustering

## Overview

### PCA
Princiapl Component Analysis is used to reduce the dimensionality of the feature set for clear visualisation fo the data. 

![pca_reduction](https://user-images.githubusercontent.com/91271318/137004271-d3fc8797-3e88-46fb-adc9-96281691acf6.png)

### KMeans
I used an arbitary number of clusters of 10 to see how players would be grouped. This is a parameter that could be tuned in future works.

Diagram of KMeans results:

![kmeans](https://user-images.githubusercontent.com/91271318/137004266-97fff260-f5b9-4356-ad7b-6408d9956a6a.png)

### Hierarchical
This dendrogram shows how each clusters could be connected depending on the cut-off distance value. This is a parameter that could be tuned in future works.

![dendrogram](https://user-images.githubusercontent.com/91271318/137004259-cae74b96-abd3-4bc9-a2ff-295407a611e5.png)

Diagram of Hierarchical results:

![hierarchical](https://user-images.githubusercontent.com/91271318/137004265-8a586b60-c3da-43af-b462-276d47d7a40f.png)

### Mean-shift 
The bandwidth of the shifting window is set to 1 as an arbitary number which also could be tuned in future works.

Diagram of Mean-shift results:

![meanshift](https://user-images.githubusercontent.com/91271318/137004269-d66cba14-8805-45d4-9327-f418cdc45c3f.png)

## Conclusion
Throughout this analysis, it could be seen that mean-shift has resulted in the largest cluster of all due to the densely populated data in the centre whereas kmeans and hierchical have relatively similar results. As kmeans and hierarchical work on the basis of finding closest Euclidean distances and assinging data points to closest clusters, it is natural that those two resulted in closer results.

The choice of algorithms depends on domain requirement. For the purpose of this analysis, perhaps it is better to group players into clusters of similar sizes using kmeans and hierarchical. For alternative purposes, we might choose to use mean-shift or even DBSCAN to seek clusters based on density of the dataset. Nonetheless, it is interesting to see that certain players have been grouped in the outlying boundaries. For example, we see a group of predominantly hall-of-famers including Kobe Bryant, Kevin Garnett, Tim Duncan, etc. (a group consisting of legendary players in NBA history) in the top right corner which are assigned to the same cluster for all three models. With more refined models and domain knowledge, one could utilise clustering to carry out more sports analytics allowing teams to make strategic game plans accordingly.
