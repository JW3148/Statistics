Resampling methods
- repeatedly draw samples from a training set 
- refit a model of interest on each sample in order to gain additional information about the fitted model
- such an approach may allow us to obtain info that would not be available from fitting the model once using the training set

Cross-Validation
- a class of methods that estimate the test error rate by holding out a subset of the observations and then applying the statistical learning
method to those held out observations

The Validation Set Approach
- randomly dividing the data into a training set and test set
- the test error rate/MSE varies depending on how you divide the data
- fitting model on subset of data, and therefore potentially overesitimate the test error for the model fit on the entire set

Leave-One-Out Cross-Validation(LOOCV)
- instead of creating two subsets of comparable size, a single observation is used for the test, and the remaining observations are used for training.
- Repeat this for all observations, then average the test error.
- good in that it return fixed test rate, there is not randomness, fiting model with most of the data
- expensive to implement, especially for complicated model, have to fit the model n times
- time consuming when n is large and the model is slow to fit

k-Fold Cross-Validation
- Randomly dividing the set of observation into k groups, or k folds
- leave one fold as test set, remaining as training set
- do this for each fold, i.e. fit the model k times, then average out the test error
- less computation cost, will need to only fit k times
- the k models are less correlated with each other, then the models in LOOCV(since they fit on almost the same set of data)
if the models are less correlated, it means the estimates are less correlated. Since the mean of many highly correlated quantities has higher variance than does the mean of many quantities that are less correlated, the test error of LOOCV has higher variance than that of k-Fold.
