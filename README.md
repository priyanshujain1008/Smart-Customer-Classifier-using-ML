# 🤖 Smart Classifier

An intelligent machine learning web app built with **Streamlit** that automatically classifies or clusters customers based on their purchasing behavior, demographics, and spending patterns using **KMeans Clustering**.

---

## 📋 Project Overview

**Smart Classifier** is an intelligent ML model that analyzes customer data to group users with similar habits, preferences, and spending patterns.  
It helps businesses create targeted marketing strategies, improve engagement, and make data-driven decisions.

---

## 🚀 Features
- Simple and interactive Streamlit interface  
- Predicts customer cluster using a trained ML model  
- Scaler and model loaded via Joblib  
- Real-time data input and instant results  

---

## 🧱 Tech Stack
- Python 3.13+
- Streamlit
- Pandas
- NumPy
- Scikit-learn
- Joblib

---

## ⚙️ How It Works

### 1️⃣ Model Training (`analysis_model.ipynb`)
- Load dataset and explore features  
- Apply preprocessing and scaling  
- Train **KMeans clustering model**  
- Save trained model and scaler as `.pkl` files  

### 2️⃣ Web App (`segmentation.py`)
- Load saved model and scaler  
- Collect user data (Age, Income, Purchases, etc.)  
- Scale and classify input data  
- Display predicted customer cluster  

---

## ▶️ Run the App
```bash

  Smart Classifier/
│
├── analysis_model.ipynb        # Model training and analysis
├── segmentation.py             # Streamlit web app
├── kmeans_model.pkl            # Saved model
├── scaler.pkl                  # Saved feature scaler
├── requirements.txt            # Dependencies
└── README.md                   # Documentation


📊 Example Features

Age
Income
Total_Spending
NumWebPurchases
NumStorePurchases
NumWebVisitsMonth
Recency

🧩 Model Insights

Each cluster represents a customer segment:
Cluster 0: Loyal high-value customers
Cluster 1: Average spenders
Cluster 2: Occasional or new buyers

pip install -r requirements.txt
streamlit run segmentation.py
