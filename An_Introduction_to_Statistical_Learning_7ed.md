# Chapter 2: Statistical Learning
## What Is Statistical Learning?
The inputs is predictors, independent variables, features, or sometimes just variables, denoted as X.

The output is response or dependent variable, denoted as Y.

For statsitical learning we want to dervice relationship between X & Y.
We can assume it is of below form

<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?Y%20%3D%20f%28X%29%20&plus;%20%5Cvarepsilon">
</div>

*f* represents the systematic information that X provides about Y
    
*ε* is a random error term, which is independent of X and has mean zero

## Why Estimate f?
### 1. Prediction

We have input X and output Y cannot be easily obtained, so we predict output Y.
<div align="center">
  <img src="https://latex.codecogs.com/svg.latex?%5Chat%7BY%7D%20%3D%20%5Chat%7Bf%7D%28X%29%2C">
</div>
Where,

<img align="left" src="https://latex.codecogs.com/svg.latex?%5Chat%7Bf%7D"> represents our estimate for f,
one is not typically concerned with the exact form of it, provided that it yields accurate predictions for Y.

<img align="left" src="https://latex.codecogs.com/svg.latex?%5Chat%7BY%7D"> represents the resulting prediction for Y

The accuracy of <img src="https://latex.codecogs.com/svg.latex?%5Chat%7BY%7D"> as a prediction for Y depends on two quantities,
which we will call the **reducible error** and the **irreducible error**.

* #### Reducible Error 

  <img src="https://latex.codecogs.com/svg.latex?%5Chat%7Bf%7D"> will not be a perfect estimate for f, and this inaccuracy will introduce some error.
This error is reducible because we can potentially improve the accuracy of <img src="https://latex.codecogs.com/svg.latex?%5Chat%7Bf%7D"> by using the most appropriate statistical learning technique to estimate f.

* #### Irreducible Error 

  However, even if it were possible to form a perfect estimate for
f, so that our estimated response took the form <img src="https://latex.codecogs.com/svg.latex?%5Chat%7BY%7D%20%3D%20f%28X%29">, our prediction
would still have some error in it! This is because Y is also a function of
ε, which, by definition, cannot be predicted using X. Therefore, variability
associated with ε also affects the accuracy of our predictions. This is known
as the irreducible error, because no matter how well we estimate f, we
cannot reduce the error introduced by ε.

### 2. Inference

In this situation we wish to estimate f, but our goal is not necessarily to make predictions for Y. We instead want to understand
the relationship between X and Y. Now <img src="https://latex.codecogs.com/svg.latex?%5Chat%7Bf%7D"> 
cannot be treated as a black box, because we need to know its exact form.
In this setting, one may be interested in answering the following questions:
  * Which predictors are associated with the response?
  * What is the relationship between the response and each predictor?
  * Can the relationship between Y and each predictor be adequately summarized using a linear equation, or is the relationship more complicated? 

### Difference between inference and prediction problem:
* *how much extra will a house be worth if it has a view of the river?* This is an inference problem.
* *is this house under- or over-valued?* This is a prediction problem.
