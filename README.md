# Public Sentiment Analysis â€” Union Budget 2024

> **Analyzing Public Sentiment Towards the Union Budget 2024: A Social Media Perspective**  
> Amrita Vishwa Vidyapeetham, Bengaluru â€” Foundations of Data Science

---

## Overview

An end-to-end **NLP and sentiment analysis pipeline** on public reaction to India's Union Budget 2024, collected from YouTube, Instagram, and Reddit. The project covers data collection, exploratory analysis, text classification, and statistical hypothesis testing.

---

## Pipeline

```
Social Media Data (YouTube Â· Instagram Â· Reddit)
    â†“
Preprocessing â€” tokenisation, stopword removal, lemmatisation (NLTK + spaCy)
    â†“
EDA â€” word clouds, bigram networks, sentiment distribution by platform
    â†“
Feature Extraction â€” TF-IDF vectorisation
    â†“
Classification â€” Logistic Regression (multiclass: Positive / Negative / Neutral)
    â†“
Evaluation â€” Accuracy, ROC-AUC, Precision-Recall, Learning Curves
    â†“
Hypothesis Testing â€” ANOVA / Kruskal-Wallis across platforms
```

---

## Dataset

`prepared_fds_sorted.xlsx` â€” included in this repository  
- **Source:** Web-scraped from YouTube, Instagram, Reddit (Union Budget 2024 discussions)
- **Columns:** `COMMENT`, `LABEL`, `WEBSITE`, `sentiment`
- **Labels:** Positive, Negative, Neutral

---

## Files

| File | Description |
|---|---|
| `1.1.ipynb` | EDA â€” word clouds, bigrams, network graphs, spaCy NLP |
| `SEP1.ipynb` | TF-IDF + Logistic Regression + ROC/PR curves |
| `STEP3.ipynb` | Hypothesis testing â€” Shapiro-Wilk, Levene, ANOVA, Kruskal-Wallis, Pearson/Spearman |
| `prepared_fds_sorted.xlsx` | Dataset |

---

## Requirements

```bash
pip install pandas numpy nltk spacy scikit-learn matplotlib seaborn scipy wordcloud networkx
python -m spacy download en_core_web_sm
```

---

## Key Concepts

- **TF-IDF** â€” Term Frequency Ã— Inverse Document Frequency; downweights common words, upweights distinctive words
- **Logistic Regression for text** â€” linear classifier on high-dimensional sparse TF-IDF vectors; strong baseline for sentiment classification
- **ROC-AUC (multiclass)** â€” One-vs-Rest AUC; measures class separability
- **Kruskal-Wallis vs ANOVA** â€” Kruskal-Wallis is the non-parametric alternative when normality assumption (Shapiro-Wilk) is violated
- **Social media bias** â€” selection bias: users who comment tend to have stronger opinions; sample is not representative of all citizens

---

## Authors

Geda Tejesh Chowdary Â· Paramkusam Sriharsha Â· Yelipe Gowtham  
Amrita Vishwa Vidyapeetham, Bengaluru
