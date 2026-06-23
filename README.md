
 # End-to-End Sales Analytics Data Platform on AWS

## Overview

This project demonstrates the design and implementation of a complete cloud-based data platform for sales analytics using AWS services and Infrastructure as Code (IaC).

The solution extracts transactional data from a MySQL database hosted on Amazon RDS, transforms it into a dimensional Star Schema using AWS Glue, and stores the processed data in Amazon S3 using the Parquet format. Amazon Athena provides a serverless analytics layer that enables business users to query historical sales data efficiently without impacting the operational database.

The entire infrastructure is provisioned and managed through Terraform, ensuring repeatable, scalable, and automated deployments.

## Business Problem

The retail company maintains customer, order, and product information within a production MySQL database. Running analytical workloads directly against the operational system can negatively affect performance and user experience.

To address this challenge, a dedicated analytical platform was built to separate reporting workloads from transactional operations while enabling fast and cost-effective business intelligence.

## Solution Architecture
 ![Architecture diagram](./assets/ETL.drawio.png)

### Data Source

* Amazon RDS (MySQL)
* Customers, Orders, Products, Payments, Employees, and related transactional tables

### Data Processing

* AWS Glue ETL Jobs
* Data cleansing and transformation
* Star Schema modeling
* Conversion to Parquet format for optimized analytics

### Storage Layer

* Amazon S3 Data Lake
* Partitioned and analytics-ready datasets

### Query & Analytics Layer

* Amazon Athena
* SQL-based serverless querying
* Integration with Jupyter Notebook for exploratory analysis and reporting

### Infrastructure Automation

* Terraform
* Automated provisioning of AWS resources
* Reproducible and version-controlled infrastructure

## Key Features

* End-to-End ETL Pipeline
* Star Schema Data Modeling
* Serverless Analytics with Athena
* Infrastructure as Code using Terraform
* Optimized Storage with Parquet
* Cloud-Native Data Architecture
* Scalable and Cost-Efficient Design

## Technologies

* AWS Glue
* Amazon S3
* Amazon Athena
* Amazon RDS (MySQL)
* Terraform
* Python
* SQL
* Jupyter Notebook

## Outcome

The solution enables analysts and business stakeholders to perform sales analysis on historical data through a scalable and serverless analytics platform while preserving the performance and reliability of the production database.
