# 🏭 PPG Case Study Pipeline: Inventory Risk Management

> A cloud-based data engineering pipeline designed to resolve scattered inventory data issues and automate risk monitoring for PPG Coatings (Malaysia) Sdn. Bhd.[cite: 1]

**Prepared By:** Group 7, Faculty of Computing, Universiti Teknologi Malaysia (UTM)[cite: 1]

---

## 📖 Overview

This project delivers an end-to-end data engineering solution to address the challenges of disjointed operational datasets[cite: 1]. By integrating fragmented data into a unified cloud platform, the system automates the monitoring and identification of critical inventory risks[cite: 1]. It classifies items into actionable categories—such as Recoverable Assets (RA), Magna Carta (MC) Dead Stock, and Expired Materials—enabling the business to quantify financial exposures and make proactive, data-driven decisions[cite: 1].

## 🏗️ System Architecture

The pipeline utilizes the **Medallion Architecture** framework to progressively process and refine data across three distinct stages[cite: 1]:

| Layer | Function | Description |
| :--- | :--- | :--- |
| 🥉 **Bronze** | **Raw Data** | Ingests and stores raw operational data from six CSV files (materials, inventory snapshots, purchase orders, production orders, suppliers, and sales orders) into an immutable data lake to maintain historical auditability[cite: 1]. |
| 🥈 **Silver** | **Processed Data** | Cleans, validates, standardizes, and integrates the data[cite: 1]. Complex business logic is applied here to detect excess stock, dead stock, and expired materials[cite: 1]. |
| 🥇 **Gold** | **Analytics-Ready** | Structures the validated data into a Star Schema (fact and dimension tables) within a data warehouse, optimized for high-performance querying and reporting[cite: 1]. |

## 💻 Technology Stack

*   **Ingestion & Orchestration:** `Azure Data Factory`[cite: 1]
*   **Data Storage (Bronze/Silver):** `Azure Data Lake Storage Gen2`[cite: 1]
*   **Transformation:** `Azure Databricks` (PySpark/SQL)[cite: 1]
*   **Data Warehouse (Gold):** `Azure SQL Database`[cite: 1]
*   **BI & Visualization:** `Microsoft Power BI`[cite: 1]

## ✨ Key Features

- [x] **Automated Data Pipeline:** Eliminates manual data entry and integrates scattered datasets seamlessly[cite: 1].
- [x] **Inventory Risk Detection:** Automatically identifies recoverable assets (e.g., 17 items found), Magna Carta dead stock, and expired supplies based on specific consumption business rules[cite: 1].
- [x] **Financial Provisioning:** Calculates strict financial write-down provisions required for obsolete inventory (e.g., RM147,565.00 identified in testing)[cite: 1].
- [x] **Impact Traceability:** Maps material shortages to unfulfilled production runs and flags at-risk customer sales orders downstream[cite: 1].
- [x] **Interactive Dashboards:** Provides real-time insights tailored for procurement, warehouse, finance, and senior management teams[cite: 1].

---

## 💡 Project Reflection

<details>
<summary><b>Click to expand the project reflection</b></summary>

### The Business Value of Modern Data Engineering
Traditional inventory tracking utilizing manual spreadsheets or isolated ERP systems is highly prone to human error and heavily reactive, often resulting in undetected "dead stock" and severe financial write-downs[cite: 1]. This project successfully demonstrated that transitioning to a proactive, cloud-based data engineering pipeline resolves these operational bottlenecks[cite: 1]. By automating the extraction, transformation, and loading (ETL/ELT) of data, businesses can achieve real-time transparency across their entire supply chain[cite: 1]. 

### Key Learnings & Takeaways
*   **Architectural Discipline:** Implementing the Medallion Architecture (Bronze, Silver, Gold) proved critical for avoiding a "data swamp"[cite: 1]. Retaining raw data in the Bronze layer ensured auditability, while isolating business logic in the Silver layer and structuring analytical schemas in the Gold layer guaranteed high-performance reporting[cite: 1].
*   **Bridging Data and Strategy:** The project highlighted the importance of translating raw data into actionable business intelligence[cite: 1]. Structuring the transformed data into a Star Schema allowed Power BI to effectively answer specific, high-stakes business questions regarding financial provisions and stockout impacts[cite: 1].
*   **Real-World Application:** Working with industry case study datasets provided invaluable experience in handling data integration challenges, such as tracking material lifecycles, understanding the financial impact of overstocking, and mitigating customer fulfillment delays[cite: 1]. Ultimately, leveraging platforms like Microsoft Azure and Power BI drastically reduces carrying costs and enhances operational efficiency[cite: 1].

</details>
