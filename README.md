# User-Profile-Prediction

Machine Learning with Python Group Project (Group 6)

Team : Laki, Meng, Hui, Rui

This Project used NLP and ML to predict user Gender and Age based on browsing history.

### I. Data Preprocess
(A) Combine Word Frequency
- STEP 1: List to Dictionary
- STEP 2: Key * Values = Complete  corpus

(B) NLP Preprocess 
- STEP 1: Word Tokenization by nltk
- STEP 2: Remove symbols and stopwords by spacy (remove not recgonised vector)
- STEP 3: Lemmetizer and stemmer by English & French libraries together

### II. Feature Engineering
(A) Restrict Length
- keep the rows with more than 50 words to prevent the sparse matrix
(without this step, the f1 score will only be about 0.6)

(B) TF-IDF
- restrict the min_df = 0.01 to avoid noise

### III. Model and Evaluation
(A) Best weak estimator - Naive Bayes (f1-score:0.74)

(B) Stacking Model:
- week estimators : Logistic Regression, Naive Bayes, KNN
- performance : 0.73

###  Reflection:
- Naives Bayes does outperfom other weak estimators in the text classicifation problem
- TF-IDF outperforms the count vectorizer. Restrict the min or max frequency will also help improve the performance
- Keywords length matters a lot in this project. Reduce noise and avoid sparse matrix will help get higher scores.
