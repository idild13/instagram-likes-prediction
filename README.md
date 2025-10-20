# Instagram Likes Prediction 📸➡️📈

A machine learning project predicting **Instagram post likes** from follower and engagement data, developed during Le Wagon’s Data Analytics Bootcamp.  

The project demonstrates end-to-end regression modeling — from data cleaning and feature engineering to evaluation and model improvement.

---

## 🔍 Goal

Estimate the number of likes an Instagram post receives based on:
- the author’s **follower count**, and  
- their **historical engagement** (median likes from previous posts).

This illustrates how a simple additional feature can dramatically improve predictive accuracy.

---

## 🧰 Tools & Libraries

- **Python**, **pandas**
- **scikit-learn** (Linear Regression, metrics, scaling)
- **plotly** for visualization
- **Jupyter / Google Colab** environment

---

## 📑 Data Overview

- Original dataset: `posts.csv`  
  ~2.26 million posts across **9,298 authors**
- Key columns:
  - `id` – author identifier  
  - `followers` – number of followers  
  - `comments`, `posts`, `likes` – engagement metrics  
  - `ts` – timestamp  

After cleaning:
- One record per author (their latest post)
- Added feature: **`historical_likes`** = median likes from that author’s previous posts

---

## 🧠 Modeling Process

1. **Data Preparation**
   - Sorted posts by timestamp  
   - Kept each author’s latest post  
   - Computed median historical likes for previous posts  
   - Merged into a single modeling table  

2. **Modeling**
   - Split into training (80%) and test (20%)
   - Scaled features with `StandardScaler`
   - Trained Linear Regression using scikit-learn  

3. **Evaluation Metrics**
   - R², MAE, RMSE for train and test sets  

---

## 📊 Results

| Model | Features | Test R² | Test MAE | Test RMSE |
|--------|-----------|----------|-----------|------------|
| **Baseline** | followers | 0.13 | 28.45 | 37.38 |
| **Improved** | followers + historical_likes | **0.56** | **23.41** | **31.73** |

> Adding one historical feature raised R² from **0.13 → 0.56** and reduced prediction error by about **5 likes** on average.

---

## 📂 Suggested Repo Structure
```text
instagram-likes-prediction/
├─ notebooks/
│  └─ 01_instagram_likes_prediction.ipynb
├─ data/
│  ├─ raw/                 # (not uploaded to GitHub)
│  └─ processed/
├─ reports/figures/
├─ requirements.txt
└─ README.md
```

---

## 🔒 Ethics & Notes

- No personal or identifying data is included.  
- The dataset is used only for educational purposes.  
- The project focuses on modeling concepts, not real user data.

---

## 🙌 Author

**Idil Dorak**  
Data & Marketing Analytics Professional  
📍 Based in Berlin | 💼 [Le Wagon Data Analytics Bootcamp Graduate]
