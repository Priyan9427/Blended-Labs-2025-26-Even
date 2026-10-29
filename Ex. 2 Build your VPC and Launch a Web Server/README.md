# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: Priyan U
* **Register Number**: 212224040254
* **Date of Submission**: 29-10-2026

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

1\. Created a VPC with the CIDR block `10.0.0.0/16` to provide an isolated network for AWS resources.

2\. Created a public subnet with the CIDR block `10.0.1.0/24` and enabled automatic public IPv4 address assignment.

3\. Created and attached an Internet Gateway to the VPC, then configured a route table with the default route `0.0.0.0/0` to enable internet connectivity.

4\. Created a security group allowing SSH (port 22) and HTTP (port 80), then launched an EC2 instance using Amazon Linux 2 in the public subnet.

5\. Installed and started the Apache web server on the EC2 instance, created a simple HTML page, and accessed it through the instance's public IP address using a web browser.

---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1918" height="1095" alt="Screenshot 2026-10-29 155754" src="https://github.com/user-attachments/assets/833b9950-92c6-4fe2-bae5-0ccba6dbb68c" />

<img width="1918" height="1090" alt="Screenshot 2026-10-29 155901" src="https://github.com/user-attachments/assets/6edb4e2f-cdbf-44a9-b088-5c1a3ec9f373" />

---

### Screenshot 2: EC2 Instance Running


<img width="1918" height="1088" alt="Screenshot 2026-10-29 160513" src="https://github.com/user-attachments/assets/b5092a8a-3abe-4aed-b011-ec85c0bee067" />


---

### Screenshot 3: Web Server Output in Browser

<img width="1600" height="809" alt="555779211-f0fa2eef-f9e2-46c0-a73a-043c4c44931a" src="https://github.com/user-attachments/assets/73480fca-6f66-4e51-835e-3c87ec5aaef2" />

---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
