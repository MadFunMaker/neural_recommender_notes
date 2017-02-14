## [Restricted Boltzmann Machines for Collaborative Filtering](https://www.cs.toronto.edu/~rsalakhu/papers/rbmcf.pdf)

#### Problem
- That of Collaborative filtering (CF)

#### Why is this important and difficult?
- Most of the exising approaches to CF can't handle very large dataset. (What is the exact size of this untreatable large dataset?)

#### Solution
- RBM for one user, which has few connections if the user rated only a few movies. If user a and user b rated the same item,
their RBMs share weights connected to the corresponding visible unit

#### Result
- The proposed conditional factored RBM shows slightly lower RMSE compared to SVD model.

### Thoughts
- The proposed RBM methods consist of 2 layers, not deep enough to capture hierarchical latent factors of users and items and more accurately modeling ratings. Then, is the deep generative model tractable with dimensionality reduction?
- Autoencoder model with pretrained RBM may work as well. (But, is it bettern than batch normalization?) 
