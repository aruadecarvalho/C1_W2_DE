# Data Engineering Lifecycle Example - Week 2 Assignment

## Overview

This repository contains an example project that demonstrates the full data engineering lifecycle. As part of the Week 2 assignment for my Data Engineering course, this lab walks through the setup and execution of a data pipeline on AWS. The source system used is a MySQL database hosted on Amazon RDS. AWS Glue is used for the ETL (Extract, Transform, Load) process, with Amazon S3 as the storage destination. The pipeline concludes by querying the data via Amazon Athena and visualizing the results using Jupyter Lab.

The objective of the project is to transform the source data into a more query-efficient format, enabling data analysts to perform quick analytical queries without impacting the performance of the production database.

## Problem Statement

The project simulates a scenario where a retailer specializing in classic car scale models stores historical purchases and customer information in a relational MySQL database. The marketing team is interested in analyzing this data to understand customer behavior, sales distribution across countries, and product line performance. However, querying this data from the production system is not efficient for analytical purposes. 

As a Data Engineer, my responsibility is to design and implement a data pipeline that extracts, transforms, and loads the data into a query-optimized format, allowing the marketing team to analyze it with ease and efficiency.

## Architecture

![image](https://github.com/user-attachments/assets/42b3fe24-bf24-495b-b089-b3646c1479bc)

The data pipeline is built on the following AWS services:
- **Amazon RDS (Relational Database Service):** Hosts the source MySQL database.
- **AWS Glue:** Handles the ETL process to extract and transform the data.
- **Amazon S3:** Serves as the destination for the transformed data.
- **Amazon Athena:** Provides the querying capability for the stored data.
- **Terraform:** Infrastructure as Code (IaC) tool used to provision and manage the AWS services.

## Database Schema

![image](https://github.com/user-attachments/assets/c84844f3-d5c4-49a9-8009-80f35fe7e97f)

## Pipeline Workflow

1. **Data Exploration:** Query and explore the sample MySQL database stored in Amazon RDS.
2. **ETL Process:** Use AWS Glue to extract the data from the MySQL database, transform it as needed, and load it into Amazon S3.
3. **Data Querying:** Use Amazon Athena to query the data stored in S3, making it available for analysis.
4. **Data Visualization:** Build a dashboard using Jupyter Lab to visualize the queried data.
