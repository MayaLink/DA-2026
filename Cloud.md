Cloud Architecture

The Bottom (Storage): AWS S3 / Azure Blob / GCS (The Lake part).
The Middle (Metadata Layer): Delta Lake / Apache Iceberg / Apache Hudi. This is the "manager" that keeps track of versions and transactions.
The Top (Compute Engine): Databricks / Snowflake / BigQuery (The Warehouse part).


Data Storage

Warehouse: Fast and organized, but expensive and rigid.
Lake: Cheap and holds everything, but can become a "swamp" of unorganized files.
Lakehouse: Uses a metadata layer (like Delta Lake) to give you the speed of a Warehouse on the cheap storage of a Lake.


SQL vs noSQL

### Database Comparison: SQL vs. NoSQL


| Feature | SQL (Postgres/MySQL) | MongoDB (NoSQL) | Redis (NoSQL) |
| :--- | :--- | :--- | :--- |
| **Storage** | Hard Drive (Tables) | Hard Drive (JSON Docs) | **RAM (Memory)** |
| **Schema** | Rigid (Fixed columns) | Flexible (JSON/BSON) | Simple (Key-Value) |
| **Speed** | Moderate | Fast | **Extreme (Low Latency)** |
| **Best For** | Financials / Reporting | Mobile Apps / Catalogs | Caching / Real-time |
| **Data Type** | Structured | Semi-Structured | Unstructured/Temporary |


