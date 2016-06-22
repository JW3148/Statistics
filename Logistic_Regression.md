Logistic Regression

Description: Linear Regression models the probabily of Y belong to a particular class given the an observation.
It applys logistic function to transfrom a linear combination of X to restrict the output between 0 and 1

Logistic function f(x) = exp(x)/(1+exp(x))

Assumptions:
- assumes a linear relationship between the log odd ratio of being a class and the predictors, as always, the model formulation itself is a assumption

Advantages:
- vary good interpretability, can directly present the probabity of a class given X
- resistent to over-fitting, less flexible model
- 




Estimating the coefficients:
- maximum likehood is prefered, since it has better statistics properites
- by the model fomulation, giving a coeffiecent, the probability of Y being class 1 can be calculated; multiply each point will give the
joined probability, whoever maximize this will be the MLE estimator

Extend to Multiple Classes
- Consider a baseline class
- Assumes the presense of other classes will not affect the preference between two classes
