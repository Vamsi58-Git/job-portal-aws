## Serverless Job Application Portal

A fully functional **Serverless Web Application** built using AWS services with a frontend hosted on a VPS using Nginx.

---

#  Live Website

🔗 http://3.230.125.31

---

#  Project Objective

To build a **Job Application Portal** using a serverless architecture where users can view job details and submit applications without any traditional backend server.

---

#  Architecture Diagram


User
↓
Frontend (HTML / CSS / JavaScript on VPS + Nginx)
↓
Amazon API Gateway (REST API)
↓
AWS Lambda (Backend Logic)
↓
Amazon DynamoDB (Database)
↓
Amazon CloudWatch (Logs & Monitoring)


---

# ☁️ AWS Services Used

## 🟠 AWS Lambda
- Handles backend logic
- Generates unique application ID
- Stores data in DynamoDB

## 🔵 Amazon API Gateway
- Exposes REST API endpoint `/apply`
- Connects frontend with Lambda

## 🟡 Amazon DynamoDB
- NoSQL database
- Stores all job applications

## 🟢 Amazon CloudWatch
- Monitors logs
- Debugging and performance tracking

---

# Features

✔ Job details display  
✔ Responsive application form  
✔ Form validation  
✔ Serverless backend  
✔ Unique application ID generation  
✔ Real-time database storage  
✔ Cloud monitoring  

---
## DynamoDB Table Structure

Table Name: JobApplications

Field	Type
applicationId	String (Primary Key)
fullName	String
email	String
phoneNumber	String
qualification	String
experience	String
skills	String
coverLetter	String
appliedDate	String
---
## VPS + Nginx Setup
Ubuntu VPS hosted on AWS Lightsail
Nginx used to serve frontend files
Public IP exposes application

##  Tech Stack
HTML5
CSS3
JavaScript (Vanilla)
AWS Lambda
Amazon API Gateway
Amazon DynamoDB
Amazon CloudWatch
Linux VPS (Ubuntu)
Nginx
---
#  API Endpoint

## ➤ POST /apply


https://dqg1tvzuu0.execute-api.us-east-1.amazonaws.com/prod/apply


---

#  Test JSON Payload

Use this format to test API:

```json
{
  "fullName": "Vamsi Krishna",
  "email": "vamsi@gmail.com",
  "phoneNumber": "9876543210",
  "qualification": "B.Tech",
  "experience": "2",
  "skills": "AWS, Java, SQL",
  "coverLetter": "I am interested in this role"
}
📤 Lambda Response Example
{
  "message": "Application submitted successfully",
  "applicationId": "550e8400-e29b-41d4-a716-446655440000"
}
