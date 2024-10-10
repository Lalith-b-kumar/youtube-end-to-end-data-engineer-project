# Youtube-end-to-end-data-engineer-project
## Overview

This project is mainly to perform a complete ETL operation using Aamzon Cloud Service. Extracting Youtube Data through API, transform it to readable format and 
load in Amazon Data Store using Python code.
   

## Services we will be using
1. Amazon S3: Amazon S3 is an object storage service that provides manufacturing scalability, data availability, security, and performance.
2. AWS Glue: A serverless data integration service that makes it easy to discover, prepare, and combine data for analytics, machine learning, and application development.
3. AWS Lambda: Lambda is a computing service that allows programmers to run code without creating or managing servers.
4. AWS Cloudwatch :  Cloudwatch is scheduling service , which helps to trigger the functions
5. AWS Athena: Athena is an interactive query service for S3 in which there is no need to load data it stays in S3.

## Dataset Used
We are using GoogleAPI client which contains information like video,channel,comment details and more ,as available in Youtube . Datas are extracted in real time

## Scenarios Covered
1. Extracting details of a Youtube Video by providing video Id
2. Extracting list of Cooking Videos based on search query 
3. Extracting list of Pediatrician Channels based on search query
4. Extracting Comment Thread details of any particular Video by providing video Id

## Execution Flow
Lambda Trigger (every 10 mins) -> Extract Code Run( Connecting to API and extracting Data) -> Store Raw Json Data in Amazon S3 -> Trigger Transform Code -> 
Transform the RAW JSON Data to csv Format and store in S3-> Creating Database/Tables using Amazon Glue - > Reading/Query the Data in Amazon Athena

