# Data-Engineering-Project / Uber Data Analysis

## 1. Description of the Problem:
In the arena of urban transportation planning and ride-hailing services, data analysts frequently utilize historical ride data to develop predictive models. These models are used to forecast future demand, optimize route planning, and inform strategic business decisions.

Take, for instance, an analyst at Uber. The predictive model they work with employs a time-series analysis approach, utilizing historical data such as ride timestamps, origin-destination pairs, ride duration, and wait times, among other relevant indicators.

However, one significant challenge with this approach arises due to the dynamic and unpredictable nature of the urban transportation environment. Unforeseen events like sudden changes in weather conditions, major city events, traffic disruptions, and changes in local regulations can all significantly impact ride demand and availability.

![image](https://github.com/Irf4n-Muhammad/Data-Engineering-Project_Uber-Data-Analysis/assets/121205860/d7eb4dd5-5130-44bc-bba1-0aa456100c6b)

Using the Uber datasets as an example, user behavior and ride demand patterns can differ significantly based on the aforementioned factors. A prediction algorithm that relies heavily on historical data might generate inaccurate forecasts, leading to inefficient resource allocation, suboptimal service levels, and potential revenue loss.

Another complication could arise when these datasets are used across different geographical locations. Uber operates in numerous countries, and the ride data is influenced by local context, such as traffic patterns, cultural practices, and regional regulations. If an analyst does not factor in these local variations while analyzing the datasets, it could lead to incorrect conclusions and decisions.

These scenarios underline the importance of combining historical data analysis with a keen understanding of current local context, relevant events, and other crucial factors to make informed and prudent business decisions.

## 2. Objective:
The datasets containing historical ride data from Uber are invaluable for a multitude of applications. They can be used by urban planners, transportation analysts, and economists for in-depth analysis of urban mobility patterns, demand forecasting, and traffic management.

For Uber and other ride-hailing services, these datasets can serve to optimize service levels, pricing strategies, and resource allocation. By analyzing past ride data, the company can anticipate demand hotspots, identify peak service times, and uncover trends and patterns that can guide strategic and operational decisions.

Furthermore, the datasets can be used for academic and educational purposes, allowing students and researchers to understand urban mobility patterns, study the impact of events on ride demand, and analyze the effects of ride-hailing services on urban transportation systems.

Each Uber dataset, typically structured in .csv files, includes fields like ride timestamps, origin and destination coordinates, ride duration, and wait times. However, despite their immense utility, these datasets have certain limitations. They represent historical patterns, do not account for sudden external events or local context variations, and rely on the accuracy of the recorded data. It's essential to consider these limitations when using this data for predictive modeling or decision-making purposes.

Lastly, it's crucial to use this dataset responsibly, maintaining user anonymity, ensuring data privacy, and complying with all applicable laws and regulations.
## 3. Technologies:

The choosen technologies is variative and depends on the case and condition. There are some option for certain case and in this case, I am using this option since it's the easiest.

- Jupyter notebook
- Mage
- Google VM Instances
- GCS (Google Cloud Storage)
- Google Bigquery
- Google Data Studio

## 4. Data Architecture:
<img width="700" alt="image" src="https://github.com/Irf4n-Muhammad/Data-Engineering-Project_Uber-Data-Analysis/assets/121205860/75b47d8f-2dea-4b43-89bf-c3b504181c2e">

## 5. Data Description:

The data include all track record of the Uber or NYC taxi data. It consists some columns which we will be generated to be some tables.

These data was collected from kaggle : https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

## 6. Draw.io

![image](https://github.com/Irf4n-Muhammad/Data-Engineering-Project_Uber-Data-Analysis/assets/121205860/c8f876ea-4e45-45e1-9b1b-68cb902375dc)

1. Design the database by building main table (fact table) and branch table (dimension table)
2. Fact table consist the numeric data and the dimension table consist the context of that numeric data.
3. Put the id (Primary key and foreign key).

![image](https://github.com/Irf4n-Muhammad/Data-Engineering-Project_Uber-Data-Analysis/assets/121205860/791287db-7496-4b9d-98e5-bd6c15570201)


## 7. Jupyter Notebook

![image](https://github.com/Irf4n-Muhammad/Data-Engineering-Project_Uber-Data-Analysis/assets/121205860/ad17d8d4-0ad7-4ebe-8f12-6606b826bd25)

1. To access the jupyter notebook can use the VM instances (which be provided in GCP) or just use your initial OS.
2. Create the github repo and run 'git clone' in new directory.
3. Import the necessary package
4. Download the data from the website using ( !wget <link address> )
5. Create the table by duplicate the column from the initial big table
6. Generate the id (Primary key of the table) by using the index (It will generate the number from 1)
7. Arrange the sequence of the column of each table
8. Do the same thing for all table
9. Lastly, merge all the table and arrange the sequence of the table column.

   
## 8. Mage:

![image](https://github.com/Irf4n-Muhammad/Data-Engineering-Project_Uber-Data-Analysis/assets/121205860/34f73eaf-6bf1-4b6d-9409-0a435138996d)


In this project, we will use mage which is the modern data pipeline platform. We can do many things here such as load, transform, and export.

1. So the firstly, we need to open our Virtual Machine (In this case, I am using google cloud VM Instances)
2. Run the requirement environment
3. Initialize the mage tool by using the command in mage website
4. Start the project by typing ( mage start <name-of-project> )
5. Now, in your google account, please set the permission to allow the 6789 port which we gonna use for our localhost (Set in the firewall section in GCP)
6. Also, copy your external IP address of your VM instances and add the port ( <externalIPAddress>.6789 )
7. Then, your mage webpage will be opened
8. Then, we gonna create the data pipeline for three steps (extract, load, transformation)


## Google Bigquery:

<img src="https://github.com/Irf4n-Muhammad/Data-Engineering-Project_Uber-Data-Analysis/assets/121205860/9ac37ead-7a01-4829-b7e1-96bc6f90d817" width="600" height="400">

Bigquery platform can be accessed in GCP. Since in the previous step, the load step has created the table in bigquery, so we can directly write the SQL comman to create one table that will be used for data visualization. This table will consist all the information from the entire table but referring to that table (we use join command to connect all of them)

1. Join the fact tables with the dimension tables
2. Select all the columns and merge to become one table

## 7. Google Data Studio:

<img width="700" alt="image" src="https://github.com/Irf4n-Muhammad/Data-Engineering-Project_COVID19-Dataset/assets/121205860/5e3bd7a1-eee6-43a8-8912-985be393722e">

It's pretty simple, you can connect your bigquery with google data studio and use the created table to be visualized. Build your dasboard which with the hope, it can answer all the problem solving question clearly.

These are my dashboard:

<img width="722" alt="image" src="https://github.com/Irf4n-Muhammad/Data-Engineering-Project_Uber-Data-Analysis/assets/121205860/5909905f-6c24-4bf7-b1b5-e4b23cc22696">



From this two data visualization, we could get many information:
1. Number of services usage in certain location
2. The amount of that services in certain interval time
3. The most frequent used services in total
4. etc
