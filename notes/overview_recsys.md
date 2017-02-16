## Overview of Recommender System (RS)

#### Category
- Collaborative Filtering (CF)
  - Memory-based CF (can think of it as neighborhood method)
    - Item-oriented approach
    - User-oriented approach
  - Model-based CF (can think of it as latent factor model)
- Content-based methods
- Miscellaneous recommender systems
  - Demographic information about user
  - Applying the utility function to the items and determine its rank for user.
  - Knowledge-based recommendation
  - Graph-based recommendation
  - Co-occurrence item recommendation
  
**Hybrid methods include more than one of the above methods.**

#### Collaborative Filtering (CF)
- Use user's usage data (either explicit rating or implicit data)
- Advantage
  - Domain free
  - Proved to show better performance than content-based model
- Disadvantage
  - Cold start problem (when there is no usage data, either rating or implicit data)
- Memory-based CF
  - Think of it simply as a recommendation made based on similarity values. (Pearson correlation, Cosine similarity, etc)
- Model-based CF
  - Recommendation based on machine learning or data mining models. (e.g. Naive Bayesian, Clustering, MF, PMF)
  - Latent facotr models (MF) are the best single model so far.
  - Learning algorithm : Gradient Descent based method (GD), Alternaing least square based method (ALS)
    - ALS is preferable in two cases, that are 1) when parallelization is needed and 2) when systems are centered on implicit data.
    - 1) Parallelization: In ALS, the system computes each qi independently of the other item factors and computes each pu independently of the other user factors.
    - 2) Implicit data: the training set cannot be considered sparse, looping over each single training case—as gradient descent does—would not be practical.
  - Adding biases
    - Much of the observed variation in rating values is due to effects associated with either users or items, known as biases or intercepts, independent of any interactions. 
    - $\hat{r_{ui}} = µ + b_i + b_u + q^{T}_{i}p_u$
  - Additional Input sources
    - We need it due to few ratings by user (or cold start problem)
    - Use implicit feedback (For user-item interaction)
    - Use user information such as demographics (For user-associated attribute)
    - Integrate above two sources to represent new user latent factor $p'_u$
    
#### Content-based methods
- Use user profiles, item information, reviews (Collaborative topic modeling)
- Advantage
  - Deal with cold start problem
- Disadvantage
  - Not domain free
  - Proved to show worse performance than CF
