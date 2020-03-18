Trees are a very common structure in programming that is used in a variety of ways. They can be used for sorting, searching, decision trees and many others. In the case of data science they can be used as decision trees in both regression and classification models. In order to create a decision tree a metric for classification is used, this could be entropy, gini impurity or other metrics. The tree then splits at each node along whatever minamizes the metric. Once the tree is built, new points are classified by traversing the decision tree and once a leaf node is reached the majority or mean is used to predict the value of the new point. ScikitLearn makes it very easy to make these structures by using DecisionTreeClassifier.

```python
from sklearn.tree import DecisionTreeClassifier
ct = DecisionTreeClassifier(criterion='entropy') # using entropy
ct.fit(X_train, y_train) # X_train is the training data predictors and y_train is the target of the training data
```
