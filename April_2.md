Priciple component analysis is a powerful data manipulation tool that can reduce the dimension of data. When data has a lot of features it is harder to finds points that are close together. This makes sense because with more dimensions there are more directions the points can move away from eachother. This is where principle component analysis comes in, It allows for the reduction of a points dimension. Essentially it transforms the origininal vector space into a new one. Though there can be some complicated math behind it, principle component analysis is easy to implement with scikit-learn. 
```python 
from sklearn.decomposition import PCA

pca = PCA()
transformed = pca.fit_transform(X)
```
