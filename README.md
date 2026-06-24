# TaskManager

## Architecture Diagram

![AWS Laravel Production Architecture](arch.png)

# AWS Laravel Production Deployment Architecture

This project demonstrates a production-ready Laravel application deployment on AWS cloud infrastructure using a custom VPC architecture, Docker containerization, and CI/CD automation.

The infrastructure includes a secure network setup with IAM, VPC, EC2, RDS, Route Tables, Internet Gateway, Security Groups, CloudWatch monitoring, Docker, and GitHub Actions CI/CD pipeline.

## Architecture Overview

- Created a custom AWS VPC with an isolated network environment.
- Configured public and private subnets for secure resource separation.
- Deployed Laravel application on an EC2 instance inside the public subnet.
- Containerized Laravel application using Docker and Docker Compose.
- Hosted MySQL database using Amazon RDS inside the private subnet.
- Configured Internet Gateway to provide internet access to public resources.
- Configured Route Tables for public and private subnet traffic management.
- Implemented Security Groups to allow secure communication between EC2 and RDS.
- Created IAM user and assigned required permissions for AWS resource management.
- Integrated Amazon CloudWatch for monitoring EC2 and RDS metrics, logs, and alarms.
- Automated application deployment using GitHub Actions CI/CD pipeline.
- Configured CI/CD workflow to automatically build Docker images and deploy updates to EC2.

## CI/CD Pipeline Flow

Developer Push → GitHub Repository → GitHub Actions → Docker Build → EC2 Deployment → Running Laravel Container

## Docker Deployment

- Created Dockerfile for Laravel application.
- Configured Docker Compose for application services.
- Ran Laravel application inside Docker containers on EC2.
- Managed application deployment and updates through automated pipeline.

## AWS Services Used

- Amazon VPC
- Amazon EC2
- Amazon RDS (MySQL)
- AWS IAM
- Internet Gateway
- Route Tables
- Security Groups
- Amazon CloudWatch

## DevOps Tools Used

- Docker
- Docker Compose
- GitHub Actions
- Linux (Ubuntu)
- Git

## Deployment Flow

User → Internet → Internet Gateway → EC2 (Docker Container - Laravel App) → RDS (Private Database)
