# EasyShop Data Warehouse

## Project overview

This project demonstrates the creation of an ETL pipeline for an EasyShop data warehouse using SQL Server Integration Services (SSIS).

Customer data from multiple Excel sources is extracted, cleaned, standardized, merged and loaded into SQL Server through a Bronze–Silver–Gold architecture.

## Architecture

* **Bronze layer:** ingestion of raw source data
* **Silver layer:** data cleaning, conversion and standardization
* **Gold layer:** preparation of structured data for reporting and analysis

## ETL transformations

The SSIS package performs several operations:

* Importing data from multiple Excel files
* Trimming and standardizing text fields
* Converting data types
* Aligning columns from different sources
* Combining datasets with `Union All`
* Identifying and removing duplicates
* Loading transformed data into SQL Server tables

## Technologies

* SQL Server
* SQL Server Integration Services (SSIS)
* SQL
* Microsoft Excel
* Visual Studio

## Repository contents

* `EasyShop_ETL.dtsx`: SSIS package containing the ETL workflow

## Author

Julien Mbolekome

Junior Data & BI professional based in Brussels
