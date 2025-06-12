# Serverless Contact Form on AWS

A fully serverless **Contact Us** application built using AWS services from form submission to database storage and email notification.

This project showcases how to build a complete frontend + backend workflow using AWS Lambda, API Gateway, DynamoDB, SNS, and S3 all tied together with CloudWatch for logging and monitoring.

---

## Features

- Frontend hosted on S3 with a modern HTML+JS form
- HTTP API built with API Gateway to trigger Lambda
- Lambda function (Python) handles form submissions
- Data stored in DynamoDB
- Email notifications sent via SNS
- CloudWatch monitoring and logging enabled
- Fully secured and CORS-compliant
- Optional: Custom domain + HTTPS via CloudFront

---

## Tech Stack (AWS Services Used)

- **Amazon S3** – Static website hosting
- **Amazon API Gateway (HTTP API)** – HTTP entry point for form submissions
- **AWS Lambda** – Python backend logic
- **Amazon DynamoDB** – NoSQL storage for submitted data
- **Amazon SNS** – Email notification service
- **Amazon CloudWatch** – Logs and metrics

---

## Architecture

![Architecture Diagram](./architecture.png)

---

## Prerequisites

Before you begin, make sure you have:

- An AWS account with access to Lambda, API Gateway, DynamoDB, SNS, S3
- IAM permissions to create and manage these services
- A domain (optional) if you want to configure custom HTTPS with CloudFront
- Familiarity with the AWS Console or CLI

---

## Project Structure

| File                | Purpose                          |
|---------------------|----------------------------------|
| `README.md`         | Project overview and quickstart  |
| `api.md`            | API Gateway setup instructions   |
| `lambda.md`         | Lambda code + deployment steps   |
| `dynamodb.md`       | DynamoDB table creation steps    |
| `sns.md`            | SNS topic + subscription setup   |
| `s3.md`             | Frontend upload + S3 hosting     |
| `index.html`        | Contact Us frontend page         |
| `lambda_function.py`| Python Lambda backend code       |
| `architecture.png`  | Visual overview of architecture  |

---

## Quick Setup

Each service in this project is documented separately. Follow them in order:

1. [Set up DynamoDB](./dynamodb.md)
2. [Deploy Lambda Function](./lambda.md)
3. [Create API Gateway](./api.md)
4. [Configure SNS for email](./sns.md)
5. [Host frontend on S3](./s3.md)

---

## Demo Flow

index.html (S3) ──> API Gateway (POST /contact) ──> AWS Lambda ──> DynamoDB (store submission) ──> SNS (send email notification)

---

## Result

- A working contact form hosted at 
- Form submissions get stored in DynamoDB
- You receive an email notification instantly

---



