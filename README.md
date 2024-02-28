# Initial_Data_Engineer_Task
NYC taxi analysis for January 2023


This project focuses on analyzing New York City yellow taxi trip data. The primary goal is to aggregate and visualize the total taxi fare amount per day for a specific month, January 2023. The project utilizes PySpark for data processing to handle large datasets efficiently, and Matplotlib for visualization to illustrate daily revenue trends.

Setup Instructions
1. Click on the link for the whole code

Discussion
Problem-Solving Process
The project began with understanding the structure and content of the NYC yellow taxi trip dataset. The main challenge was to efficiently process and aggregate large volumes of data. PySpark was chosen for its ability to handle large datasets distributed across clusters.

Challenges Faced
Data Quality: Encountered issues with incorrect or outlier tpep_pickup_datetime values. Implemented filters to ensure the analysis was restricted to January 2023.
Visualization: Needed to ensure that the aggregated data was correctly sorted by date before visualization.

Overcoming Challenges:
Data Filtering: Added explicit filters for tpep_pickup_datetime to include only January 2023 data.
Data Sorting: Ensured data was sorted in ascending order by date before plotting with Matplotlib.
