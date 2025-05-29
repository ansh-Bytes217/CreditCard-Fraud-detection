# CreditCard-Fraud-detection

---

 Overview

Credit card fraud detection is a binary classification problem where transaction data is analyzed to determine whether a transaction is **legitimate** or **fraudulent**. Detecting fraudulent activities is crucial for financial institutions to minimize loss and ensure trust.

Fraud detection techniques typically fall under two categories:

1. **Fraud Analysis (Misuse Detection)**
   Supervised learning methods are used to classify transactions based on labeled data. Models such as **Decision Trees**, **Random Forests**, and other classification algorithms are trained to distinguish between fraudulent and non-fraudulent transactions.

2. **User Behavior Analysis (Anomaly Detection)**
   This unsupervised approach focuses on identifying deviations from typical behavior patterns. The core assumption is that fraudulent behavior significantly differs from normal user behavior.

 Why Anomaly Detection?

Anomaly detection, also known as **outlier detection**, **deviation detection**, or **novelty detection**, is especially effective when fraudulent transactions are rare and lack sufficient labeled data for supervised learning. Instead of learning what fraud looks like, the model learns what *normal* looks like—and flags deviations as potential fraud.

 Role of AutoEncoders

AutoEncoders, a type of neural network, are commonly used for anomaly detection. Here's how they work in this context:

* The AutoEncoder is trained exclusively on **legitimate (normal)** transactions.
* Once trained, the model attempts to reconstruct input data.
* For normal transactions, the reconstruction error remains low.
* For fraudulent transactions (which differ from the training data), the reconstruction error is significantly higher—helping to flag them as anomalies.

 Key Takeaways

* The system leverages the behavioral differences between genuine users and fraudsters.
* Training is performed on legitimate transactions only.
* Fraudulent activities are detected as outliers based on reconstruction error.

