
# 🎓 Early Dropout Detection Using Personalized Learning Data

> Predicting student dropout risk using behavioural and academic indicators through machine learning.

## 📘 Project Overview

This project focuses on early dropout prediction in personalized learning environments. Using the *Personalized Learning and Adaptive Education* dataset, we explored how student interaction patterns, academic performance, and engagement levels influence the likelihood of dropping out. We developed and deployed machine learning models to identify at-risk students, enabling timely intervention by educational institutions.

---

## 🎯 Objectives

- Analyze student behaviour and engagement patterns.
- Identify key features influencing dropout risk.
- Develop and evaluate predictive models for early dropout detection.
- Deploy a data product for real-time prediction and intervention support.

---

## 📂 Dataset

The dataset consists of 10,000 student records with:
- **Categorical features**: Gender, Education Level, Learning Style, Course Name, etc.
- **Numerical features**: Age, Time Spent on Videos, Quiz Scores, Forum Participation, Final Exam Score, etc.
- Target variable: `Dropout_Likelihood` (`Yes`/`No`)

> 🧼 No missing values were found. Preprocessing involved encoding, resampling, feature engineering, and scaling.

---

## 📊 Exploratory Data Analysis

- **Univariate Analysis**: Boxplots and histograms to examine distributions.
- **Bivariate Analysis**: Correlation heatmaps, count plots, and stacked bar charts to explore relationships with dropout likelihood.

Key insight: ~20% of students were classified as likely to drop out.

---

## 🤖 Models Used

We trained four machine learning models:
- Logistic Regression
- Random Forest
- Gradient Boosting
- CatBoost Classifier

> **SMOTE** was applied to address class imbalance before training.

| Model             | Accuracy | AUC-ROC | F1-Score |
|------------------|----------|---------|----------|
| Logistic Regression | 0.76     | 0.76    | 0.75     |
| Random Forest       | 0.88     | 0.88    | 0.86     |
| Gradient Boosting   | 0.84     | 0.85    | 0.82     |
| CatBoost Classifier | 0.86     | 0.85    | 0.83     |

> ✅ **Random Forest** had the best recall (ideal for early intervention), while **CatBoost** provided the best balance of performance and interpretability.

---

## 🧠 Feature Engineering Highlights

New features derived:
- `Learning_Efficiency`
- `Low_Engagement`
- `Low_Final_Exam_Score`
- `Is_Young`, `Is_Senior`, etc.

These helped capture nuanced behaviour and improve model accuracy.

---

## 📓 Jupyter Notebook

This project includes a Jupyter Notebook demonstrating the full pipeline:

- Data loading and preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering and selection
- Model training and evaluation
- Model deployment preparation

🔗 **View the notebook:** [notebook.ipynb](./notebook.ipynb)

---

## 🛠️ Installation

Clone the repository:

```bash
git clone https://github.com/deebtarmizi104/Early-Dropout-Detection-Using-Personalized-Learning-Data.git
cd Early-Dropout-Detection-Using-Personalized-Learning-Data
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Notebook

To launch the Jupyter Notebook:

```bash
jupyter notebook
```

Open the file `notebook.ipynb` and run through the cells to reproduce the results.

---

## 🌐 Deployment

The best-performing model (**CatBoost**) was deployed as an interactive web application using **Streamlit** and hosted via **Google Colab + Pyngrok**.

🧪 **Try it here (Colab runtime required):**  
[▶️ Interactive Web App Demo](https://d81e-34-91-203-36.ngrok-free.app)

---

## 🔁 Reproducibility

- All code and steps documented in Google Colab notebook.
- Follows the **OSEMN** framework.
- Dataset is publicly available on [Kaggle](https://www.kaggle.com/datasets/adilshamim8/personalized-learning-and-adaptive-education-dataset).

📦 **Key Libraries**:
```
pandas, numpy, scikit-learn, seaborn, matplotlib, catboost, streamlit, imblearn, pyngrok
```

---

## 🧑‍💻 Team Members

- Wan Nurul Adibah Binti Wan Tarmizi  
- Nur Anis Insyirah Binti Jowanis  
- Nur Izzati Binti Juhari  
- Puteri Safa Balqis Binti Megat Sharizal Amri  
- Yuhan Silvian

---

## 📌 Future Work

- Transition app from Colab to Streamlit Community Cloud or similar.
- Extend to longitudinal datasets and real-time learning dashboards.
- Integrate alert systems for real-time intervention.

---

## 📄 References

- Jayaprakash et al. (2016). *Early alert of academically at-risk students*. Journal of Learning Analytics.
- Prokhorenkova et al. (2018). *CatBoost: Unbiased boosting with categorical features*.
