# Data-ingestion-into-an-Azure-SQL-table

Environment Setup

Data Set:
Custom curated data set – for one table only. One CSV file of 27 GB, 110 M records with 36 columns. The input data set has one file with columns of type int, nvarchar, datetime etc.
Database:
Azure SQL Database – Business Critical, Gen5 80vCores

ELT Platform:
Azure Databricks – 6.6 (includes Apache Spark 2.4.5, Scala 2.11)
Standard_DS3_v2 14.0 GB Memory, 4 Cores, 0.75 DBU (8 Worker Nodes Max)

Storage:
Azure Data Lake Storage Gen2

Overview of Loading Data into Columnstore Indexes here: Data Loading performance considerations with Clustered Columnstore indexes
In this project, the data was loaded from a CSV file located on Azure Data Lake Storage Gen 2. The CSV file size is 27 GB having 110 M records with 36 columns. This is a custom data set with random data.

A typical high-level architecture of Bulk ingestion or ingestion post-transformation (ELT\ETL) would look similar to the one given below:
	
![image](https://github.com/josh2511/Data-ingestion-into-an-Azure-SQL-table/assets/47291459/5f9934b9-86f4-4abe-9599-5f5233d81120)

	
	
