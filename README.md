
# Chat GPT Clone App Deployment on Kubernetes

This project demonstrates the deployment of a Chat GPT clone application on a Kubernetes cluster using Terraform and Jenkins CI/CD pipeline. The setup automates the provisioning of infrastructure and the deployment of the application, providing a scalable and efficient solution for managing AI-powered chat services.

![ar](https://github.com/user-attachments/assets/593aee6c-6d87-4616-8ba7-7b7facf9b673)

## Introduction

This repository contains the source code and deployment scripts for a Chat GPT clone app. The deployment process involves:
- Infrastructure provisioning using Terraform
- Containerization and orchestration with Kubernetes
- Continuous Integration and Continuous Deployment (CI/CD) using Jenkins

The project is based on the [Medium article by Aakib Khan](https://aakibkhan1.medium.com/project-11-deployment-of-chat-gpt-clone-app-on-kubernetes-using-terraform-and-jenkins-ci-cd-904d9460aaf5), which provides a detailed guide on setting up and deploying the application.

## Prerequisites

Before you begin, ensure you have the following installed on your local machine:

- **Terraform**: Infrastructure as Code (IaC) tool for provisioning resources
- **Docker**: For containerizing the application
- **Kubernetes**: For orchestrating containerized applications
- **Jenkins**: For setting up the CI/CD pipeline
- **kubectl**: Command-line tool for Kubernetes management
- **Git**: Version control system

## Installation

1. **Clone the repository**:
`
   ```bash
   git clone https://github.com/amanpn01/Chat-gpt-clone.git
   cd your-repo-name
   ```

2. **Infrastructure Setup**:

   - Navigate to the Instance-terraform directory and initialize Terraform:

    ```bash
     cd Instance-terraform
     terraform init
    ```
   - Apply the Terraform configuration to provision the required resources:

    ```bash
     terraform apply
    ```

3. **Deploy on Kubernetes**:

   - Navigate to the k8s directory and initialize Terraform:

    ```bash
     cd /Chat-gpt-deployment/k8s
     terraform init
    ```
   - Apply the Kubernetes manifests:

    ```bash
     kubectl apply -f chatbot-ui.yaml
     kubectl get all
    ```

5. **CI/CD Pipeline Setup**:

   - Set up Jenkins and configure the pipeline using the provided Jenkinsfile.

## Usage

Once the deployment is complete, the Chat GPT clone app will be accessible via the external IP of the Kubernetes service. You can interact with the application using the provided frontend interface or API endpoints.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
