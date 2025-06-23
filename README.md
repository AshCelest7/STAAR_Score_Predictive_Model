# STAAR Score Predictive Model  
**Predicting 8th Grade STAAR Scores with Polynomial Regression**

This project explores how to use classroom assessment trends to build a predictive model for 8th Grade Math STAAR (State of Texas Assessments of Academic Readiness) scores. The analysis supports instructional planning, intervention strategies, and student performance forecasting using real classroom data.

---

## 🎯 Objective

To predict STAAR scores using assessment data collected throughout the 2024–2025 school year and evaluate the effectiveness of a nonlinear regression model.

---

## 📊 Dataset

- **Assessment Types**:
  - *Blue assessments*: Mid-6 weeks (8–10 questions on 1–2 TEKS)
  - *White assessments*: End-of-6 weeks (12–18 questions covering multiple TEKS)
  - *Benchmark*: Semester mock STAAR with 70% of TEKS taught
- **Sample Size**: 1st period class  
  - 30–40% of students with learning disabilities  
- **Assessment Range**: 7+ assessments + benchmark + final STAAR score

---

## ⚙️ Tools & Technologies

- Python: `pandas`, `scikit-learn`
- Power BI: DAX formulas, visual trend exploration
- Google Sheets: data formatting and tracking

---

## 🧠 Model Used

- **Polynomial Regression** (degree = 2)  
  - Chosen to reflect nonlinear student performance trends
  - python
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import PolynomialFeatures
from sklearn.pipeline import make_pipeline

---

## 🧪 Approach
1. Visualized trends using Power BI and calculated assessment averages with DAX
2. Identified a nonlinear pattern and selected a polynomial regression model
3. Trained the model on assessment data
4. Predicted STAAR scores and compared with actual scores
5. Measured prediction error to evaluate model accuracy

## 📈 Outcome
- Predictions closely mirrored actual STAAR performance
- Enabled early identification of students needing support
- Provided data-driven insights to guide instruction and reteach plans

## 🤖 Sample Code
python
Copy code
model = make_pipeline(PolynomialFeatures(degree=2), LinearRegression())
model.fit(X, y_dummy)

df['STAAR_Predicted'] = model.predict(X) * 100
df['Prediction Error'] = df['STAAR_Predicted'] - df['8th Grade STAAR']


## 🧩 Future Plans
- Apply model to all class periods for full predictive analysis
- Use benchmark predictions to inform mid-year interventions
- Present findings to administrators and teaching teams to support student growth

## 🔗 Let’s Connect
Feel free to explore the code and connect with me on LinkedIn to discuss educational data science, predictive modeling, or collaboration opportunities.

## Tags
#Python #Regression #PowerBI #EducationData #STAAR #MachineLearning
