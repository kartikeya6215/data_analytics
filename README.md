# Amazon Reviews Analytics: From Raw JSON to Data Preprocessing and Exploratory Review Analysis with Python
# 📦 Amazon Review Data Cleaning & Sentiment Analytics

This project demonstrates an end-to-end data analytics workflow on the **Amazon Cell Phones and Accessories Review Dataset**, starting from raw JSON to cleaned, structured data, followed by exploratory visualizations and sentiment classification using machine learning models.

---

## 📁 Dataset Overview

- **Source**: `Cell_Phones_and_Accessories_5.json` (public Amazon reviews dataset)
- **Volume**: 500,000+ product reviews (subset used)
- **Fields**:
  - `reviewText`: full review body
  - `summary`: short title of the review
  - `overall`: star rating (used to derive sentiment)
  - `helpful`: list of helpful/unhelpful votes
  - `reviewTime`, `unixReviewTime`: review timestamps
  - `reviewerID`, `asin`: reviewer & product identifiers

---

## 🧹 Data Cleaning & Preprocessing

- Converted raw JSON into a structured `pandas` DataFrame
- Dropped duplicates and null entries
- Cleaned review text using:
  - Regex for removing special characters and numbers
  - Lowercasing, tokenization, and stopword removal
  - TextBlob for spelling correction
- Derived binary sentiment labels based on star ratings:
  - Ratings 1–2 → Negative  
  - Rating 3 → Neutral  
  - Ratings 4–5 → Positive

---

## 📊 Exploratory Data Analysis (EDA)

Visualizations created using **matplotlib**, **seaborn**, **Altair**, and **Plotly**:
- Rating distribution histogram
- Word cloud and most frequent terms
- Helpful vs unhelpful vote analysis
- Bar chart of model accuracy comparisons

---

## 🤖 Machine Learning Models

Six classifiers trained and evaluated:
- Logistic Regression
- Decision Tree
- Random Forest
- Naive Bayes
- K-Nearest Neighbors

### 🔍 Evaluation
- 10-fold cross-validation for model comparison
- Accuracy, precision, recall metrics displayed
- Confusion matrix visualization included

---

## 🧠 Key Results

- **Cleaned data size**: ~29,000 reviews after preprocessing
- **Top accuracy**: ~91% with Random Forest (varies with parameters)
- **Final cleaned dataset** saved to `train_file.csv`
- Interactive visual outputs available for Power BI integration

---

## 🧰 Tech Stack

| Tool / Library | Purpose |
|----------------|---------|
| Python (pandas, numpy) | Data handling & preprocessing |
| TextBlob | Spelling correction & sentiment tools |
| Matplotlib / Seaborn / Altair / Plotly | Visualizations |
| Scikit-learn | ML model training & evaluation |
| Jupyter Notebook | Interactive development |

---

## 📌 How to Use

1. Download the dataset (`Cell_Phones_and_Accessories_5.json`)
2. Open `final (1).ipynb` in Jupyter Notebook / VS Code
3. Run all cells in order to:
   - Clean the data
   - Explore visuals
   - Train models
4. Optional: Export cleaned CSV and visuals for external tools




## 📄 License

This project is open-source and available under the MIT License.
