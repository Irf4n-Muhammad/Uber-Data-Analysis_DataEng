# Data-Engineering-Project / Uber Data Analysis

# (STILL IN PROGRESS, WILL BE UPDATED SOON)


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
3. Put the id (Primary key and foreign key.

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


### 6.2 Terraform:

<img width="700" alt="image" src="https://github.com/Irf4n-Muhammad/Data-Engineering-Project_COVID19-Dataset/assets/121205860/2faa8507-d149-4bc5-889d-9381c84f21be">

The terraform will help us to make the stable and organizable environment for our google cloud and it's very easy to monitor since we only use python file to control. You can even share it to other team member if you work in group, so you all can assure using the same environment set up.

1. Set the main.tf
2. Set the variable.tf
3. Run the terraform through some command :
   1. terraform init = initialize the terraform
   2. terraform validate = check and validate that it's proper update
   3. terraform plan = you can see what's the update and what's new in your environment
   4. terraform apply = run and make the update

## 7. Airflow:

<img width="700" alt="image" src="https://github.com/Irf4n-Muhammad/Data-Engineering-Project_COVID19-Dataset/assets/121205860/0b299387-a421-49b7-aa4c-97c7816b37a9">

Airflow is a tool to help the data engineer to monitor the ingesting data process. We can create the workflow by our own using python file and we can edit as like as we want. Here are some sets up to run the Airflow:

1. Prepare the Dockerfile (check the environment that will be used for ingesting the data)
2. Prepare the docker-compose.yaml (fill some specific variable based on your personal data)
3. Prepare .env file
4. Prapare the requirements.txt file
5. Open the virtual machine and connect to the host (you can find it on vs code)
6. Set the port (8080), make sure there is no machine using the same port
7. Run the docker-compose build in directory that has docker-compose.yaml and Dockerfile
8. Run the docker-compose up airflow-init to initialize the airflow
9. Run the docker-compose up, wait until all the image has settled
10. Open the search engine (google, bing, etc) and open the web ( localhost:8080 )
11. Wait until the loading ended
12. Sign in the airflow using the password and username that you set before (in docker-compose.yaml)
13. Choose the DAG file that you want to run
14. Trigger the DAG
15. If all task has dark green color (which means succeed), then please check your gcs bucket or bigquery (only if your DAG file has a task sending the file to the bgquery)
16. If there is an error, then click the square task and click log button to see what's the message giving to you the error information
    There are several thing that I ever experienced that cause an error:
    1. Airflow version is too low - Solution = Set the latest version in your Dockerfile and when you run the docker-compose build
    2. DAG issue - Solution = Since it would be very specific, so please check the log to see what's error there
    3. PORT is occupied - Solution : If you're using the docker, then you can find out what's machine that may use that port and you can delete that image in the docker (you can use docker apps or type the command in the git bash)

## 8. Apache Spark

<img width="700" alt="image" src="https://github.com/Irf4n-Muhammad/Data-Engineering-Project_NIFTY-50-Stock-Market-Data/assets/121205860/0e5461ea-cd71-4472-9707-ba22cf96488b">

Spark is the best tool to handle large dataset and transform it to be useful and clean data. It will be used to download(extract) and will ingest into the google cloud storage bucket or bigquery using dataproc. 

The general idea about what we gonna do in spark:
So basically we wanna try to transfrom all 50+ data to be one file that cover the essential information that we need. We will merge the whole stocks data, which we have identified has the same number and column name. In case, there is an issue (according to name or data type that probably a bit different (in my case, I found one column that supposed to be date and not integer)). Then, there is one file that is additional informatiion of the entire stocks that we will join that as well using .join. After that we gonna partition by years for each company to see the progress of the stock year by year. 

1. Firstly, set the virtual machines using linux or in my case, I am using google cloud VM.
2. Export the python argument to the terminal to init the pyspark, so it can be connected to the jupyter notebook eventually.
3. Open jupyter notebook and create the new folder.
4. Set the connection into the google cloud platform
5. Import the pyspark and any package you need
6. Create the spark variable using SparkSession.builder
7. Read the file using spark.read
8. Check the schema using .schema or printSchema()
9. Edit the schema if needed to decrease the number of storage and fasthen the sending process
10. Add and renamed the column if you think it will be benefitial
11. Do the join if you need
12. Input registerTempTable("file-nname")
13. Using spark.sql to use the SQL command to your file
14. Send to the bigquery afterwards
15. Convert it to the pyhton script
16. Using argparse package to receive the variable from our python command which will be inserted into our terminal
17. Set up the cluster and run the job
18. If succeed, please check the bigquery to make sure.
19. Your work has done

## 9. Google Data Studio:

<img width="700" alt="image" src="https://github.com/Irf4n-Muhammad/Data-Engineering-Project_COVID19-Dataset/assets/121205860/5e3bd7a1-eee6-43a8-8912-985be393722e">

It's pretty simple, you can connect your bigquery with google data studio and use the created table to be visualized. Build your dasboard which with the hope, it can answer all the problem solving question clearly.

These are my dashboard:

<img width="725" alt="image" src="https://github.com/Irf4n-Muhammad/Data-Engineering-Project_NIFTY-50-Stock-Market-Data/assets/121205860/9f39fa24-adfc-43e8-9c3c-2bda5d5d8006">
<img width="720" alt="image" src="https://github.com/Irf4n-Muhammad/Data-Engineering-Project_NIFTY-50-Stock-Market-Data/assets/121205860/15c07694-dfa6-497d-b841-104f7ac13a28">


From this two data visualization, we could get many information:
1. The most expensive stocks since 2000 - 2021
2. The progress of stock indicator in every year
3. The industrial category that going up and down in different era
4. Analyze why certain stock was booming and others was not
5. Find the pattern of similar situation that can use to predict the future stocks
6. etc



## Reference Link:

https://w0.peakpx.com/wallpaper/252/11/HD-wallpaper-stock-market-perfect-line-chart-representation-chart-pattern-thumbnail.jpg
