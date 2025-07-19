# Serverless Lambda with API Gateway, SNS, and S3

This mini-project demonstrates a **serverless architecture** using **AWS Lambda**, integrated with **API Gateway**, **SNS**, and **S3**.  
It processes HTTP requests, sends email notifications via SNS on success, and logs errors to S3 on failure.

---

## Architecture

- **API Gateway** – Handles HTTP requests and triggers the Lambda function.  
- **Lambda Function** – Processes the event and integrates with SNS and S3.  
- **SNS Topic** – Sends email notifications when Lambda executes successfully.  
- **S3 Bucket** – Stores logs or failed invocation records.

---

## How It Works

1. A request is made to the API Gateway endpoint.  
2. The Lambda function runs and returns `"Hello from Lambda!"`.  
3. On success, SNS sends an email notification to the subscriber.  
4. On failure, Lambda writes logs to S3 automatically.

---

## Setup Steps

1. Create a Lambda function (Python 3.12 runtime).  
2. Attach API Gateway as a trigger (HTTP endpoint).  
3. Create an SNS topic and subscribe your email.  
4. Create an S3 bucket for error logs.  
5. Configure:
   - SNS as the **success destination**  
   - S3 as the **failure destination**  
6. Deploy and test via the API Gateway URL.

---

## Technologies Used

- AWS Lambda  
- Amazon API Gateway  
- Amazon SNS  
- Amazon S3  
- Python 3.12 (default runtime)

---

## Architecture Diagram

![Architecture Diagram](architecture-diagram.png)
