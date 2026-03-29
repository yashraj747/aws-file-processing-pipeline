# 🚀 AWS Event-Driven File Processing Pipeline

## 📌 Overview

This project demonstrates a fully serverless, event-driven architecture built on AWS. When a file is uploaded to Amazon S3, it automatically triggers a pipeline that processes the file and sends an email notification using Amazon SES. The system is designed to be scalable, decoupled, and production-ready.

---

## 🏗️ Architecture

S3 → Lambda → SQS → Lambda → SNS → Lambda → SES → Email 📧

---

## ⚙️ AWS Services Used

* 🪣 Amazon S3 (File Storage & Trigger)
* ⚡ AWS Lambda (Compute Functions)
* 📬 Amazon SQS (Message Queue)
* 📢 Amazon SNS (Notification Service)
* 📧 Amazon SES (Email Delivery)
* 📊 Amazon CloudWatch (Logging & Monitoring)

---

## 🚀 Workflow

1. 📤 A file is uploaded to the S3 bucket
2. ⚡ S3 triggers a Lambda function (s3-to-sqs-producer)
3. 📬 Lambda sends a message to SQS
4. ⚡ SQS triggers another Lambda (sqs-worker-processor)
5. 📢 Lambda publishes a message to SNS
6. ⚡ SNS triggers a Lambda (sns-to-ses-forwarder)
7. 📧 SES sends an email notification to the user

---

## ✨ Features

* 🔄 Event-driven architecture
* 🔗 Decoupled system using SQS
* ⚡ Fully serverless (no servers required)
* 📧 Automated email notifications
* 📊 Logging and monitoring using CloudWatch
* 🚀 Scalable and fault-tolerant design

---

## 📸 Screenshots

### 🪣 S3 Upload

![S3 Upload](screenshots/01-s3-bucket-upload.png)

### ⚡ Lambda (S3 → SQS)

![Lambda Producer](screenshots/02-lambda-s3-to-sqs-producer.png)

### 📬 SQS Queue

![SQS](screenshots/03-sqs-queue-dashboard.png)

### ⚡ Lambda (SQS Worker)

![Worker Lambda](screenshots/04-lambda-sqs-worker-processor.png)

### 📢 SNS Topic

![SNS](screenshots/05-sns-topic-subscription.png)

### ⚡ Lambda (SNS → SES)

![SNS to SES Lambda](screenshots/06-lambda-sns-to-ses-forwarder.png)

### 📊 CloudWatch Logs

![Logs](screenshots/07-cloudwatch-logs-success.png)

### 📧 Email Output

![Email](screenshots/08-gmail-notification-output.png)

---

## 🧠 Learning Outcomes

* 🏗️ Designed a real-world event-driven system
* ⚡ Built serverless workflows using AWS Lambda
* 🔗 Implemented decoupling using SQS
* 📢 Used SNS for message broadcasting
* 📧 Integrated SES for email notifications
* 📊 Debugged and monitored using CloudWatch

---

## 🧪 Testing & Validation

* ✅ Tested end-to-end pipeline using S3 file uploads
* ✅ Verified message flow using SQS and Lambda triggers
* ✅ Monitored execution through CloudWatch logs
* ✅ Confirmed successful email delivery via Amazon SES

---

## 📧 Output Example

An email is automatically sent when file processing is completed, containing details about the uploaded file.

---

## 🔗 Repository

Add your GitHub repository link here after uploading.

---

## 🏁 Conclusion

This project showcases a production-style AWS serverless architecture using multiple services working together seamlessly. It demonstrates strong understanding of event-driven design, cloud integration, and scalable system building.

---
