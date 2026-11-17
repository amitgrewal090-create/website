# Intellipaat Analytics Pvt Ltd – DevOps Capstone Project 2

## Project Overview
This project demonstrates an automated website deployment pipeline using GitHub, AWS CodeBuild, Docker, Docker Hub, AWS Systems Manager (SSM), and Amazon EC2.

## Technologies Used
- GitHub – Source Code Management
- AWS CodeBuild – CI/CD Pipeline
- Docker – Containerization
- Docker Hub – Image Registry
- Amazon EC2 – Website Hosting
- AWS Systems Manager – Remote Deployment
- AWS EventBridge Scheduler – Monthly Release Automation
- Nginx – Web Server

## Project Workflow
1. Developer pushes code to the GitHub master branch.
2. GitHub webhook automatically triggers AWS CodeBuild.
3. CodeBuild builds the Docker image.
4. Docker image is pushed to Docker Hub.
5. AWS SSM sends deployment commands to EC2.
6. EC2 pulls the latest image and restarts the website container.

## Docker Information
- Docker Hub Repository: amitkumardevops2026/intellipaat-website
- Image Tag: latest
- Container Name: intellipaat-capstone-website
- Container Port: 8082

## AWS Configuration
- AWS Region: eu-north-1
- CodeBuild Project: Intellipaat-Capstone-Project-2
- Deployment Method: AWS Systems Manager (SSM)
- Release Schedule: 25th of every month at 9:00 AM IST

## Live Website
http://51.20.181.236:8082

## Deployment Verification
Successfully tested automatic deployment by committing a change to the GitHub master branch.

Verified:
- Automatic CodeBuild trigger
- Docker image build
- Docker Hub image push
- SSM command execution
- EC2 container deployment
- Updated website content visible in browser

## Project Status
Successfully completed and tested.
