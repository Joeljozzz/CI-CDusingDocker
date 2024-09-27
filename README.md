# CI/CD Pipeline for Docker Deployment to Azure

This repository showcases a CI/CD pipeline built with Azure DevOps that automates the process of building a Docker image, pushing it to Azure Container Registry (ACR), and deploying it to Azure App Service. 

## Overview

The CI/CD pipeline is designed to facilitate continuous integration and continuous deployment (CI/CD) for applications packaged in Docker containers. The main components of the pipeline include:

- **Docker**: For building and managing container images.
- **Azure Container Registry (ACR)**: To store the built Docker images.
- **Azure App Service**: To host the web application using the Docker images from ACR.

## Pipeline Workflow

The pipeline consists of two main stages:

1. **Build Stage**: 
   - The Docker image is built from the specified Dockerfile.
   - The built image is pushed to the Azure Container Registry.

2. **Deploy Stage**:
   - The Docker image from ACR is deployed to the Azure App Service.

## Pipeline Configuration

The pipeline is defined in the `azure-pipelines.yml` file with the following key components:

### Trigger

The pipeline is triggered on changes to the `main` branch:

```yaml
trigger:
- main
