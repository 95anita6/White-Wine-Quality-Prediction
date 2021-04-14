# White-Wine-Quality-Prediction
This project aims to predict the quality of white wine given their properties. 

## Data Collection:
The dataset was obtained from Kaggle : https://www.kaggle.com/xuzihe2010/wine-quality-red.

## Estimating weights using user defined function:
The dataset had most of the wine in quality '6'. The weight estimation done here is based on the matrix multiplication and optimizing the cost function of the linear regression using gradient descent method.

The dataset is split using a function split_train_test which takes the dataset and the split percentage as its parameters. It splits the dataset based on the specified percentage and returns the train and test datasets.

An initial weights matrix with all zero values is initialized. The shape of the weight matrix would be nX1 where n are number of variables for which the weights estimation is to be done. A prediction function is defined that does the prediction uisng dot product of the weight and the features matrix. A feature matrix is basically the value of each of the features that help in predicting the target. The shape of the feature matrix is mXn where m is number of observations and n is the number of feature variables.

myerror function calculates the error value for each of the prediction made. It takes target, features and weights matrix. A traget matrix is a nX1 matrix having all the actual output values. This function calls in the prediction function to calculate predicted values and then finds out the errors (Actual value - Predicted value). 

A mycost function then takes in targets, features and weights as parameters. It calls in the error function and the cost function value can be obtained by the dot product of the error matrix and transpose of error matrix. The dot product of these error matrix given the cost function that is the sum of square of the error value. 

The cost function is optimized by differentiating the equation. A gradient function then calculates the gradient by taking dot product of transpose of the feature matrix and the error matrix. The final function takes in the target matrix, feature matrix and a learning rate as paramaters. The learning rate is defined as the rate in which one would move down the cost function in order to get at the optimal value. The optimal value is obtained where the tangent of the cost function is zero. The function calculates the weights by multiplying the negative learning rate and the gradient and returns the weights estimated.  
