# E-Portfolio-SECP3843

# 🚀 Data Engineering & Machine Learning Portfolio

[![Institution](https://img.shields.io/badge/Institution-Universiti%20Teknologi%20Malaysia%20(UTM)-800000?style=for-the-badge&logo=academic)]()
[![Course](https://img.shields.io/badge/Course-SECP3843--01%20Special%20Topic%20in%20Data%20Engineering-blue?style=for-the-badge)]()

Welcome to the central repository for this Data Engineering and Machine Learning portfolio! This repository hosts a collection of comprehensive projects developed during our studies at **Universiti Teknologi Malaysia (UTM)**. The primary focus of this repository is on automated cloud-based data pipelines, business analytics, and deep learning implementations.

---

## 📂 Project Catalog

This repository consists of several major projects. Please click on the respective project directories to view the full details, documentation, and source code.

| 📁 Project Directory | 📝 Brief Description | 🛠️ Core Technologies |
| :--- | :--- | :--- |
| **[1. PPG-Inventory-Pipeline](./PPG-Inventory-Pipeline)** | An automated Azure-based pipeline to monitor inventory risks (dead stock, recoverable assets, expired materials) and calculate financial provisions. | `Azure Data Factory`, `Databricks`, `Power BI` |
| **[2. Retail-Sales-Analytics](./Retail-Sales-Analytics)** | An end-to-end data pipeline utilizing the Medallion Architecture (Bronze, Silver, Gold) to process retail sales data at scale. | `PySpark`, `Azure Data Lake`, `Azure SQL` |
| **[3. Heart-Disease-Prediction](./Heart-Disease-Prediction)** | A PySpark pipeline for cleansing clinical data, mapping targets to ICD-10 medical standards, and predicting heart disease using Random Forest. | `PySpark`, `Spark MLlib`, `Lakehouse` |
| **[4. CNN-Image-Classification](./CNN-Image-Classification)** | Implementation and optimization of a Convolutional Neural Network (CNN) to automatically classify images using the CIFAR-10 dataset. | `Python`, `TensorFlow`, `Keras` |

### Key Overarching Takeaways

* **End-to-End Pipeline Thinking:** Across both the **PPG Inventory Pipeline** and the **Retail Sales Analytics** projects, we experienced the critical importance of the **Medallion Architecture**. We learned that isolating raw data (Bronze), applying rigorous cleaning and business logic (Silver), and structuring it for performance (Gold) is the only way to prevent a data lake from becoming an unmanageable "data swamp." 
* **The Power of Cloud & Distributed Computing:** Transitioning from local Python scripts to **Azure Databricks** and **PySpark** was a major paradigm shift. Whether we were processing massive retail transactions or preparing clinical datasets for the **Heart Disease Prediction** model, leveraging distributed computing taught us how to engineer solutions that scale seamlessly with growing data volumes.
* **Context is Everything (Business & Domain Value):** A recurring theme across all projects was the necessity of domain context. In the inventory pipeline, we had to translate raw CSVs into actionable Magna Carta financial provisions. In the healthcare project, mapping binary targets to real-world **ICD-10 medical codes** bridged the gap between pure data science and practical informatics. Even in the **CNN Image Classification** project, analyzing error patterns (e.g., confusing similar animal classes) taught us to look beyond raw accuracy metrics and understand how a model will actually perform in the real world.
* **Designing for the End-User:** Ultimately, data engineering and machine learning do not exist in a vacuum. Building interactive **Power BI** dashboards taught us that our backend engineering is only as successful as the insights it provides to stakeholders. Standardizing KPIs, ensuring data quality, and designing intuitive star schemas proved essential for driving data-driven decision-making.

> **Note:** Each sub-directory in this repository contains its own dedicated `README.md` that explains the system architecture, methodology, and setup instructions in greater detail.
