# FUTURE_ML_02 — Support Ticket Classification System

**Future Interns | Machine Learning Track | Task 2**

---

## 📌 Project Overview

An NLP-based machine learning system that automatically classifies customer support tickets into categories and assigns priority levels — helping support teams respond faster and smarter.

---

## 🎯 What It Does

- **Classifies** tickets into: `Billing` / `Technical` / `Shipping` / `Account`
- **Assigns priority**: `High` / `Medium` / `Low`
- **Compares** two ML models: Naive Bayes vs Logistic Regression
- **Shows confidence scores** for each prediction

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.10+ | Programming language |
| NLTK | Text preprocessing (tokenize, lemmatize, stopwords) |
| Scikit-learn | TF-IDF, ML models, evaluation |
| Pandas | Data loading and manipulation |
| Matplotlib / Seaborn | Visualizations |
| Pickle | Saving trained models |

---

## 🤖 ML Pipeline

```
Raw Ticket Text
      ↓
Text Preprocessing (lowercase → clean → tokenize → lemmatize)
      ↓
TF-IDF Feature Extraction (text → numbers)
      ↓
Train/Test Split (80% / 20%)
      ↓
┌─────────────────┐     ┌──────────────────────┐
│   Naive Bayes   │     │  Logistic Regression  │
└─────────────────┘     └──────────────────────┘
      ↓                           ↓
       ──────── Evaluation ────────
                    ↓
         Best Model → Saved (.pkl)
                    ↓
         Predict: Category + Priority
```

---

## 📁 Project Structure

```
FUTURE_ML_02/
├── data/
│   ├── tickets.csv               ← Dataset
│   ├── eda_distribution.png      ← EDA charts
│   ├── model_comparison.png      ← Accuracy comparison
│   └── confusion_matrices.png    ← Confusion matrix plots
├── model/
│   ├── category_model.pkl        ← Saved category classifier
│   ├── priority_model.pkl        ← Saved priority classifier
│   └── tfidf_vectorizer.pkl      ← Saved TF-IDF vectorizer
├── notebook/
│   └── ticket_classification.py  ← Main project code
├── requirements.txt              ← Python dependencies
└── README.md                     ← This file
```

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/FUTURE_ML_02.git
cd FUTURE_ML_02

# 2. Create folders
mkdir data model

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the project
cd notebook
python ticket_classification.py
```

---

## 📊 Results

| Model | Category Accuracy | Priority Accuracy |
|-------|:-----------------:|:-----------------:|
| Naive Bayes | ~85% | ~70% |
| Logistic Regression | ~90% | ~75% |

---

## 💡 Key Learnings

- **TF-IDF** converts text to meaningful numerical features
- **Lemmatization** reduces vocabulary size and improves accuracy
- **Logistic Regression** outperforms Naive Bayes on structured ticket data
- **Confusion matrix** reveals which categories the model struggles with

---

## 👤 Author

**[BHARATI KUMARI GUPTA]**
Future Interns — ML Track
GitHub: [@Bharatigupta]

---

*Submitted as part of Future Interns Machine Learning Internship Program*
