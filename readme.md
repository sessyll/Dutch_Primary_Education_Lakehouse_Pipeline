# Dutch Primary Education Lakehouse Pipeline

An end-to-end Lakehouse pipeline built with Databricks, PySpark and Delta Lake for historical analysis of Dutch primary education data.

**PySpark • Delta Lake • Spark SQL • Databricks • Lakehouse Architecture • Window Functions**

## Overview

The project begins with data exploration and preparation before implementing a Bronze, Silver and Gold Lakehouse pipeline in Databricks.

Using PySpark, Spark SQL and Delta Lake, the pipeline transforms, validates and models Dutch primary education data into business-ready analytical tables.

## Project Objectives

- Build a modern Lakehouse pipeline using the Medallion Architecture
- Store data in Delta format across Bronze, Silver and Gold layers
- Clean, transform and validate educational datasets
- Perform historical trend analysis from 1996 to 2025
- Demonstrate core PySpark, Spark SQL and Delta Lake features

## Dataset

The project uses two Dutch primary education datasets:

- School establishment information
- Historical student counts (1996–2025)

The datasets are joined using school identifiers to create a unified analytical dataset for historical reporting.

## Architecture

```
                    CSV Source Files
                           │
                           ▼
                  Data Exploration
                           │
                           ▼
             Data Preparation & Cleaning
                           │
                           ▼
               Bronze Delta Tables
             ├── schools
             └── students
                           │
                           ▼
                 Silver Delta Tables
             ├── schools_students
             └── students_long
                           │
                           ▼
                  Gold Delta Tables
             ├── denomination_summary
             ├── largest_schools
             └── province_year_trends
```

## Pipeline Overview


1. Explore and profile the raw datasets
2. Clean and prepare the data
3. Build Bronze Delta tables
4. Create Silver transformation tables
5. Generate Gold analytical tables
6. Validate pipeline outputs

## Key Features

- Medallion (Bronze, Silver, Gold) architecture
- Delta Lake tables
- Spark SQL
- Window Functions
- Schema Evolution
- Time Travel
- UPDATE, DELETE and MERGE
- Broadcast Join
- Execution Plan analysis
- Repartition and Coalesce
- Wide-to-Long transformation
- Data validation

## Results

| Layer | Output |
|-------|--------|
| Bronze | Raw Delta tables |
| Silver | Cleaned and transformed datasets |
| Gold | Business-ready analytical tables |


### Final Pipeline Metrics

- Bronze tables: **2**
- Silver tables: **2**
- Gold tables: **3**
- Schools: **6,122**
- Historical years: **30**
- Long-format records: **183,660**

### Data Source

The datasets were obtained from the Dutch Ministry of Education (DUO) open data portal.

Source:
https://duo.nl/open_onderwijsdata/# Dutch_Primary_Education_Lakehouse_Pipeline
