## NLP Recommendation System 
A minimal, explainable content-based recommender built in Python. It vectorizes article text with TF-IDF and ranks similar items using cosine similarity.


✨ What this repo does
Turns text (title/description) into vectors with TfidfVectorizer(stop_words="english")

Computes pairwise similarity using cosine_similarity

Returns the Top-K most similar items to a given article

Fully contained in a single Jupyter notebook for clarity and learning

## 🧠 How it works (high level)
DataFrame setup (sample in the notebook):

Vectorize text
TfidfVectorizer(stop_words="english").fit_transform(df["text"])

Compute similarity
cosine_similarity(tfidf_matrix) → an N x N matrix where [i, j] is how similar item i is to j.

Rank
For a chosen article index q, sort row similarity_matrix[q] descending; skip q itself, return top-K.

