# Databricks Development Workflow - Phase 2

<img src="https://cloud.githubusercontent.com/assets/4307137/10105283/251b6868-63ae-11e5-9918-b789d9d682ec.png" width="30%"></img> 

This project focuses on the second phase of the Databricks Development Workflow, which aims to streamline the development and deployment process for Databricks notebooks and scripts. The main objective is to establish a seamless integration between the development and production environments using Git branches and GitHub Actions.

## Key Features

1. **Dual Workspace Setup**:
   - The project includes two Databricks workspaces - one for development (dev) and another for production (prod).
   - This separation allows for a controlled and organized development process.

2. **Git Branch Integration**:
   - The project leverages Git branches to manage the development workflow.
   - The `dev` branch is associated with the development workspace, while the `prod` branch is linked to the production workspace.
   - This enables developers to work on features and bug fixes in isolation and promotes a structured release process.

3. **GitHub Actions Automation**:
   - GitHub Actions is utilized to automate the deployment and execution of Databricks notebooks and scripts.
   - When a Data Engineer (DE) merges code changes to the `dev` branch, GitHub Actions automatically copies the script to the development workspace and triggers its execution on the associated cluster.
   - The execution status and results are then reported back to the GitHub repository.

4. **Automated Production Deployment**:
   - Upon successful validation and testing in the development environment, the Data Engineer can initiate a pull request to merge the changes from the `dev` branch to the `prod` branch.
   - GitHub Actions seamlessly handles the deployment process by copying the approved code to the production workspace, ensuring a smooth transition from development to production.

## Workflow Overview

1. **Feature Development**:
   - The Data Engineer creates a new branch from the `dev` branch to work on a specific feature or bug fix.

2. **Pull Request to Dev**:
   - Once the code changes are complete, the Data Engineer opens a pull request to merge the changes into the `dev` branch.

3. **Automated Development Deployment**:
   - GitHub Actions is triggered automatically when the pull request is created.
   - It copies the modified script to the development workspace and executes it on the designated cluster.
   - The execution status and results are captured and reported back to the GitHub repository.

4. **Validation and Testing**:
   - The changes are thoroughly tested and validated in the development environment.

5. **Pull Request to Prod**:
   - After successful validation, the Data Engineer initiates a pull request to merge the changes from the `dev` branch to the `prod` branch.

6. **Automated Production Deployment**:
   - GitHub Actions takes charge, copying the approved code to the production workspace.
   - This ensures a consistent and reliable deployment process.

By following this structured workflow and leveraging the power of GitHub Actions, the Databricks Development Workflow - Phase 2 project enables efficient collaboration, automated testing, and seamless deployment of Databricks notebooks and scripts. This streamlined process enhances productivity, reduces manual errors, and ensures the stability and reliability of the production environment.