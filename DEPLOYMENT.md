# Deployment Details — AWS EC2

## Overview
This document describes the exact steps used to deploy a containerized web application
to AWS EC2 using Docker.

---

## Environment
- Cloud Provider: AWS
- Region: us-east-1
- Instance Type: t3.micro (free tier)
- OS: Amazon Linux 2023

---

## Security Configuration
- SSH (22): restricted to my IP
- HTTP (80): open for public access
- Authentication: SSH key pair

---

## Deployment Steps
1. Launch EC2 instance
2. Connect via SSH using key pair
3. Install Docker
4. Enable and start Docker service
5. Add ec2-user to docker group
6. Pull image from Docker Hub
7. Run container with port mapping

---

## Docker Command Used

```bash
docker run -d -p 80:80 --name joey-app jkanodev/joey-web-app:latest
