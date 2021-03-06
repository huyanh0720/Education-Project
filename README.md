# Education Project's Description

Hi everyone,

This is the first project of Anh Huy Ha. My project topic is Evaluating class quality based on teachers, students, subject information, and feedback.

The scenario: One very well-known education center X has one dataset of the students’ reviews. This company wants to analyze the class quality by student feedback based on their report card.

The Guideline:
- Here is the roadmap of what I do from generating data to visualizing them.

![Roadmap](https://github.com/nhinguyen78/Project_Group1_education/blob/master/DataRoadMap.jpg)

- First of all, what I do is I generate data by Python code as OLTP data and we save it as a .csv file, named (untitled RawData.csv)

- Second, I create a data pipeline in SQL Server Integration Services (SSIS), which is we load the .csv file. From the file, we ETL it to other Dim tables such as Dim Instructor, Dim Student, Dim Course. Each dims have their unique Primary key in order to create a relationship with the Fact table later.

- After the data in all dims has been transformed, I load them to the Cloud destination, called Snowflake. Our server name is: cf43998.southeast-asia.azure.snowflakecomputing.com

- After all, dims are all there, I will load the big Fact table on the Cloud too.

- Next our 3 dims and 1 fact is at the Cloud server, I create relationships between these tables with the lookup tool in SSIS one last time.

- Finally, the data model is finished and ready to visualize by PowerBI tool.

How to setup
1. Use the raw data in raw-code
2. Login MSSQL and run the script
3. Authen Snowflake and run
Please click [Snowflake](https://cf43998.southeast-asia.azure.snowflakecomputing.com/console#/partner)

User for tester 1: longbv
Password: password123

Use for tester 2: mainq
Password: password123

4. Link to PowerBI Visualization
Please click [PowerBI](https://app.powerbi.com/links/sSEb4dRLaw?ctid=f01e930a-b52e-42b1-b70f-a8882b5d043b&pbi_source=linkShare)
