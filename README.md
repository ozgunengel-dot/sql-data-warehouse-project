# SQL Data Warehouse Project

This project is a hands-on implementation of a modern **data warehouse using SQL Server**. I built it as part of my SQL learning process to practice data warehousing concepts, ETL development, data modeling, data quality, and analytical reporting in a complete end-to-end project.

The solution follows the **Medallion Architecture**, consisting of Bronze, Silver, and Gold layers, and integrates data from two different source systems into a business-ready analytical model.

---

##  Data Architecture

The project uses a three-layer Medallion Architecture:

### Bronze Layer

The Bronze layer stores the source data in its original form.

Data from CRM and ERP systems is provided as CSV files and loaded into SQL Server without applying business transformations.

### Silver Layer

The Silver layer is responsible for improving data quality and preparing the data for integration.

This includes:

* Data cleansing
* Standardization
* Handling invalid or inconsistent values
* Data type corrections
* Data normalization
* Integration of CRM and ERP datasets

### Gold Layer

The Gold layer contains business-ready datasets designed for reporting and analytical use cases.

The final model follows a **star schema**, using fact and dimension tables to make analytical queries simpler and more efficient.

---

## 📖 Project Overview

The project covers the main stages of building a data warehouse:

* **Data Architecture:** Designing the Bronze, Silver, and Gold layers.
* **ETL Development:** Extracting data from source files, transforming it, and loading it into the appropriate warehouse layers.
* **Data Quality:** Identifying and resolving inconsistencies, missing values, duplicates, and formatting issues.
* **Data Integration:** Combining ERP and CRM datasets into a unified structure.
* **Data Modeling:** Creating fact and dimension tables based on a star schema.
* **Analytics:** Writing SQL queries and reports to analyze customers, products, and sales performance.
* **Documentation:** Documenting the architecture, data flows, naming conventions, and data models.

The main purpose of the project was to apply SQL concepts in a realistic data engineering and analytics scenario rather than working only with isolated queries.

---

## 🎯 Project Requirements

### Data Warehouse

The main objective is to consolidate sales-related data from different source systems into a structured SQL Server data warehouse that can support reporting and analysis.

### Data Sources

The project uses two source systems:

* CRM
* ERP

The source datasets are provided as CSV files and imported into SQL Server.

### Data Quality

Before making the data available for analysis, several data quality checks and transformations are performed in the Silver layer.

These include correcting inconsistent values, standardizing formats, handling unwanted spaces, validating date ranges, and checking relationships between datasets.

### Data Integration

CRM and ERP datasets are integrated into a single analytical model.

The Gold layer provides a simplified structure that allows users to query business information without having to work directly with the raw source tables.

### Scope

The project focuses on the latest available dataset. Historical tracking and Slowly Changing Dimension implementations are outside the scope of this version.

---

## 📊 Analytics & Reporting

After building the warehouse, SQL-based analysis is performed on the Gold layer.

The analytical part of the project focuses mainly on:

* **Customer Behavior**
* **Product Performance**
* **Sales Trends**

The project also includes techniques such as:

* Exploratory Data Analysis
* Ranking analysis
* Change-over-time analysis
* Cumulative analysis
* Year-over-year performance comparison
* Part-to-whole analysis
* Customer and product segmentation

Customer and product reporting views are also created to provide reusable datasets for further reporting or BI tools.

---

## 🛠️ Technologies & Tools

The project was developed using:

* **SQL Server**
* **SQL Server Management Studio (SSMS)**
* **T-SQL**
* **Git & GitHub**
* **Draw.io**
* **CSV datasets**

---

## 📂 Repository Structure

```text
data-warehouse-project/
│
├── datasets/                           # Raw CRM and ERP datasets
│
├── docs/                               # Architecture and project documentation
│   ├── etl.drawio                      # ETL process documentation
│   ├── data_architecture.drawio        # Data warehouse architecture
│   ├── data_catalog.md                 # Dataset and column descriptions
│   ├── data_flow.drawio                # Data flow diagram
│   ├── data_models.drawio              # Star schema and data models
│   ├── naming-conventions.md           # Naming standards used in the project
│
├── scripts/                            # SQL scripts
│   ├── bronze/                         # Raw data loading scripts
│   ├── silver/                         # Data cleansing and transformation scripts
│   ├── gold/                           # Analytical model creation scripts
│
├── tests/                              # Data quality and validation scripts
│
├── README.md                           # Project documentation
├── LICENSE                             # License information
├── .gitignore                          # Git ignored files
└── requirements.txt                    # Project requirements
```

---

## 📌 What I Practiced

While working on this project, I practiced:

* Designing a layered data warehouse architecture
* Loading external CSV data into SQL Server
* Writing reusable SQL scripts and stored procedures
* Performing data quality checks
* Cleaning and standardizing data
* Integrating data from multiple source systems
* Designing fact and dimension tables
* Building a star schema
* Creating analytical SQL queries
* Using CTEs and window functions
* Creating reusable reporting views
* Documenting a data warehouse project
* Managing the project with Git and GitHub

---

## 📚 Learning Context

This project was developed while following the **Data with Baraa SQL course**.

The original project structure and dataset were provided as part of the training. I reproduced the project in my own SQL Server environment, worked through the different warehouse layers, and uploaded my implementation and project files to this repository as part of my SQL and data warehousing learning process.

---

## 🛡️ License

This project is licensed under the MIT License. See the `LICENSE` file for more information.
