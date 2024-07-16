# Infrasturcture_description

This document describes the infrastructure needs for the Udagram project. The following AWS services are utilized:

## AWS Services

### 1. Amazon RDS (Relational Database Service)
- **Purpose**: To host the PpostgreSQL database for storing user metadata, such as user credentials.
- **Details**:
    - Instance Type: db.ts.micro
    - Region & AZ: us-east-1
    - Multi-AZ: No

### 2. Amazon S3 (Simple Storage Service)
- **Purpose**: To host the frontend files.
- **Details**:
    - Bucket Name: aws-deployment-test-920911
    - AWS Region: us-east-1
    - Bucket website endpoint: http://aws-deployment-test-920911.s3-website-us-east-1.amazonaws.com

### 3. AWS Elastic Beanstalk
- **Purpose**: To deploy and manage the API.
- **Details**:
    - Domain: http://udagram-api-dev.us-east-1.elasticbeanstalk.com
    - Platform: Node.js 14 running on 64bit Amazon Linux 2/5.9.3
    - Instance Type: t2.medium

### 4. AWS IAM (Identity and Access Management)
- **Purpose**: To manage access permissions for AWS resources.
- **Details**:
    - Roles: Defined for different services with least privilege principle.

## Architecture Diagram
![Architecture Diagram](./Architecture%20Diagram%20of%20Infrastructure.drawio.png)