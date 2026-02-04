# Data Warehouse & Business Intelligence Term Project (Fall 2023)

**BS Data Science – Data Warehouse & Business Intelligence Lab**  

## Objective

This project demonstrates the complete **Business Intelligence lifecycle** by:
- Extracting data from two heterogeneous OLTP sources (Northwind_Source1 & Northwind_Source2)
- Integrating external gender files
- Performing ETL in SSIS with staging, transformations, and deduplication
- Designing and populating a dimensional data warehouse (DW_Northwind)
- Building a multidimensional OLAP cube in SSAS with hierarchies and measures
- Performing OLAP operations (roll-up, drill-down, slice, dice)
- Answering analytical questions using the cube
- (Optional) Developing a Power BI dashboard for visual insights

## Project Components

- **BPMN Diagrams**  
  - Control Flow BPMN (high-level ETL workflow)  
  - Data Flow BPMN (detailed entity movement & transformations)

- **ETL Implementation (SSIS)**  
  - Multi-source extraction (Source1, Source2, gender files)  
  - Staging load with SourceSystem tracking  
  - Gender standardization & overlap resolution  
  - Dimension loading (surrogate/business keys, deduplication, lookups)  
  - Sales fact loading with SalesAmount calculation and all dimension key lookups

- **Data Warehouse Schema**  
  - Star schema with Sales fact and dimensions: Customer, Employee, Time, Product, Supplier, Shipper, Category, CustomerContactCategory, EmployeeCity  
  - Continuous Time dimension (YYYYMMDD keys)

- **SSAS OLAP Cube**  
  - Dimensions with hierarchies:  
    - Time: Year → Quarter → Month → Day  
    - Product: Category → Product  
    - Employee Geography: Country → City → Employee  
  - Measures: Total Sales Amount, Total Quantity, Average Unit Price, Average Discount, Order Count, Average Order Size (calculated)

- **OLAP Operations Demonstrated**  
  - Roll-up, drill-down, slice, dice (screenshots included)

- **Analytical Questions Answered**  
  - Highest revenue employee in 2025  
  - Best category per quarter  
  - Top supplier per category  
  - Shipper with most high-value orders  
  - Product with highest average order size  
  - Male vs Female customer profitability  
  - Months with unusual sales drops  
  - Top 5 customers by revenue  
  (all answered with cube browser screenshots)

