/*
============================================
create database and schema
============================================

Script purpose
    This script creates a new database 'Datawarehouse' after checking if it already exists.
	if the database exists, it is dropped and recreated, additionally, the script sets up three schemas 
	within the database: 'bronze', 'silver', 'gold'.

Warning
      Running this script will dropp the entire 'DataWarehouse' database if it exists.
	  all data in the database will be permanently deleted. proceed with caution
	  and ensure you have proper backup before running this script
*/



USE MASTER;
GO

IF EXISTS (SELECT 1 FROM sys.databases	WHERE name = 'DataWarehouse')
BEGIN 
  ALTER DATABASE DataWarehouse SET SINGLE_USER WITH rollback immediate ;
  DROP DATABASE DataWarehouse;
  END;
  GO

-----Create the 'DataWarehouse' database
CREATE DATABASE DataWarehouse;
GO

USE DataWarehouse;
GO

CREATE SCHEMA bronze;
GO

CREATE SCHEMA silver;
GO

CREATE SCHEMA gold;
GO
