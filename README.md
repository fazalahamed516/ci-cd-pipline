# ci-cd-pipline
# Installing Docker and Jenkins on AWS EC2 Instance (Amazon Linux 2)

This guide provides step-by-step instructions to install Docker and Jenkins on an AWS EC2 instance running Amazon Linux 2.

## Prerequisites

- An AWS account.
- Key pair: **Devops key** for SSH access.
- Basic knowledge of using SSH and command line.

## Step 1: Launch an EC2 Instance

1. Go to the AWS Management Console and navigate to **EC2**.
2. Launch a new EC2 instance:
   - Choose **Amazon Linux 2 AMI** as the AMI.
   - Select an **instance type** (e.g., `t2.micro`).
   - Configure the **key pair** to connect via SSH (**Devops key**).
   - **Configure security group**:
     - Allow **SSH (port 22)** for your IP.
     - Allow **HTTP (port 80)** and **Jenkins (port 8080)**.
   - Launch the instance.
3. Connect to your EC2 instance using SSH:
   ```bash
   ssh -i "Devops key.pem" ec2-user@3.25.55.93
