# Reading Notes 13 - Linear Regressions #

### Linear Regression ###

Linear regression is a useful technique for gaining deeper insight into how several attributes in a dataset are related. It is also useful in making predictions based on previous knowledge of variable relationships. A high level overview is that we're trying to plot a linear function that is a good theoretical estimate to of the data's dependent variable to the independent variable for each of the observations.

### Sum of Squared Residuals ###

One metric for quantifying the "accuracy" of a linear regression function is the Sum of Squared Residuals. Residuals are the difference of each observations y output for a certain value of x, and the functions theoretical y output for a certain value of x. The reason these values are squared and summed is so that we can equally account for values that are above AND below the estimated response for a given value of X. The Sum of Squared Residuals function can be written as follows:  for each i in the data set. 

This is an extremely interesting topic and I can't wait to learn how to implement these linear regressions in Python with scikit-learn 