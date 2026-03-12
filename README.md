# Jenkins CI/CD pipeline that builds, tests and deploys a React application to Netlify using Docker.

This repository demonstrates a **CI/CD pipeline built with Jenkins** that builds, tests, and deploys a **Node.js / React web application** to Netlify.

The pipeline is defined using **Pipeline as Code (Jenkinsfile)** and runs inside a **Docker build environment**. Jenkins automates the process of installing dependencies, running tests, building the application, and deploying it to production.

The pipeline is currently **triggered manually from Jenkins**, after which all build, test, and deployment steps run automatically.

---

## Pipeline Workflow

Developer pushes code to GitHub  
↓  
Manual trigger from Jenkins  
↓  
Install dependencies (`npm ci`)  
↓  
Run automated tests (`npm test`)  
↓  
Generate JUnit test reports  
↓  
Build production application (`npm run build`)  
↓  
Deploy to Netlify using Netlify CLI  

---

## Technologies Used

- Jenkins
- Docker
- GitHub
- Node.js
- React
- Netlify CLI
- CI/CD pipelines
- JUnit test reporting
- Linux shell commands

---

## DevOps Concepts Demonstrated

This project demonstrates several core DevOps practices:

- **Continuous Integration (CI)**  
  Automatically building and testing the application.

- **Continuous Deployment (CD)**  
  Deploying the built application to a production hosting platform.

- **Pipeline as Code**  
  Using a Jenkinsfile stored in the repository to define the pipeline.

- **Automated Testing**  
  Running tests as part of the CI/CD process.

- **Build Automation**  
  Automatically compiling and preparing the production build.

- **Deployment Automation**  
  Deploying the build to Netlify using the Netlify CLI.

- **Secrets Management**  
  Using Jenkins credentials to manage the Netlify API token securely.

---

## Repository Structure

Key files in this project:

- **Jenkinsfile**  
  Defines the CI/CD pipeline stages.

- **package.json**  
  Node.js project configuration and scripts.

- **src/**  
  Source code of the React application.

- **public/**  
  Static assets used by the application.

---

## Attribution / Learning Source

This project is based on the **Learn Jenkins App** created by **Valentin Despa**.

Original repository:  
https://github.com/vdespa/learn-jenkins-app

The CI/CD pipeline implementation was developed while following the tutorial:

**Introduction to Jenkins, CI/CD, and DevOps (2025)**  
by Valentin Despa.

The purpose of this repository is to practice **Jenkins pipelines, CI/CD workflows, and automated deployments**.

---

## Future Improvements

Potential improvements to extend this project:

- Configure **GitHub webhooks** to automatically trigger Jenkins pipelines
- Containerise the application using **Docker**
- Deploy the application to **AWS or Azure**
- Implement **Infrastructure as Code** using Terraform
- Add **monitoring and logging** for deployments
