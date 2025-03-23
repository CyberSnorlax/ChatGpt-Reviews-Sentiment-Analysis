# 📱 ChatGPT App Reviews: User Sentiment and Feature Insights


## 🚀 Overview

This project analyzes user reviews of the **ChatGPT Android app** using natural language processing (NLP). Our goal is to extract insights into user sentiment, feature satisfaction, and the impact of version updates.

### 🔍 Objectives
- Analyze sentiment trends across app versions
- Identify feedback on core features (e.g., performance, UI, response quality)
- Investigate prompt handling challenges using bigram analysis

---

## 📊 Dataset

- **Source:** Kaggle (Google Play Store reviews of ChatGPT)
- **Total Reviews:** 278,337
- **Key Fields:** Rating, Review Text, App Version, Date, Country, Thumbs-Up Count

---

## 🧹 Data Processing

- **Text Cleaning:** Lowercasing, punctuation cleanup, emoji retention
- **Tokenization, Stopword Removal & Lemmatization**
- **Language Filtering:** Used `fastText` to retain primarily English reviews (~90% of data)
- **Sentiment Analysis:** Used `VADER` to calculate compound sentiment scores (text + emoji)
- **Feature Tagging:** Reviews classified into 5 categories using custom keyword matching:
  - `Performance`
  - `User Interface`
  - `Response Quality`
  - `Prompt Handling`
  - `Updates`

---

## ❓ Research Questions

1. **What features are most frequently mentioned across different sentiment categories?**
2. **How does sentiment for these features evolve across app versions?**
3. **What do bigrams reveal about prompt handling challenges and trends?**

---

## 📈 Key Findings

### RQ1: Feature Sentiment Breakdown
- **Most Discussed:** Response Quality (15,000+ mentions)
- **Most Positive:** Response Quality
- **Most Polarized:** Prompt Handling & Updates
- **Least Mentioned:** Performance

### RQ2: Sentiment Trends Over Versions
- Positive sentiment increased in early updates, but declined in later versions as user expectations grew
- Comments around `Updates` dropped significantly by GPT-4, reflecting app maturity

### RQ3: Bigrams & Prompt Handling
- Positive bigrams: `"good app"`, `"best app"`
- Negative bigrams: `"wrong answer"`, `"input field"`, `"keeps crashing"`
- **Prompt Handling Feedback:**
  - 79% Positive
  - 13% Negative — indicating issues with:
    - Response accuracy
    - UI limitations
    - App speed/crashes

---

## 🧠 Tools & Techniques

### 🔧 From Class:
- Data Cleaning
- Tokenization & Lemmatization
- Sentiment Analysis (VADER)

### 🌱 New Techniques:
- Emoji Sentiment Analysis
- Language Detection (FastText)
- Feature Keyword Matching
- Bigram Extraction (`CountVectorizer`)
- Functional Feature Tagging & Trend Analysis

---

## ⚠️ Limitations

- Some non-English reviews (in Roman script) were not filtered out
- Feature keyword matching is rule-based and may lack context sensitivity
- VADER struggles with sarcasm, slang, and complex emojis
- High-frequency bigrams often include generic praise


