# Serverless-Data-Engineering-AWS
This is a project using AWS Lambda, SQS, DynamoDB, CloudWatch, AWS comprehend and S3 that does sentiment analysis services automatically.

## Workflow Diagram
![image](https://user-images.githubusercontent.com/37522943/113690487-73afdd00-9699-11eb-9580-ce20aa204b06.png)

First, a CloudWatch Event triggers a Lambda function ('producer')
