# EECS-738: Probably Interesting Data (Assignment-1)
This repository contains our submission for EECS-738: Assignment-1.

## Members
- Waqar Ali (2873101)
- Pushkar Singh Negi (2946319)

## Datasets
We have used the following datasets from UCI-ML site:
- [Auto-MPG Dataset](https://www.kaggle.com/uciml/autompg-dataset)
- [Indian Liver Patient Dataset](https://www.kaggle.com/uciml/indian-liver-patient-records)

## Algorithms
As part of this assignment, we have implemented the following algorithms:
- K-Means
- K-Nearest Neighbors

## Demonstration
The implementation and documentation of both of these algorithms along with their demonstration on the chosen datasets can be seen in the following notebooks:
- [K-Means Notebook](notebooks/kmeans.ipynb)
- [K-NN Notebook](notebooks/knn.ipynb)

---
<p align="center">Code Summary</b></p>

### K-Means
__Function:__ kmean (points, clusters, DEBUG)
Input:
- points: A dictionary of points
- clusters: Number of clusters to form
- DEBUG: Enable visualization and print debugging information every step of the way in the algorithm

Output:
- centers: A list of cluster centers formed by Kmeans
- clusters: A dictionary of points classified in specified number of clusters

__Function:__ pointify (series_1, series_2, ..., series_i)
Input:
- series_i: A number of series (i.e., column of pandas data frame or an array of values)

Output:
- points: A dictionary of points which can be passed to kmeans algorithm
