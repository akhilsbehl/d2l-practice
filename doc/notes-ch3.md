# 3. Linear Neural Networks for Regression

## 3.1. Linear Regression

[3.1.1.4. Minibatch Stochastic Gradient Descent](https://d2l.ai/chapter_linear-regression/linear-regression.html#minibatch-stochastic-gradient-descent)

consider only a single example at a time and to take update steps based on one observation at a time. The resulting algorithm, stochastic gradient descent (SGD) can be an effective strategy (Bottou, 2010), even for large datasets. Unfortunately, SGD has drawbacks, both computational and statistical. One problem arises from the fact that processors are a lot faster multiplying and adding numbers than they are at moving data from main memory to processor cache. It is up to an order of magnitude more efficient to perform a matrix-vector multiplication than a corresponding number of vector-vector operations. This means that it can take a lot longer to process one sample at a time compared to a full batch. A second problem is that some of the layers, such as batch normalization (to be described in Section 8.5), only work well when we have access to more than one observation at a time.


