# 🫀 Heart Disease Prediction & Data Pipeline

> A robust PySpark data engineering pipeline and machine learning implementation designed to process clinical data, map conditions to medical standards, and predict heart disease[cite: 4].

---

## 📖 Overview

This project demonstrates an end-to-end data pipeline built with PySpark to process the Cleveland heart disease dataset[cite: 4]. The workflow encompasses raw data ingestion, schema enforcement, data cleansing, and feature engineering[cite: 4]. Notably, it integrates healthcare standards by mapping binary classification targets to ICD-10 medical codes[cite: 4]. The processed data is persisted into a local lakehouse, which then fuels a Random Forest machine learning model to classify patient health outcomes[cite: 4].

## 🏗️ System Architecture

The pipeline follows a structured data engineering and machine learning workflow:

| Stage | Function | Description |
| :--- | :--- | :--- |
| 📥 **Ingestion** | **Data Loading** | Initializes a `SparkSession` and reads the `processed.cleveland.data` file while enforcing a strict 14-column schema (e.g., age, sex, cp, chol, target) using `StructType`[cite: 4]. |
| 🥈 **Transformation** | **Cleaning & Mapping** | Replaces `'?'` characters with `None`, drops null values, and binarizes the target variable (values `> 0` become `1.0`, else `0.0`)[cite: 4]. Maps `1.0` to ICD-10 code `I25.1` (Atherosclerotic heart disease) and `0.0` to `Z00.0` (General medical examination)[cite: 4]. |
| 💾 **Storage** | **Lakehouse Sink** | Joins the clinical data with an ICD-10 reference table and writes the final structured dataset to a directory named `heart_disease_lakehouse` in `parquet` format using `overwrite` mode[cite: 4]. |
| 🤖 **Machine Learning** | **Classification** | Uses `VectorAssembler` to compile 9 clinical features (age, sex, cp, trestbps, chol, thalach, oldpeak, ca, thal) into a feature vector[cite: 4]. Splits data into 80% training and 20% testing sets to train a `RandomForestClassifier`[cite: 4]. |

## 💻 Technology Stack

*   **Core Engine:** `PySpark` (Python 3)[cite: 4]
*   **Data Processing:** `Spark SQL` (`StructType`, `functions.col`, `functions.when`)[cite: 4]
*   **Machine Learning:** `pyspark.ml` (`VectorAssembler`, `RandomForestClassifier`, `MulticlassClassificationEvaluator`)[cite: 4]
*   **Storage Format:** `Parquet`[cite: 4]

## ✨ Key Features

- [x] **Automated Data Cleansing:** Natively handles missing data and schema casting (e.g., casting `ca` and `thal` to `DoubleType`) for robust downstream processing[cite: 4].
- [x] **ICD-10 Integration:** Contextualizes raw numerical targets by mapping them to real-world medical classifications (Atherosclerotic heart disease vs. General medical examination)[cite: 4].
- [x] **Optimized Storage:** Saves the curated dataset as Parquet files, ensuring high performance and compressed storage for the machine learning layer[cite: 4].
- [x] **Predictive Analytics:** Implements a Random Forest Classifier equipped with 100 trees (`numTrees=100`, `seed=42`)[cite: 4]. 
- [x] **High Accuracy:** Evaluated using a `MulticlassClassificationEvaluator`, the model achieves an impressive predictive accuracy of approximately **84.78%** on the test dataset[cite: 4].

---

## 💡 Project Reflection

<details>
<summary><b>Click to expand the project reflection</b></summary>

### Unifying Data Engineering and Healthcare Analytics
Processing medical datasets requires strict attention to data integrity and clinical context. This project highlights the power of PySpark in unifying data engineering pipelines with machine learning[cite: 4]. By establishing a predefined schema upfront, the pipeline prevents data type mismatches that often derail predictive models[cite: 4]. Furthermore, mapping simple binary targets to ICD-10 descriptions bridges the gap between raw data science and practical healthcare informatics, making the outputs immediately readable by medical professionals[cite: 4].

### Key Learnings & Takeaways
*   **Spark's Ecosystem Efficiency:** Transitioning smoothly from Spark SQL DataFrames for data manipulation directly into `pyspark.ml` components like `VectorAssembler` proves highly efficient[cite: 4]. It eliminates the need to switch between disjointed libraries like Pandas and Scikit-Learn for large-scale operations.
*   **Data Quality Drives Performance:** The steps taken to handle `'?'` characters and drop nulls early in the pipeline were critical[cite: 4]. Clean data combined with a robust Random Forest algorithm directly contributed to the strong 84.78% accuracy rate[cite: 4].
*   **Scalable Architecture:** Writing the intermediate cleaned data to a Parquet "lakehouse" directory establishes a scalable pattern[cite: 4]. In a production environment, this allows other analytical tools or dashboards to query the historical data without having to rerun the entire ingestion and cleaning pipeline.

</details>
