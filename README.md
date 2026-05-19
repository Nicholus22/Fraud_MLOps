# 🛡️ Fraud Detection System (MLOps Project)

## What this project is about

This project is about detecting scam and phishing messages like fake traffic fines, bank alerts, or WhatsApp/SMS fraud attempts.

It was built to show how data and machine learning can help identify suspicious messages before people fall victim to scams.

---

## The problem

Scammers are using very simple but effective tricks:

* Fake urgent messages (“pay immediately or account will be blocked”)
* Malicious links
* Pretending to be banks or government agencies

The goal here is to build a system that can automatically detect these patterns.

---

## How it works

The system follows a simple pipeline:

SQL database → Python (Jupyter) → Feature engineering → Machine learning model → Prediction API

---

## What I used

* Python
* SQL (PostgreSQL / SQLite)
* Pandas & NumPy
* Scikit-learn
* NLP (TF-IDF)
* MLflow (for tracking experiments)
* FastAPI (for deployment)
* Jupyter Notebook

---

## How I built it

First, I stored all messages in a SQL database.

Then I pulled the data into Python and cleaned it.

After that, I created features like:

* Message length
* Presence of urgency words (urgent, blocked, final notice)
* Whether the message contains a link
* Fraud-related keywords (AARTO, fine, traffic)

I then trained a machine learning model to classify messages as:

* Legitimate (0)
* Fraudulent (1)

---

## Model training

I tested a few models and started with Logistic Regression.

I evaluated it using:

* Accuracy
* Precision
* Recall
* Confusion matrix

The goal was not just accuracy, but making sure fraud cases are detected properly.

---

## What makes this project MLOps

This is not just a model — it’s a full pipeline:

* Data stored in SQL
* Feature engineering in Python
* Model tracking with MLflow
* API for real-time predictions
* Structured for deployment using Docker (optional)

---

## Example prediction

Input:

> “Urgent: pay your traffic fine immediately or your license will be suspended”

Output:

> FRAUD

---

## What I learned

* Fraud patterns are actually very predictable in data
* Simple features like urgency words and links are very powerful
* The biggest challenge is keeping the system updated as scammers change tactics
* MLOps is what turns a model into a real-world system

---

## Future improvements

If I take this further, I would add:

* Real-time message streaming
* Model drift detection
* Cloud deployment (Azure/AWS)
* Dashboard for monitoring fraud trends

---

## Author

Built by Khangwelo Maphaha
Focused on Data Engineering, MLOps, and Analytics

