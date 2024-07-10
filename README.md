# Spotify-etl-pipeline-project

A robust ETL pipeline for Spotify data using Python and AWS services. This project automates data extraction with Spotipy and AWS Lambda, transforms data on-the-fly, and loads it into S3. AWS Glue and Amazon Athena enable efficient schema inference and querying for seamless analysis.

This project involves building a data pipeline for extracting, transforming, and loading Spotify data using Python and AWS services. The pipeline is designed to automate the data processing workflow, ensuring data is collected, transformed, and made available for analysis efficiently and reliably.

![image](https://github.com/Shushma-thatipamula/spotify-etl-pipeline-project/assets/56660510/59e1de0c-a912-473f-876e-131a8a0e9cb1)


## Key Features:

Automated Data Extraction: Utilizes Spotipy, a Python library, to interact with the Spotify Web API for extracting data. AWS Lambda and CloudWatch are used to schedule and trigger the extraction process daily.

Efficient Data Transformation: AWS Lambda is employed to execute data transformation logic whenever new data is added to the raw data S3 bucket, ensuring the data is ready for analysis.

Seamless Data Loading: AWS Glue Crawler and AWS Glue Data Catalog manage metadata and infer schema on the transformed data stored in S3. Amazon Athena is then used for querying the data, making it simpler to analyze.

## Technologies Used:

**Python:** For writing the extraction and transformation logic.

**AWS Lambda:** To deploy and run the extraction and transformation functions.

**AWS CloudWatch:** To schedule and trigger the extraction process.

**Amazon S3:** For storing raw and transformed data.

**AWS Glue:** For schema inference and metadata management.

**Amazon Athena:** For querying and analyzing the data.

## How It Works:

**Extract**: The data extraction function is triggered daily by AWS CloudWatch, using Spotipy to communicate with the Spotify Web API. The extracted raw data is stored in an S3 bucket.

**Transform**: When new data is added to the raw data S3 bucket, an AWS Lambda function is triggered to transform the data. The transformed data is then stored in another S3 bucket.

**Load**: AWS Glue Crawler infers the schema of the transformed data, and AWS Glue Data Catalog manages the metadata. The data can then be queried using Amazon Athena for analysis.

This project demonstrates the power of combining Python with AWS services to build a robust and scalable data pipeline for real-time data processing and analysis.
