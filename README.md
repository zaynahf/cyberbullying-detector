# Cyberbullying Detection Using Text Analysis

This project explores the detection of *sexist tweets* through machine learning models. It was developed as part of an academic research paper to analyze the performance of traditional NLP techniques versus modern transformer-based models.

---

## 🔍 Problem Statement

Social media platforms are widely used for public expression but are also home to increasing instances of *cyberbullying. This project focuses on **detecting sexism in tweets* using automated text classification.

---

## 📁 Dataset

- Source: Twitter (Parsed Dataset)
- Format: CSV
- Two classes:
  - sexism (label = 1)
  - none (label = 0)
- Size: ~3000+ rows (1000 used for baseline testing)

---

## 🧠 Models Used

### ✅ Baseline Model: TF-IDF + Logistic Regression
- Preprocessing: Text cleaning (lowercasing, removing URLs, mentions, punctuation)
- Feature extraction: TF-IDF (with bigrams, max 3000 features)
- Classifier: Logistic Regression
- Tools: scikit-learn, pandas, re, matplotlib

### 🔜 Final Model (Planned): DistilBERT
- Library: HuggingFace Transformers
- Architecture: Fine-tuned transformer-based model
- Goal: Improve recall on minority class (sexism)

---

## 📊 Results (Baseline Model)

| Class      | Precision | Recall | F1-score |
|------------|-----------|--------|----------|
| None (0)   | 0.81      | 0.99   | 0.89     |
| Sexism (1) | 0.80      | 0.10   | 0.17     |

- Accuracy: *81%*
- Challenge: Low recall on sexist tweets due to class imbalance

---

## 💻 Try It Out (Coming Soon)

A simple web interface to test the model using [Gradio](https://gradio.app/) is planned for the next phase.

You'll be able to:
- Type in any tweet or comment
- Instantly get a prediction: "Sexism" or "None"

Example:
python
Input: "Women are terrible drivers"
Output: Predicted class → Sexism
---

📄 Research Paper

This repository is part of an academic project titled:

> Cyberbullying Detection Using Text Analysis
Submitted by: Zaynah Farid
Institution: Amity University Lucknow Campus
---

📌 Future Improvements

Train on a larger, balanced dataset

Integrate real-time tweet scraping + classification

Deploy via Streamlit or Flask + frontend

---

🤝 Acknowledgments

Dataset inspiration from Kaggle & Twitter

HuggingFace for pretrained DistilBERT

Developed using Google Colab
