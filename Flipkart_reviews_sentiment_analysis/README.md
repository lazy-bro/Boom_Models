# 📝 Flipkart Reviews Sentiment Analysis

This project implements a **Sentiment Analysis** model to classify customer reviews from Flipkart as either **positive (1)** or **negative (0)**. The analysis covers the full machine learning pipeline, from **Data Exploration and Preprocessing** to **Model Training and Evaluation**, utilizing two distinct classification algorithms.

---

## 🚀 Project Overview

The core objective is to analyze a dataset of Flipkart product reviews and their corresponding ratings to build a model that can automatically determine the sentiment (positive or negative) expressed in the text.

### Key Technologies Used:
* **Data Manipulation:** `pandas`
* **Text Preprocessing:** `nltk` (for stopwords removal)
* **Data Visualization:** `matplotlib`, `seaborn`, `WordCloud`
* **Machine Learning:** `scikit-learn` (for TF-IDF, Model Training, and Evaluation)

---

## 📊 Data Exploration and Visualization

The initial dataset contains **9976 rows** with two main columns: `review` (text) and `rating` (1 to 5).

### 1. Rating Distribution
The distribution of the raw 1-5 star ratings shows a strong skew towards positive reviews:

| Rating | Count | Percentage |
| :----: | :---: | :--------: |
| **5** | 5726 | **57.4%** |
| **4** | 2365 | **23.7%** |
| **3** | 884 | 8.9% |
| **1** | 691 | 6.9% |
| **2** | 310 | 3.1% |

The high count of 5-star and 4-star reviews (over 81%) indicates an **imbalanced dataset** even before sentiment conversion.



### 2. Sentiment Conversion and Distribution

A new `sentiment` column was created for **binary classification** by mapping the `rating` column:
* **Positive Sentiment (1):** Ratings **4 and 5**.
* **Negative Sentiment (0):** Ratings **1, 2, and 3**.

The resulting binary sentiment distribution is:

| Sentiment | Count | Percentage |
| :-------: | :---: | :--------: |
| **1 (Positive)** | 8091 | **81.1%** |
| **0 (Negative)** | 1885 | 18.9% |



### 3. Word Cloud for Positive Reviews

To visualize the most frequent words in the positive reviews after **text cleaning** (lowercasing and **stopwords removal**), a Word Cloud was generated. This helps quickly identify key terms associated with favorable reviews.



---

## 🛠️ Preprocessing and Feature Engineering

### 1. Text Preprocessing
The review text was preprocessed to clean and normalize the data:
* **Lowercasing**
* **Stopwords Removal** (using `nltk`'s English stopwords list)

### 2. Feature Extraction (TF-IDF)
The cleaned text data was converted into numerical features using **TF-IDF (Term Frequency-Inverse Document Frequency)**, which assigns weight to a word based on its importance within a document and across the entire corpus.
* The `TfidfVectorizer` was initialized to consider the **top 5000 features** (`max_features=5000`).

---

## 🤖 Model Training and Evaluation

The data was split into **80% training** and **20% testing** sets (`test_size=0.2`) for model validation. Both models were compared based on their **accuracy** and **Confusion Matrix** to assess performance.

### 1. Decision Tree Classifier

The **Decision Tree** model served as a baseline. The Confusion Matrix helps visualize correct predictions (True Positives and True Negatives) and errors (False Positives and False Negatives).

* **Accuracy:** **0.8497**



### 2. Random Forest Classifier

The **Random Forest** model, an **ensemble method**, was used to improve generalization and stability.

* **Accuracy:** **0.8978**



### 🎯 Conclusion on Performance

The **Random Forest Classifier** achieved the highest accuracy of **~89.8%**, outperforming the Decision Tree Classifier (~85.0%). The Random Forest model offers a better balance between bias and variance, making it the preferred choice for this sentiment analysis task.
