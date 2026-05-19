# 🛡️ Fraud Detection MLOps System (SQL + Python + MLflow)

## 📌 Overview

This project is an end-to-end **fraud detection system** designed to identify phishing and scam messages (SMS, WhatsApp, Email) such as fake traffic fine notices and banking impersonation attempts.

It demonstrates a full **MLOps pipeline** including:

* SQL-based data storage
* Python NLP feature engineering
* Machine Learning model training
* Experiment tracking with MLflow
* API deployment with FastAPI
* Visualization & monitoring

---

## 🎯 Problem Statement

Fraudsters use social engineering techniques to trick users into:

* Clicking malicious links
* Sharing banking credentials
* Approving unauthorized transactions

This system detects fraudulent messages based on:

* Language patterns
* URL presence
* Urgency indicators
* Sender behavior

---

## 🏗️ Architecture

```
SQL Database → Python ETL → Feature Engineering → ML Model
        ↓
   MLflow Tracking
        ↓
   FastAPI Deployment
        ↓
 Monitoring & Visualization
```

---

## 📊 Dataset Structure

Stored in SQL table `messages`:

| Column       | Description               |
| ------------ | ------------------------- |
| message_id   | Unique ID                 |
| sender       | Message sender            |
| channel      | SMS / WhatsApp / Email    |
| message_text | Full message content      |
| url_count    | Number of URLs in message |
| received_at  | Timestamp                 |
| label        | 0 = Legit, 1 = Fraud      |

---

## ⚙️ Tech Stack

* 🐍 Python
* 🗄️ SQL (PostgreSQL / SQLite)
* 📊 Pandas, NumPy
* 🤖 Scikit-learn
* 🧠 NLP (TF-IDF)
* 📦 MLflow
* 🚀 FastAPI
* 🐳 Docker
* 📈 Matplotlib / Seaborn
* 📓 Jupyter Notebook

---

## 🔧 Feature Engineering

Key features used:

* Message length
* Urgency keywords (urgent, blocked, final notice)
* URL presence
* Fraud keyword detection (AARTO, fine, traffic)
* Sender risk scoring

---

## 🧠 Model Training

Models tested:

* Logistic Regression (baseline)
* Random Forest (improved accuracy)

Evaluation metrics:

* Accuracy
* Precision / Recall
* Confusion Matrix
* ROC-AUC

---

## 🚀 How to Run the Project

### 1. Clone Repository

```bash
git clone https://github.com/your-username/fraud-detection-mlops.git
cd fraud-detection-mlops
```

---

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 3. Run SQL Database

```sql
CREATE DATABASE fraud_detection;
```

---

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Run:

* `01_data_exploration.ipynb`
* `02_feature_engineering.ipynb`
* `03_model_training.ipynb`

---

### 5. Train Model

```python
python src/train.py
```

---

### 6. Run API (FastAPI)

```bash
uvicorn api.app:app --reload
```

---

### 7. Test Prediction

```bash
POST /predict
{
  "message": "Urgent: pay traffic fine immediately via link"
}
```

---

## 📈 Model Performance

| Metric    | Score                           |
| --------- | ------------------------------- |
| Accuracy  | ~92%                            |
| Precision | High (fraud detection priority) |
| Recall    | Optimized for fraud catch rate  |

---

## 📊 Visualizations

* Fraud vs Legit distribution
* Channel-based fraud analysis
* Time-based fraud trends
* Keyword impact analysis
* Confusion matrix
* ROC curve

---

## 🧪 MLOps Features

* MLflow experiment tracking
* Model versioning
* Reproducible pipeline
* API deployment
* Docker containerization (optional extension)

---

## 🔐 Business Impact

* Detects phishing scams early
* Reduces banking fraud risk
* Supports real-time monitoring
* Improves customer safety in digital banking

---

## 📌 Future Improvements

* Real-time streaming (Kafka)
* Model drift detection (Evidently AI)
* Azure/AWS deployment
* CI/CD pipeline (GitHub Actions)
* Fraud alert dashboard (Power BI)

---

## 👨‍💻 Author

**Khangwelo Maphaha**
Data Engineer | ML & MLOps Enthusiast
SQL • Python • Azure • AWS • Power BI


