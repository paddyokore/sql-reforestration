Data located in the data folder and instructions to set up database
```SQL
-- Create the land_area table
CREATE TABLE "land_area" (
    "country_code" VARCHAR(3),
    "country_name" VARCHAR(255),
    "year" INT,
    "total_area_sq_mi" NUMERIC
);

-- Import data from land_area.csv into the land_area table
COPY land_area 
FROM 'C:\Program Files\PostgreSQL\16\data\forestation_data\la.csv' 
DELIMITER ',' CSV HEADER;

-- Create the forest_area table
CREATE TABLE forest_area (
    country_code VARCHAR(3),
    country_name VARCHAR(255),
    year INT,
    forest_area_sqkm NUMERIC
);

-- Import data from forest_area.csv into the forest_area table
COPY forest_area 
FROM 'C:\Program Files\PostgreSQL\16\data\forestation_data\fa.csv' 
DELIMITER ',' CSV HEADER;

-- Create the regions table
CREATE TABLE regions (
    country_name VARCHAR(255),
    country_code VARCHAR(3),
    region VARCHAR(255),
    income_group VARCHAR(255)
);

-- Import data from regions.csv into the regions table
COPY regions 
FROM 'C:\Program Files\PostgreSQL\16\data\forestation_data\r.csv' 
DELIMITER ',' CSV HEADER;
```
