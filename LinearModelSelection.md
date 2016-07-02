Linear Model Selection
-

1) Subset Selection
- Find the best model with k variables, for k=1,...,p, say best model with 1 variable, best model with 2 variables...you will end up with
p diffrenect models, then find the best among these p models, based on testing error, which can be estimated directely or indirectly
- How to find the best model given number of variables? say what's the best model with 5 variables. 
- Three way to find out: Best Subset Selection, Forward Stepwise Selection, Backward Stepwise Selection
- Best Subset Selection: at each level, try all possible combination. Together, at all level, need to fit 2^p times, computational expensive
- Forward Stepwise Selection: start with no variable. add one variable each step to go to the next level. add which one? choose the model with best RSS or R-square
- Backward Stepwise Selection: start with all variables, drop one  each step to go the next level. drop which one, the model with the best RSS or R-square

Cp, AIC, BIC, and adjusted R-square in Least Square setting
- pays a price for the inclusion of additional variables
- Adjusting the traning error to estimate the testing error, or to accomodate the extra variance brought in by extra flexibiity
- Cp: Cp=(RSS+2*d*sigma^2)/n (Mellow's Cp defined as RSS/sigma^2 + 2d-n), which d is the number of predictors. the estimator considers the numbers of predictors. note that sigma^2 is the residual mean square after fiting the complete set of variables
- AIC(Akaike information criterion): (RSS+2*d*sigma^2)/(n*sigma^2) [will have same effect as Cp when used with least square]
- BIC(Bayesian information criterion): (RSS+log(n)*d*sigma^2)/n. [Large panalty for for model with nany variables, the multiplier for for d is log(n)*sigma^2, compared to 2 in Cp]
- Adjusted R-square: 1- [RSS/(n-d-1)]/[TSS/(n-1)](without adjust it is defined as 1-RSS/TSS)



2) Shrinkage(also known as regularization)

3) Dimension Reduction
