# STAAR_Score_Predictive_Model
Predicting 8th Grade STAAR Scores with Polynomial Regression
# Predicting 8th Grade STAAR Scores with Polynomial Regression

This project explores how to use classroom assessment trends to build a predictive model for 8th Grade Math STAAR (State of Texas Assessments of Academic Readiness) scores. The analysis supports instructional planning, intervention strategies, and student performance forecasting using real classroom data.

## 🎯 Objective

To predict STAAR scores using assessment data collected throughout the 2024–2025 school year and evaluate the effectiveness of a nonlinear model.

## 📊 Dataset

- **Student assessments**: Periodic tests (Blue = mid-6 weeks, White = end of 6 weeks)
- **Sample size**: 1st period class (30–40% of students with learning disabilities)
- **Assessments included**: 7+ assessments + benchmark + final STAAR score

## ⚙️ Tools & Technologies

- Python (Pandas, scikit-learn)
- Power BI (DAX, visual trends)
- Google Sheets (data formatting and tracking)

## 🧠 Model Used

Polynomial Regression (Degree 2)

```python
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import PolynomialFeatures
from sklearn.pipeline import make_pipeline
