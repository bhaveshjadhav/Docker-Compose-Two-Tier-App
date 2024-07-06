# Containerization of a Two-Tier Application using Docker, Docker Compose, and Image Scanning with Docker Scout

## Tools Required
- **Docker**: For creating and managing containers.
- **Docker Compose**: For defining and running multi-container Docker applications.
- **Docker Scout**: For scanning Docker images for vulnerabilities.
- **Code Editor**: Any (e.g., Visual Studio Code, Atom).

## Overview
This project involves containerizing a two-tier application (web application with a database) using Docker and orchestrating the deployment using Docker Compose. Docker Scout is used to scan the Docker images for security vulnerabilities. This provides practical experience in containerization, orchestration, and security.

## Code Repository
- **GitHub**: [Two-Tier Application Project](https://github.com/rajnishkaushik5/two-tier-application-project2.git)

## Requirements

### Functional Requirements
- Containerize each application component using Docker.
- Use Docker Compose for multi-container setup.
- Ensure network communication between containers.
- Scan Docker images with Docker Scout and address vulnerabilities.

### Non-Functional Requirements
- **Performance**: Optimize containers for image size and startup time.
- **Security**: Implement Docker security best practices.
- **Documentation**: Provide clear instructions for building, running, and scanning the application.

## Deployment Steps

### 1. Launch an EC2 Instance
- **Instance Type**: t2.micro
- **AMI**: Ubuntu
- **Security Group Rules**: Ports 22, 80, 5000

### 2. Install Docker
```sh
sudo apt-get update
sudo apt-get install docker.io
