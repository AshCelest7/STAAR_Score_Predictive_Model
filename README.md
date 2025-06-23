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

## 🧪 Approach

- 1. Used Power BI to visualize trends and compute class averages via DAX
- 2. Chose a polynomial model based on trend dip near Benchmark assessment
- 3. Trained the model on assessment data and predicted STAAR scores
 -4. Compared predictions to actual STAAR scores using Python

## 📈 Outcome
- Predictive model closely mirrored actual STAAR outcomes
- Enabled early identification of students needing intervention
- Highlighted the importance of assessment trends for planning

## 🤖 Sample Code
model = make_pipeline(PolynomialFeatures(degree=2), LinearRegression())
model.fit(X, y_dummy)
df['STAAR_Predicted'] = model.predict(X) * 100
df['Prediction Error'] = df['STAAR_Predicted'] - df['8th Grade STAAR']

##🧩 Future Plans
- Apply model across all class periods
- Use benchmark predictions for mid-year interventions
- Share insights with educators/admin to guide instruction

##🔗 Let's Connect
Feel free to explore the code and connect on LinkedIn for collaboration or discussion on educational data science!
