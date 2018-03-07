# Cross-Validation
CS 6301 Leave one out vs K-Fold Cross Validation in R
Validation Set (Simple Approach)
• Randomly divide dataset into training and test subsets
• Create model on training set
• Calculate test MSE on test set
• Problem: May be highly variable; different selections of training sets
can produce very different test MSEs for the same model

LOOCV
• For each data point in the dataset, do the following:
• Compute the model leaving the point (x,y) out
• Compute MSEi
Then, compute an overall average test MSE: Sum(for all i; MSEi)/n

K-fold Cross Validation
• Divide the dataset in k folds, and for each fold:
• Compute the model leaving the fold out
Compute MSEi and Overall Average like before.

K-fold Versus LOOCV
• Test MSE is made up of two parts: bias and variance
• LOOCV tends to overestimate test MSE variance
• The models are highly correlated
• K-fold tends to overestimate the bias
• Generally, K-fold is more accurate
