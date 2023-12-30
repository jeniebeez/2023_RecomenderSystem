# 2023_RecomenderSystem
This is the project of school, I use ml-100k data to implement collaborative filtering and content based filtering.The main library that i use is scikit-surprise. (https://surpriselib.com/)

## Data
Link: https://grouplens.org/datasets/movielens/100k/

## Collaborative Filtering
I use SVD as algorithm to fullfil the sparse matrix of ratings and predictions.

### SVD
1. When SVD in Gridsearch Cross Validation, SVD predicts the empty rating with a range of learning rate, regulation rate and epochs. When it running, the predicted rating will follows the epochs number as the iteration time of SGD. (https://surprise.readthedocs.io/en/stable/matrix_factorization.html#surprise.prediction_algorithms.matrix_factorization.SVD)

2.  With Cross Validation, it will choose one range of data as TEST and jump to next of those each iteration. Gridsearch will follows the key value ["rmse", "mae"] to find the best parameters.

3. After use train_test_split to separate the TRAIN and TEST dataset, SVD do predictions from test dataset and do comparation with it. We get the NDCG value after that.

## Content Based Filtering
Cosine Similarty is the main algorithm, it also do predictions to sparse matrix of ratings and TEST dataset.

### Cosine Similarity
1. Set up Cosine Sim as algo base. Finish the sparse matrix predictions with settings of k-nearest =10.
   
2. Calculate the RMSE value with Cross Validation of 5, we take the Mean value of it to do comparison of Collaborative Filtering.

3. Do prediction with TEST dataset and gets the NDCG score.

## Summary
It seems like Collaborative filtering is better then Content Based filtering when depends on RMSE and NDCG score.
