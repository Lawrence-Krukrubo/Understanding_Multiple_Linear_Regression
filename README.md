<h1 align="center">Understanding_Multiple_Linear_Regression (MLR)</h1>
<h2 align="center">Hard-coding an MLR Model from scratch in Python to Predict CO2 emissions using Matrix-Algebra and LSE</h2>

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
