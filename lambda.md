# AWS Lambda Function Setup

This document covers the setup and configuration of the backend logic using AWS Lambda.

---

## Purpose

The Lambda function is the core backend handler that:

1. Parses incoming form data from the API Gateway
2. Stores the data in a DynamoDB table
3. Sends an email notification via SNS
4. Returns a response back to the frontend

---

## Lambda Configuration

- **Runtime:** Python 3.12 (or your preferred version)
- **Function name:** `contactUsHandler`
- **Handler:** `lambda_function.lambda_handler`
- **Execution Role:** Custom IAM role with access to:
  - `dynamodb:PutItem`
  - `sns:Publish`
  - CloudWatch logging

---
