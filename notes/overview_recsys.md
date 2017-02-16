## Overview of Recommender System (RS)

#### Category
- Collaborative Filtering (CF)
  - Memory-based CF (= neighborhood method)
    - Item-oriented approach
    - User-oriented approach
  - Model-based CF (= latent factor model)
- Content-based recommender system
- Miscellaneous recommender systems
  - Demographic information about user
  - Applying the utility function to the items and determine its rank for user.
  - Knowledge-based recommendation
  - Graph-based recommendation
  - Co-occurrence item recommendation
  
**Hybrid methods include more than one of the above methods.**

#### Method Description
- Memory-based CF
  - Think of it simply as a recommendation made based on similarity values. (Pearson correlation, Cosine similarity, etc)
- Model-based CF
  - Recommendation based on machine learning or data mining models. (e.g. Naive Bayesian, Clustering, MF, PMF - the best single model so far)
  - Learning algorithm : Gradient Descent based method (GD), Alternaing least square based method (ALS)
    - ALS is preferable in two cases, that are 1) when parallelization is needed and 2) when systems are centered on implicit data.
    - 1) Parallelization: In ALS, the system computes each qi independently of the other item factors and computes each pu independently of the other user factors.
    - 2) the training set cannot be considered sparse, looping over each single training case—as gradient descent does—would not be practical.
- Content-based recommender system
  - Use user profiles, item information, reviews (Collaborative topic modeling)

#### Matrix Factorization Techniques for RS
