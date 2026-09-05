# BookMyShow CI/CD Pipeline Project

## Project Overview
This repository contains an end-to-end automated Continuous Integration and Continuous Deployment (CI/CD) pipeline for the **BookMyShow** web application built with Node.js, Docker, Jenkins, AWS ECR, and AWS EC2.

---

## Tech Stack & Tools
* **Source Control:** GitHub
* **CI/CD Server:** Jenkins
* **Containerization:** Docker
* **Registry:** AWS Elastic Container Registry (ECR)
* **Cloud Infrastructure:** AWS EC2 (Ubuntu)

---

## Pipeline Workflow
1. **Source Code Checkout:** Jenkins automatically pulls the latest codebase from GitHub.
2. **Containerization:** Builds the Node.js application into a Docker container image.
3. **Registry Push:** Authenticates with AWS ECR and pushes the image tagged with `${BUILD_NUMBER}` and `latest`.
4. **Deployment:** Pulls the ECR image onto the deployment server and runs the container, binding it to port 3000 / HTTP port 80.
