<h1 align="center">Understanding_Multiple_Linear_Regression (MLR)</h1>
<h2 align="center">Hard-coding an MLR Model in Python to Predict CO2 emissions using Matrix-Algebra and LSE</h2>

<p align="center">
  <img src="https://github.com/Lawrence-Krukrubo/Understanding_Multiple_Linear_Regression/blob/master/mlr-correlation.jpg?raw=true" height=400 width= 600 alt="mlr correlation">
</p>

Let’s see how a Multiple Linear Regression(MLR) model computes the ideal parameters, given the features matrix **(_X)** and target variable **(_y)**, using Linear Algebra.

_**X**_ is an (_m_ * _n_ feature matrix) and _y_ is an(_m_* 1 column vector)
Where:

* _m_ is the number of observations or rows in the data set
* _n_ is the number of attributes or variables selected for the prediction
* _X_ is the m * n feature matrix of independent variables
* _y_ is the target or dependent variable

In Multiple Linear Regression, we try to predict a continuous dependent variable, using two or more features or independent variables.
In this case, we want to predict **CO2_EMISSIONS**, using two or more features from the data set. Features could be _Engine_Size, Cylinders, Make, Model_, e.t.c.
So to define our feature matrix _X_, we need to select ideal features from the data set that are correlated with CO2_EMISSIONS.


<h3>Structure:</h3>

<h4>1. Exploring Real-World Data</h4>

We shall use the Fuel consumption rating data set for car sales in Canada. See [link to download](https://open.canada.ca/data/en/dataset/98f1a129-f628-4ce4-b24d-6f16bf24dd64).

**Tasks Include:**

* Importing the data.
* Importing required libraries
* Reading to a pandas DataFrame
* Exploring the data
* Cleaning the data
* Checking for missing values
* Renaming attributes 

<h4>2. Computing the ideal coefficients of the Model</h4>

First we define the shapes and create the feature matrix, target vector and the coefficients vector.

**Task A:**

Defining <em><b>X</b></em> the Feature matrix.<br>
This includes the following:-

* Standardizing the data
* Computing the Feature-Target-Correlation matrix.
* Checking for Multicolinearity
* Computing Variance Inflation Factor (VIF)

**Task B:**

Defining <em><b>X</b></em> the Coefficients matrix.<br>
This Matrix is made up of the Slopes or Gradients <em><b>(b1…bn)</b></em> and the intercept or bias unit<b><em>(b0)</b></em>

We compute the Least Squares Estimate method **(LSE)**

* Step 1: Compute X-transposed matrix
* Step 2: Compute X-transposed post-multiplied by matrix X
* Step 3: Compute the inverse of X-transposed post-multiplied by matrix X
* Step 4: Post-multiply inverse of X-transposed-X by X-transposed
* Step 5: Finally, we post-multiply X-transposed-X-Inverse-X-transposed by vector y

<h4>3. Predictions and Evaluation:</h4>

After computing the ideal coefficients of the model via the LSE above, the next thing is to simply substitute the coefficints into the Multiple Linear regression Model equation:-  <b><em>Y_hat = B0 + b1x1 + b2x2 + b3x3 ... + bnxn</em></b>.

After the substitution, we make predictions on the test set and evaluate our predictions using the **MSE**, **MAE**, **RMSE** or any relevant metrics.

<h4>4. Dependencies:</h4>

To follow along with these exercises, you need to install and import the following libraries

* `import matplotlib.pyplot as plt`
* `import pandas as pd`
* `import seaborn as sns`
* `import pylab as pl`
* `import numpy as np`
* `import missingno as msno`
* `from sklearn.model_selection import train_test_split`
* `from sklearn.linear_model import LinearRegression`
* `from sklearn.metrics import mean_squared_error, r2_score`

<h4>5. Blog-Post:</h4>

Kindly see my article published in TowardsAI publication in Medium that goes through this entire project. I explain every code cell and intuition. For example the fact that LSE can only be done in a Feature matrix where the independent variables are linearly-dependent.<br>See link [here](https://medium.com/towards-artificial-intelligence/understanding-multiple-linear-regression-1b4a5b939f5a)

<h4>6. Summary:</h4>

This project demonstrates how multiple linear regression(MLR) works step by step using Matrix Algebra.
I built an MLR Model from scratch by first determining correlated variables, determining multicollinearity and selecting 3 moderately linear-independent variables.

Then I trained the model with the training data set using matrix multiplication in line with the **Least-Squares-Estimate** formula and used the model to make predictions on the test data set that is not yet known to the model(out of sample data set).
Finally, I evaluated the model using MSE, RMSE and r2_score and compared it to a model from the Sklearn library.

<h4>7. License:</h4>

Every analysis, file or document in the project is covered by the **MIT** license attached in the Repo.







