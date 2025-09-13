# 🎬 Hybrid Movie Recommender System  
_A Lights, Camera, Recommend! Project_

## 📌 Overview
This project builds a **Hybrid Movie Recommendation System** that suggests movies tailored to a user’s taste.  
It blends **Collaborative Filtering** (user–item interactions) with **Content-Based Filtering** (movie metadata like genres and ratings) to deliver accurate, personalized recommendations.

Key Highlights:
- **Hybrid Approach**: Combines matrix-factorization (SVD) with genre-based similarity.
- **Interactive Analysis**: Built and explored using Google Colab notebooks.
- **MovieLens Dataset**: Uses the well-known [MovieLens](https://grouplens.org/datasets/movielens/) dataset.

You can **run the notebook directly in Colab** here:  
[Open in Colab](https://colab.research.google.com/drive/1PetYy6DDdwaJo2E6LeavCL7BD2N_Hq3F?usp=sharing)

---

## 🗂️ Project Structure

---

## 📊 Dataset
- **Source**: MovieLens (small/1M/other variant depending on your download).
- **Contents**: User–movie ratings, movie metadata (titles, genres, etc.).
- **Preprocessing**:  
  - Merged ratings and movies tables  
  - Handled missing values  
  - Created user–item rating matrix

---

## Implementation Details

### 1. Collaborative Filtering (SVD)
- Factorizes the user–item matrix to learn latent user and movie features.
- Predicts ratings for unseen movies.

### 2. Content-Based Filtering
- Calculates similarity between movies using genres and average ratings.
- Provides recommendations even for new users with few ratings.

### 3. Hybrid Strategy
- Combines both approaches:  
  `final_score = α * SVD_prediction + (1-α) * Content_similarity`
- Adjustable parameters:
  - `sim_threshold` : similarity cutoff
  - `min_common`    : minimum common movies for neighbors
  - `shrinkage`     : regularization to handle sparse data
  - `svd_k`         : number of latent factors





