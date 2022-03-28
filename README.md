# My Own Implementation of K-Nearest Neigbours
I developed a K-NN model which I used to classify the flower type in the Iris dataset. I developed as well my own implementation of nested cross validation

## Project Overview
* Developed my own K-NN using only numpy and pandas for the classification task of the Iris dataset, achiving an accuracy of 96.67% using k=10 and euclidean distance.
* Created a visualisation for Exploratory Data Analysis
* Created my own function for K-NN
* created my own evaluation functions for accuracy calculation and confution matrix creation
* Created my own function for Nested k-Fold Cross validation.
* Trained and tested the implematation using the Iris dataset and a the same dataset with addition of random noise.
* The first implementation of K-NN with k=10 and euclidean distance achieved an accuracy of 96.67%
* The Nested Cross validation achieved an accuracy of 96.00 $\pm$ 3.27

## Code and Resources Used
* **Python version:** 3.7
* **Packages:** matplotlib, pandas, numpy, sklearn.datasets

## Exploratory Data Analysis
I created the following graph, similar to the seaborn pair plot

[](https://github.com/CarolinaKra/K-NNmyOwnImplementation/blob/main/Images/EDA.png)

## Created my own function for K-NN
* I created functions to calculate different distances which will be the users options: 'euclidean' and 'manhatan'
* I created a function 'find neighbours'. Given the training data, a specific test point, the distance metric and the 'k' number of neighbors, the function finds the closest neighbors.
* I created the k-NN which predicts the category for a set of test points using the previosly created functions
* I created my own functions for model evaluation.
* I tested the function using the Iris dataset, k=10 and euclidean distance, which achieved an accuracy of 96.67%

The confusion matrix looked as follows:

[](https://github.com/CarolinaKra/K-NNmyOwnImplementation/blob/main/Images/ConfMatrix.png)

## Created my own function for Nested k-fold validation
* I created two helper functions:
  * One function to split the data into training sets(training input, training targets) and test sets (test input, test target) for the different iteration of the nested cross validation
  * A second function to find the most frequent value in a list
* I created the nested k-fold cross validation for K-NN. Given the initial data, the number of folds, the list of Ks, a list of metric systems and a seed number, the function performs a nested cross-validation with kNN and returns a list of accuracies and prints at each fold the best k, the best distance, the accuracy and the confusion matrix.

A summary of the results were as follows:

[](https://github.com/CarolinaKra/K-NNmyOwnImplementation/blob/main/Images/kfoldresults.png)

