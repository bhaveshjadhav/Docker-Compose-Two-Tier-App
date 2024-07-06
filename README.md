 Containerization of a Two-Tier Application using Docker, Docker Compose, and Image Scanning with Docker Scout
Tools Required
Docker: For creating and managing containers.
Docker Compose: For defining and running multi-container Docker applications.
Docker Scout: For scanning Docker images for vulnerabilities.
Code Editor: Any (e.g., Visual Studio Code, Atom).
Overview
This project involves containerizing a two-tier application (web application with a database) using Docker and Docker Compose. Docker Scout is used to scan the Docker images for security vulnerabilities, providing practical experience in containerization, orchestration, and security.

Code Repository
GitHub: Two-Tier Application Project
Requirements
Functional Requirements
Containerize each application component using Docker.
Use Docker Compose for multi-container setup.
Ensure network communication between containers.
Scan Docker images with Docker Scout and address vulnerabilities.
Non-Functional Requirements
Performance: Optimize containers for image size and startup time.
Security: Implement Docker security best practices.
Documentation: Provide clear instructions for building, running, and scanning the application.
Deployment Steps
1. Launch an EC2 Instance
Instance Type: t2.micro
AMI: Ubuntu
Security Group Rules: Ports 22, 80, 5000
2. Install Docker
sh
Copy code
sudo apt-get update
sudo apt-get install docker.io
3. Access Docker Daemon
sh
Copy code
sudo chown $USER /var/run/docker.sock
4. Install Docker Compose
sh
Copy code
sudo apt install docker-compose
5. Clone the Repository
sh
Copy code
git clone https://github.com/rajnishkaushik5/two-tier-application-project2.git
cd two-tier-application-project2
6. Configure Docker
Write a Dockerfile for the backend.
Use the base image mysql:5.7 for the database.
7. Create docker-compose.yml
sh
Copy code
docker-compose up -d
8. Access the Application
Visit http://localhost:5000.

9. Interact with Containers
sh
Copy code
docker exec -it <container_id> bash
10. MySQL Container Interaction
sh
Copy code
docker exec -it <mysql_container_id> mysql -u root -p
Commands:
sql
Copy code
SHOW DATABASES;
USE KYC;
SHOW TABLES;
SELECT * FROM messages;
INSERT INTO messages (message) VALUES ("your message");
11. Install Docker Scout
sh
Copy code
mkdir -p ~/.docker/cli-plugins/
cd ~/.docker/cli-plugins/
curl -sSfL https://raw.githubusercontent.com/docker/scout-cli/main/install.sh | sh -s --
12. DockerHub Login
sh
Copy code
docker login
13. Scan Docker Images
sh
Copy code
docker scout quickview <image:tag>
docker scout cves <image:tag>
docker scout cves -o <image:tag> > scan_report.txt
14. Clean Up
sh
Copy code
docker-compose down
docker-compose up -d
15. Terminate EC2 Instance
Terminate the EC2 instance after use.
