# Collaborative Filtering
Uses similarities between users and items to provide recommendations. This allows for serendipitous recommendations (i.e.  the model can recommend an item to user A based on the interests of a similar user B). The embeddigns can be learned automatically without relying on hand-engineered features.



- Suffers from cold-start problem


## User-Based vs Item-Based Collaborative Filtering
- **User-based** - for a user `U` with a set of similar users determined based on rating vectors the rating for item `I` which hasn't been rated is found by picking out N users from the similarity list who have rated the item `I` and calculating the rating based on these N ratings.
- **Item-based** - for an item `I` with a set of simlar items determined based on rating vectors, the rating for user `U` who hasn't rated it is found by picking out N items from the similarity list that have been rated by `U` and calculating the rating based on these N Ratings.


### Resources:
- [google-developer-guide](https://developers.google.com/machine-learning/recommendation/collaborative/basics)
- [kaggle-deep-dive](https://www.kaggle.com/code/jhoward/collaborative-filtering-deep-dive)
- [example-python](https://realpython.com/build-recommendation-engine-collaborative-filtering/)
- [matrix-factorization-from-scratch](https://towardsdatascience.com/recommender-systems-matrix-factorization-using-pytorch-bd52f46aa199)