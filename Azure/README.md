# 🛒 Retail Sales Data Engineering Pipeline on Microsoft Azure

> An end-to-end cloud data engineering pipeline built on Microsoft Azure to process, transform, and analyze retail sales data for advanced business analytics.

**Prepared By:** * Neo Li Xin
* Richard Yonathan Julio Clay Heng
* Jeanette Hauw Chandra

**Institution:** Faculty of Computing, Universiti Teknologi Malaysia (UTM)  
**Course:** SECP3843-01 - Special Topic in Data Engineering  

---

## 📖 Overview

In the modern retail landscape, analyzing sales data effectively is key to understanding consumer behavior and optimizing inventory. This project delivers an end-to-end data engineering pipeline hosted entirely on **Microsoft Azure**. The system extracts raw retail sales data, transforms it into a structured format using modern cloud computing frameworks, and loads it into a data warehouse to feed interactive Business Intelligence (BI) dashboards.

## 🏗️ System Architecture

This project implements the **Medallion Architecture** to guarantee data quality and fast querying capabilities:

| Layer | Function | Description |
| :--- | :--- | :--- |
| 🥉 **Bronze** | **Ingestion** | Raw retail data (transactions, customer info, store details) is extracted and loaded into Azure Data Lake Storage (ADLS) Gen2 in its original, immutable format. |
| 🥈 **Silver** | **Transformation** | Data is cleaned, filtered, and joined using Azure Databricks (PySpark). Missing values are handled, and standardized business rules are applied. |
| 🥇 **Gold** | **Analytics-Ready** | The refined data is structured into a Star Schema (Fact and Dimension tables) and loaded into Azure SQL Database/Synapse for high-speed BI querying. |

## 💻 Technology Stack

* **Data Orchestration:** `Azure Data Factory (ADF)`
* **Data Lake Storage:** `Azure Data Lake Storage Gen2 (ADLS Gen2)`
* **Data Processing:** `Azure Databricks` (PySpark, Spark SQL)
* **Data Warehouse:** `Azure SQL Database`
* **Data Visualization:** `Microsoft Power BI`

## ✨ Key Features

- [x] **Automated ETL/ELT Workflows:** Scheduled pipelines via Azure Data Factory that require zero manual intervention.
- [x] **Scalable Big Data Processing:** Leverages distributed computing in Azure Databricks to handle large volumes of daily retail transactions.
- [x] **Optimized Data Modeling:** Utilizes a Star Schema design to bridge complex sales relationships (Products, Time, Customers, Stores).
- [x] **Actionable Business Insights:** Power BI dashboards that track Key Performance Indicators (KPIs) such as total revenue, top-selling items, and seasonal sales trends.

---

## 💡 Project Reflection

<details>
<summary><b>Click to expand the project reflection</b></summary>

### The Value of Cloud Data Engineering in Retail
Handling retail sales data usually involves managing massive daily transaction volumes that easily overwhelm traditional on-premise databases. Through this project, we explored how a cloud-native approach using Microsoft Azure solves issues of scalability and data fragmentation. By creating a fully automated pipeline, businesses can transition from looking at outdated spreadsheet reports to interacting with real-time, dynamic insights.

### Key Learnings & Takeaways
* **Mastering the Azure Ecosystem:** We gained practical experience integrating multiple Azure services. Setting up automated triggers in Azure Data Factory to orchestrate Databricks notebooks taught us the true definition of an automated pipeline.
* **Data Quality is Paramount:** The Silver layer processing in Databricks highlighted the importance of data cleaning. Ensuring data types were correct and handling null values natively in PySpark prevented major reporting errors downstream.
* **Connecting Engineering to Analytics:** Building the Gold layer required us to think like analysts. Designing a proper Star Schema was critical because the final Power BI dashboards are only as performant and intuitive as the data model sitting beneath them. Ultimately, this project demonstrated how raw, messy data is turned into strategic business value.

</details>
