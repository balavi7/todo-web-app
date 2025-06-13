# DynamoDB Setup

This document gives the steps to create and configure the DynamoDB table for storing Contact Us form submissions.

---

## Purpose

We use DynamoDB as a **NoSQL database** to store form submissions, including:

- First name
- Last name
- Email address (used as the unique identifier)
- Message content
- Timestamp of submission

---

##Steps to Create the Table (AWS Console)

1. Go to **AWS Console > DynamoDB > Tables > Create table**
2. **Table name:** `ContactUsSubmissions`
3. **Partition key:** `email` (type: String)
4. Leave sort key empty (not needed here)
5. Leave the rest (capacity mode, encryption) at default
6. Click **Create Table**

✅ The table will be created and ready for use by the Lambda function.

---

## Example Data Stored

```json
{
  "email": "john.doe@example.com",
  "firstName": "John",
  "lastName": "Doe",
  "message": "This is a test submission.",
  "timestamp": "2025-06-08T15:20:34Z"
}
