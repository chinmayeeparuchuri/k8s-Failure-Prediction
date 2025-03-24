#  Kubernetes Failure Prediction using AI/ML

## 📌 Project Overview
This project aims to predict failures in Kubernetes clusters using advanced AI/ML techniques. By analyzing system logs and performance metrics, we build a highly optimized **LightGBM** model to detect potential failures such as:

- ✅ **Pod crashes**
- ✅ **Resource bottlenecks**
- ✅ **Network failures**

This model enables proactive issue resolution, reducing downtime and improving cluster reliability.

---

## 📁 Project Structure

## 📁 Project Structure

```
K8S_FAILURE_PREDICTION
├── data
│   ├── assuremoss_dataset                # Contains different elastic datasets from various timeframes
│   │   ├── elastic_february2022_data.csv
│   │   ├── elastic_may2021_benign_data.csv
│   │   ├── elastic_may2021_malicious_data.csv
│   │   ├── elastic_may2022_data.csv
│   │   ├── README.md                      # Description of dataset contents
│   ├── features                           # Extracted features from datasets for model input
│   │   ├── features_processed_elastic_february2022_data.csv
│   │   ├── features_processed_elastic_may2021_benign_data.csv
│   │   ├── features_processed_elastic_may2021_malicious_data.csv
│   │   ├── features_processed_elastic_may2022_data.csv
│   │   ├── features_processed_TestJMeterData.csv
│   │   ├── features_processed_TestK8sData.csv
│   │   ├── features_processed_TrainData.csv
│   ├── horizontal_scaling_dataset         # Contains horizontal scaling data for cluster behavior analysis
│   │   ├── TestJMeterData.csv
│   │   ├── TestK8sData.csv
│   │   ├── TrainData.csv
│   ├── processed                           # Cleaned and preprocessed datasets
│   │   ├── processed_elastic_february2022_data.csv
│   │   ├── processed_elastic_may2021_benign_data.csv
│   │   ├── processed_elastic_may2021_malicious_data.csv
│   │   ├── processed_elastic_may2022_data.csv
│   │   ├── processed_TestJMeterData.csv
│   │   ├── processed_TestK8sData.csv
│   │   ├── processed_TrainData.csv
├── logs                                   # Logs generated during model training
│   ├── train_log_lgb.txt
├── models                                 # Saved models for predictions
│   ├── k8s_failure_model_lgb.pkl
├── notebooks                              # Jupyter notebooks for EDA and data visualization
│   ├── data_exploration.ipynb
├── scripts                                # Scripts for data preprocessing, feature engineering, and model training
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   ├── model_training.py
```



---

## 🛠 Technologies Used

- **Machine Learning Framework:** LightGBM
- **Programming Language:** Python
- **Data Handling:** Pandas, NumPy
- **Model Evaluation:** Scikit-learn

---

## 📊 Dataset & Feature Engineering

-  **Dataset Source:** Extracted from Kubernetes logs and performance metrics.
-  **Feature Engineering:** Includes log-based features, resource utilization, network latency, and time-series aggregations.

---

## 🏗 Model Training

- 🚀 **Model Used:** LightGBM (Gradient Boosting Framework)
- 🔧 **Optimizations:**
  - Feature selection
  - Hyperparameter tuning
  - Regularization to prevent overfitting

---

## 🎯 Model Evaluation

📊 **Final Model Performance:**

- ✅ **Mean Squared Error (MSE):** 0.004833
- ✅ **Root Mean Squared Error (RMSE):** 0.069520
- ✅ **R² Score:** 0.990315
- ✅ **Regression Accuracy:** 96.26%
- ✅ **Testing RMSE:** 0.069520

---

## 🚀 How to Run the Project

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/chinmayeeparuchuri/k8s-failure-prediction.git
cd k8s-failure-prediction
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 3️⃣ Preprocess Data
```bash
python scripts/preprocess.py
```

### 4️⃣ Train the Model
```bash
python scripts/train_model.py
```

---

## 📌 Future Enhancements

- ✅ Incorporate Deep Learning (**LSTMs for time-series prediction**)
- ✅ Improve dataset generalization with **real-world Kubernetes failure logs**
- ✅ Deploy the model as a **REST API** or Kubernetes-native solution

---

## 🤝 Contributing

We welcome contributions to enhance the project!

1. **Fork the repository**
2. Create a new branch:
```bash
git checkout -b feature-xyz
```
3. Push to GitHub:
```bash
git push origin feature-xyz
```
---

## ⭐ Acknowledgments

Huge thanks to Kubernetes, ML researchers, and open-source contributors who inspire AI-driven automation in cloud systems. 

