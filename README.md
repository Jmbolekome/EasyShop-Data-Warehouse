# EasyShop Data Warehouse

## Project overview

EasyShop Data Warehouse is an end-to-end Business Intelligence project that demonstrates the design and implementation of an ETL pipeline using SQL Server Integration Services (SSIS).

Customer data from multiple Excel sources is extracted, cleaned, standardized, deduplicated and loaded into SQL Server using a Bronze–Silver–Gold architecture.

The project illustrates how heterogeneous operational data can be transformed into reliable, structured data ready for reporting and analysis.

## Architecture

### Bronze layer

The Bronze layer stores raw customer data imported from the Excel source files with minimal transformation.

### Silver layer

The Silver layer improves data quality through:

* Text trimming and standardization
* Data-type conversion
* Column alignment between different sources
* Data validation
* Dataset consolidation using `Union All`
* Duplicate identification and removal

### Gold layer

The Gold layer prepares clean and structured data for analytical use, reporting and future Power BI dashboards.

## ETL workflow

The SSIS package performs the following steps:

1. Extract customer data from multiple Excel files.
2. Load the raw data into Bronze tables.
3. Clean and standardize the source datasets.
4. Convert columns into consistent data types.
5. Align the schemas of the different sources.
6. Merge the datasets using `Union All`.
7. identify and remove duplicate records.
8. Load the transformed data into SQL Server.
9. Prepare structured Gold-layer data for analysis.

## Technologies

* Microsoft SQL Server
* SQL Server Integration Services (SSIS)
* SQL
* Microsoft Excel
* Visual Studio
* Git and GitHub

## Repository contents

* `01_create_easyshop_dw.sql` — SQL script used to create the EasyShop Data Warehouse structure
* `EasyShop_ETL.dtsx` — SSIS package containing the complete ETL workflow
* `EasyShop_ETL.dtproj` — Visual Studio Integration Services project file
* `EasyShop_ETL.sln` — Visual Studio solution
* `Project.params` — SSIS project parameters
* `.gitignore` — Git exclusion rules for generated and user-specific files

## How to run the project

### Requirements

* Microsoft SQL Server
* SQL Server Management Studio
* Visual Studio with the SQL Server Integration Services extension
* Access to the required Excel source files

### Execution

1. Run `01_create_easyshop_dw.sql` in SQL Server Management Studio.
2. Open `EasyShop_ETL.sln` in Visual Studio.
3. Configure the Excel and SQL Server connection managers for the local environment.
4. Verify the source-file paths and project parameters.
5. Execute `EasyShop_ETL.dtsx`.
6. Validate the loaded data in the Bronze, Silver and Gold layers.

> The original Excel source files and local connection settings are not included in this repository. They must be configured locally before execution.

## Skills demonstrated

* ETL pipeline development
* Data warehouse architecture
* Data cleaning and standardization
* Data-type conversion
* Multi-source data integration
* Duplicate management
* SQL database development
* SSIS workflow design
* Git version control
* Technical documentation

## Future improvements

* Add data-quality checks and error logging
* Add automated package execution
* Create Power BI dashboards from the Gold layer
* Add visual documentation of the ETL workflow and data model

## Author

**Julien Mbolekome**
Junior Data & BI professional based in Brussels
