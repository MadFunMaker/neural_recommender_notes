## [Collaborative Deep Learning for Recommender Systems](http://dl.acm.org/citation.cfm?id=2783273)

#### Problem
- The sparsity problems of user ratings and item auxilary information in recommender system.

#### Why is this important and difficult?
- The sparsity problems are really common in the real world datasets, e.g. It always occurs for new users and items.
- The existing solutions are not tightly coupled methods (the extracted features from auxilary information interact with the learning from the ratings) 

#### Solution
- Hierarchical bayesian model called Collaborative Deep Learning (CDL), which tightly couples deep representation learning for the content information and collaborative filtering for the ratings (feedback) matrix, allowing two-way interaction between the two. Although they present CDL as using SDAE for its feature learning component, CDL is actually a more general framework which can also admit other deep learning models such as deep Boltzmann machines, recurrent neural networks, and convolutional neural networks.
**(I don't understand the details of this algorithm yet.)**

#### Result
- Datasets : citeulike-a, citeulike-t, and Netflix
- Evaluation scheme : recall@M, mAP
- Comparing methods : CMF, SVDFeature, DeepMusic, CTR

### Thoughts
- Why do they say that "Although deep learning models are more appealing than shallow models in that the features can be learned automatically (e.g., effective feature representation is learned from text content), they are inferior to shallow models such as CF in capturing and learning the similarity and implicit relationship between items."? Is there any clue?
