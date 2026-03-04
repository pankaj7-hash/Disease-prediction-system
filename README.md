# 🩺 AI Disease Prediction System

An end-to-end Machine Learning system that predicts possible diseases based on selected symptoms.

This project demonstrates:

* ✅ 120+ structured symptoms
* ✅ 40+ medically mapped diseases
* ✅ Class imbalance handling (SMOTE)
* ✅ Random Forest ML model
* ✅ Feature importance visualization
* ✅ FastAPI backend
* ✅ Streamlit interactive frontend
* ✅ Interview-ready architecture

---

# 🚀 Project Demo

## 🖥️ Streamlit UI

![Streamlit UI Screenshot](assets/streamlit_ui.png)

## 📊 Prediction Confidence Chart

![Prediction Chart](assets/prediction_chart.png)

## 📈 Feature Importance

![Feature Importance](assets/feature_importance.png)

## 📡 FastAPI Swagger Docs

![Swagger API](assets/swagger_docs.png)

> 📌 Place your screenshots inside an `assets/` folder with the same file names.

---

# 🏗️ System Architecture

```
User (Streamlit UI)
        │
        ▼
Symptom Selection
        │
        ▼
Prediction Module (src/predict.py)
        │
        ▼
Trained RandomForest Model (.pkl)
        │
        ▼
Top-3 Disease Predictions
        │
        ▼
Confidence Visualization
```

For API usage:

```
Client → FastAPI → ML Model → JSON Response
```

---

# 📂 Project Structure

```
Disease-prediction-system/
│
├── app/
│   └── app.py                 # Streamlit frontend
│
├── api/
│   └── main.py                # FastAPI backend
│
├── data/
│   └── disease_dataset.csv    # Structured dataset
│
├── model/
│   ├── disease_model.pkl
│   ├── label_encoder.pkl
│   └── feature_names.pkl
│
├── src/
│   ├── train.py
│   ├── predict.py
│   ├── generate_dataset.py
│   └── feature_importance.py
│
├── notebooks/
│   ├── eda.ipynb
│   └── model_training.ipynb
│
├── requirements.txt
└── README.md
```

---

# 🧠 Machine Learning Details

## Model Used

* Random Forest Classifier
* 300 trees
* Max depth: 20
* SMOTE for class imbalance handling

## Why Random Forest?

* Handles high-dimensional symptom data well
* Robust to noise
* Provides feature importance
* Good performance for multi-class classification

---

# 📊 Model Pipeline

1. Load dataset
2. Encode disease labels
3. Handle class imbalance using SMOTE
4. Train RandomForest model
5. Save model artifacts
6. Use probability-based Top-3 prediction ranking

---

# 🏥 Diseases Covered

Includes diseases across multiple body systems:

* Respiratory
* Digestive
* Circulatory
* Nervous
* Urinary
* Skeletal
* Muscular
* Endocrine
* Reproductive
* Lymphatic
* Integumentary
* Exocrine

Total: **40+ diseases**

---

# 🔮 Prediction Output Format

Example JSON response:

```json
{
  "top_predictions": [
    {"disease": "Asthma", "confidence_percent": 82.4},
    {"disease": "Pneumonia", "confidence_percent": 10.2},
    {"disease": "Bronchitis", "confidence_percent": 5.3}
  ]
}
```

---

# 📈 Feature Importance

The system extracts top important symptoms influencing predictions using:

```
model.feature_importances_
```

This helps explain:

* Which symptoms matter most
* Model interpretability
* Clinical reasoning transparency

---

# 🖥️ How To Run The Project

## 1️⃣ Clone Repository

```
git clone <your-repo-url>
cd Disease-prediction-system
```

## 2️⃣ Install Dependencies

```
pip install -r requirements.txt
```

## 3️⃣ Train Model

```
python src/train.py
```

## 4️⃣ Run Streamlit App

```
streamlit run app/app.py
```

## 5️⃣ Run FastAPI Backend

```
uvicorn api.main:app --reload
```

Open:

```
http://127.0.0.1:8000/docs
```

---

# 🧪 Example Use Case

Select symptoms:

* Fever
* Cough
* Chest pain
* Fatigue

System returns:

* Top 3 predicted diseases
* Confidence percentage
* Visual bar chart

---

# 🎯 Explanation (Short Version)

> This project is a multi-class disease prediction system built using Random Forest with SMOTE for class imbalance handling.
> It includes structured symptom-disease mapping, probability-based ranking, and a full-stack implementation using FastAPI and Streamlit.
> The model also provides feature importance for interpretability.

---

# 📦 Requirements

```
pandas
scikit-learn
imbalanced-learn
matplotlib
streamlit
fastapi
uvicorn
joblib
```

---

# 🔥 Future Improvements

* Cross-validation
* Hyperparameter tuning
* XGBoost comparison
* Docker deployment
* Cloud hosting (Render / AWS)
* User authentication
* Disease description explanation panel

---

# 👨‍💻 Author

**Pankaj Mahure**

AI / ML Enthusiast
Building real-world healthcare ML systems.

---

# ⚠️ Disclaimer

This system is for educational purposes only.
It does not replace professional medical diagnosis.

---

# ⭐ If You Like This Project

Give it a star on GitHub and connect for collaboration!
