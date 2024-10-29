# AWS Node.js Express Tutorial

## Project Overview
This project demonstrates how to set up and deploy a Node.js and Express application on an AWS EC2 instance. The goal is to provide an AWS-specific guide that complements [this tutorial,](https://code.visualstudio.com/docs/remote/ssh-tutorial) and serve as a continuation of my markdown practice, initiated in [this repository.](https://github.com/Roy-Kibe/skills-communicate-using-markdown) 
## Step 1: GitHub Repository Setup

### 1.1 Creating the Repository
1. Go to [GitHub](https://github.com/) and create a new repository.
2. Name the repository `AWS-NodeJS-Express-Tutorial` and add a short description.
3. Choose **Private** for initial development.
4. Initialize with:
   - A README file
   - A Node `.gitignore` to avoid pushing unnecessary files (e.g., `node_modules/`).

### 1.2 Cloning the Repository Locally
1. Copy the HTTPS URL for the repository from GitHub.
2. In your terminal, navigate to the folder where you want to store the project, then run:
   ```bash
   git clone https://github.com/username/AWS-NodeJS-Express-Tutorial.git

## Step 2: Set up and an AWS EC2 Instance.
### 2.1 Log into the AWS Management Console
- Navigate to the [AWS Management Console,](https://aws.amazon.com/console/) and log in with your account credentials.
### 2.2 Launch an EC2 Instance.
- In the AWS Management Console, locate the EC2 Dashboard by searching for "EC2" in the services menu, and click on **Launch Instance**.
![Launch Instance](/Pictures/Screenshot%20from%202024-10-29%2016-54-51.png)
### 2.3 Choose the Amazon Machine Image (AMI)
- Select Amazon Linux 2 AMI from the list of available AMIs.
![Choose AMI](/Pictures/Screenshot%20from%202024-10-29%2017-02-55.png)
### 2.4 Choose an Instance Type
- Select the **t2.micro** instance type.
- This type is free, making it suitable for testing and development.
![Instance Type](/Pictures/Screenshot%20from%202024-10-29%2017-19-51.png)
### 2.5 Configure KeyPair
- Create a new key pair or select an existing one.
- If creating a new key pair:
  - Choose a descriptive name.
  - Download the private key file (.pem) and keep it secure. You won’t be able to download it again.
- The public key will be stored on the EC2 instance, while the private key is used for SSH access.
### 2.6 Configure Security Group
- Edit the Network Settings to configure the security group.
- Set up inbound rules for the following ports:
  - SSH (Port 22): Allows secure remote access. Restrict to your IP address for better security.
  - HTTP (Port 80):Enables web traffic to your application.
Set source: Open to "Anywhere".
  - Custom TCP (Port 3000):Allows access to your Node.js application. Source: Open to your IP address only.
![Security Group](/Pictures/Screenshot%20from%202024-10-29%2017-52-05.png)
### 2.7 Launch Your Instance
- Review your configuration settings and click on Launch.



