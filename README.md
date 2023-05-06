# Clustering Class
Clustering is a Python class that implements flat clustering algorithms from scratch. The code for the algorithms is inside the src folder, while the Clustering class contains the call for the algorithm and other plot methods (plot the output, plot the history of the iteration, generate a gif of the iterations).

The implemented clustering algorithms are:

  - K-means
  - K-means++
  - K-medoids
  - K-medoids++
  - C-means
 
The Clustering class has the following attributes:

  - k: the number of clusters to form.
  - z: the final assignment of each point to a cluster.
  - loss: the total loss after clustering, defined as the sum of the squared distances between each point and its assigned cluster center.
  - C: the final cluster centers.
  - n_iterations: the number of iterations required to converge.
  - C_history: a record of the cluster centers at each iteration.
  - z_history: a record of the assignment of each point to a cluster at each iteration.
  - algorithm_variant: the variant of the algorithm to use.
  - TIME: the time required to fit (s).
  - U: the matrix of "probabilities".
  
  
## Installation

Clone the repository:
`git clone https://github.com/your_username/clustering.git`

## Usage

Here's an example of how to use the Clustering class:

```
import numpy as np
from sklearn.datasets import make_blobs
from Clustering import Clustering

# Generate random data
X, _ = make_blobs(n_samples=1000, centers=5, random_state=42)

# Create an instance of Clustering class
clustering = Clustering(k=5)

# Fit the data
clustering.fit(X)

# Print running time to fit
clustering.time()
```
`something `
```

# Plot the scree test
clustering.scree_test(X, k_max=15)
```
![Clustering Plot](images/clustering_plot.png "Clustering Plot")

![](kmeans.gif)
