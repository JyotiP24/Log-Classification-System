# 🔍 Log Classification System

A hybrid log classification pipeline that leverages **Regex**, **Machine Learning (Logistic Regression)**, **NLP (BERT)**, and **Large Language Models (LLMs)** to classify and triage large-scale log data for enhanced **security monitoring** and **incident response**.

## 🚀 Features

- Combines rule-based (Regex), statistical (ML), and semantic (LLM) methods for accuracy and flexibility.
- Handles both frequent and rare log patterns efficiently.
- Scalable design with FastAPI REST interface for real-time classification.
- Feedback loop with LLM to improve model understanding of unseen logs.

## 🧠 Methodology

1. **Log Aggregation & Preprocessing**
   - Parsed and cleaned logs from multiple sources (timestamps, levels, messages).
   - Normalized and structured logs in CSV format.

2. **Exploratory Analysis & Manual Categorization**
   - Identified log categories like authentication failures, privilege escalations, etc.
   - Created a taxonomy for classification.

3. **Embedding + Clustering**
   - Used **BERT embeddings** to vectorize log messages.
   - Applied **DBSCAN** to detect frequent patterns and outliers.

4. **Regex-based Classification**
   - Classified logs using hand-crafted Regex for known patterns.
   - Passed unmatched logs to the next stage.

5. **BERT + Logistic Regression**
   - Trained logistic regression on BERT vectors for confident classification.
   - Sent low-confidence logs to the LLM.

6. **LLM-based Semantic Classification**
   - Used **LLaMA LLM** to infer labels for rare/unseen logs.
   - Incorporated a feedback loop for retraining.

7. **Deployment**
   - Deployed as an API using **FastAPI**.
   - Tested with **Postman** for real-time log classification.

