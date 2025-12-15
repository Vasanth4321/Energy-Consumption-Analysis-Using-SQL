## Importing CSV Data into MySQL (MySQL Workbench)

This folder contains the raw CSV files used to populate the `ENERGYDB` database tables for the **Global Energy Consumption** project. Follow the steps below to import each CSV into MySQL Workbench.

### Prerequisites

- MySQL Server and MySQL Workbench installed.  
- The database schema created by running `sql_scripts/database_schema.sql` (tables such as `country`, `emission_3`, `population`, `production`, `consumption`, `gdp_3` must already exist).

### Recommended file–table mapping

Adjust names if your actual CSV filenames differ.

- `country.csv` → `country` table  
- `emission_3.csv` → `emission_3` table  
- `population.csv` → `population` table  
- `production.csv` → `production` table  
- `consumption.csv` → `consumption` table  
- `gdp_3.csv` → `gdp_3` table  

### Method 1 – Table Data Import Wizard (GUI)

1. Open MySQL Workbench and connect to your MySQL server.  
2. In the **SCHEMAS** panel, select the `ENERGYDB` database.  
3. Right‑click the target table (for example, `emission_3`) and choose **Table Data Import Wizard**.
4. Browse and select the corresponding CSV file from this `data/` folder, then click **Next**.  
5. Confirm the column mappings (ensure each CSV column is mapped to the correct table column and data type).  
6. Click **Next** and then **Finish** to start the import.
7. Repeat steps 3–6 for each remaining table/CSV pair.

After import, you can verify using:

SELECT * FROM COUNTRY;
SELECT * FROM EMISSION_3;
SELECT * FROM POPULATION;
SELECT * FROM PRODUCTION;
SELECT * FROM GDP_3;
SELECT * FROM CONSUMPTION;

### Notes

- Ensure the first row of each CSV contains column headers, and that the order and data types match the table definitions. 
- For large files, imports may take some time; avoid interrupting the process.  
- Once all CSVs are imported, you can run the analysis queries in `sql_scripts/analysis_queries.sql`.
