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
<p align="center"><b>Code Summary</b></p>

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


## Dataset: Indian Liver Patient Records
### Columns:

- 1. Age
- 2. Gender
- 3. Total_Bilirubin
- 4. Direct_Bilirubin
- 5. Alkaline_Phosphotas
- 6. Alamine_Aminotransferase
- 7. Aspartate_Aminotransferase
- 8. Total_Protiens
- 9. Albumin
- 10. Albumin_and_Globulin_Ratio
- 11. Dataset (Label)

### Data Analysis:
- Loaded the dataset in a dataframe using pandas.
- Checked for null values and handled the null values by replacing them with the mean of the column.
- Encoded the Gender column i.e., (to convert the datatype of Gender column from object to int)
   Encoded 'Male' as 1
   Encoded 'Female' as 2
- Now our datatset is ready to be passed through KNN algoirthm

## KNN Algorithm:
Implemented the KNN algorithm by defining following functions.

### Function 1:
- Name: functionToCalEuclideanDistance
- Purpose: To find the euclidean distance between the the two records/data (i.e. between each training data and test data).
- Input: Training Dataset, Testing Dataset and number of columns of testing dataset
- Returns: The euclidean distance between each training dataset and testing dataset

### Function 2:

- Function Name: functionForKNNAlgo
- Purpose: Function to implement KNN algorithm and prints the k nearest neighbors and predicted class of the test data.
- Input: Value of K, Training Dataset, Testing Dataset and Auto/manual i.e., whether value of k has to be auto generated or manually - inputted by the user
- Output: Prints the k nearest neighbors and predicted class of the test data.

### Function 3:

- Function Name: functionToFindTheClass
- Purpose: Function to parse and to find the class of all the neighbors and then sort in to find the class that has maximum occurances (predicted class).
- Input: listOfNeighbors and trainingDataSet
- Returns: The first element of the sorted list i.e., the predicted class of the test dataset

### Function 4:

- Function Name: roundUpToLowestodd
- Purpose: To calculate the nearest odd integer (helpful in finding the auto generated value of k from the square root of number of records of training dataset).
- Input: varSqRootNoTrainDS (square root of number of records in training dataset)
- Returns: Nearest odd integer
