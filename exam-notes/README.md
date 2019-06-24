# Exam Notes

## Table of Contents

**Compute**

* [Elastic Compute Cloud (EC2)](./compute/elastic-compute-cloud.md) - virtual machines

* Lightsail

* ECR

* EC2 Container Service (ECS) - virtual environment for containers

* EKS

* Lambda - serverless function endpoint

* Batch - batch computing

* Elastic Beanstalk (EBS) - handles deployment from capacity provisioning, load balancing, auto-scaling and health monitoring

* Serverless Application Repository

**Storage**

* [Simple Storage Service (S3)](./storage/simple-storage-service.md) - object-based storage

* Elastic File Storage (EFS) - network-attached block-based storage

* S3 Glacier - data archiving

* [Storage Gateway](./storage/storage-gateway.md) - virtual machines installed in data center that can be replicated in S3

* AWS Backup

**Database**

* Relational Database Service (RDS) - SQL-based databases

* DynamoDB - NoSQL-based database

* ElastiCache - caches common-queried requests in a server

* Neptune

* Amazon Redshift - data warehousing for business intelligence

* Amazon DocumentDB

**Migration & Transfer**

* AWS Migration Hub - tracking service for migration to AWS

* Application Discovery Service - automated set of toolsto detect applications and their dependencies

* Database Migration Service - migrate on-premise to AWS database

* Server Migration Service - migrate on-premise to AWS servers

* AWS Transfer for SFTP

* [Snowball](./migration-and-transfer/snowball.md) - migrate large amount of data (TB) to AWS data centers

* DataSync

**Network & Content Delivery**

* Virtual Private Cloud (VPC)

* CloudFront

* Route 53

* API Gateway

* Direct Connect

* AWS App Mesh

* AWS Cloud Map

* Global Accelerator

**Developer Tools**

* CodeStar - project management of code, collaboration

* CodeCommit - source code repository

* CodeBuild - compiles code, performs testing and builds packages

* CodeDeploy - automates deployment to EC2, on-premise or lambda

* CodePipeline - visualize devops pipeline

* Cloud9 - web IDE

* X-Ray - debug and analyze serverless applications

**Robotics**

* AWS RoboMaker
 
**Blockchain**

* Amazon Managed Blockchain
 
**Satellite**

* Ground Station

**Management & Governance**

* AWS Organizations

* CloudWatch - monitoring service for AWS

* AWS Auto Scaling

* CloudFormation - scripting infrastructure to code

* CloudTrail - audit log for any AWS actions performed (e.g., clicks)

* Config - monitors the configuration of AWS environment

* OpsWorks - similar to Elastic Beanstalk that automates environment creation but uses both Chef and Puppet

* Service Catalog - manages catalog of IT services

* Systems Manager - interface to manage AWS resources, patch maintenance and group resources by department

* Trusted Advisor - provides advices in security and costs

* Managed Services - managed services for EC2

* Control Tower

* AWS License Manager

* AWS Well-Architected Tool

* Personal Health Dashboard
 
**Media Services**

* Elastic Transcoder - takes a video and resizes to different platforms

* Kinesis Video Streams

* MediaConnect

* MediaConvert - file-based video transcoding service, converts to different media files, broadcast

* MediaLive - video broadcasting streamlined for all screens

* MediaPackage - protects video for delivery to internet

* MediaStore - storage service for media files

* MediaTailor - toggled advertising in video streams
 
**Machine Learning**

* Amazon SageMaker - deep-learning while coding for environment

* Amazon Comprehend - sentiment analysis for data

* AWS DeepLens - artificially aware camera (physical device)

* Amazon Lex - powers Amazon Alexa Service, chatbot

* Machine Learning - different from SageMaker, general machine learning, process dataset to create models

* Amazon Polly - takes text to speech

* Rekognition - uploads a file and it tells what is the content of file

* Amazon Transcribe - transcribes videos, automatic speech recognition to text

* Amazon Translate - translates English to other languages

* Amazon Personalize

* Amazon Forecast

* Amazon Textract

* AWS DeepRacer
 
**Analytics**

* Athena - runs SQL queries against S3 buckets

* Elastic MapReduce (EMR) - processing large data for big data analysis

* CloudSearch - search capability

* Elasticsearch Service - search capability

* Kinesis - injest large amount of textual data to AWS (e.g., social media feeds)

* QuickSight - business inteligence tools

* Data Pipeline - moving data across different AWS services

* AWS Glue - extract-transform-load (ETL), converts data from a datasource to another format

* MSK

**Security, Identity, & Compliance**

* [Identity & Access Management (IAM)](./security-identity-and-compliance/identity-and-access-management.md)

* Resource Access Manager

* Cognito - device auth (sso) for temporary access to AWS resources

* Secrets Manager

* GuardDuty - monitors for malicious activities in account

* Inspector - agent installed in EC2 to run security tests, can be scheduled

* Amazon Macie - scans S3 for personally identifiable information

* AWS Single Sign-On

* Certificate Manager - for free SSL certificates

* Key Management Service

* CloudHSM (Hardware Security Modules) - dedicated-hardware to store security keys

* Directory Service - integrate Azure AD services with AWS services

* Web Application Firewall (WAF) & Shield - stops XSS, SQLI

* Artifact - for audit and compliance; portal for compliance reports

* Security Hub
 
**AWS Cost Management**

* AWS Cost Explorer

* AWS Budgets

* AWS Marketplace Subscriptions
 
**Mobile**

* AWS Amplify

* Mobile Hub - management console for AWS services

* AWS AppSync - updates data in web and mobile applications, updates offline data when you connect online

* Device Farm - testing apps on live devices
 
**AR & VR**

* Amazon Sumerian - first language written, common set of tools
 
**Application Integration**

* Step Functions - manage lambda functions

* Amazon MQ - message queues

* Simple Notification Service (SNS)

* Simple Queue Service (SQS) - oldest service launched in 2006

* Simple Workflow Service (SWF) -  workflow jobs which can include human interaction as part of the flow
 
**Customer Engagement**

* Amazon Connect - contact center, like AWS call center

* Pinpoint

* Simple Email Service (SES) - smtp
 
**Business Applications**

* Alexa for Business - dialin to a meeting room, inform IT printer is broken, order ink for printer

* Amazon Chime - video conferencing like Google Hangouts

* WorkMail - using email in Amazon
 
**End User Computing**

* WorkSpaces - VDI solution where OS is run in AWS Cloud, streaming down to the user

* AppStream 2.0 - streaming actual applications that is running in cloud; like citrix; the only service that has version in name

* WorkDocs

* WorkLink
 
**Internet of Things**

* IoT Core

* Amazon FreeRTOS - OS for microcontrollers

* IoT 1-Click

* IoT Analytics

* IoT Device Defender

* IoT Device Management - managing IoT devices

* IoT Events

* IoT Greengrass - software run local compute, messaging, data caching, sync and machine learning interface capabilities for devices securely

* IoT SiteWise

* IoT Things Graph
 
**Game Development**

* Amazon GameLift - develop games which may be a AR/VR
