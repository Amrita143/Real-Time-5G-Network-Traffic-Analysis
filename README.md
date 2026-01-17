# 📡 Real-Time 5G Network Traffic Analysis & Anomaly Detection

### **Project Overview**

This project implements a scalable **end-to-end data engineering and data science pipeline** to analyze [Kaggle's 5G Traffic Dataset](https://www.kaggle.com/datasets/kimdaegyeom/5g-traffic-datasets/) for video conferencing applications (Google Meet).

Using **Databricks** and **PySpark Structured Streaming**, the system ingests raw packet logs, calculates real-time Quality of Service (QoS) metrics (Jitter, Throughput, Packet Loss), and deploys an **unsupervised Machine Learning Algorithm** **Isolation Forest** model to detect network anomalies and potential call drops.

### 🚀 Key Features

* **Medallion Architecture:** Implemented a Bronze (Raw)  Silver (Features)  Gold (Insights) pipeline using Delta Lake.
* **Real-Time QoS Monitoring:** Calculates Jitter (Inter-Arrival Time variance) and Throughput via PySpark Window functions.
* **Anomaly Detection:** Unsupervised ML model (Isolation Forest) to flag network degradation without labeled data.
* **Protocol Analysis:** Deep packet inspection revealing application-layer behavior (e.g., TCP tunneling vs. UDP transport).

### 🛠️ Tech Stack

* **Platform:** Databricks (Community Edition / Azure)
* **Processing:** PySpark (Structured Streaming & Batch)
* **Storage:** Delta Lake (Unity Catalog)
* **Machine Learning:** Scikit-Learn (Isolation Forest), Pandas UDFs
* **Visualization:** Matplotlib, Seaborn

### 📊 Key Insights (Google Meet Dataset)

Analysis of **27M+ packets** revealed distinct traffic patterns:

* **Protocol Tunneling:** Identified **98% TCP/TLS usage** (vs. standard UDP), indicating application-layer adaptation to network/firewall constraints.
* **Stability Benchmark:** Established a **1.16 Mbps** throughput baseline for 720p HD video.
* **Reliability:** Achieved a **99.99% Service Reliability Score** with jitter consistently below 6ms.
---

*This project was developed to demonstrate Big Data handling and Telecom domain expertise for high-scale network operations.*
