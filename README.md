# Project Name: COVID-19 Data Engineering Project

## Overview
This project focuses on extracting, transforming, and loading (ETL) COVID-19 related datasets into Amazon Redshift. The ETL process involves querying data from AWS Athena, storing it on Amazon S3, and finally loading it into Amazon Redshift. The project utilizes AWS services such as Athena, S3, and Redshift, along with Python libraries like boto3, pandas, and redshift_connector.

## Prerequisites
- AWS Account: Ensure you have an AWS account with necessary permissions for Athena, S3, and Redshift.
- Python Environment: Set up a Python environment with required libraries installed.

## Configuration
1. Set up your AWS credentials in the `proj.config` file.
2. Update Redshift connection details in the script.

## AWS Services Used
- **Amazon Athena:** Querying data from different datasets.
- **Amazon S3:** Storing intermediate and final data files.
- **Amazon Redshift:** Data warehousing solution for storing and querying data.

## Instructions

### 1. Extract Data from Athena
- Connect to Athena and run queries to fetch data from various datasets.

### 2. Transform Data in Python
- Perform data transformation using Pandas to create fact and dimension tables.

### 3. Store Data on S3
- Write the transformed data to CSV files and upload them to an S3 bucket.

### 4. Create Redshift Tables
- Connect to Redshift and execute SQL commands to create tables.

### 5. Load Data into Redshift
- Use the `COPY` command to load data from S3 to Redshift tables.

## Project Structure

### Code Files
- **`covid_data_etl.py`:** Python script for ETL process.
- **`proj.config`:** Configuration file for AWS credentials.

### Output Files
- **`output/factCovid.csv`:** Fact table data.
- **`output/dimDate.csv`:** Dimension table data.
- **`output/dimHospital.csv`:** Dimension table data.
- **`output/dimRegion.csv`:** Dimension table data.

## Running the ETL Process
1. Execute `covid_data_etl.py` script: `python covid_data_etl.py`
2. Check S3 bucket for the output files.
3. Verify data in Redshift tables.

## Additional Notes
- Make sure to monitor and manage AWS costs associated with Athena, Glue, Redshift, and S3.
- Adjust Redshift table definitions and COPY commands based on your data structure.


