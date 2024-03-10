# Assignment 2: Static Webserver Application Deployment

## Introduction
This assignment guides you through the process of creating a Dockerfile, building a Docker image, and deploying a Docker container on an Amazon Linux EC2 instance for a static web server application.

### Author
- Rohan Pamnani

## Table of Contents
1. [Using Terraform code to Deploy EC2 instance in public subnet](#terraform-ec2-deployment)
2. [Using GitHub action to create Docker images and push them to Amazon ECR](#github-action-docker-images)
3. [Using EC2 instance to host the application and database container](#ec2-kubernetes-deployment)
4. [Using Browser to Display the application web pages](#browser-access)
5. [Using Terraform to deploy EC2 instance in public subnet](#terraform-ec2-in-public-subnet)

## Using Terraform code to Deploy EC2 instance in public subnet <a name="terraform-ec2-deployment"></a>
Follow the steps below to deploy an EC2 instance in a public subnet using Terraform:

```bash
# Clone the repo to your local machine
git clone <repository_url>
cd terraform_code/prod/instances/

# Initialize Terraform
terraform init

# Format Terraform configuration files
terraform fmt

# Validate Terraform configuration
terraform validate

# Generate an execution plan
terraform plan

# Apply the changes
terraform apply

```
Using EC2 instance to host the application and database deployment using Kubernetes <a name="ec2-kubernetes-deployment"></a>
Follow the instructions below to use an EC2 instance to run Kubernetes commands:

SSH into the EC2 instance.
Supply AWS learner lab credentials using aws configure.
Login into ECR from the EC2 instance.
Run the Kubernetes command using pod, replicaset, deployment, and service manifests to create app and SQL deployments.
Using Browser to Display the application web pages
To access the application web page, follow these instructions:

Copy the public IP of the EC2 instance.
Open a web browser.
Access http://<EC2_public_IP>:30000 for version 1.
Access http://<EC2_public_IP>:300001 for version 2.
