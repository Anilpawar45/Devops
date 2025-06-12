# AWS Three Tier Web Architecture
## Description:
This workshop is a hands-on walk through of a three-tier web architecture in AWS. We will be manually creating the necessary network, security, app, and database components and configurations in order to run this architecture in an available and scalable manner.

## Architecture Overview
![Screenshot (46)](https://github.com/user-attachments/assets/ec2e37df-9379-4b09-afba-372f3f2e30f3)

In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.

# Creating 3 Tier Architecture & Integrating Other AWS Resources
## Step 1: Download Code from GitHub in Your Local System
## Step 2: Create Two S3 Buckets
1.Create one S3 bucket for storing web-server & app-server code.
2.Upload the code to your S3 from your local system.
3.Create another S3 bucket for VPC flow logs.
