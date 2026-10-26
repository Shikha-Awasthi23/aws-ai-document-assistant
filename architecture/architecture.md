# AWS AI-Powered Document Assistant — Architecture

## Overview

This project uses AWS serverless services to retrieve text documents stored in Amazon S3 through an HTTP API.

## Architecture Diagram

```text
          +------------------+
          |       User       |
          +--------+---------+
                   |
                   | HTTP POST
                   v
          +------------------+
          |  API Gateway     |
          |    POST /ask     |
          +--------+---------+
                   |
                   v
          +------------------+
          |   AWS Lambda     |
          | Request Handler  |
          +--------+---------+
                   |
                   | S3 GetObject
                   v
          +------------------+
          |    Amazon S3     |
          |  Text Documents  |
          +--------+---------+
                   |
                   | Document Content
                   v
          +------------------+
          |   AWS Lambda     |
          | JSON Response    |
          +--------+---------+
                   |
                   v
                 User
```

## Workflow

1. The user sends a POST request to the API Gateway endpoint.
2. API Gateway invokes the Lambda function.
3. Lambda reads the requested document from Amazon S3.
4. S3 returns the document content.
5. Lambda sends a JSON response to the caller.

## Security

- IAM controls access between Lambda and S3.
- The Lambda execution role should have only the permissions required by the application.
- API authentication should be configured before production use.
- AWS credentials and sensitive information must not be committed to GitHub.

## Current Status

S3 document storage, Lambda document retrieval, and API Gateway have been configured. Further API testing is required after the latest code update.

Generative AI integration is planned but remains incomplete.
