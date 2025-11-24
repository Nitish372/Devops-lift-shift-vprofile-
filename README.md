# AWS Lift-and-Shift Deployment: vProfile Application

This project demonstrates migrating the vProfile Java application from local setup to AWS using a simple lift-and-shift approach.  
No Docker, no Terraform, and no CI/CD have been used in this project — the infrastructure was created manually on AWS.

---

## 1. Project Summary

- Migrated a monolithic Java + MySQL application to AWS
- Deployed the application on EC2 with Tomcat and Java 11
- Configured MySQL 8 on AWS (EC2 or RDS)
- Imported the database from the provided SQL dump
- Ensured the application runs end-to-end over the internet

This project focuses purely on **AWS deployment**, not rewriting or modernizing the application.

---

## 2. Architecture Overview

- **EC2 Instance** — Application server (Ubuntu + Java 11 + Maven + Tomcat)
- **MySQL Database** — Running on AWS (EC2 or RDS)
- **Security Groups** — Allowed HTTP/8080, SSH, and MySQL (3306)
- **GitHub** — Version control for the application code

---

## 3. Tools Used

- AWS EC2
- MySQL 8
- Java 11
- Apache Tomcat
- Maven
- Linux (Ubuntu)
- Git & GitHub

---

## 4. Database Setup

The project includes a MySQL dump file:

src/main/resources/db_backup.sql