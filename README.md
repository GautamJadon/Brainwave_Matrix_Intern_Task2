# Brainwave_Matrix_Intern_Task2
Credit Card Fraud Detection 🚀

Overview

This project implements a Credit Card Fraud Detection System using Machine Learning and Deep Learning techniques. It utilizes a Random Forest Classifier and an Autoencoder-based Anomaly Detection model to identify fraudulent transactions. The system is deployed using Flask and Ngrok for easy access.

Features

Random Forest Model for supervised fraud classification.

Autoencoder-based Anomaly Detection for unsupervised fraud detection.

Flask API for real-time fraud prediction.

Ngrok Integration to make the API publicly accessible.

Dataset

The project uses a dataset with credit card transactions, containing 30 numerical features derived from PCA transformation, including a Class label where:

0 → Legitimate Transaction

1 → Fraudulent Transaction

Tech Stack 🛠️

Python (NumPy, Pandas, Scikit-Learn, TensorFlow, Flask)

Machine Learning (Random Forest, StandardScaler)

Deep Learning (Autoencoder using TensorFlow/Keras)

Deployment (Flask, Ngrok)

Installation & Setup

1️⃣ Clone the repository

git clone https://github.com/yourusername/credit-card-fraud-detection.git
cd credit-card-fraud-detection

2️⃣ Install dependencies

pip install -r requirements.txt

3️⃣ Train and Save Models

Run the following scripts to train the models and save them:

python train_rf.py  # Train Random Forest Model
python train_autoencoder.py  # Train Autoencoder Model

4️⃣ Start the Flask API

python app.py

5️⃣ Expose the API using Ngrok

ngrok http 5000

Copy the public URL and use it to make API requests.

API Endpoints 📡

POST /predict

Description: Predicts if a transaction is fraudulent or not.

Request Body (JSON):

{
  "features": [0.1, -1.2, 2.3, ..., 0.5]  # Example transaction features
}

Response:

{
  "RandomForest_Prediction": 0,
  "Anomaly_Detection_Prediction": 1
}

Future Improvements 🛠️

Implement a hybrid decision-making strategy combining both models.

Use additional feature engineering techniques to improve accuracy.

Deploy the model using FastAPI for better performance.
