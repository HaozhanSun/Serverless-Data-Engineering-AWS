# Serverless-Data-Engineering-AWS
This is a project using AWS Lambda, SQS, DynamoDB, CloudWatch, AWS comprehend and S3 that does sentiment analysis services automatically.

## Workflow Diagram
![image](https://user-images.githubusercontent.com/37522943/113690487-73afdd00-9699-11eb-9580-ce20aa204b06.png)

```
First, a CloudWatch Event triggers a Lambda function ('producer').
Second, the 'producer' Lambda grabs data from DynamoDB, and send the data to AWS SQS (a queue that acts as an intermediary to connect two Lambdas).
Third, another Lambda ('consumer') consumes the data in SQS and send them to Amazon Comprehend to do sentiment analysis.
Fourth, Amazon Comprehend outputs the processed results (company names that are originally in DynamoDB, and now with predicted sentiment) into S3 buckets.
```

In this way, we have built a machine learning pipeline that automatically grabs the data in DynamoDB database and does sentiment analysis, then outputs them into our desired storage.

