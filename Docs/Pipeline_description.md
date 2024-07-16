# Pipeline Description

This document explains the steps in the CI/CD pipeline for the Udagram Application.

## CI/CD Pipeline Steps

### 1. Code Commit
- **Description**: Developers push code changes to the version control system (Github).
- **Tool**: GitHub

### 2. Continuous Integration
- **Description**: Automatically build the application on code commit. If the build step failed, a message will be sent to the developer.
- **Tool**: CircleCI

### 3. Build Step
- **Description**: CircleCI installs specific version of node, checks out code from repository, installs dependencies of both front-end and API, runs linting on the front-end, builds both the front-end and the API.
- **Details**:
    - Frontend: Runs the Angular build command
    - API: Runs the build process for the API

### 4. Hold for Manual Approval
- **Description**: The pipeline pause and waits for manual approval before proceeding to deployment.
- **Tool**: CircleCI hold step

### 5. Deploy to AWS
- **Description**: CircleCI installs specific version of node, sets up Elastic Beanstalk, sets up AWS CLI, checks out code from repository, and deploy both the API and the front-end.
- **Tools**: CircleCI, AWS CLI, Elastic Beanstalk

## Pipeline Diagram
![Pipeline Diagram](./Pipeline%20Diagram.drawio.png)