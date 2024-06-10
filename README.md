# Dotnet-Github-Workflow

# My GitHub Actions Testing Repository

Welcome to my GitHub Actions testing repository! This repository serves as a sandbox for experimenting with GitHub Actions workflows and various commands for automating tasks.

## Description

This repository contains sample workflows and scripts to demonstrate the use of GitHub Actions for continuous integration (CI), continuous deployment (CD), and other automation tasks.

![GitHub Actions Logo](https://github.githubassets.com/images/modules/site/logos/actions-actions.png)

# Workflows Overview

This repository utilizes GitHub Actions workflows to automate various tasks related to managing a .NET project, including building, testing, and releasing.

## Master Workflow (master.yml)

[![Master Workflow Status](https://github.com/your-username/your-repository-name/workflows/Master%20Workflow%20Dispatcher/badge.svg)](https://github.com/your-username/your-repository-name/actions/workflows/master.yml)

The **Master Workflow Dispatcher** is triggered by pushes or pull requests to the `main` or `release` branches. It dispatches the appropriate workflow based on the branch:
- For the `main` branch, it triggers the `main.yml` workflow, which builds the .NET project.
- For the `release` branch, it triggers the `release.yml` workflow, which publishes a NuGet package.

## Main Workflow (main.yml)

[![Main Workflow Status](https://github.com/your-username/your-repository-name/workflows/Build%20.NET%20Project/badge.svg)](https://github.com/your-username/your-repository-name/actions/workflows/main.yml)

The **Build .NET Project** workflow is triggered manually or by the Master Workflow Dispatcher. It performs the following tasks:
- Checks out the repository.
- Sets up the .NET environment.
- Restores dependencies.
- Builds the .NET project in Release configuration.

## Release Workflow (release.yml)

[![Release Workflow Status](https://github.com/your-username/your-repository-name/workflows/Publish%20NuGet%20Package/badge.svg)](https://github.com/your-username/your-repository-name/actions/workflows/release.yml)

The **Publish NuGet Package** workflow is triggered manually or by the Master Workflow Dispatcher when changes are pushed to the `release` branch. It automates the process of releasing a new version of the NuGet package:
- Checks out the repository.
- Sets up the .NET environment.
- Restores dependencies.
- Builds the .NET project in Release configuration.
- Packs the NuGet package.
- Creates a GitHub tag and release.
- Uploads the NuGet package as a release asset.

Each workflow contributes to streamlining the development, testing, and release processes of the .NET project, improving productivity and ensuring consistent quality.


