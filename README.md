# 📚 Book Recommendation System

This project implements a collaborative filtering-based recommendation system to suggest personalized books for users based on their prior ratings and preferences. The system uses matrix representations, cosine similarity, and weighted scoring to deliver meaningful book recommendations.

---

## 🎯 Objective

To build a recommender system that provides each user with a list of books tailored to their reading behavior, using collaborative filtering and user similarity analysis.

---

## 🧰 Tools & Libraries

- Python 3.x
- pandas, numpy, tqdm
- scikit-learn (cosine similarity)
- scipy (sparse matrices)
- Jupyter Notebook

---

## 🗃️ Project Highlights

- **Data Format**: Transformed raw ratings into efficient `.libsvm` sparse matrix formats
- **Similarity Engine**: Used cosine similarity to compute nearest neighbors (top 10 similar users per user)
- **Recommendation Pipeline**:
  - Extract books rated by similar users
  - Calculate weighted average ratings using similarity scores
  - Recommend top 5 unseen books with highest scores

---

## 📂 Project Structure

```
book-recommender-system/
├── book_ratings.libsvm                      # Sparse matrix of user-book ratings
├── book_ratings_with_user_age.libsvm        # Ratings for users with known age
├── book_ratings_without_user_age.libsvm     # Ratings for users with unknown age
├── Book_recommendation.csv                  # Final recommendations (top 5 per user)
├── Project Step 1_Task Selection and Data Cleaning.docx   # Data cleaning and matrix construction
├── Project Step 2_Data Analysis.docx        # Similarity analysis and recommendation logic
├── README.md                                # Project documentation
```

---

## 🔍 Recommendation Methodology

1. **User Similarity**:
   - Cosine similarity is computed for all users using their sparse rating vectors.
   - For each user, the 10 most similar users are identified.

2. **Book Candidate Pool**:
   - Books rated by similar users (excluding already-rated books) are collected.

3. **Weighted Scoring**:
   - Each book’s predicted score is calculated using the weighted average of ratings from similar users, scaled by similarity scores.

4. **Top-N Recommendations**:
   - The 5 highest-scoring unseen books are selected as final recommendations.

---

## 📝 Notes

- Implemented sparse matrix optimizations for scalability (over 100,000 users and 340,000+ books).
- Age-based filtering was performed to allow further segmentation of users.
- All similarity and recommendation calculations were batched to avoid memory issues.

---

## 👤 Authors

- Rahul Muddhapuram  
- Akilesh Shankar  
- Likhitha Mallarapu  
- Kranthi Kumari Sepuri

---

## 📄 License

This project is shared for educational purposes only. Redistribution or commercial use is not permitted without permission from the authors.

---

## 📬 Contact

For questions or collaborations, feel free to reach out via GitHub or LinkedIn.
