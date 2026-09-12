# ML-Assisted Cloud Service Selection Using QoS with AHP-TOPSIS

## 📌 Project Overview

This project develops an intelligent cloud service selection framework that evaluates and ranks cloud services using multiple Quality of Service (QoS) parameters.

The system combines **AHP (Analytic Hierarchy Process)** for calculating criteria weights, **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** for service ranking, and **Random Forest Regression** for QoS score approximation.

---

## 🎯 Problem Statement

Cloud services have different performance characteristics such as latency, response time, bandwidth, throughput, and resource utilization.

Selecting the most suitable service becomes difficult when multiple QoS parameters need to be considered simultaneously.

This project provides a systematic multi-criteria decision-making approach to rank cloud services and recommend high-performing services.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Joblib
* Google Colab

---

## 📊 Dataset

The dataset contains **1,000 cloud service records and 18 attributes**.

Important parameters include:

* CPU Utilization
* Memory Usage
* Storage Usage
* Network Bandwidth
* Service Latency
* Response Time
* Throughput
* Load Balancing
* QoS Score
* Cloud Provider
* Service Type
* Edge Node

---

## 🔄 Methodology

```text
Dataset
   ↓
Data Cleaning & Exploration
   ↓
QoS Feature Selection
   ↓
AHP
Criteria Weight Calculation
   ↓
TOPSIS
Cloud Service Ranking
   ↓
Random Forest
QoS Score Approximation
   ↓
Model Evaluation
MAE | RMSE | R²
   ↓
Service Recommendation
```

---

## ⚖️ AHP Criteria Weights

AHP was used to determine the relative importance of the selected QoS criteria.

| Criterion         | Weight |
| ----------------- | -----: |
| Throughput        | 0.2295 |
| Network Bandwidth | 0.1864 |
| Service Latency   | 0.1629 |
| Response Time     | 0.1393 |
| Load Balancing    | 0.0985 |
| CPU Utilization   | 0.0719 |
| Memory Usage      | 0.0609 |
| Storage Usage     | 0.0507 |

**Throughput was the most influential criterion with a weight of 0.2295.**

---

## 🏆 TOPSIS Results

TOPSIS was used to rank cloud services based on their distance from the ideal best and ideal worst solutions.

| Rank | Service ID | Service Type | Cloud Provider | TOPSIS Score |
| ---: | ---------- | ------------ | -------------- | -----------: |
|    1 | S0281      | Storage      | Google Cloud   |       0.8829 |
|    2 | S0875      | Compute      | IBM            |       0.8657 |
|    3 | S0290      | Database     | Azure          |       0.8376 |
|    4 | S0107      | Network      | AWS            |       0.8316 |
|    5 | S0439      | Database     | Google Cloud   |       0.8156 |

### 🥇 Best Recommended Service

**Service ID:** S0281
**Service Type:** Storage
**Cloud Provider:** Google Cloud
**TOPSIS Score:** 0.8829

---

## 🤖 Random Forest Model

A Random Forest Regression model was trained using the selected QoS features to approximate the TOPSIS-derived service scores.

### Model Performance

| Metric | Result |
| ------ | -----: |
| MAE    | 0.0185 |
| RMSE   | 0.0233 |
| R²     | 0.9649 |

The model achieved an **R² score of 0.9649** for approximating the TOPSIS-derived scores.

> Note: The Random Forest model uses the same QoS features involved in the TOPSIS calculation. Therefore, the model performance represents approximation of the decision scores rather than independent real-world QoS forecasting.

---

## 📈 Project Features

* QoS data analysis
* AHP-based criteria weighting
* TOPSIS-based cloud service ranking
* Random Forest regression
* Model evaluation using MAE, RMSE and R²
* Feature importance analysis
* Cloud provider comparison
* Service type comparison
* QoS correlation analysis
* Automated service recommendation
* Trained model export using Joblib

---

## 📁 Project Structure

```text
cloud-service-selection-qos/
│
├── Cloud_Service_Selection_Using_QoS.ipynb
├── README.md
├── cloud_qos_random_forest.pkl
├── cloud_service_ranking.csv
└── multi_cloud_service_dataset.csv
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/akankshyapradhan2004-pixel/cloud-service-selection-qos.git
```

### 2. Open the notebook

Open:

```text
Cloud_Service_Selection_Using_QoS.ipynb
```

in Google Colab or Jupyter Notebook.

### 3. Install dependencies

```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib
```

### 4. Run the notebook

Upload or use the included dataset and execute the notebook cells sequentially.

---

## 🔮 Future Improvements

* Real-time cloud QoS monitoring
* Additional cost and security criteria
* Real-time QoS prediction
* REST API deployment
* Interactive web dashboard
* Docker-based deployment
* Integration with cloud monitoring systems

---

## 👩‍💻 Author

**Akankshya Pradhan**

B.Tech — Computer Science and Artificial Intelligence & Machine Learning

---

## 📌 Conclusion

This project demonstrates how **AHP, TOPSIS and Machine Learning** can be combined to support intelligent cloud service selection.

The AHP-TOPSIS framework provides a transparent ranking mechanism, while Random Forest provides a machine-learning-based approximation of the resulting service scores.

The framework can be extended into a real-time cloud service recommendation and deployment system.
