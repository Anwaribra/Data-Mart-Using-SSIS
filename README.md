# Data Mart Using SSIS
- A data mart is a *subset of a data warehouse* that is focused on a specific business area or team, such as sales, finance, or marketing. It is designed to meet the specific needs of a particular group of users who need access to a specific segment of data for analysis and decision-making purposes.   
  
**There are three main types of data marts:**    

- Independent Data Marts: These are developed without a centralized data warehouse and are created by extracting data directly from operational systems or external sources.
- Dependent Data Marts: These are created from a centralized data warehouse. This ensures that the data mart contains consistent, cleansed, and integrated data.
- Hybrid Data Marts: These combine input from existing data warehouses with additional operational source data.

 ## Setting Up SSIS 
- Install SQL Server Data Tools (SSDT): SSDT includes templates and tools for building SSIS packages.
- Create an SSIS Project: In Visual Studio with SSDT, create a new Integration Services project.
  
 ### _Developing SSIS Packages_ 
   + Data Flow Tasks: Create data flow tasks for each ETL process. These tasks will extract data from source systems, transform it (e.g., cleaning, aggregating, merging), and load it into the data mart.
   + Control Flow: Design the control flow to manage the order of execution and the logical sequence of data flow tasks.
   + Transformations: Implement transformations such as lookups, derived columns, conditions, etc., to prepare the data for the data mart.
  + Connection Managers: Set up connection managers to connect to your data sources and destinations.

#### _Loading the Data Mart_
+ Incremental Loads: Implement logic to handle incremental data loads if the data mart will be refreshed periodically. This may involve timestamp or change data capture (CDC) mechanisms.
+ Error Handling: Add error handling within your SSIS packages to manage and log errors during ETL processes.
+ Performance Tuning: Optimize package performance through techniques like proper indexing, minimizing data at the source, using appropriate transformations, and managing transaction sizes.

#####  _Deployment and Scheduling_ 
 + Deploy the SSIS Packages:Deploy your SSIS packages to an SQL Server instance or SSIS Catalog.
 +  Schedule the Packages: Use SQL Server Agent or another scheduler to execute the SSIS packages at regular intervals (e.g., nightly, weekly).
