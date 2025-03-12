# ASSIGNMENT: Building a Recommendation System | Item-Based Collaborative Filtering (KNN)

## Introduction
The **Pratilipi Recommendation System** is designed to suggest Pratilipi content to users based on their past reading behaviors. The system leverages **Item-Based Collaborative Filtering** using **K-Nearest Neighbors (KNN)** to recommend Pratilipis that are similar to those previously read by the user. This project aims to enhance content discovery and user engagement on the platform.

## About This Project
This is a **collaborative filtering-based** Pratilipi recommender system that suggests relevant Pratilipis based on user interest.

## Dataset
The dataset consists of user interactions with various Pratilipis, structured as a **user-item interaction matrix**.
- **Users:** Represent individuals engaging with Pratilipis.
- **Items:** Pratilipis (books/articles) available on the platform.
- **Interactions:** Recorded as implicit feedback (clicks, reads, etc.) or explicit feedback (ratings, likes).

![image](https://github.com/user-attachments/assets/e6d6a79e-8da2-418f-9017-f72ce580267c)

![image](https://github.com/user-attachments/assets/165bfb5a-4eac-4a77-adbe-353e242faad0)

## Model Used: **Item-Based Collaborative Filtering (KNN)**

### Why Collaborative Filtering?
Collaborative filtering is chosen because it effectively predicts user preferences based on their interaction history without requiring explicit content descriptions. It is particularly useful when:
- Content metadata is limited or unavailable.
- User interactions are rich and provide meaningful patterns.
- Recommendations should be based on user behavior rather than content attributes.

### Mathematical Justification
**Cosine Similarity** is used to measure the similarity between two Pratilipis:

![image](https://github.com/user-attachments/assets/10485a2f-d0c6-49c5-b67c-d617de40b6bd)


This ensures that recommendations are based on how similar the engagement patterns of two items are.

## How the Model Works
1. **Build a User-Item Matrix**: Convert interactions into a sparse matrix representation.
2. **Compute Similarities**: Calculate cosine similarity between items to determine which Pratilipis are most similar.
3. **Find Nearest Neighbors**: Identify the top-K most similar Pratilipis for each item.
4. **Generate Recommendations**: Suggest items that are highly similar to those previously engaged with by the user.

## Types of Recommendation Systems
### 1️⃣ Content-Based Filtering
- Uses item attributes (e.g., genre, author) to recommend similar Pratilipis.
- **Limitations**: Suffers from over-specialization, limiting diversity in recommendations.

### 2️⃣ Collaborative Filtering (Used in this Project)
- Uses user-item interactions to recommend content based on similarity patterns.
- **Advantages**:
  - Works well without requiring explicit content metadata.
  - Captures evolving user interests dynamically.
- **Challenges**:
  - Cold start problem for new users and items.
  - Computational complexity for large datasets.

### 3️⃣ Hybrid Recommendation Systems
- Combine both methods to improve recommendation quality.
- Used in modern large-scale recommender systems.

## Model Implementation Steps
1. **Load Data**: Preprocess user-item interactions.
2. **Define Similarity Metric**: Compute cosine similarity between items.
3. **Select Neighbors**: Identify the top-K most similar Pratilipis.
4. **Generate Recommendations**: Suggest items that match user interests.
5. **Evaluate Performance**: Measure Precision@K, Recall@K, and sparsity effects.

## Built With
- **scikit-learn** (Machine Learning & KNN algorithm)
- **pandas & numpy** (Data processing)
- **Google Colab** (For model training and evaluation)

## Data Analysis
### Exploratory Data Analysis (EDA)
- **User Behavior Analysis**: Understanding reading patterns.
- **Popular Categories**: Identifying frequently read genres.
- **Sparsity Analysis**: Checking how many users interact with each Pratilipi.
- **Interaction Distribution**: Analyzing how users engage with different types of content.

### Data Preparation
- **User-Item Matrix**: Converting interactions into a sparse matrix.
- **Handling Missing Data**: Strategies for cold-start users.
- **Feature Engineering**: Extracting relevant features for improved recommendation accuracy.

## Dependencies
```txt
pandas
numpy
scikit-learn
```

## Workflow
Recommendation systems are becoming increasingly important in today’s extremely busy world. People are always short on time with the myriad tasks they need to accomplish in the limited 24 hours. Therefore, recommendation systems help users make the right choices without expending too much cognitive effort.

The purpose of a recommendation system is to search for content that would be interesting to an individual. It involves various factors to create personalized lists of useful and relevant content specific to each user. Recommendation systems use Artificial Intelligence-based algorithms to analyze user behavior, browsing history, and similarities with other users to generate customized recommendations. This is achieved through predictive modeling and heuristics based on available data.

This system helps users **discover new content efficiently** while improving their engagement with the Pratilipi platform.

---






