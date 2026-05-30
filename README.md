# 📊 Employee Belonging & Engagement Analysis
### *"Employees who feel a sense of belonging are more engaged"*

A statistical investigation of this analytical statement using the **IBM HR Analytics dataset (1,470 employees)**, applying a full three-stage pipeline in Python.

---

## 🔗 Links
- 📓 [Google Colab Notebook](https://colab.research.google.com/drive/1IxoUJp42TCGQ_pNRsMZScLoYLaKe9AHI?usp=sharing)
- 📁 Dataset: [IBM HR Analytics – Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

---

## 📌 Problem Statement

Many organisations struggle with low employee engagement and turnover. This study investigates:

> *"Do employees who feel a stronger sense of belonging become more engaged?"*

---

## 🎯 Objectives

- Analyse the relationship between employee belonging and engagement
- Identify patterns using **Descriptive Analysis**
- Determine statistical significance using **Inferential Analysis**
- Evaluate predictive power using **Predictive Analysis**

---

## 🧱 Feature Engineering

The dataset had no direct Belonging or Engagement column, so two composite scores were engineered:

| Feature | Formula | Meaning |
|---|---|---|
| `BelongingScore` | (RelationshipSatisfaction + EnvironmentSatisfaction) ÷ 2 | How included and valued an employee feels |
| `EngagementScore` | (JobInvolvement + JobSatisfaction) ÷ 2 | How dedicated and satisfied an employee is |

---

## 📈 Results Summary

### Descriptive Analysis
| Group | BelongingScore (mean) | EngagementScore (mean) |
|---|---|---|
| Stayed | 2.753 | 2.775 |
| Left | 2.532 | 2.494 |

### Inferential Analysis (Independent Samples t-test)
| Test | Statistic | p-value | Decision |
|---|---|---|---|
| Pearson Correlation (Belonging vs Engagement) | r = -0.0015 | p = 0.9531 | ✖ No individual-level relationship |
| t-test: BelongingScore (Stayed vs Left) | t = 4.06 | p = 0.0001 | ✔ Significant difference |
| t-test: EngagementScore (Stayed vs Left) | t = 6.17 | p < 0.001 | ✔ Significant difference |

### Predictive Analysis
| Model | Accuracy | ROC-AUC |
|---|---|---|
| Logistic Regression | **86.1%** | **0.792** |
| Decision Tree | 85.0% | 0.754 |

Both `BelongingScore` and `EngagementScore` were significant **negative predictors** of attrition.

---

## ✅ Conclusion

The statement is **partially supported**:
- ✔ True at the **organisational level** — employees low on both scores are significantly more likely to leave
- ✖ Not true at the **individual level** — belonging does not directly predict engagement score-to-score
- Belonging and engagement appear to be two dimensions of the same underlying workplace wellbeing

---

## 🛠️ Tech Stack
`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Scikit-learn` · `SciPy` · `Google Colab`

---

## 👥 Team — Group KND_08

| Student No. | Name |
|---|---|
| IT23580176 | K A G T N Waidyarathne |
| IT23642232 | S R M P T Rathnayake |
| IT23728844 | M D A K Mahagamage |
| IT23599154 | P A Tennakoon |
