# 2023_RecomenderSystem
This is the project of school, I use ml-100k data to implement collaborative filtering and content based filtering.The main library that i use is scikit-surprise. (https://surpriselib.com/)

## Data
Link: https://grouplens.org/datasets/movielens/100k/

## Collaborative Filtering
I use SVD as algorithm to fullfil the sparse matrix of rating and prediction.

### SVD
1. When SVD in Gridsearch Cross Validation, SVD predicts the empty rating with a range of learning rate, regulation rate and epochs. When it running, the predicted rating will follows the epochs number as the iteration time of SGD. (https://surprise.readthedocs.io/en/stable/matrix_factorization.html#surprise.prediction_algorithms.matrix_factorization.SVD)

2.  
