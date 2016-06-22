LDA 

Description: Classify Y as class K if the probability of being class K is highest, given X, among the other classes.
LDA trys to estimate this probabilty by modeling the distribution of the predictors X separately in each of the response classes, 
and then use Bayes' theorem to flip these around.

Assumptions:
- X is normal in each of the classes
- X in different class shares a common covariance matrix

Advantage:
- Can be easily applied to cases where there are more than two response classes
- Good when X is approximately normal in each of the classes

Disadvantages:
- LDA is trying to approximate the bayes classifer, which is trying to find the lowest TOTAL error rate, 
irrespective of which class the error come from. For example, a credit card company might particularly want to avoid classifying
an individual who will default(this can be resolved by setting a higher threshold)
- Assumes X is normal in each of the classes, this can be fundamental wrong
- Assumes X in different class shares a common covariance matrix
- Will need to estimate covariance matrix, class specific mean, and prior probabilify
- The estimation of covariance matrix involves estimation P(P+1)/2 parameters


QDA

Description: Similar to LDA, except that we model class specific covariance matrix

Assumptions:
- Observations within each class follow multivariate Gaussian distribution
- Each class has its own covariance matrix

Advantages:
- QDA is recommened over LDA when the training set is vary large(Variance brought by flexibility wil not be a issue), when  the assumption of a shared covariance matrix is badly off(Bias will be high for LDA)


Disadvanges:
- Can be a lot of parameters to estimate, k*P(P+1)/2, for covariance matrixes
- Much flexible than LDA(with its quadratic boundries), but introduces more variance
- 
