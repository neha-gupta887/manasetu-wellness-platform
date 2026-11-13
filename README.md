
# 🧠 MindBridge – Mental Health Awareness & Prediction System

MindBridge is a Machine Learning-powered mental health assessment platform designed to promote mental health awareness among students. It combines web development and Machine Learning to provide preliminary mental health score predictions based on user responses.

## 🚀 Features

- Interactive mental health assessment
- Machine Learning-based mental health score prediction
- Random Forest Regression model
- REST API integration using FastAPI
- User-friendly web interface
- Mental health awareness and support

## 🛠️ Tech Stack

**Frontend**
- React.js
- Vite
- JavaScript
- HTML & CSS

**Backend**
- Python
- FastAPI
- REST APIs

**Machine Learning**
- Scikit-learn
- Random Forest Regressor
- Pandas
- Joblib

## 🧠 Machine Learning Model

The project uses a trained Scikit-learn Pipeline stored in `Mental_Health_Model.pkl`.

The pipeline consists of:

1. **Preprocessor:** Processes input data.
2. **Random Forest Regressor:** Predicts the mental health score.

The model is loaded using Joblib and integrated with the FastAPI backend.

## ⚙️ Installation & Setup

### 1. Clone Repository

```bash
git clone https://github.com/neha-gupta887/S-02-Mental-Health-Awareness-Campaign-for-First-Year-Students.git
```

### 2. Backend Setup

```bash
cd ml-service
pip install fastapi uvicorn pandas scikit-learn joblib
```

### 3. Run Backend

```bash
uvicorn main:app --reload --port 8001
```

Backend runs at:

`http://localhost:8001`

### 4. Frontend Setup

Open another terminal:

```bash
cd client
npm install
npm run dev
```

## 🔮 Future Enhancements

- Improve prediction accuracy
- Personalized mental wellness recommendations
- User authentication
- Mental health progress tracking
- Advanced analytics dashboard

## ⚠️ Disclaimer

MindBridge is an educational project for mental health awareness and preliminary assessment. It does not provide medical diagnoses or replace professional mental health advice.

## 👩‍💻 Developer

**Neha Gupta**

BE Computer Science Engineering

- GitHub: [neha-gupta887](https://github.com/neha-gupta887)
- LinkedIn: [Neha Gupta](https://www.linkedin.com/in/neha-gupta-82201a360/)

---

⭐ If you like this project, don't forget to give it a star!
