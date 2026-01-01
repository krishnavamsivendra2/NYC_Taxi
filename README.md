🚕 NYC Taxi Data Engineering Project (Azure + Databricks)
📌 Project Overview

This project implements an end-to-end data engineering pipeline using the NYC Taxi dataset, designed to simulate a real-world analytics data platform on Azure.

The focus is on:

    Scalable data ingestion
    
    Clean layered architecture
    
    Delta Lake–based analytics tables
    
    BI-ready Gold layer design
🏗️ Architecture
Azure Data Lake Storage Gen2 -> Bronze -> Silver -> Gold (Delta Lake)

🔧 Tech Stack

    Azure Data Lake Storage Gen2 (ADLS)

    Azure Databricks

    Apache Spark (PySpark)

    Delta Lake

    Hive  Metastore

    Power BI (conceptual consumption)
🥉 Bronze Layer

    Raw NYC Taxi data ingestion

    Explicit schema enforcement

    Minimal transformations

    Stored in ADLS Gen2
🥈 Silver Layer

      Data cleansing and standardization

    Handling:

        Null values

        Deprecated columns (e.g., ehail_fee)

        Inconsistent formats

        Prepared datasets for analytics use cases
  🥇 Gold Layer

    Analytics-ready Delta Lake tables

    Aggregated and curated business datasets

    Stored as Delta tables and registered using Hive Metastore

    Optimized for BI and reporting use cases

>Note:
>Unity Catalog admin features were not available in the personal Databricks environment, so Hive Metastore was used.
>The design is fully compatible with Unity Catalog in enterprise environments.

📊 Analytics & BI

    Gold tables are designed to be consumed by BI tools like Power BI

    Integration can be achieved via:

    Databricks SQL

    Or curated Parquet exports (if required)
🧠 Key Learnings

    Real-world schema handling and evolution

    Delta Lake fundamentals (ACID, MERGE, time travel)

    Practical understanding of:

    Hive Metastore vs Unity Catalog

        Platform constraints in personal environments
    Designing BI-ready data models
    
🚀 Future Enhancements

    Enable Unity Catalog in enterprise setup

    Incremental Gold layer updates using MERGE

    Advanced Delta optimizations (OPTIMIZE, Z-ORDER)

    Full Power BI dashboards

🙌 Acknowledgements

    This project was built with a learn-by-doing approach, focusing on practical challenges faced in real data engineering systems.

📬 Contact

    Feel free to connect or provide feedback via LinkedIn or GitHub.
