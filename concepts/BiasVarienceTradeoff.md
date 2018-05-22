# Bias Varience Tradeoff

This is the problem of simultaneously minimizing two sources of error that prevent supervised learning algorithms from generalising beyond their training set.

1. Bias is an error caused by wrong assumptions in the learning algorithm, high bias causes relevant relationships between features and target outputs to be missed. Also known as underfitting. It is the difference between the expected (or average) prediction of our model and the correct value which we are trying to predict. With high Bias the models predictions are far off the correct values.
2. Varience is an error caused from sensitivity to small fluctuations in the training set, high varience can cause the algorithm to model random noise in the training data rather than the intended outputs. The algorithm is highly tied to the training data set and a new training data set will cause the resulting model to be very different any other. Also know as overfitting. 

The trade off is that we would like some middle ground, to be able to capture relationships in the data while not being tied completely to the training data, generalised enough to predict new data.

The different combinations of Bias vs Varience are:

![error function](../images/BiasVarienceTradeoff.png)

[Source](http://scott.fortmann-roe.com/docs/BiasVariance.html)

### Managing BvV

Firstly it is important not to minimise bias at the expense of varience. That may fix the model for one dataset but will not create a strong generalised model. There are strategies for managing BvV such as

##### Bagging and Resampling

Also known as Bootstrap Aggregating, (a special case of model averaging), given a training set D of size n, we break it into m number of new training sets, Di, by sampling from D uniformly and with replacement(1) (The same observations may appear multiple times in the sample). We then train our model m times using the new training sets and combining the average output. This has been seen to improve the stability of unstable procedures like NN and classification or regression trees, but causes issues in stable methods such as kNN

### Useful links
1. https://en.wikipedia.org/wiki/Sampling_(statistics)#Replacement_of_selected_units
2. http://scott.fortmann-roe.com/docs/BiasVariance.html
