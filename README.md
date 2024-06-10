# Dotnet-Github-Workflow

# My GitHub Actions Testing Repository

Welcome to my GitHub Actions testing repository! This repository serves as a sandbox for experimenting with GitHub Actions workflows and various commands for automating tasks.

## Description

This repository contains sample workflows and scripts to demonstrate the use of GitHub Actions for continuous integration (CI), continuous deployment (CD), and other automation tasks.

![GitHub Actions Logo](https://github.githubassets.com/images/modules/site/logos/actions-actions.png)

## Workflow Examples

### Workflow 1: Continuous Integration for .NET Project

#### Purpose:
- To automate the build and test process for a .NET project on GitHub.

#### Events Triggering the Workflow:
- `push` events to the `main` branch
- `pull_request` events targeting the `main` branch

#### Steps:
1. ![Checkout code](https://example.com/checkout.png)
   - Uses the `actions/checkout@v2` action to retrieve the repository's code.
   
2. ![Setup .NET Core](https://example.com/setup-dotnet.png)
   - Uses the `actions/setup-dotnet@v2` action to set up the .NET Core SDK.

3. ![Restore dependencies](https://example.com/restore.png)
   - Runs `dotnet restore` to restore project dependencies.

4. ![Build](https://example.com/build.png)
   - Runs `dotnet build --no-restore`

5. ![Test](https://example.com/test.png)
   - Runs `dotnet test --no-restore --verbosity normal`

#### Permissions:
- Default permissions for read-only access to repository contents.

---

### Workflow 2: Continuous Deployment for Dockerized .NET Project

#### Purpose:
- To automate the deployment of a Dockerized .NET project to a container registry.

#### Events Triggering the Workflow:
- Manual trigger

#### Steps:
1. ![Checkout code](https://example.com/checkout.png)
   - Uses the `actions/checkout@v2` action to retrieve the repository's code.
   
2. ![Login to Container Registry](https://example.com/login.png)
   - Logs in to the container registry to push Docker images.

3. ![Build Docker Image](https://example.com/build-docker.png)
   - Builds the Docker image.

4. ![Push Docker Image](https://example.com/push-docker.png)
   - Pushes the Docker image to the container registry.

5. ![Deploy](https://example.com/deploy.png)
   - Deploys the Docker image to the target environment.

#### Permissions:
- Additional permissions for pushing Docker images to the container registry.

