# MEAN Stack CI/CD Deployment using Docker and AWS EC2

## Project Overview

This project demonstrates the containerization and automated deployment of a full-stack MEAN (MongoDB, Express.js, Angular, Node.js) application using Docker, GitHub Actions, and an AWS EC2 Ubuntu virtual machine.  
The objective of this assignment was to build a production-ready deployment workflow with automated CI/CD integration.

---

## Architecture

Code changes pushed to the GitHub repository automatically trigger a CI/CD pipeline using GitHub Actions.  
The pipeline builds Docker images for the frontend and backend services, pushes them to Docker Hub, and deploys the updated containers on an AWS EC2 instance using Docker Compose.  
Nginx is configured as a reverse proxy to expose the application through port 80.

---

## Technologies Used

- MongoDB  
- Express.js  
- Angular  
- Node.js  
- Docker  
- Docker Compose  
- GitHub Actions  
- AWS EC2 (Ubuntu)  
- Nginx  

---

## Containerization

Separate Dockerfiles were created for both frontend and backend services.  
Docker Compose was used to manage multiple containers including the application services and MongoDB database.  
The official MongoDB Docker image was used for database deployment.

---

## CI/CD Pipeline

GitHub Actions was configured to automate the deployment workflow.  
On every push to the main branch, the pipeline performs the following steps:

1. Builds Docker images for frontend and backend services  
2. Pushes the images to Docker Hub  
3. Connects securely to the EC2 instance using SSH  
4. Pulls the latest images on the server  
5. Restarts containers using Docker Compose  

This ensures that application updates are deployed automatically without manual intervention.

---

## Nginx Reverse Proxy

Nginx is configured as a reverse proxy to route incoming traffic to the application containers.  
The application is accessible through port 80 using the EC2 public IP address.

---

## Deployment Process

1. Created a GitHub repository and pushed application source code  
2. Containerized frontend and backend services using Docker  
3. Built and pushed Docker images to Docker Hub  
4. Provisioned an Ubuntu EC2 virtual machine  
5. Installed Docker and Docker Compose on the server  
6. Configured Docker Compose for multi-container deployment  
7. Set up Nginx as a reverse proxy  
8. Implemented automated deployment using GitHub Actions  

---

## Live Application 

http://16.171.47.170 
http://13.60.245.135

---

## Screen Shots 

![docker imgs](https://github.com/user-attachments/assets/ab946c15-4ae1-419a-adfb-c63134d6b786)
![WhatsApp Image 2026-02-24 at 2 52 05 AM](https://github.com/user-attachments/assets/f4e6a7db-807b-4587-bfd5-378890855edd) 




## Author

Anuj Kumawat
