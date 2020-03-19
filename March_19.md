Ensemble models are an improvement on normal models that seek to reduce overfitting by taking the average of multiple models. In the case of decision trees a random forest model can be made to get a better model. This is done by bagging. First we can sample from the total training set with replacement. Then we choose random traits in order to create a decision tree from each subsample. Predictions by this model are made by taking the majority or average of the predictions of all the decision trees made. Using sklearn it is easy to get a model up and running.

```python
from sklearn.tree import RandomForestClassifier
rfc = RandomForestClassifier(n_estimators = 100, criterion = 'entropy')
cv_rfc.fit(X, y) # With X and y as training data
```

With this model you can acheive better predictions than with a single decision tree.
