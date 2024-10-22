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

# Step-by-Step Guide to Setting Up AWS EKS

## Step 1: Prerequisites

1. **Create an AWS Account**:
   - If you don't have an account, sign up at [AWS](https://aws.amazon.com/).

2. **Install Required Tools**:
   - **AWS CLI**: Follow the installation guide [here](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html).
   - **kubectl**: Install from the [Kubernetes documentation](https://kubernetes.io/docs/tasks/tools/install-kubectl/).
   - **eksctl**: Install using the following command:
     ```bash
     curl --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
     sudo mv /tmp/eksctl /usr/local/bin
     ```

3. **Configure AWS CLI**:
   ```bash
   aws configure

