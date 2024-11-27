# Data Exploration and Analysis with SQL

# Overview
This project explores the COVID-19 pandemic's global impact using SQL queries to analyze datasets containing information on deaths, infections, and vaccinations across different locations. The analysis involves a series of data exploration steps, such as filtering, aggregating, and calculating various metrics (e.g., infection rates, death rates, and vaccination progress). The goal is to extract actionable insights using advanced SQL techniques including joins, Common Table Expressions (CTEs), temporary tables, window functions, and data aggregation.

#Structure
This project is divided into multiple SQL queries, each focused on a specific aspect of COVID-19 data exploration:

- **Initial Data Extraction**:
    - Extracts data from the CovidDeaths and CovidVaccinations tables to review the raw data.
- **Infection Rate Analysis**:
    - Calculates the percentage of the population infected with COVID-19 across different locations.
    - Identifies countries with the highest infection rates.
- **Death Rate Analysis**:
    - Calculates the death percentage in relation to total cases, providing insight into the likelihood of dying from COVID-19 in different countries.
    - Identifies countries with the highest death counts per population.
- **Global Overview**:
    - Provides a global summary of new COVID-19 cases, deaths, and the death percentage based on aggregated data.
- **Continental Breakdown**:
    - Breaks down the data by continent to analyze which continents experienced the highest death counts relative to population.
- **Vaccination Analysis**:
    - Compares the total population to the number of people vaccinated.
    - Shows the percentage of the population vaccinated based on new vaccination data, using both rolling sums and window functions for calculations.
- **CTE & Temporary Tables for Aggregation**:
    - Uses Common Table Expressions (CTEs) and Temporary Tables to perform calculations and store intermediate results for analysis. This ensures that calculations on cumulative vaccinations are partitioned by location.
- **View Creation**:
    - Creates a view to store the data for later use in visualizations and further analysis.

# Key Techniques Used
- **Joins**: Used to combine CovidDeaths and CovidVaccinations data based on common columns (location and date).
- **Common Table Expressions (CTEs)**: Used for cleaner SQL code, enabling complex calculations, especially when partitioning data (e.g., calculating rolling sums of vaccinations).
- **Temporary Tables**: Used to store intermediate results for further querying and analysis, particularly in the calculation of vaccination percentages.
- **Window Functions**: SUM() OVER (PARTITION BY ...) was used to calculate cumulative or rolling totals, such as total vaccinations.
- **Aggregate Functions**: Utilized SUM(), MAX(), and other aggregate functions to perform data summarization, such as total cases, total deaths, and death percentages.
- **Data Type Conversion**: Ensures correct data types for calculations, especially when dealing with numeric columns.

  
