# Flipkart Grid 5.0
# Problem Statement : Personalized Product Recommendations


# Team Name
686157-UH2363RM

# Team Members Details 
Kaushal Agrawal - Dr. BR Ambedkar National Institute of Technology, Jalandhar

# Objective
The objective of this project is to develop an algorithm or model that enhances user experience through a personalized product ranking system. The system should be capable of generating accurate and relevant product rankings for individual users based on their preferences, past interactions, product popularity, and user similarity.

# Key Tasks:

-Algorithm Design: Develop an algorithm or model that combines user preferences, interaction history, and popularity-based recommendations to create personalized rankings.

-User Profiles: Create representative user profiles with different preferences, behaviors, and demographics. These profiles will serve as the basis for generating personalized rankings.

-Product Categories: Define various product categories or types to diversify the recommendations. Each category can have its own popularity and user preferences.

-Interaction Simulation: Simulate user interactions with products, such as ratings, purchases, or views. Use these interactions to train and evaluate your personalized ranking system.

-Evaluation Metrics: Design appropriate evaluation metrics to measure the effectiveness of your ranking system. Metrics may include accuracy, precision, recall, and user engagement.

-Presentation of Results: Present the results of your solution in terms of personalized rankings. Compare and contrast the performance of your personalized ranking system with popularity-based recommendations.

## Dataset

I have used an amazon dataset on user ratings for electronic products. To avoid biases,  each product and user is assigned a unique identifier instead of using their name or any other potentially biased information.

* You can find the [dataset](https://www.kaggle.com/datasets/vibivij/amazon-electronics-rating-datasetrecommendation/download?datasetVersionNumber=1) here 



## My Approach :

To provide product suggestions, the strategy investigates both popularity-based and collaborative filtering techniques. While popularity-based recommendations are based on the overall popularity of the product, collaborative filtering uses user-item interactions to generate personalised recommendations. The executive summary highlights the significance of personalised suggestions for improving user engagement and experience.

1. **Data Loading and Preprocessing**:
   - Load the dataset and perform initial data preprocessing.
   - Filter out unnecessary columns and a subset of data.
   - Remove users with too few ratings.

2. **Popularity-Based Recommender**:
   - Group products by count of user ratings to determine popularity.
   - Generate a ranking based on rating counts.
   - Select top-ranked products as popularity-based recommendations.
   - Build a function to offer these recommendations.

3. **Collaborative Filtering using KNN**:
   - Transform data into the Surprise `Dataset` format.
   - Split the data into training and testing sets.
   - Apply KNNWithMeans collaborative filtering with specified similarity measure.
   - Train the model on the training data.
   - Predict ratings on the test set.
   - Define a function to extract top-N recommendations from predictions.

4. **Collaborative Filtering using SVD**:
   - Convert data into the Surprise `Dataset` format.
   - Split the data into training and testing sets.
   - Utilize the SVD algorithm for collaborative filtering.
   - Train the algorithm on the training data.
   - Generate predictions for the test set.
   - Create a function to provide top-N recommendations using predictions.

5. **Manual SVD (Optional)**:
   - Implement Singular Value Decomposition on the user-item ratings matrix.
   - Predict ratings using the decomposed matrices.
   - Build a function to suggest items based on predicted ratings.

6. **Evaluation and Comparison**:
   - Compute Root Mean Squared Error (RMSE) for both collaborative filtering methods.
   - Compare RMSE values to assess model performance.

7. **Recommendation Generation and Comparison**:
   - Generate personalized recommendations using collaborative filtering methods.
   - Compare these recommendations with popularity-based ones.
   - Highlight the personalized nature of collaborative filtering.

8. **Summary of Findings**:
   - Summarize results from different recommendation strategies.
   - Emphasize that model-based collaborative filtering offers personalized suggestions.
   - Contrast this with non-personalized popularity-based recommendations.

