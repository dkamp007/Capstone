# 🏦 Loan Approval Predictor Bot 🤖

## 🚀 Overview

This Streamlit-based web application helps users **predict whether their loan application is likely to be approved or rejected** based on their financial and demographic information. Built as a Capstone Project, this bot uses a **pre-trained machine learning model** (Logistic Regression with SMOTE for class balancing) and natural language processing to extract insights from user inputs and provide meaningful predictions.

The app also uses **OpenAI's LLM** to explain the model’s decision in plain English, making it both intelligent and user-friendly.

---

## ✨ Features

- 🔍 **Loan Approval Prediction** using a pre-trained ML model.
- 🧠 **NLP-based Input Parsing**: Enter financial info in natural language, and the app extracts key features automatically.
- 📊 **Loan Eligibility Calculator**: Get insights into how much loan you can afford based on your income and EMI.
- 📈 **Dynamic Visuals**: Interactive UI built with Streamlit for a smooth user experience.
- 🤖 **Explainable AI**: Model decisions explained using OpenAI’s language model.
- 📦 **Categorical Feature Encoding**: All categorical inputs are automatically label-encoded to match model expectations.
- 🏗️ **Box-Cox Transformation**: Applied on income feature for better model performance.

---

## 🧠 Tech Stack

- **Frontend & App**: Streamlit
- **Machine Learning**: Scikit-learn (`Logistic Regression` with SMOTE)
- **NLP**: spaCy (`en_core_web_sm`)
- **LLM Integration**: OpenAI GPT via `langchain`
- **Model Deployment**: GitHub-hosted `.joblib` model file
- **Libraries**: `pandas`, `numpy`, `joblib`, `requests`, `spacy`, `streamlit`, `openai`, `langchain`

---

## 📂 Directory Structure

```
Loan-Approval-Predictor/
├── Loan_app.py # Main Streamlit app script
├── Capstone_PreProcess_DKP_Final.ipynb # Preprocessed data
├── Capstone_ML_Modelling_DKP-Final-Copy2.ipynb # ML model training
├── Logistic2_Smote_Model.joblib # Pre-Trained model (auto-downloaded)
├── README.md # Project overview
└── requirements.txt # Python dependencies
```
---

## 🔧 Setup Instructions

**1.** Clone the repository

```bash
git clone https://github.com/dkamp007/Capstone.git
cd Capstone
```

**2.** Install Dependencies
```bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

**3.** Set your OpenAI API Key

Create a `.streamlit/secrets.toml` file:
```toml
apikey = "your_openai_api_key"
```

**4.** Run the app
```bash
streamlit run Loan_app.py
```

Check out the [webapp!](https://dkamp007-capstone-loan-app-ejtmmg.streamlit.app/)
