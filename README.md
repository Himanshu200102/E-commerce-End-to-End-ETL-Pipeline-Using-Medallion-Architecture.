# E-commerce End-to-End ETL Pipeline Using Medallion Architecture

This repository contains the implementation of an end-to-end ETL (Extract, Transform, Load) pipeline for e-commerce data using the Medallion Architecture. The project automates data ingestion, transformation, and analytics while ensuring data quality and consistency at each stage.

## Project Overview

The project is designed to:
- **Automate Data Ingestion**: Utilize Azure Data Factory (ADF) for ingesting raw e-commerce data, converting it to Parquet format, and storing it in the Bronze Layer of Delta Lake.
- **Ensure Data Quality**: Perform ETL transformations in Apache Spark (PySpark) on Databricks, including deduplication, normalization, and schema enforcement, and store the processed data in the Silver Layer.
- **Enable Analytics**: Aggregate and optimize data in the Gold Layer for SQL-based analytics and reporting using Databricks SQL Warehouse. Delta Lake's ACID transactions, partitioning, and caching enhance query performance.

## Architecture

The ETL pipeline is implemented using the **Medallion Architecture**, which consists of three layers:
1. **Bronze Layer**:
   - Stores raw, unprocessed data in Parquet format.
   - Data is ingested and loaded via Azure Data Factory.
   
2. **Silver Layer**:
   - Contains cleaned, structured, and deduplicated data.
   - Transformations are performed using PySpark on Databricks.

3. **Gold Layer**:
   - Aggregated and optimized data for analytics and reporting.
   - Stored in Databricks SQL Warehouse for efficient querying.
