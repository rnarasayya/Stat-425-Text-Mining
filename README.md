# 📚 Beyond the Stars: Text Mining Amazon Book Reviews

This project explores how **language, sentiment, and book metadata** influence reader satisfaction and review scores on Amazon. Using large-scale text mining and machine learning techniques, we analyze millions of book reviews to uncover patterns in reader sentiment, thematic content, and rating behavior.

> Final Project for **STAT 425 – Text Mining**  
> UCLA | Rohan Narasayya & Justin Huang

---

## 🔍 Project Overview

Online reviews play a critical role in shaping consumer decisions. In this project, we combine **unstructured review text** with **structured book metadata** to answer questions such as:

- What language patterns distinguish 1-star from 5-star reviews?
- Which genres, authors, and publishers receive higher ratings?
- Can we predict whether a book will be recommended based on review text?
- What themes emerge across different ratings and genres?
- Can review behavior support a basic recommendation system?

The analysis spans **sentiment analysis, topic modeling, classification, and recommendation systems**, with an emphasis on interpretability and real-world business insights.

---

## 📊 Data

We use two large-scale datasets:

- **Amazon Book Reviews Dataset**  
  - Over 3 million reviews  
  - Fields include review text, rating, helpfulness, time, and user ID

- **Book Metadata Dataset**  
  - Title, authors, genres, publisher, price, publication date, ratings count

Datasets are merged on book title and cleaned for downstream analysis.

---

## 🧠 Methods & Techniques

### 1. Sentiment Analysis
- Tokenization and stopword removal
- Polarity and subjectivity analysis using **TextBlob**
- Comparison of sentiment trends across review scores

### 2. Exploratory Text Analysis
- Most frequent words in 1-star vs. 5-star reviews
- Genre-, author-, and publisher-level sentiment patterns

### 3. Topic Modeling
- **Latent Dirichlet Allocation (LDA)**
- Topics extracted by:
  - Review score (1-star, 3-star, 5-star)
  - Book genre (e.g., Self-Help, Cooking, Juvenile Fiction)
- Interpretation of thematic differences across reader sentiment

### 4. Classification Models
- Predict whether a book is “recommended” (≥ 4 stars)
- Models used:
  - Logistic Regression
  - Random Forest
  - XGBoost
  - Neural Network
- Addressed class imbalance using **SMOTE**
- Evaluated with precision, recall, F1 score, and accuracy

### 5. Recommendation System
- Implemented **Bayesian Personalized Ranking (BPR)**
- Learned user and item embeddings
- Evaluated using:
  - BPR loss
  - Hit Rate @10
  - AUC

---

## 📈 Key Findings

- **Sentiment polarity increases monotonically with review score**, while subjectivity is highest in extreme reviews.
- Book **genre and author strongly influence ratings**, while price has negligible correlation with sentiment or score.
- Topic modeling reveals:
  - Negative reviews focus on unmet expectations, formatting issues, and controversial content
  - Positive reviews emphasize emotional attachment, storytelling, and high-quality editions
- Classification models achieve solid performance despite heavy class imbalance.
- The recommendation system demonstrates reasonable ranking performance (AUC ≈ 0.75).

---

## 🧰 Tools & Technologies

- **Languages:** Python, R  
- **NLP:** TextBlob, LDA  
- **ML:** scikit-learn, XGBoost, TensorFlow  
- **Visualization:** matplotlib, ggplot2  
- **Techniques:** SMOTE, topic modeling, sentiment analysis, collaborative filtering

---

## ⚠️ Limitations

- Strong class imbalance toward positive reviews
- Inconsistent or missing genre metadata
- Computational constraints (Google Colab free tier)
- LDA limitations with short, informal review text

---

## 📌 Business Applications

- Publishers can identify themes that resonate with readers across genres
- E-commerce platforms can improve discovery using sentiment-driven recommendations
- Insights suggest content quality matters more than pricing in reader satisfaction

---

## 📄 Paper

The full report is available in the repository:  
**`Stat_425_Final_Paper.pdf`**
