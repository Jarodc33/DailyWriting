There are two main strategies for a recomendation system. One is the content based strategy which uses similarity between different content to recomend new content. The second strategy is using a collaborative system that gives recomendations based on the similarity of the users. For these systems some similarity metric is used in order to relate points to each other. One simple metric is using cosine similarity to relate points. There are also many other ways for solving these recomendations systems such as alternating least squares for a collaborative system. Using cosine similarity is a quick way to get a crude recomendation system running and this can be done with a couple of line of code:
```python
import numpy as np
# Where the arr is a 2d matrix with rows as users and arr[0] is the user we want to recomend things to
numerators = np.array([arr[0].dot(arr[i]) for i in range(1, 4)])
denominators = np.array([np.sqrt(sum(arr[0]**2)) *\
                         np.sqrt(sum(arr[i]**2)) for i in range(1, 4)])

numerators / denominators
# The highest number corresponds to the most related item.
```
