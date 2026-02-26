# Automated CI/CD Pipeline on AWS with CircleCI

## Project Overview

This project demonstrates the design and implementation of a fully automated CI/CD pipeline for deploying a full-stack cloud application to AWS.

The objective is to automate the complete deployment lifecycle — from code commit to production release — using modern DevOps principles and industry best practices.

Each code change triggers a pipeline that:

- Builds and tests the application  
- Provisions infrastructure  
- Configures servers  
- Deploys using a Blue/Green strategy  
- Monitors application health  
- Automatically rolls back on failure  

This implementation mirrors real-world production DevOps workflows focused on reliability, automation, and observability.

---

## Architecture Diagram

![CI/CD Architecture Diagram](instructions/screenshots/udapeople_app_architecture.png)

_Architecture of the automated CI/CD pipeline with Blue/Green deployment and integrated monitoring._

---

## Deployment Workflow

The pipeline follows this structured flow:

1. **Code Commit**  
   Developer pushes code to the repository, triggering the CI pipeline.

2. **Build & Test**  
   Application is compiled and validated within CircleCI.

3. **Infrastructure Provisioning**  
   AWS resources are created and managed using CloudFormation.

4. **Configuration Management**  
   EC2 instances are configured automatically using Ansible playbooks.

5. **Application Deployment**  
   Blue/Green deployment strategy ensures zero-downtime releases.

6. **Monitoring & Validation**  
   Prometheus monitors system health and application metrics.

7. **Automated Rollback (If Required)**  
   On failure detection, traffic is reverted to the last stable environment.

---

## Technology Stack

| Category | Tools & Services |
|----------|------------------|
| CI/CD Platform | CircleCI |
| Cloud Provider | Amazon Web Services (AWS) |
| Infrastructure as Code | AWS CloudFormation |
| Configuration Management | Ansible |
| Monitoring & Observability | Prometheus |
| CLI Tooling | AWS CLI |
| Application Runtime | Node.js |

---

## Key DevOps Concepts Demonstrated

### Continuous Integration & Continuous Delivery  
Ensures consistent, repeatable, and automated releases with minimal manual intervention.

### Infrastructure as Code (IaC)  
Cloud infrastructure is provisioned declaratively using CloudFormation templates.

### Blue/Green Deployment  
Reduces deployment risk and eliminates downtime by switching traffic between environments.

### Configuration Management  
Server provisioning and application setup are automated using Ansible.

### Observability & Monitoring  
Prometheus provides real-time visibility into application health and system metrics.

### Failure Handling & Rollback  
Automated rollback mechanism preserves production stability in case of deployment issues.

---

## Repository Structure
- .circleci/        -  CI/CD pipeline configuration
- cloudformation/   - Infrastructure as Code templates
- ansible/          - Configuration management playbooks
- backend/          - Application source code
- frontend/         - Application frontend
