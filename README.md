## Cloud based Youtube Data Analysis and Data Engineering Project

### The  Requirement from the client:
- Want to launching new data-driven campaign, and for that they want to do marketing via advertisement 
- Main advertising channel: YouTube (Why youtube because it is second most- visited website(34.6 billion))
- Which category has the most number of likes? (For example, people and blogs, entertainment and music, and so on.)
- Which category has the most viewers?
- Which region (Europe, North America, etc.) has the most views?

### Dataset of youtube:
- Youtube uses factors, including users interactions
  e.g. number of views , shares,  comments and likes.
- Sources: Kaggle . Data Collected using Youtube API

### Why used Cloud?

#### Cloud vs On-Premise Data Center

#### On-premise data center :
- Company has it is own hardware
- They have to maintain it;
  e.g.
    - Purchase,fix and upgarade hardware
    - Install and maintain Oprating system and other software 
    - shipping ,installation, electricity and cooling systems..
    - underutilized vs overutilized
    - Sustainability issues 

#### Cloud :
- Reliability 
- Scalability
- No up-front cost
- Disaster Recovery
- Go global in a seconds   

### Flow of the Project [(Cloud Architecture)](https://github.com/Manav-56/Cloud-based-Youtube-Data-Analysis-and-Data-Engineering-Project/blob/main/Diagrams/Diagram.png) :

- Data Ingestion: Data coming from various sources 
- Data Lake: Design and build a new data lake architecture for organizing data and build data pipeline around it (The data architecture should be scalable , so choose AWS Cloud )
- ETL Design: Extract, Transform and load data efficiently
- Build Dashboard for get to know business insights

### Steps followed:

- Create IAM User(with administrator access but not bills, cost and all things), followed least Privileged  rule
- Used AWS CLI for interact with AWS Services
- Stored all data in Data Lake (AWS S3)
- Configured AWS Glue Crawler  on top of raw Data
- Created AWS Glue Catalog (Information about the data means, what is contains, metadata etc.)
- Queried data using AWS Athena (Ad-hoc query tool)
- Used AWS Lambda for Pre-Processing data (Transform, cleaning and Normalization) 
- Constructed ETL Pipeline [(View)](https://github.com/Manav-56/Cloud-based-Youtube-Data-Analysis-and-Data-Engineering-Project/blob/main/Diagrams/ETL%20AWS%20Glue.png) Using AWS Glue ETL and Created Job for performing it
- Configured AWS Glue Crawler on top of clean data 
- Created Trigger in AWS Lambda for automate task whenever any raw data come into S3
- Store Reporting/Analytics data in S3
- Visualized data using AWS QuickSight 

### Analysis from the data [(View)](https://github.com/Manav-56/Cloud-based-Youtube-Data-Analysis-and-Data-Engineering-Project/blob/main/Diagrams/Dashboard.jpg):

- The most liked videos are in the People and Blogs Category.
- The music category has the most video views.
- The Europe region has the most video views.

### Gained Knowledge On :

- how to Build a Data Lake from scratch in Amazon s3 
- joining semi-structured and structured data
- Data Lake vs Data Warehouse
- Data Lake design in layers, partitioned for cost-performnace 
- AWs Data Catalogue (Using AWS Glue)
- ETL in AWS Glue Spark jobs
- IAM Services(User,Role)
- SQL Using Amazon Athena and spark SQL
- Ingest changes incrementally and schema evolution 
- BI dashboard in amzon Quicksight

### AWS Services Used :

- AWS IAM
- AWS S3
- AWS Lambda
- AWS Glue
- AWS Athena
- AWS QuickSight

