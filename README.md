
# 🧠 MindBridge – AI-Powered Mental Health Assessment & Awareness Platform

<p align="center">
  <b>Bridging the Gap Between Mental Health Awareness and Technology</b>
</p>

<p align="center">
  A Machine Learning-powered platform designed to promote mental health awareness and provide preliminary mental health score predictions through intelligent data analysis.
</p>

---

## 📌 Table of Contents

- [About the Project](#-about-the-project)
- [Problem Statement](#-problem-statement)
- [Project Objectives](#-project-objectives)
- [Key Features](#-key-features)
- [Technology Stack](#-technology-stack)
- [System Architecture](#-system-architecture)
- [Machine Learning Implementation](#-machine-learning-implementation)
- [Backend Development](#-backend-development)
- [Frontend Development](#-frontend-development)
- [Project Workflow](#-project-workflow)
- [Project Structure](#-project-structure)
- [Installation and Setup](#-installation-and-setup)
- [API Integration](#-api-integration)
- [Model Details](#-model-details)
- [Challenges and Solutions](#-challenges-and-solutions)
- [Future Enhancements](#-future-enhancements)
- [Limitations](#-limitations)
- [Disclaimer](#-disclaimer)
- [Author](#-author)

---

## 🌟 About the Project

**MindBridge** is a technology-driven mental health awareness and assessment platform developed with the aim of making mental health awareness more accessible, especially among college students.

Mental health is an important part of overall well-being. However, many students experience stress, academic pressure, anxiety, and emotional challenges without having access to proper awareness or preliminary assessment resources.

MindBridge combines Web Development and Machine Learning to create a platform where users can provide assessment-related information and receive a predicted mental health score through a trained Machine Learning model.

The project integrates a React-based frontend with a Python FastAPI backend and a Machine Learning model built using Scikit-learn.

### Our Vision

To encourage mental health awareness through accessible technology and help individuals become more conscious of their mental well-being.

---

## ❗ Problem Statement

Mental health challenges among students are often overlooked due to:

- Lack of awareness about mental well-being.
- Academic pressure and stressful environments.
- Hesitation in discussing emotional difficulties.
- Limited access to preliminary assessment resources.
- Difficulty understanding personal mental well-being.

There is a need for an accessible digital platform that can support mental health awareness and provide an initial, data-driven assessment.

MindBridge aims to address this problem through an interactive web platform integrated with Machine Learning.

---

## 🎯 Project Objectives

1. Promote mental health awareness among students.
2. Develop an accessible and user-friendly mental health assessment platform.
3. Integrate Machine Learning for preliminary mental health score prediction.
4. Connect a trained ML model with a web application using REST APIs.
5. Demonstrate the practical application of Artificial Intelligence in the mental health domain.
6. Encourage users to pay attention to their mental well-being.

---

## ✨ Key Features

### 1. Mental Health Assessment
Provides an assessment interface where users can submit relevant information through the application.

### 2. Machine Learning-Based Prediction
Uses a trained Random Forest Regression model to generate a predicted mental health score based on input features.

### 3. Automated Data Processing
The Scikit-learn preprocessing pipeline prepares input data before passing it to the prediction model.

### 4. REST API Integration
FastAPI connects the frontend application with the Machine Learning model.

### 5. Interactive Web Interface
React provides the frontend interface through which users interact with the system.

### 6. Data-Driven Assessment
Uses Machine Learning predictions to support preliminary mental health awareness.

---

## 🛠️ Technology Stack

| Component | Technologies |
|---|---|
| Frontend | React.js |
| Frontend Build Tool | Vite |
| Programming Language | JavaScript |
| Markup | HTML5 |
| Styling | CSS3 |
| Backend | Python |
| Backend Framework | FastAPI |
| API Communication | REST API |
| Machine Learning | Scikit-learn |
| ML Algorithm | Random Forest Regressor |
| Data Processing | Pandas |
| Model Serialization | Joblib |
| Model Format | Pickle (.pkl) |
| Development Environment | VS Code |
| Version Control | Git & GitHub |

---

## 🏗️ System Architecture

MindBridge follows a frontend-backend-machine-learning architecture.

### Architecture Overview

```text
          USER
            |
            v
    REACT FRONTEND
            |
            v
       USER INPUT
            |
            v
      FASTAPI BACKEND
            |
            v
    INPUT DATA PROCESSING
            |
            v
    SKLEARN PIPELINE
            |
            v
       PREPROCESSOR
            |
            v
  RANDOM FOREST REGRESSOR
            |
            v
   PREDICTED MENTAL HEALTH
            |
            v
       API RESPONSE
            |
            v
      REACT FRONTEND
            |
            v
      DISPLAY RESULTS
```

### Architecture Explanation

**Step 1: User Interaction**

The user interacts with the React frontend and provides assessment-related information.

**Step 2: API Request**

The frontend sends the required information to the Python backend through an API request.

**Step 3: Data Processing**

FastAPI receives the input and prepares it for the Machine Learning model.

**Step 4: Model Prediction**

The trained Scikit-learn pipeline processes the input and generates a prediction using the Random Forest Regressor.

**Step 5: API Response**

The backend returns the prediction result to the frontend.

**Step 6: Result Display**

The frontend displays the received result to the user.

---

## 🤖 Machine Learning Implementation

Machine Learning is one of the core components of MindBridge.

The project uses a trained Machine Learning model to predict a mental health score based on assessment-related input features.

### Algorithm Used: Random Forest Regression

Random Forest Regression is an ensemble learning algorithm that combines multiple decision trees to generate a prediction.

Instead of relying on a single decision tree, it combines predictions from multiple trees to produce the final output.

### Why Random Forest?

- Handles complex relationships between input features.
- Combines multiple decision trees.
- Can model non-linear patterns.
- Supports regression-based prediction.
- Provides a practical approach for structured data.

### ML Model Pipeline

The trained model is stored in:

`Mental_Health_Model.pkl`

The model is loaded using Joblib.

The Scikit-learn Pipeline contains two major steps:

**1. Preprocessor**

- Processes input features.
- Applies the preprocessing operations learned during training.
- Prepares data for the prediction algorithm.

**2. Random Forest Regressor**

- Receives the processed input.
- Uses the trained decision trees.
- Generates the predicted mental health score.

### Model Pipeline Structure

```text
INPUT DATA
    |
    v
PREPROCESSOR
    |
    v
RANDOM FOREST REGRESSOR
    |
    v
PREDICTED SCORE
```

### Model Loading

The trained model is loaded using Joblib:

```python
import joblib

model = joblib.load("Mental_Health_Model.pkl")
```

### Prediction Process

The prediction pipeline follows these steps:

1. Receive input data.
2. Convert the input into the expected data format.
3. Pass the input to the trained pipeline.
4. Apply preprocessing.
5. Generate prediction using Random Forest.
6. Return the predicted score.

**Note:** The actual prediction performance depends on the training dataset, feature quality, preprocessing and model evaluation.

---

## ⚙️ Backend Development

The backend is developed using **Python and FastAPI**.

FastAPI provides REST API endpoints that allow the frontend to communicate with the Machine Learning model.

### Backend Responsibilities

- Receive input data from the frontend.
- Validate incoming requests.
- Load the trained ML model.
- Process assessment-related information.
- Generate predictions.
- Return responses in JSON format.

### Backend Technologies

- Python
- FastAPI
- Uvicorn
- Pandas
- Scikit-learn
- Joblib

### Running the Backend

The backend development server runs on:

`http://localhost:8001`

Run the following command:

```bash
uvicorn main:app --reload --port 8001
```

FastAPI documentation can be accessed at:

`http://localhost:8001/docs`

---

## 💻 Frontend Development

The frontend is developed using React.js and Vite.

React provides a component-based architecture for building interactive user interfaces.

### Frontend Responsibilities

- Display the application interface.
- Collect user assessment inputs.
- Communicate with the backend API.
- Send input data for prediction.
- Receive and display prediction results.

### Frontend Technologies

- React.js
- Vite
- JavaScript
- HTML5
- CSS3

### Running the Frontend

```bash
npm install
npm run dev
```

The Vite development server provides the local frontend URL in the terminal.

---

## 🔄 Project Workflow

The overall workflow of MindBridge is:

1. User opens the MindBridge application.
2. User interacts with the assessment interface.
3. User submits the required information.
4. Frontend sends the data to the FastAPI backend.
5. Backend validates and processes the input.
6. Machine Learning pipeline receives the input.
7. Preprocessor transforms the input.
8. Random Forest Regressor generates a prediction.
9. Backend returns the predicted score.
10. Frontend displays the result.

---

## 📂 Project Structure

The logical organization of the application is:

```text
MindBridge/
│
├── client/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── assets/
│   │   └── ...
│   │
│   ├── public/
│   ├── package.json
│   └── ...
│
├── ml-service/
│   ├── main.py
│   ├── Mental_Health_Model.pkl
│   └── ...
│
├── README.md
└── ...
```

Note: This is a logical project layout. Adjust it to match the actual folders and files in your repository.

---

## 🚀 Installation and Setup

Follow these steps to run the project locally.

### Prerequisites

Make sure you have installed:

- Python 3.10 or compatible version
- Node.js and npm
- Git
- Visual Studio Code

### Step 1: Clone the Repository

```bash
git clone https://github.com/neha-gupta887/S-02-Mental-Health-Awareness-Campaign-for-First-Year-Students.git
```

### Step 2: Navigate to the Project

```bash
cd S-02-Mental-Health-Awareness-Campaign-for-First-Year-Students
```

### Step 3: Configure the Backend

Navigate to the actual ML backend directory:

```bash
cd ml-service
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate the environment on Windows:

```bash
.venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install fastapi uvicorn pandas scikit-learn joblib
```

**Important:** Use the same compatible Scikit-learn version used to train and serialize the model. Install other dependencies required by your actual project.

### Step 4: Run the Backend

```bash
uvicorn main:app --reload --port 8001
```

### Step 5: Configure the Frontend

Open another terminal and navigate to the frontend directory:

```bash
cd client
```

Install dependencies:

```bash
npm install
```

Run the frontend:

```bash
npm run dev
```

The application will be available at the local URL displayed by Vite.

---

## 🔗 API Integration

The frontend and backend communicate through REST APIs.

### API Communication Flow

```text
React Frontend
      |
      | HTTP Request
      v
FastAPI Backend
      |
      | Model Prediction
      v
Machine Learning Model
      |
      | Prediction Result
      v
FastAPI Response
      |
      v
React Frontend
```

The API receives assessment-related input and returns the Machine Learning prediction.

The exact API endpoint, HTTP method, request schema and response format are defined in the backend source code.

---

## 📊 Model Details

| Parameter | Details |
|---|---|
| Model Type | Machine Learning |
| Learning Approach | Supervised Learning |
| Algorithm | Random Forest Regressor |
| Task | Regression |
| Model Pipeline | Scikit-learn Pipeline |
| Preprocessing | Preprocessor |
| Model Serialization | Joblib |
| Saved Model | Mental_Health_Model.pkl |
| Backend Integration | FastAPI |

### Model Evaluation

Model performance should be evaluated using appropriate regression metrics, such as:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

Actual evaluation values should be added after testing the trained model.

---

## 🧩 Challenges and Solutions

During development, several technical challenges were encountered.

### 1. Model Compatibility

**Challenge:** The saved Machine Learning model encountered compatibility issues when loaded in a different Scikit-learn environment.

**Solution:** Checked and aligned the installed Machine Learning library versions with the model's training environment.

### 2. Model Serialization

**Challenge:** Loading the trained model correctly into the backend.

**Solution:** Used Joblib to load the serialized Scikit-learn Pipeline.

### 3. Backend Integration

**Challenge:** Connecting the Machine Learning model with the web application.

**Solution:** Used FastAPI to expose prediction functionality through REST APIs.

### 4. Prediction Quality

**Challenge:** The model did not always detect stress-related patterns as expected.

**Future Direction:** Improve data quality, feature selection, model evaluation and training methodology.

---

## 🔮 Future Enhancements

MindBridge can be further improved through the following enhancements:

- Improve Machine Learning model performance.
- Use larger and more representative datasets.
- Explore additional Machine Learning algorithms.
- Add personalized mental wellness recommendations.
- Introduce user authentication and secure profiles.
- Add assessment history and progress tracking.
- Develop interactive analytics dashboards.
- Improve model explainability.
- Enhance accessibility and user experience.
- Deploy the application for wider accessibility.

---

## ⚠️ Limitations

- Predictions depend on the quality and representativeness of the training data.
- Machine Learning predictions may not always be accurate.
- The system does not replace professional psychological assessment.
- The model should not be used independently for medical decisions.
- The results should be interpreted as preliminary assessment outputs only.

---

## 🔒 Privacy and Data Considerations

Mental health-related information is sensitive.

A production-ready version should implement:

- Secure handling of user information.
- Appropriate data access controls.
- Encryption of sensitive information.
- User consent before collecting information.
- Responsible data retention policies.

---

## ⚠️ Disclaimer

MindBridge is an educational and awareness-oriented project developed to demonstrate the application of Machine Learning in the mental health domain.

It is not a medical diagnostic tool and does not provide clinical diagnoses or replace professional mental health advice.

Users experiencing mental health difficulties should seek support from qualified healthcare professionals.

---

## 👩‍💻 Author

### Neha Gupta

Computer Science Engineering Student

**Areas of Interest:**
- Artificial Intelligence
- Machine Learning
- Web Development
- Problem Solving
- Software Development

### Connect With Me

- GitHub: https://github.com/neha-gupta887
- LinkedIn: https://www.linkedin.com/in/neha-gupta-82201a360/

---

## ⭐ Support

If you find this project interesting, consider giving the repository a ⭐ star on GitHub.

Your support and feedback are appreciated!

---

<p align="center">
  <b>MindBridge – Technology with a Purpose. Building Awareness, One Step at a Time.</b>
</p>
