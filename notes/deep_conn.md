## [Joint Deep Modeling of Users and Items Using Reviews for Recommendation](http://dl.acm.org/citation.cfm?id=3018665)

#### Problem
- Given ratings and reviews, minimize MSE of ratings.

#### Why is this important and difficult?
- This is why recommender system with explicit ratings is important.

#### Solution
- Two parallel neural networks coupled in the last layer. One is for user review and the other is for item review. It interacts with each other in the last layer. The first layer of two parallel neural networks is look-up layer, which use pre-trained word embeddings(Word2Vec). The next layers are the common layers used in CNN based models to discover multiple levels of features for users and items, including convolution layer, max pooling layer, and fully connected layer. Also, a top layer is added on the top of the two networks to let the hidden latent factors of user and item interact with each other. This layer calculates an 426 objective function that measures the rating prediction error using the latent factors produced by two parallel neural networks.

#### Result
- Datasets : YELP (reviews & ratings), Amazon, Beer
- Evaluation scheme : MSE (Mean Square Error) - Why? The related works use this
- Comparing methods : MF, PMF, LDA, CTR, HFT, CDL
- As # of training reviews increases, it gains more MSE reductions.

### Thoughts
- It doesn't consider implicit feedback, can I extend it?
