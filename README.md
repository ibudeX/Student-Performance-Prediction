# 🎓 Student Performance Prediction — Multiple Linear Regression & Random Forest

## 📌 Objective
This project predicts the **Performance Index** of students using features such as study hours, previous scores, extracurricular activities, sleep hours, and the number of sample papers practiced.  
It compares **Multiple Linear Regression** and **Random Forest Regressor** to determine the most accurate model for predicting performance.

---

## 📂 Dataset Overview & Cleaning

| Property | Value |
|----------|-------|
| Initial Shape | 500 rows × 6 columns |
| Missing Values | None |
| Duplicate Rows | 127 |
| Final Shape | 500 rows (after cleaning) |
| Target Variable | `Performance Index` (continuous) |

**Columns**:
- `Hours Studied`  
- `Previous Scores`  
- `Extracurricular Activities` (`Yes`/`No`)  
- `Sleep Hours`  
- `Sample Question Papers Practiced`  
- `Performance Index`  

**Data Cleaning Actions**:
- Removed duplicate rows.
- Mapped categorical values (`Yes` → 1, `No` → 0) for `Extracurricular Activities`.

---

## 🔍 Exploratory Data Analysis (EDA)

### Key Findings:
- **Positive correlations**:
  - More hours studied → higher performance.
  - Higher previous scores → higher performance.
  - More practice papers → higher performance.
- **Slight negative correlation** with extracurricular activities.
- Sleep hours show mild positive impact.

### Example Visualizations:

| Hours Studied Distribution | Correlation Heatmap |
|----------------------------|---------------------|
| ![Hours Studied](https://github.com/user-attachments/assets/e0ddde10-e29b-4467-8d6e-09525cf80c99) | ![Heatmap](https://github.com/user-attachments/assets/72d0e279-8890-4943-8fb0-dc91fa41faac) |

---

## ⚙️ Preprocessing Pipeline

**Numerical Features**:
- Median imputation for missing values.
- Standardization using `StandardScaler`.

**Categorical Features**:
- Most frequent value imputation.
- Encoding with `OneHotEncoder`.

✅ Implemented using `ColumnTransformer` and `Pipeline` for clean, reproducible workflows.

---

## 🤖 Model Training & Evaluation

**Train-Test Split**: 80% training / 20% testing  

| Model | R² Score | Notes |
|-------|----------|-------|
| **Linear Regression** | ~0.97 | High accuracy, interpretable coefficients. |
| **Random Forest Regressor** | ~0.98 | Slightly higher accuracy, handles non-linear patterns well. |

---

## 📊 Insights
- Strongest predictors:
  - `Hours Studied`
  - `Previous Scores`
  - `Sample Question Papers Practiced`
- Random Forest performs slightly better overall.
- Linear Regression remains valuable for interpretability.

---

## ✅ Conclusion & Recommendations
- **Recommendation**: Deploy the Random Forest model for production use.
- Possible applications:
  - School dashboards for real-time student performance prediction.
  - Personalized academic improvement plans.
- **Future Improvements**:
  - Include more features like attendance, subject preferences, and parental involvement.
  - Experiment with ensemble learning techniques.

---
