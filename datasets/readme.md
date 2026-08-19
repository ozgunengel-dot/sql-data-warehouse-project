# Datasets

The raw CSV files are **not tracked in this repository**. They come from the
course materials of the "SQL Data Warehouse Project" by Data with Baraa and are
kept locally to keep the repo lightweight.

## How to get the data

Download the project materials from:
https://www.datawithbaraa.com/ (SQL Ultimate Course → course materials)

## Expected folder structure

After downloading, place the files exactly like this:

datasets/
├── source_crm/
│   ├── cust_info.csv
│   ├── prd_info.csv
│   └── sales_details.csv
└── source_erp/
    ├── CUST_AZ12.csv
    ├── LOC_A101.csv
    └── PX_CAT_G1V2.csv

## Source systems

| Source | File | Content |
|---|---|---|
| CRM | cust_info.csv | Customer master data |
| CRM | prd_info.csv | Product info incl. historical prices |
| CRM | sales_details.csv | Sales transactions |
| ERP | CUST_AZ12.csv | Customer birth date and gender |
| ERP | LOC_A101.csv | Customer country |
| ERP | PX_CAT_G1V2.csv | Product categories and subcategories |

## Note on file paths

The `BULK INSERT` statements in `scripts/bronze/proc_load_bronze.sql` use
absolute paths. Update them to match your local directory before running
the ETL.
