# DevOps Task 2 - Jenkins CI/CD Pipeline

This repository contains a demo project for a Jenkins CI/CD pipeline setup.

## Overview
- The project is connected to Jenkins using a `Jenkinsfile`.
- Every push to the `main` branch can trigger a build in Jenkins.
- The Jenkins pipeline pulls the latest code from this repository and executes the build steps defined in the `Jenkinsfile`.

## Jenkins Setup
1. Jenkins is running via Docker:

```bash
docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts
