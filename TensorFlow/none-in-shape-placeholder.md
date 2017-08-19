# Significance of `None` in placeholder shape

> `None` indicates that the first dimension, corresponding to the batch size, can be of any size.

For example, in MNIST dataset, We assign a shape of [None, 784] which indicates that there can be any number of batch sizes of images of single flattened 28x28 pixels (dimensionality). 

### References

* [StackOverflow](https://stackoverflow.com/a/39305493/4411757)
* [Placeholder](https://www.tensorflow.org/api_docs/python/tf/placeholder)