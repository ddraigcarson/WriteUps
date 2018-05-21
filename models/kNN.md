# kNN - k Nearest Neighbours

The long and short of this is that a data point is the same as the others around it.

kNN is one of the more simple predictive models used in regression and classification. It is a type of instance based learning in that it does not use the training data to create a generalised model, rather it relys on its training data to make predictions. It is very math light in that it only assumes:

- the data has some notion of distance,
- that points close to each other are similar.
 

Imagine the data below, Gen 1 is our training data and Gen 2 is our test data. The plot is the attack and defense of pokemon from generation 1 and 2 for the fire and grass types. Scraped from bulbapedia.

![error function](../images/kNN.png)

The simplest distance measurement is Euclidean distance:

![error function](../images/EuclideanDistance.gif)

Where x, y and z is the difference between our test point and all the training data points in the respective dimensions. Using this we get a list of distances where we can pick a number of them (k) that have the smallest values i.e. the nearest neighbours. We can then see the majority of the types of the k nearest neighbours and that is our prediction for our test point.

Using all points within our training data range, we can start to draw boundaries:

![error function](../images/kNN_Boundaries.png)

Higher values of k should reduce the effect of noise on the classification but generally make the boundaries less distinct. In two choice (or binary) systems, it is best to pick an odd k so that there is always a majority. 

There is a variation that adds a weighting to the nearest neighbours equal to one over the distance so that the closer the neighbour the more impact it has on the classification.

A potential downside is that at higher dimensions the points are further away from each other (because there are extra values in the Euclidean distance) which can cause the classification to be less accurate.
