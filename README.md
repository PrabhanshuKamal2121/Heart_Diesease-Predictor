# ❤️ Heart Disease Predictor

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn)
![Joblib](https://img.shields.io/badge/Joblib-FFDB3A?style=flat-square)

> A warm-gradient, responsive Streamlit app for instant heart disease risk prediction.

---

## 🎯 Table of Contents

- [Tech Stack](#-tech-stack)
- [Features](#-features)
- [About the Project](#-about-the-project)
- [How It Works](#-how-it-works)
- [Architecture](#-architecture)
- [Model & Data](#-model--data)
- [Quick Start](#-quick-start)
- [Contact](#-contact)
- [Disclaimer](#️-disclaimer)

---

## 🛠️ Tech Stack

| Layer                | Tools & Libraries                                       |
|-------------------|------------------------------------------------------------|
| **Core**          | Python, Streamlit                                          |
| **Data**          | Pandas, scikit-learn, Joblib                               |
| **Styling**       | Custom CSS via `st.markdown`                               |
| **Visualization** | Streamlit widgets (slider, selectbox, number_input)        |
| **Deployment**    | Local / Streamlit Cloud                                    |


---

## ✨ Features

- **Interactive Form**: Two-column layout for personal info, vitals, and lab data.  
- **Instant Prediction**: Logistic regression with one-hot encoding and scaling.  
- **Warm Theme**: Dark background with gold–amber gradients and modern card UI.  
- **Clear Feedback**: Styled alerts: ✅ Low Risk, ⚠️ High Risk.  
- **Mobile‑Friendly**: Fully responsive design.

---

## 💡 About the Project

**Heart Disease Predictor** is a lightweight, user‑friendly web application built with Streamlit that leverages a pre‑trained logistic regression model to estimate a patient’s risk of heart disease in seconds. Designed for clinicians, students, and health enthusiasts alike, this tool offers:

- **Intuitive UI**  
  A two‑column form layout groups demographic information, clinical assessments, and vital signs into clearly labeled “cards,” making data entry fast and error‑free.

- **Robust Modeling**  
  Under the hood, the app uses a logistic regression model trained on standardized clinical datasets. Inputs are one‑hot encoded to capture categorical variables (sex, chest pain type, ECG patterns, etc.) and scaled so each feature contributes appropriately to the prediction.

- **Instant Feedback**  
  As soon as you click **Predict**, the app displays a styled alert:
  - ✅ **Low Risk** (green–apricot background)  
  - ⚠️ **High Risk** (red–apricot background)  
  Each result includes a brief recommendation to either maintain healthy habits or seek professional care.

- **Custom Warm Theme**  
  A dark, warm‑gradient background accented with gold and amber highlights gives the app a professional yet inviting look. Smooth animations and hover effects on input cards enhance the interactive experience without sacrificing performance.

- **Mobile-Responsive Design**  
  All UI components automatically adjust for screen size, ensuring the app remains usable on tablets and smartphones.

### 🔍 How It Works

1. **User Input**  
   Collects 11 key features: 
   - Age, Sex  
   - Chest Pain Type, Resting ECG, Exercise Angina, ST Slope  
   - Resting BP, Cholesterol, Fasting Blood Sugar, Max HR, Oldpeak  
2. **Preprocessing**  
   - **One‑Hot Encoding**: Converts categorical fields into binary indicator columns.  
   - **Scaling**: Applies a saved `StandardScaler` so that continuous features share the same scale as the training data.  
3. **Prediction**  
   - Feeds the processed inputs into the saved logistic regression model (`logistic_regression_heart.pkl`).  
   - Outputs a binary class (0 = low risk, 1 = high risk).  
4. **Result Rendering**  
   - Displays the prediction with a styled alert box and personalized recommendation.  

### 🏗️ Architecture

```bash
Heart-Disease-Predictor/
├── app.py                        # Streamlit app with warm CSS theme
├── logistic_regression_heart.pkl # Trained model
├── scaler.pkl                    # Standard scaler
├── columns.pkl                   # Model feature columns
├── requirements.txt              # Dependency list
└── README.md                     # Project overview (this file)
```

### 📈 Model & Data

- **Model**: Logistic Regression  
- **Training Data**: Standard open‑source heart disease datasets (Cleveland, Framingham, etc.)  
- **Performance**: ~80–85% accuracy on hold‑out test sets  

---

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/PrabhanshuKamal2121/Heart-Disease-Predictor.git
cd Heart-Disease-Predictor

# Install dependencies
pip install -r requirements.txt

# Launch the app
streamlit run app.py

---

## 📧 Contact

Made by **PrabhanshuKamal**  
For any questions or collabs → [prabhanshukamal2121@gmail.com]  
GitHub: [github.com/PrabhanshuKamal2121](https://github.com/PrabhanshuKamal2121)

---

### ⚖️ Disclaimer

This app is **for educational use only**. It is not a substitute for professional medical advice, diagnosis, or treatment. Always consult a qualified healthcare provider for medical recommendations.
