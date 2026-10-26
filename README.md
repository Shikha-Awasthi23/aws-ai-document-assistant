AWS AI-Powered Document Assistant

Project Overview

This project demonstrates a serverless document retrieval system built using Amazon Web Services (AWS).

Users send an HTTP POST request to Amazon API Gateway. AWS Lambda processes the request and retrieves the requested text document from Amazon S3.

AWS Services Used

Amazon S3: Stores text documents.

AWS Lambda: Processes requests and retrieves document contents.

Amazon API Gateway: Exposes the document retrieval endpoint.

AWS IAM: Controls access permissions.

Amazon CloudWatch: Supports logging and troubleshooting.

Architecture

User → Amazon API Gateway → AWS Lambda → Amazon S3

Lambda returns the retrieved document content as a JSON response.

Example Request

{
  "document_key": "aws_notes.txt"
}

Current Features

Serverless document retrieval.

S3 object access through Lambda.

HTTP POST endpoint.

JSON response handling.

IAM-based access control.

Project Status

The S3, Lambda, and API Gateway components have been configured. The API requires further testing following a recent code update.

Generative AI integration is planned but is not yet complete.

Future Enhancements

Integrate a generative AI model.

Support questions about document contents.

Add API authentication.

Improve error handling and testing.

Learning Outcomes

This project provides practical experience with AWS serverless architecture, object storage, IAM permissions, and API integration.
