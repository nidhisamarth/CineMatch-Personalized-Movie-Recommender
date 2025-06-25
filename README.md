# CineMatch-Personalized-Movie-Recommender using Content-Based Filtering

This Python script implements a content-based movie recommendation system using the IMDb dataset. The project involves data preprocessing, text processing, and feature extraction to create a recommendation model. The primary steps include:

1. **Data Loading and Selection:**
   - The IMDb dataset is loaded using Pandas from a CSV file.
   - Relevant columns (Series_Title, Genre, Overview, Director, Star1, Star2, Star3, Star4) are selected for analysis.

2. **Data Cleaning and Text Processing:**
   - Text data in selected columns is converted to lowercase for consistency.
   - Spaces are removed from columns like 'Director', 'Star1', 'Star2', 'Star3', 'Star4'.
   - The 'Overview' column is split into a list of words.

3. **Feature Engineering:**
   - Each word in 'Director', 'Star1', 'Star2', 'Star3', 'Star4', 'Genre', and 'Overview' is converted to lowercase.
   - Lists from these columns are combined into a new column 'Tags'.
   - Redundant columns are dropped.

4. **Text Stemming:**
   - Porter stemming is applied to the 'Tags' column to reduce words to their root form.

5. **Feature Extraction using CountVectorizer:**
   - The CountVectorizer is utilized to convert the 'Tags' column into a matrix of token counts.
   - The matrix is limited to 4000 features, and English stop words are removed.

6. **Cosine Similarity Calculation:**
   - Cosine similarity is computed between movies based on the extracted features.

7. **Movie Recommendation Function:**
   - The 'recommend' function takes a movie title as input, finds its index, and calculates cosine similarity with other movies.
   - It then prints the top 5 recommended movies based on similarity.

8. **Example Recommendation:**
   - An example recommendation is provided for the movie 'The Dark Knight'.

## How to Use:
1. Clone the repository.
2. Ensure Python and required libraries (NumPy, Pandas, scikit-learn, NLTK) are installed.
3. Run the script in a Jupyter Notebook or any Python environment.

Feel free to contribute and enhance the project for more advanced features and scalability. If you have any questions or suggestions, please open an issue.

**Note:** The provided IMDb dataset file can be downloaded form Kaggle.
