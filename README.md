# README : itc6001
# Basic Recommendation System

### Project Overview
- **Objective**: Build a simple recommendation system.
- **Dataset**: MovieLens 100k
- **Methodology**:
  - Recommend items based on their number of rating or based on `random.sample`
  - Separate original dataset to train and test set 
  - Evaluate the system using MAE, RMSE, Precision, Recall, and F1 Score.

### Steps

#### 1. 2 versions of recommendations
- Compute the number of ratings for all items and find top N
- Compute random recommendations using `random.sample`

#### 2. Top-N Recommendations
- Recommend the top N items for each user for the two above versions
- Store results for later evaluation

#### 3. Ratings for users in test set
- For each user in the test set, compute the actual ratings (test set) and the predicted ratings (train set)

### Evaluation Metrics

#### a. Error Metrics
- **Mean Absolute Error (MAE)**: Average absolute difference between actual and predicted ratings.
- **Root Mean Squared Error (RMSE)**: Square root of the average squared differences between actual and predicted ratings.

#### b. Precision, Recall, and F1 Score
- Rating threshold (3.5) to sort items as relevant or not.
- Calculate:
  - **Precision**: Proportion of all positive classifications that are actually positive.
  - **Recall**: Proportion of correct identification of all of the actual positive points in a data set.
  - **F1 Score**: Harmonic mean of precision and recall.


# Collaborative filtering recommendation system
### Project Overview
- **Objective**: Build and evaluate a recommendation system using collaborative filtering (CF).
- **Dataset**: MovieLens 100k
- **Methodology**:
  - Compute cosine similarity to identify similar users.
  - Predict ratings based on similar users' ratings.
  - Evaluate performance using MAE, RMSE, Precision, Recall, and F1 Score.

### Steps

### 1. Compute Cosine Similarity
- Use the `findKSimilar` function to calculate cosine similarity between users.
- Identify the top `k` most similar users for each user.

### 2. Predict Ratings
- `predict` function to compute ratings for items based on ratings from similar users.
- Only predict ratings for hidden values.

### 3. Hide Random Data
- Randomly hide 20% of data using the `hide_random_data` function.
- With this dataset. test the predictions.

### 4. Generate Recommendations
- For each user, recommend the top 5 items with the highest predicted ratings.
- Store recommendations in a df for easy viewing.

  # Optimization
### Project Overview
- **Objective**: Evaluate top-rated movies for specific user demographic data (gender)
- **Dataset**: MovieLens 100k
- **Methodology**:
  - Make recommendations for women and men separately
  - Compute MAE, RMSE, Precision, Recall and F1 for each gender


