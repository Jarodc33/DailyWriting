K-Nearest Neighbors is a machine learning method that uses distances from points in order to make predictions. This is acheived by calculating the distance between a novel point and all the training points. Then the algorithm takes the K closest of those points and uses them to make a predicted value for the novel point. This predicted value is made by taking the majority or the average of the K closest points. The algorithm can be tuned by changing things such as the K values (number of neighbors used for prediction) or the type of distance used (minkowski/euclidean/manhattan). Some problems with the algorithm is that it has a very long run time for big data sets as each new prediction must sort the training points by distance which starts to get very taxing when there are hundreds of thousands of points. 
```python
  predictions = np.zeros(X_test.shape[0])
        
  for i, point in enumerate(X_test):
    distances = self._get_distances(point)
    k_nearest = self._get_k_nearest(distances, k)
    prediction = self._get_predicted_value(k_nearest)
    predictions[i] = prediction
```

This code snipet shows that for each test point we need to find the distance of all the points in the training data then we need to find the k closest. This takes an exponential amount of time as the amount of data increases.
