## [Multiverse Recommendation: N-dimensional Tensor Factorization for Context-aware Collaborative Filtering](https://xamat.github.io//pubs/karatzoglu-recsys-2010.pdf)

#### Problem
- Collabortaive filtering based on tensor factorization, HOSVD, which allows a flexible and generic integration of contextual information by modeling the data as a User-Item-Context N-dimensional tensor instead of the traditional 2D User-Item matrix. 

#### Why is this important and difficult?
- Matrix factorization has the limitation that it can't embrace contextual information other than user and item information.
- Contextual information is useful in recommendation. For example, when recommending music item for users, not only song, but also other contextual information such as artist, time, and gender influence on the success of recommendation.

#### Solution
- HOSVD with simple regularization term based on the l2 norm of user, item, context factors.

#### Result
- It shows better MAE on Yahoo! Webscope movie, Adom, and Food datasets compared to non-context-aware regular matrix factorization and context-aware methods.

### Thoughts
- For me, this is the first official paper applying tensor facotorization on recommender system. Even though the metric (MAE) is old-fashioned, it reveals the possibility of tensor factorization on recommender systems.
- Inspired by this work, I think we can do more than that. Actually, the type of contextual information critical to the success of recommendation differs by the item. For example, some songs may be especially loved by women while other songs are especially loved at night. Thus, we can consider the learning method that selectively choose the type of contextual information depending on the item.
