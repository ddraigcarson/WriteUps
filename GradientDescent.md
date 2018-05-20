# Gradient Descent

Gradient descent is a first order iterative optimization algorithm used for finding the minimum of a function. 
First order in that it uses the first differential of a function, iterative as in it requires multiple steps to work.
We look for a minimum of a function by finding the first order differential which tells us the gradient at a point.
Starting from a random point, we then take steps along the negative gradient (the step size is the learning rate and is a hyper-parameter) with the assumtion that after many small steps along the negative gradient we will eventually end up to the minimum of the function.

In ML, GD is commonly used to find the minimum of an error function.

A gotcha can occur when a function has multiple valleys, once GD hits the minimum of one valley it has no reason to look for other valleys even if they may be lower. 

There are three variations of gradient descent.
1 Mini batch GD
2 Stochastic GD
3 Batch GD

###### Mini batch
Instead of using the full data set we use a small sample. Good choice for very large data sets.

###### Stochastic GD
We use only a single data point, during each iteration we shuffle the training set order.
