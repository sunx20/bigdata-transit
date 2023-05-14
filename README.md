# bigdata-transit

Project Overview: 
The purpose of this project is to analyze transit data for Chattanooga from 2020 to 2022, with the goal of identifying trends and correlations between transit usage, demographic variables, weather patterns, and COVID-19 impacts. To achieve this goal, we will merge data from multiple sources, including the census data, weather data, and APC data of Chattanooga. We will use Spark and AWS Athena for queries and joins, and create interactive plotly charts as well as seaborn graphs to visualize our findings.

Main Project Tasks: 
- Data Integration: We will merge the census data, weather data, and APC data of Chattanooga into a single dataset. This will involve cleaning and preprocessing the data, as well as performing data quality checks to ensure that the merged dataset is accurate and complete.
- Route Analysis: We will analyze the top five used routes specifically on their directions and trip times over the last two years. We will demonstrate how their trends have changed per month. This analysis will help us identify any seasonal variations in transit usage.
- Demographic Analysis: We will correlate transit usage with demographic variables in each census tract. This will involve merging the census data with the transit data, and using statistical analysis to identify any correlations between transit usage and demographic variables such as median household income. Finally, interactive plotly charts will be used to visualize the results.
- Weather Analysis: We will analyze the impact of weather on transit usage. We will identify if there is any correlations between weather patterns (e.g., temperature, precipitation) and transit usage. We will use seaborn to visualize the correlation.
- COVID-19 Analysis: We will compare transit usage during the COVID-19 pandemic to transit usage from recent times. This will involve analyzing changes in transit ridership, as well as any changes in the most popular routes and directions. Interactive plotly charts will be employed to compare the percentage drop in ridership in different areas and their corresponding economic status.

Design of Solutions:
To handle the specific work of merging census data, weather data, and APC data for analysis of transit usage in Chattanooga, we will use Amazon S3 for data storage. S3 is an excellent choice for storing large amounts of data, and we will store each type of data in a separate folder within S3 for ease of access and organization.
We will use Apache Spark for data merging, as it is a highly scalable processing engine that can handle large-scale data processing tasks quickly. We will join the data sets using common attributes such as date, time, and location, and the merged data will be stored back in S3.

For data querying and analysis, we will use AWS Athena, which will allow us to query and analyze the data stored in S3 using SQL queries. Athena crawlers will automatically infer the schema of the data and create tables for querying, and we will aggregate the data to calculate trends in the most used routes, directions, and trip times. The query results will be stored back in S3 for later use.

Finally, we will use Plotly and Seaborn for data visualization, as they provide a flexible and powerful way to create interactive charts and dashboards. We will use Plotly to generate charts that show transit usage in a census tract and correlate it with demographic variables. We will use Seaborn to identify any trends or correlations between weather and transit usage. The data visualization will be presented through an html web interface, allowing for easy access and use of the visualizations.
