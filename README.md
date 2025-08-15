## 🧬 Cancer genome classification using Machine Learning  

This project focuses on automating the classification of genetic mutations into cancer-related classes using machine learning techniques, thereby reducing manual diagnostic workload for pathologists.

### 🔍 Objective
To predict the type of cancer (1 of 9 classes) based on a combination of Gene name, Variation, and associated medical literature text for each patient mutation record.

---

### 🗃️ Data Source & Preprocessing
- Dataset from Kaggle: *MSKCC - Redefining Cancer Treatment*
- Two files: `training_variants.csv` and `training_text.csv` (3321 samples)
- Merged on `ID`, filled missing TEXT entries with Gene + Variation string
- Applied extensive **text preprocessing**: lowercase, stopword removal, stemming
- Bag-of-Words / TF-IDF vectorization for text features
- Combined categorical `Gene` and `Variation` with text features via one-hot and sparse matrix

---

### ⚙️ Modeling & Techniques
- Tried multiple models: **Naive Bayes**, **Logistic Regression**, **Linear SVM**, **XGBoost**
- Performed hyperparameter tuning using Grid Search (for SVM, XGBoost)
- Implemented **Stacking Classifier** with base models (NB, SVM, LR) and meta-model (Logistic Regression)
- Used **class probabilities** for multi-class classification as required

---

### 🧾 Business Impact
- Automates the most time-consuming step of mutation classification from text
- Helps pathologists focus on selection of relevant mutations, improving turnaround time

---

### 🛠️ Tools & Libraries
- Python, pandas, NumPy, scikit-learn, XGBoost, NLTK, mlxtend
