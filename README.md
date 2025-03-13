# NYC Taxi End-to-End Data Engineering Project

Overview

This project demonstrates a complete data engineering pipeline using Azure services to process and analyze New York City taxi data. The pipeline follows the Medallion Architecture (Bronze, Silver, Gold) and integrates various Azure tools for ingestion, transformation, storage, and visualization.

## Architecture Diagram

![1](https://github.com/user-attachments/assets/79e5aafc-6f8c-47c9-b19b-f26757a3d812)


## Tech Stack

* **Azure Data Factory (ADF)** – For dynamic data ingestion
* **Azure Data Lake Storage Gen2 (ADLS Gen2)** – To store raw and processed data
* **Azure Databricks** – For data transformation using PySpark
* **Delta Lake** – For optimized data storage and versioning
* **Power BI** – For data visualization

## Data Ingestion (Bronze Layer)

1. Downloaded NYC taxi data from the NYC Taxi & Limousine Commission website in Parquet format.
2. Used Azure Data Factory (ADF) to ingest 12 monthly parquet files dynamically into Azure Data Lake Gen2.
3. Implemented ForEach activity, If-condition activity, and Copy activity to automate the ingestion process.

## Data Transformation (Silver Layer)

1. Connected Azure Data Lake Gen2 with Azure Databricks using access connectors.
2. Created credentials and external storages for secure access to containers.
3. Used PySpark functions such as:
  * withColumn, withColumnRenamed for column modifications
  * split, concat, when for data transformation
4. Stored the cleaned and structured data into the Silver Layer in ADLS Gen2.

## Delta Tables & Versioning (Gold Layer)
1. Created Delta Tables in Databricks using external tables concept.
2. Performed CRUD operations on the Delta tables.
3. Used Delta Lake’s time travel & versioning functionality to maintain table history and restore previous versions.

## Data Visualization

1. Connected Databricks Notebooks to Power BI.
2. Created interactive visualizations to analyze taxi trip trends and insights.

## Key Features

✔ Automated Data Ingestion using ADF

✔ Scalable Data Transformation with PySpark

✔ Structured Storage with Medallion Architecture

✔ Delta Lake Versioning & Time Travel for data integrity

✔ Actionable Insights using Power BI visualizations
