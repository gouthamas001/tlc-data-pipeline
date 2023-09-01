Exploring Google cloud for building data engineering pipelines

USE-CASE:

Use mage which is deployed on google vm to load data from google cloud storage, tranform the data into fact & dimension models and ingest fact and dimension files into Google Bigquery.

Technologies Used :

1. Google Compute Engine
2. Google Cloud Storage
3. Mage
4. Python
5. Google BigQuery

Intitial Steps (Data Analysis Stage):

1. Downloaded TLC (Newyork Taxi) dataset
2. Analyzed the data and designed a star schema to split the data into Fact and Dimension Tables
3. Python code to split the raw data into fact and dimension dataframes

DE Pipeline steps :

1. Create an Google cloud account
2. Upload a sample TLC dataset into Google Cloud Storage
3. Spawn a google virtual machine
4. Install software updates and dependencies
   - Update the package lists on your vm
   - Install python and pip
   - Install mage, pandas and google cloud sdks (google cloud, google cloud bigquery)
5. Deploy mage on VM
   - Mage needs a runtime environment to process data(using python and pandas) and access google cloud services ( i.e. google cloud packages)
6. Create a role in GCP account which can access google bigquery.
7. Go to mage ui and start developing the pipline
   1. Data Loader Module - To load data from Google cloud storage
   2. Transformer Module - Implement logic to tranform the data into fact and dimension dataframes
   3. Data Exporter Module - Ingesting dataframes into BigQuery
   4. io_config.yaml - Provide the google cloud credentials here (so that mage can interact with gcp services)ss
