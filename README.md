# 🚀 Cloud Billing Anomaly Detection using GCP & BigQuery

This project analyzes Google Cloud Platform (GCP) billing data and detects unusual cost spikes using BigQuery and Python's machine learning libraries.

## 📊 Project Objective

The primary goal is to:
- Gain visibility into GCP cloud spending across services.
- Detect abnormal cost spikes using unsupervised anomaly detection.
- Provide visual insights into billing trends using data visualization.

## 🧰 Tech Stack

- **Google Cloud Platform (GCP)**
- **BigQuery**
- **Python (pandas, matplotlib, scikit-learn)**
- **GCP Billing Export**

## ⚙️ Features

- Connected GCP Billing Export table with BigQuery.
- Queried cost and usage data across multiple GCP services.
- Plotted time series cost trends using `matplotlib`.
- Used `IsolationForest` to detect billing anomalies.
- Tried enabling **real-time logging** through BigQuery export, but due to limitations in the newly created GCP account, logs weren’t received.

## 📈 Sample Visualizations

- 📅 **Daily Cost Trend Graph**
- 🔍 **Anomaly Detection Output** using ML model

## 🛠️ How It Works

1. Exported billing data to BigQuery from GCP Billing Export.
2. Queried data using SQL via Python's `google-cloud-bigquery` client.
3. Converted results into `pandas` DataFrame.
4. Plotted line chart showing daily costs.
5. Applied **Isolation Forest** to flag unusually high-cost days.

## ❌ Limitation

- The GCP account used was newly created.
- Although BigQuery export for logs was enabled, **no logs appeared** in BigQuery.
- Hence, real-time monitoring and log-based analysis was **not achieved**.

✅ **This is a valid limitation**, as GCP often delays log exports or requires additional configurations (billing account permissions, IAM roles, audit log settings) which may not be fully accessible in new accounts.

## 💡 Future Optimizations

- Use **GCP Pub/Sub + Dataflow** to stream logs in real-time to BigQuery.
- Implement alerting system using **GCP Cloud Monitoring**.
- Integrate dashboards using **Google Data Studio** for rich visualization.
- Enable scheduled jobs via **Cloud Scheduler** for periodic anomaly scanning.

## 📂 Dataset

Sample file: `billing_data.csv`  
Contains: `date`, `service`, `cost`

## 📬 Contact

For suggestions or questions, feel free to connect via [LinkedIn](https://www.linkedin.com/in/yashika-bhandari-ab7a74253/)

