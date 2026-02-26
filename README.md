## Automated CI/CD Pipeline on AWS with CircleCI


### Project Summary

The goal of this project is to automate the entire deployment lifecycle of a full-stack cloud application, from code commit to production deployment, using modern DevOps tools and best practices.

The pipeline includes:

- Continuous Integration (CI)

- Continuous Delivery (CD)

- Infrastructure as Code (IaC)

- Automated configuration management

- Blue/Green deployment strategy

- Centralized monitoring and alerting

- Automated rollback on failure

Every change pushed to the repository triggers a fully automated pipeline that builds, provisions, deploys, verifies, and monitors the application.

![CI/CD Architecture Diagram](instructions/screenshots/udapeople_app_architecture.png)

### Architecture Overview

The deployment workflow follows this structure:

Code Commit → Triggers CI pipeline in CircleCI

Build & Test Stage → Application is compiled and tested

Infrastructure Provisioning → AWS resources created via CloudFormation

Configuration Management → Servers configured automatically with Ansible

Application Deployment → Blue/Green deployment strategy implemented

Monitoring & Validation → Prometheus surfaces errors and health metrics

Rollback (if needed) → Pipeline reverts to last stable version

This mirrors real-world production DevOps workflows.

### Tech Stack

CI/CD Platform: CircleCI

Cloud Provider: Amazon Web Services (AWS)

Infrastructure as Code: AWS CloudFormation

Configuration Management: Ansible

Monitoring: Prometheus

CLI Tooling: AWS CLI

Application Runtime: Node.js

### Key DevOps Concepts Demonstrated
1️⃣ Continuous Integration & Continuous Delivery

Automated pipeline ensures consistent, reliable releases with minimal manual intervention.

2️⃣ Infrastructure as Code (IaC)

Cloud resources are provisioned declaratively using CloudFormation templates.

3️⃣ Blue/Green Deployment

Reduces downtime and deployment risk by switching traffic between environments.

4️⃣ Configuration Management

Automated server provisioning using Ansible playbooks.

5️⃣ Observability & Monitoring

Application health and errors are surfaced using Prometheus for fast diagnosis.

6️⃣ Failure Handling & Rollback

Pipeline automatically handles failures to maintain production stability.

### Repository Structure
- .circleci/        -     CI/CD pipeline configuration
- cloudformation/   -     Infrastructure as Code templates
- ansible/          -     Configuration management playbooks
- backend/          -     Application source code
- frontend/         -     Application frontend
