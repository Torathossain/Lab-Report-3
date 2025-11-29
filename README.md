# ID-CSE412-223E2-LabReport03: News Classification using Naïve Bayes

## 🎯 Assignment Objective

This repository contains the files and code for **Lab Report 03** in **CSE 412 (Machine Learning/Data Mining)**. The primary objective was to implement a complete text classification pipeline using the **Naïve Bayes classifier** to distinguish between two categories of news: **Sports** and **Politics**.

The pipeline includes crucial steps in Natural Language Processing (NLP), such as text cleaning, feature extraction using TF-IDF, and model evaluation.

## 🗃️ Repository Contents

| File Name | Description |
| :--- | :--- |
| `naive_bayes_classifier.py` | The main Python script that performs the text cleaning, TF-IDF vectorization, 80:20 data split, Multinomial Naïve Bayes model training, and evaluation. |
| `news_data.csv` | **(Action Required: User-Generated File)** The custom dataset containing 100 news texts (50 Sports, 50 Politics) with `text` and `label` columns (0=Sports, 1=Politics). |
| `naive_bayes_metrics.csv` | Output file summarizing the evaluation metrics (Accuracy, Precision, Recall, F1-Score). |
| `README.md` | This file, providing an overview of the assignment and methodology. |

---

## 💻 Methodology

### 1. Preprocessing and Cleaning

The data underwent comprehensive text cleaning as per instructions:

* **Normalization:** Converted all text to lowercase.
* **Noise Removal:** Removed punctuation, numbers, and extra spaces.
* **Token Filtering:** Removed standard English stopwords.
* **Word Normalization:** Applied **Lemmatization** to reduce words to their base form.

### 2. Feature Extraction

The cleaned text features were converted into a numerical format using the **TF-IDF Vectorizer**. The vectorizer was fitted exclusively on the training data to prevent data leakage.

### 3. Model Training and Split

* **Model:** `sklearn.naive_bayes.MultinomialNB`
* **Split Ratio (Train:Test):** **80:20** (Stratified split to ensure equal class representation).

---

## 📈 Results

### Evaluation Metrics

| Metric | Value |
| :--- | :--- |
| **Accuracy** | [Insert Actual Accuracy] |
| **Precision (Weighted)** | [Insert Actual Precision] |
| **Recall (Weighted)** | [Insert Actual Recall] |
| **F1-Score (Weighted)** | [Insert Actual F1-Score] |

### Confusion Matrix

The confusion matrix on the test set (Layout: $\begin{pmatrix} \text{TN} & \text{FP} \\ \text{FN} & \text{TP} \end{pmatrix}$) provides insight into prediction quality:

$$\text{Confusion Matrix} = \begin{pmatrix}
[\text{TN}] & [\text{FP}] \\
[\text{FN}] & [\text{TP}]
\end{pmatrix}$$
*(Where Class 0 = Sports, Class 1 = Politics)*

### Class Analysis Summary

[Briefly summarize your analysis here, specifically addressing which class (Sports or Politics) was classified better based on the Precision and Recall values in the classification report, and provide a quick reason based on vocabulary distinctiveness.]

---

## ⚙️ How to Run the Code

1.  **Prerequisites:** Ensure you have Python installed, along with the required libraries (`pandas`, `numpy`, `scikit-learn`, `nltk`).
    ```bash
    pip install pandas numpy scikit-learn nltk
    ```
2.  **Dataset:** Ensure your custom `news_data.csv` file is in the same directory as the script.
3.  **Execution:** Run the script from your terminal:
    ```bash
    python naive_bayes_classifier.py
    ```
4.  **Output:** The script will print the metrics and confusion matrix to the console, and save the final results to `naive_bayes_metrics.csv`.

---

## 📝 Submission Requirement

The final submission is the PDF file named **`[YourID]-CSE412-223E2-LabReport03-NaïveBayes.pdf`**, which includes the full methodology, model theory, and detailed analysis.
