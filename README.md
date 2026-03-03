# Cloud-Based-Student-Management-System
The Cloud Based Student Management System is a scalable 3-tier web application developed using Java Servlets and deployed on Amazon Web Services (AWS).
The system enables administrators to manage student records efficiently with secure authentication, CRUD operations, and cloud-based file storage.
The application is designed with scalability, high availability, and security in mind using AWS services such as EC2, RDS, S3, Load Balancer, and Auto Scaling.

🏗 3-Tier Cloud Architecture
Presentation Layer: JSP, HTML, CSS
Application Layer: Java Servlets deployed on AWS EC2 (Apache Tomcat)
Database Layer: Amazon RDS (MySQL)
Storage Layer: Amazon S3 for file uploads
Traffic is distributed using an Application Load Balancer, and scalability is achieved using Auto Scaling Groups.

🛠 Tech Stack
Java (Servlets, JDBC)
JSP, HTML, CSS
MySQL
Apache Tomcat
AWS EC2
AWS RDS
AWS S3
AWS Load Balancer
Auto Scaling
CloudWatch

✨ Features
Secure Admin Login
Add / Update / Delete / View Students
JDBC Database Connectivity
File Upload to AWS S3

🚀 AWS Deployment Steps
1️⃣ Launch EC2 Instance
Select Amazon Linux AMI
Choose t2.micro (Free Tier)
Configure Security Group:
Allow SSH (22)
Allow HTTP (80)
Allow Custom TCP (8080)

2️⃣ Install Java & Apache Tomcat
Install Java (Amazon Corretto 11)
Download and configure Apache Tomcat
Start Tomcat server

3️⃣ Create Amazon RDS (MySQL)
Select MySQL engine
Configure database name, username, and password
Disable public access (for security)
Allow inbound rule from EC2 Security Group

4️⃣ Update JDBC Configuration
Replace localhost with RDS endpoint in DBConnection.java
Example:
String url = "jdbc:mysql://<RDS-ENDPOINT>:3306/studentdb";

5️⃣ Deploy WAR File
Export project as WAR file
Upload WAR to EC2
Place inside /opt/tomcat/webapps/
Restart Tomcat

6️⃣ Configure Security Groups
EC2: Allow ports 22, 80, 8080
RDS: Allow access only from EC2 Security Group

7️⃣ Access Application
Open in browser:
http://<EC2-Public-IP>:8080/ProjectName/
Cloud Deployment on EC2
Secure RDS Integration
High Availability Architecture
