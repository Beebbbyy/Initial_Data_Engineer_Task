# Initial_Data_Engineer_Task
NYC taxi analysis for January 2023


This project focuses on analyzing New York City yellow taxi trip data. The primary goal is to aggregate and visualize the total taxi fare amount per day for a specific month, January 2023. The project utilizes PySpark for data processing to handle large datasets efficiently, and Matplotlib for visualization to illustrate daily revenue trends.

A. Setup Instructions
1. Click on the link for the whole code

B. Setting Up SQL Server on Docker (Mac Specific)
Task 2 requires loading cleaned data into a SQL database. On a Mac, this involves setting up SQL Server using Docker:

Install Docker: Download and install Docker Desktop for Mac from the official Docker website.
Pull SQL Server Image: Open Terminal and pull the SQL Server Docker image:
bash
Copy code
docker pull mcr.microsoft.com/mssql/server:2019-latest
Run SQL Server Container: Start an instance of the SQL Server container:
bash
Copy code
docker run -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=YourStrong!Passw0rd' \
-p 1433:1433 --name sqlserver \
-d mcr.microsoft.com/mssql/server:2019-latest
Replace YourStrong!Passw0rd with a strong password.
Connect to SQL Server: Use a SQL client that supports SQL Server. For command-line usage, you can use sqlcmd:
bash
Copy code
docker exec -it sqlserver /opt/mssql-tools/bin/sqlcmd \
-S localhost -U SA -P 'YourStrong!Passw0rd'


**Execution Instructions**
Data Extraction and Cleaning: Refer to the previous sections for extracting and cleaning the dataset using PySpark.
Load Clean Data into SQL Server:
Ensure the SQL Server Docker container is running.
Use the provided Python script to connect to SQL Server and load the cleaned data. The script will use SQLAlchemy (or pyodbc) for database connection and operations.

**Discussion**

Insights, Challenges, and Assumptions
Mac-Specific Setup: Task 2 involves additional steps for Mac users, including using Docker to run SQL Server. This approach ensures compatibility across different operating systems.
Data Loading: The process of connecting to SQL Server from a Mac using Docker and loading data into it is detailed in the setup instructions, acknowledging that direct connectivity might differ from traditional methods.
