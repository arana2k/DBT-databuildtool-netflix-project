🎬 Netflix Analytics Engineering Pipeline (dbt + Snowflake)

An end-to-end analytics engineering project that transforms raw streaming/movie data into clean, tested, analytics-ready tables using dbt (Data Build Tool) and Snowflake — built to mirror how real data teams design production data pipelines.


📌 Project Overview

Streaming platforms like Netflix generate huge volumes of raw data (movies, ratings, users) that need to be cleaned, modeled, and validated before analysts and dashboards can trust it. This project simulates that real-world scenario:


Raw data (MovieLens dataset) is loaded into Snowflake
dbt transforms it through a layered modeling architecture (staging → intermediate → mart)
Automated tests catch data quality issues before they reach reports
Documentation and lineage graphs make the pipeline self-explanatory for any new team member


The result: a reliable, version-controlled, easy-to-extend data pipeline — the same approach used by modern data teams at companies of every size.


🧱 Architecture

Raw Source Data (MovieLens dataset)
        │
        ▼
   Snowflake (Data Warehouse)
        │
        ▼
 ┌────────────────────┐
 │   dbt Transformation │
 │  ┌────────────────┐  │
 │  │  Staging Layer  │  │  → clean & standardize raw data
 │  ├────────────────┤  │
 │  │ Intermediate    │  │  → apply business logic
 │  ├────────────────┤  │
 │  │  Mart Layer     │  │  → analytics-ready tables
 │  └────────────────┘  │
 └────────────────────┘
        │
        ▼
  Analytics / BI-ready Tables


🛠️ Tech Stack

LayerToolData WarehouseSnowflakeTransformationdbt (Data Build Tool)Modeling ApproachELT (Extract → Load → Transform)Data SourceMovieLens datasetTestingdbt native tests (not-null, unique, referential integrity)Documentationdbt-generated docs & DAG lineage graphs


✨ Key Features


✅ Layered dbt models — staging, intermediate, and mart models for clean separation of concerns
✅ Automated data quality tests — catches nulls, duplicates, and broken relationships before they hit production
✅ Auto-generated documentation — every model, column, and dependency is documented
✅ DAG-based lineage — visualize how data flows from raw source to final table
✅ Modular, version-controlled SQL — no more copy-pasted queries; each transformation is reusable and testable



📂 Project Structure

├── models/
│   ├── staging/        # Clean & standardize raw source data
│   ├── intermediate/   # Apply business logic & joins
│   └── marts/          # Final analytics-ready tables
├── tests/               # Custom data quality tests
├── dbt_project.yml      # dbt project configuration
└── README.md


🚀 What This Project Demonstrates

This project was built to practice and showcase core analytics engineering skills that are directly relevant to Data Engineer / Analytics Engineer roles:


Designing a warehouse-native ELT pipeline instead of legacy ETL scripts
Applying software engineering best practices (modularity, testing, docs, version control) to SQL
Structuring data models the way production data teams do (staging → marts)
Debugging and validating data using dbt's built-in testing framework



🙋 About This Project

This project was completed as a hands-on learning exercise while transitioning into Data Engineering, following a structured tutorial and rebuilding it independently to solidify the concepts. It reflects an actively growing skill set in dbt, SQL, and modern data warehouse design.
