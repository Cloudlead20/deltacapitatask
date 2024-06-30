# Automated Deployment of Clients API on Kubernetes with GitHub Actions

This repository contains a Clients API application and the necessary configurations for automated CI/CD using GitHub Actions. The pipeline includes stages for building, testing, SonarQube analysis, Docker image creation and pushing to AWS ECR, and deployment to a Kubernetes cluster.

## Prerequisites

Before you begin, ensure you have the following:

- A GitHub repository containing your application code.
- An AWS account with an ECR repository set up.
- A Kubernetes cluster where you can deploy your application.
- SonarQube server for code quality analysis.

## Setup


### Add the following secrets to your GitHub repository:

AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
SONAR_HOST_URL
SONAR_TOKEN
KUBE_CONFIG
To add secrets, go to Settings > Secrets and variables > Actions > New repository secret.

###  Kubernetes Deployment YAML
Ensure your k8_manifest_file/backend/backend_deployment.yaml contains a placeholder for the Docker image tag:


### Running the Pipeline
Push your changes to the main branch.
Monitor the workflow run in the Actions tab of your GitHub repository.

### Conclusion
This setup automates the CI/CD process for the Clients API using GitHub Actions, AWS ECR, and Kubernetes. For more details, refer to the official documentation of GitHub Actions, AWS ECR, SonarQube, and Kubernetes.

