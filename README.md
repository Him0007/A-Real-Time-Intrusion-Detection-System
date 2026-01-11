# 🔒 A Real-Time Intrusion Detection System Using High-Performance Ensemble Machine Learning

## 📌 Overview
With the rapid growth of network-based applications, modern networks are increasingly exposed to sophisticated cyber threats such as denial-of-service attacks, probing, brute-force attempts, and malware propagation. Traditional signature-based Intrusion Detection Systems (IDS) struggle to detect unknown or evolving attacks and often fail in real-time environments.

This project presents a **Real-Time Intrusion Detection System (IDS)** that leverages **high-performance ensemble machine learning techniques** to accurately identify malicious network traffic with low latency. The system captures live network packets, extracts flow-based features, and classifies traffic as **Normal** or **Attack** using multiple machine learning models combined through an ensemble strategy.

---

## 🎯 Objectives
- To design a real-time IDS capable of monitoring live network traffic  
- To extract meaningful flow-level features from raw packets  
- To apply ensemble machine learning for improved detection accuracy  
- To provide a real-time visualization dashboard for network monitoring  
- To minimize false positives while maintaining high detection performance  

---

## 🚀 Key Features
- 📡 Live packet capture from network interfaces  
- 🧠 Machine learning-based attack detection  
- 🔀 Ensemble learning using Stacking Classifier  
- 📊 Real-time web dashboard for monitoring traffic  
- ⚡ Low-latency flow-based analysis  
- 🔍 Supports TCP and UDP traffic  

---

## 🧠 Machine Learning Approach
The system employs multiple supervised machine learning models trained on labeled network traffic data. To enhance performance and robustness, an **ensemble stacking approach** is used.

### Models Used
- Random Forest  
- XGBoost  
- LightGBM  
- Stacking Ensemble (Final Decision Model)  

### Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- ROC-AUC  

Class imbalance is handled using **SMOTE (Synthetic Minority Over-sampling Technique)**.

---

## 🏗️ System Architecture
1. **Packet Capture**  
   - Live packets are captured using PyShark from the network interface  

2. **Flow Generation**  
   - Packets are grouped into bidirectional flows  

3. **Feature Extraction**  
   - Flow-based statistical features are computed  

4. **Preprocessing**  
   - Feature scaling and alignment with trained models  

5. **Prediction Engine**  
   - Ensemble ML models classify traffic  

6. **Visualization**  
   - Results are displayed on a real-time web dashboard  

---

## 🛠️ Technologies Used
- Python  
- Flask  
- PyShark  
- Scikit-learn  
- XGBoost  
- LightGBM  
- HTML, CSS, JavaScript  
- Ensemble Machine Learning  

---

## 📂 Project Structure
Real-Time-Intrusion-Detection-System/
│
├── src/
│ ├── app.py # Real-time IDS engine
│ ├── flow_features.py # Flow feature extraction
│ └── train_models.py # Model training pipeline
│
├── web/
│ └── dashboard.html # Real-time monitoring dashboard
│
├── trained_models/
│ ├── *.pkl # Trained ML models
│ ├── scaler.pkl
│ └── model_metrics.csv
│
├── docs/ # Project documentation
│
├── screenshots/ # Dashboard images
│
├── requirements.txt
├── .gitignore
├── LICENSE
└── README.md

---

## ⚙️ Installation

### Prerequisites
- Python 3.8 or higher  
- Administrator / root privileges (for packet capture)  

### Steps
```bash
git clone https://github.com/your-username/real-time-intrusion-detection-system.git
cd real-time-intrusion-detection-system
pip install -r requirements.txt
