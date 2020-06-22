<h1 align="center">Understanding_Multiple_Linear_Regression (MLR)</h1>
<h2 align="center">Hard-coding an MLR Model from scratch in Python to Predict CO2 emissions using Matrix-Algebra and LSE</h2>

Let’s see how a Multiple Linear Regression(MLR) model computes the ideal parameters, given the features matrix $(X)$ and target variable $(y)$, using Linear Algebra.

$X$ is an ($m$ * $n$ feature matrix) and $y$ is an($m$* 1 column vector)
Where:

* $m$ is the number of observations or rows in the data set
* $n$ is the number of attributes or variables selected for the prediction
* $X$ is the m * n feature matrix of independent variables
* $y$ is the target or dependent variable

In Multiple Linear Regression, we try to predict a continuous dependent variable, using two or more features or independent variables.
In this case, we want to predict **CO2_EMISSIONS**, using two or more features from the data set. Features could be _Engine_Size, Cylinders, Make, Model_, e.t.c.
So to define our feature matrix $X$, we need to select ideal features from the data set that are correlated with CO2_EMISSIONS.
