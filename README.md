# 💓 Heart Disease Predictor

> A full-stack predictive health analytics web application that assesses cardiovascular disease risk using a Logistic Regression model — with real-time risk prediction, feature analysis visualizations, and a Flask REST API integrated with a vanilla HTML/CSS/JavaScript frontend.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Status](https://img.shields.io/badge/Status-Completed-1D9E75?style=flat)

---

## 📌 Overview

Heart Disease Predictor is a full-stack predictive health analytics application that assesses a patient's cardiovascular disease risk from clinical health indicators. The trained Logistic Regression model is deployed via a Flask REST API and integrated with a clean, mobile-responsive vanilla JavaScript frontend — no heavy frameworks required.

---

## ✨ Features

| Feature | Description |
|---|---|
| ❤️ Cardiovascular Risk Prediction | Logistic Regression assesses heart disease risk from patient indicators |
| 📊 Feature Analysis Visualizations | Risk factor distributions and feature importance ranking charts |
| ⚡ Real-Time Risk Assessment | Instant predictions with probability score from health parameter form |
| 🔌 Flask REST API | Lightweight API with input validation, preprocessing & JSON responses |
| 🌐 Vanilla JS Frontend | Mobile-responsive UI with pure HTML5, CSS3, JavaScript — no framework |
| 🔬 Statistical Analysis | Outlier detection, correlation analysis on clinical dataset |

---

## 🧠 ML Pipeline

```
Dataset → EDA & Stats → Preprocessing → Model Training → Flask API → HTML/CSS/JS Frontend
(Clinical)  (Outliers,    (Scaling,      (Logistic Reg,   (REST)      (Real-time
             Corr.)        Encoding)      Cross-val.)                   Predictions)
```

---

## 📈 Model Performance

| Metric | Score |
|---|---|
| Accuracy | ~85% |
| Precision | High (low false positives) |
| Recall | High (low false negatives) |
| AUC-ROC | ~0.91 |

> Update with your actual evaluation results from the notebook.

---

## 🏥 Input Parameters

| Parameter | Type | Description |
|---|---|---|
| `age` | integer | Patient age in years |
| `sex` | binary | 1 = male, 0 = female |
| `chest_pain_type` | categorical | Type of chest pain (0–3) |
| `resting_bp` | float | Resting blood pressure (mm Hg) |
| `cholesterol` | float | Serum cholesterol (mg/dl) |
| `fasting_blood_sugar` | binary | > 120 mg/dl = 1, else 0 |
| `rest_ecg` | categorical | Resting ECG results (0–2) |
| `max_heart_rate` | float | Maximum heart rate achieved |
| `exercise_angina` | binary | Exercise-induced angina (1/0) |
| `st_depression` | float | ST depression induced by exercise |
| `st_slope` | categorical | Slope of peak exercise ST segment |
| `num_vessels` | integer | Number of major vessels (0–3) |

---

## 🛠️ Tech Stack

**ML & Data:** Python · scikit-learn · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook
**Backend:** Flask · REST API
**Frontend:** HTML5 · CSS3 · JavaScript (Vanilla)

---

## 📁 Folder Structure

```
heart-disease-predictor/
│
├── backend/
│   ├── app.py
│   ├── model/
│   │   ├── train_model.py
│   │   └── heart_disease_model.pkl
│   ├── notebooks/
│   │   └── eda_analysis.ipynb
│   └── requirements.txt
│
└── frontend/
    ├── index.html
    ├── css/
    │   └── style.css
    ├── js/
    │   ├── main.js
    │   ├── api.js
    │   └── charts.js
    └── assets/
```

---

## ▶️ How to Run

### 1. Clone the repository
```bash
git clone https://github.com/Darshan7484/heart-disease-predictor.git
cd heart-disease-predictor
```

### 2. Install Python dependencies
```bash
cd backend
pip install -r requirements.txt
```

### 3. Train the model (or use pre-trained .pkl)
```bash
python model/train_model.py
```

### 4. Start the Flask API
```bash
python app.py
# API runs at http://localhost:5000
```

### 5. Open the frontend
```bash
# Open frontend/index.html in your browser
# Or use Live Server extension in VS Code
```

---

## 🔗 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/predict` | Takes health parameters, returns risk prediction |
| GET | `/health` | Health check for the API server |

### Sample Request
```json
POST /predict
{
  "age": 55,
  "sex": 1,
  "chest_pain_type": 2,
  "resting_bp": 140,
  "cholesterol": 250,
  "fasting_blood_sugar": 0,
  "max_heart_rate": 150,
  "exercise_angina": 1
}
```

### Sample Response
```json
{
  "prediction": "High Risk",
  "probability": 0.82,
  "status": "success"
}
```

---

## 📸 Screenshots

> Add screenshots of the input form, risk result, and feature importance charts here.

---

## 🔮 Future Improvements

- Add Random Forest and XGBoost models for comparison
- SHAP values for prediction explainability
- Deploy on Render with live demo link
- Patient history tracking with SQLite/MySQL

---

## 👤 Author

**Darshan S**
- GitHub: [@Darshan7484](https://github.com/Darshan7484)
- LinkedIn: [darshan-s-75893b24b](https://linkedin.com/in/darshan-s-75893b24b)
- Email: darshandarahu044@gmail.com

---

## 📜 License

This project is licensed under the MIT License.
