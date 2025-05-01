# Loading and Displaying the TripAdvisor Hotel Reviews Dataset
---
---
- Display the first 5 rows using `df.head()` to understand the structure (columns: `Review`, `Rating`).

![image](https://github.com/user-attachments/assets/05d5deca-df26-4148-ad15-2d32295f8886)
![image](https://github.com/user-attachments/assets/8ab01d50-67e8-40d7-b7c4-acb35d915c01)


---
###  NLTK Setup for Text Preprocessing

- Download necessary NLTK resources: tokenizer, stopwords, lemmatizer, etc.
- Import tools for tokenization, stopword removal, stemming, and lemmatization.
---
###  Preprocess Text Reviews
- Define `preprocess()` function
- Test the function on the first review in the dataset.
---
### 📊 Add Processed Text and Token Counts

- Apply the `preprocess()` function to each review and store the lemmatized tokens.
- Calculate original token count and cleaned (lemmatized) token count.
- Display a preview with both counts.

![image](https://github.com/user-attachments/assets/d609092e-e18b-4878-b4e7-cc967d30a3ba) 
![image](https://github.com/user-attachments/assets/cea0479b-f98b-457a-8004-6ce9bfeb8919)


---
### 📈 Visualize Token Counts (Before vs After Cleaning)

- Sample 5 reviews to simplify plots.
- Plot histograms of token counts before and after cleaning.
- Use scatter and line plots to compare original and cleaned token counts.
![image](https://github.com/user-attachments/assets/e66ad794-1644-4257-8cee-4f90f8fa608f)

---
### 🧾 Create Bag-of-Words (BoW) Features

- Convert lemmatized tokens back to strings for vectorization.
- Use `CountVectorizer` to extract BoW features.
- Display first 10 feature names and BoW vector for one review.
----
###   Create TF-IDF Features

- Apply `TfidfVectorizer` to the cleaned text.
- Generate TF-IDF matrix to capture term importance.
- Show first 10 feature names and the TF-IDF vector of one sample.
---
### Train Word2Vec Embeddings

- Preprocess reviews into lemmatized tokens.
- Use Gensim’s `Word2Vec` to train word embeddings:
  - `vector_size=100`: dimensionality of vectors
  - `window=5`: context window
  - `min_count=2`: ignore rare words
- `sentences` is a list of token lists used for training.
----
### 🧾 Word2Vec: Inspect Word Embeddings

- Train Word2Vec on cleaned review tokens.
- Check if the word "hotel" exists in the model.
- Print the first 10 values of its vector representation.
---
 ### t-SNE Visualization of Word2Vec Embeddings
- Select the top 100 most frequent words from the Word2Vec model.

- Extract their vector representations.

- Apply t-SNE to reduce dimensions to 2D.

- Plot the 2D word vectors with labels.
![image](https://github.com/user-attachments/assets/328ea965-3669-4a3d-afbd-947b0e619cf1)

---
## Author 
- Mohammed Al-Shujaa
---
