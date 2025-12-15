## SQL Scripts Overview

This folder contains all SQL scripts used to build and analyze the **Global Energy Consumption** database. It is organized so you can first create the schema, then run the analysis queries, or use a single full script if you prefer.

### Files

- `database_schema.sql`  
  - Creates the `ENERGYDB` database and all core tables (`country`, `emission_3`, `population`, `production`, `consumption`, `gdp_3`).  
  - Defines primary keys, foreign keys, and relationships needed for energy–economy analysis.

- `analysis_queries.sql`  
  - Contains all `SELECT` statements used in the project to answer business questions, such as:  
    - Global and country‑level emission trends over time.  
    - Per‑capita energy consumption and production.  
    - Emission‑to‑GDP ratios and major GDP economies’ energy patterns.

- `full_script.sql`  
  - Convenience script that combines `database_schema.sql` and `analysis_queries.sql` in a single file.  
  - Useful if you want to set up the schema and immediately run all analysis queries in one go.

### How to use these scripts

1. Open your SQL client (for example, MySQL Workbench).  
2. Run `database_schema.sql` to create the `ENERGYDB` database and all tables.  
3. Import the CSV files from the `data/` folder into their corresponding tables.  
4. Run `analysis_queries.sql` to reproduce the insights and answer the analysis questions documented in the main project README.

### Notes

- Scripts are written for MySQL 8.x and use features such as window functions for growth‑rate calculations.  
- If you adapt the project to another SQL dialect, adjust data types, date functions, and window‑function syntax as needed.
