# MLProject
Optimization of KNN and Linear regression algorithms


KNN Introduction:

KNN or K-nearest neighbours is a supervised algorithm used for classification and regression by considering k nearest training data to a test data. In this implementation, KNN is used for classification by counting the majority occurring classes in k nearest training examples.
The first dataset used is IRIS dataset with the objective to classify the dataset into 3 classes - 'Iris-setosa' 'Iris-versicolor', and 'Iris-virginica'. The second dataset used is Breast cancer dataset with 30 features.

Improvement/Extension:
In some cases, the data are widely spread in feature space.After selecting the k-nearest neighbor, the basic KNN works by calculating the mode of classes in nearest neighbor data set for each test data. The limitation with this approach is when data points are widely spread in feature space, the neighbour selection is not efficient. There can be cases where test data is classified wrongly in a class that occurs more often in k nearest neighbor set while it lies closer to a less popular class in reality.
To solve this, we can classify using inverse distance weighted voting, where the training data closest to test data contributes more in classification.

Implementation:
In this implementation, after selecting k nearest neighbors, following steps were taken:
1. Computed the inverse of each distance
2. Found the sum of the inverses,
3. Divided each inverse by the sum
Vote is calculated by taking out sum of weights associated with each class. The predicted class for test data is the one with the highest vote.



Linear Regression Introduction:

Linear regression, a supervised machine learning algorithm,which assumes a linear relationship between the output and input variables. The output can be obtained from a linear combination of input variables and their weights.
In this implementation the sklearn-Boston housing database, and sklearn Diabetes Dataset have been used to study the performance of linear regression and its extension.

Improvement:
While the Linear Regression works well for small datasets but for large ones, not all input variables might be significant to predict the output. LASSO (Least Absolute Shrinkage and Selection Operator) is an extension of the Linear Regression algorithm which penalizes large weights by adding their absolute value of magnitude to the cost function. After certain iterations, the weights shrinks towards zero, thus discarding irrelevant features. This is useful in case of high dimensional dataset where some features do not contribute in classification. Weights are updated using coordinate descent algorithm where optimization is done for a single coordinate at a time.
The objective in Lasso regularization is to minimize the below cost function: E​ = E​ (w) + alpha ||w||
lasso​ in​
