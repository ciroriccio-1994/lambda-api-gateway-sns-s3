Serverless Lambda with API Gateway, SNS, and S3
This project demonstrates a simple serverless architecture using AWS Lambda, integrated with API Gateway, SNS, and S3, to process requests and trigger notifications.
Architecture
API Gateway: Receives HTTP requests and invokes the Lambda function.
Lambda Function: Handles the request and integrates with SNS and S3.
SNS Topic: Sends email notifications when the Lambda function runs successfully.
S3 Bucket: Stores logs or invocation records when the function fails.
How It Works
A request is made to the API Gateway endpoint.
The Lambda function runs and returns a "Hello from Lambda!" message.
On success, SNS sends a notification email to the subscriber.
On failure, Lambda automatically writes logs to the configured S3 bucket.
Setup Instructions
Create a Lambda function using the default Python 3.12 runtime.
Attach API Gateway as a trigger (HTTP endpoint).
Create an SNS topic and subscribe your email to it.
Create an S3 bucket for Lambda logs.
Configure:
SNS as a success destination
S3 as a failure destination
Deploy and test the function by invoking the API Gateway URL.
Technologies Used
AWS Lambda
Amazon API Gateway
Amazon SNS
Amazon S3
Python 3.12 (default runtime)
Architecture Diagram
![Architecture Diagram](architecture-diagram.png)
