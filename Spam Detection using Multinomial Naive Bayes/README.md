# 📧 Spam Detection using Naive Bayes

A machine learning project to classify SMS messages as **spam** or **ham (not spam)** using the **Multinomial Naive Bayes** algorithm. This is a fundamental example of natural language processing (NLP) and classification.

---

## 📦 Dataset

- Source: [`spam.csv`](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)
- Contains SMS messages labelled as "ham" (not spam) or "spam".

---

## 🔧 Technologies Used

- Python 🐍
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn
- imbalanced-learn (SMOTE)
- CountVectorizer (for Bag-of-Words)
- MultinomialNB (Naive Bayes Classifier)

---

## 📊 Model Workflow

1. **Load and clean dataset**
2. **Vectorize text data** using `CountVectorizer`
3. **Handle class imbalance** using `SMOTE`
4. **Split into training and testing sets**
5. **Train** a `MultinomialNB` model
6. **Evaluate** with accuracy, confusion matrix, classification report, and ROC-AUC curve

---

## ✅ Model Performance

| Metric     | Value |
|------------|--------|
| Accuracy   | 97%    |
| Precision  | 99% (Ham), 95% (Spam) |
| Recall     | 95% (Ham), 98% (Spam) |
| F1-Score   | 97% (Both classes) |
| AUC Score  | 0.99   |

### 🔥 Confusion Matrix

[[1577 84]
[ 37 1487]]

### 📈 ROC Curve

![ROC Curve](roc_curve.png)

---

## 🧠 Model Comparison

Also included is a comparison with **Logistic Regression** to contrast performance. Naive Bayes performed slightly better for this task.

---
