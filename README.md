# E-commerce-Product-recommendation-System
I created an Ecommerce Product Recommendation System to provide personalized product suggestions based on user browsing and purchase history. This system uses collaborative filtering and content-based filtering algorithms to analyze user behavior and generate recommendations, improving the shopping experience and boosting sales for e-commerce businesses.

### Dataset
I used an Amazon dataset of user ratings for electronic products, assigning unique identifiers to avoid biases. The dataset is available [here](https://www.kaggle.com/datasets/vibivij/amazon-electronics-rating-datasetrecommendation/download?datasetVersionNumber=1).

### Approach

1. **Rank-Based Product Recommendation**
   - **Objective**: Recommend the most popular products to new customers and solve the Cold Start Problem.
   - **Method**: Calculate average ratings and total number of ratings for each product. Recommend top products with specified minimum interactions.

2. **Similarity-Based Collaborative Filtering**
   - **Objective**: Provide personalized recommendations based on similar users' interactions.
   - **Method**: Convert user IDs to integers, find similar users using cosine similarity, and recommend products that similar users interacted with but the actual user has not.

3. **Model-Based Collaborative Filtering**
   - **Objective**: Provide personalized recommendations using past behavior and preferences while addressing sparsity and scalability.
   - **Method**: Use SVD on a CSR matrix of product ratings to reduce dimensionality, predict ratings, and recommend top products based on predicted ratings.
   - **Evaluation**: Calculate RMSE to evaluate model performance by comparing actual and predicted ratings.
