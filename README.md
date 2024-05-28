# DATA228_bigdata_project - Real-time Crypto-Arbitrage Analysis
Real-Time Monitoring and Analytics of Arbitrage Opportunities in Cryptocurrency Markets

**Abstract**

In this digital world of cryptocurrency, where prices vary between exchanges, there's a chance to earn profit through arbitrage. We are streaming and analyzing real-time cryptocurrency market data to find potential arbitrage opportunities. As an outcome of this project, we are creating a dashboard that continuously searches different cryptocurrency platforms to find arbitrage opportunities. We will implement special algorithms like differential to provide privacy to the user and use Bloom filters to ensure that our analyses are based on unique information. We are adding Locality-Sensitive Hashing analyzing patterns among data. For stream processing, we are using Apache Kafka and Apache Spark. To implement the project pipeline we will use cloud technologies such as AWS or Google Cloud. The main goal is to provide users with real-time insights into potential arbitrage opportunities, helping them to make informed decisions without relying on automated trading.

**Project Overview**

We are planning to implement this project for the entire pipeline in cloud technologies like AWS or Google cloud. If we are facing any issues with spark or with achieving algorithms in the cloud, we have a failback option to implement kafka and spark in the local system for streaming and cloud for storage. We want to keep both AWS and Google cloud options, so we can switch if we are facing any issues with one cloud technology and also for choosing the best cost effective option.

**Data Collection and Streaming with Kafka:**Kafka for Data ingestion from real time data which gives us the trade details for cryptocurrency exchanges to compare. There are many free API’s for cryptocurrency and we tried to get coin API and verified with code for API connection and data retrieval.
Tools: Kafka in Amazon Kinesis(AWS) or Cloud Pub/Sub(Google cloud)

**Data Processing and Analysis with Apache Spark:**We will handle the streaming data for filtering and aggregation using Apache Spark.  We will use bloom filter streaming algorithm to remove repeated data for maintaining the data uniqueness. Also, We will use Locality sensitive Hashing algorithm to find price patterns across the cryptocurrency exchanges especially to find the arbitrage opportunities. We will find logic to compare the prices for arbitrage in spark.
Tools: Amazon EMR or Cloud Dataproc for spark, Bloom filter algorithm, Locality Sensitive Hashing.

**Differential Privacy Implementation:**In this project we are implementing real trades, we are planning to create only a smart alert system. But this project can be developed later for automatic trades with user login information. Even though privacy is not an issue with our current goal, we want to add privacy techniques like differential before storing and accessing the data. This helps us to keep the individual transactions confidential with protecting the user's details and identity.
Technique: Differential Privacy Technique.
Intermediate Data Handling:While handling streaming data in spark, if we have to store intermediately before processing into structured data for databases.
Tools: Amazon S3 or cloud storage

**ETL for Data Warehouse / Database and Data storage:**We will use python pandas for ETL to extract data from streaming data, transfer and load into a data warehouse like Amazon Redshift or Big Query.
Tools: Amazon Redshift or Bigquery
Real Time Dashboard for Data Analytics:We want to create a real time dashboard to show the current prices among multiple exchanges, possible arbitrage opportunities and any issues or problems that might arise for trade.
Tools: Google Data studio or Amazon Quicksight.

**Actionable Insights and monitoring:**We will create insights from dashboards and monitor the setup for issues. We wanted to create an alert system to send alerts when arbitrage happens or set up an email system with alerts to notify the users and this step is optional. 
Tools: Amazon SNS or Cloud pub/sub
