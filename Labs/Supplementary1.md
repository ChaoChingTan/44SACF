# Supplementary Lab 1

## Objectives

- Create an EC2 instance in your sandbox environment
- Connecting to your EC2 instance via SSH
- Accessing your web server running on EC2

## Create an instance in your sandbox environment

- Start your sandbox environment
- Create a Linux EC2 instance in a public subnet (You may use the default VPC for this or create a Lab VPC)
- For instance AMI, choose the Amazon Linux 2 AMI
- Ensure that the security group allows public access to the HTTP port (port 80) and SSH port (port 22)
- Generate a new key pair for this instance. You may refer to the [AWS Documentation on how to create and download key pairs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/create-key-pairs.html) for the guide
- Take note of the following user data to be included when creating the EC2 instance
- Refer to the [AWS Documentation on user data](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html) if required

---
#!/bin/bash

sudo yum install httpd -y

sudo systemctl start httpd

sudo systemctl enable httpd

---

## Connecting to your EC2 instance via SSH

Most of you will be running Windows on your device

Refer to the [AWS Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/putty.html) on how to connect to your Linux instance from Windows using PuTTY

While connected to your EC2 instance via SSH, run the command: **ip address show** and capture a print screen to be submitted later.

## Accessing your web server running on EC2

- From the EC2 dashboard, locate the public IP address of your EC2 instance and connect to it via a web browser.

## Submission

- The printscreen from the SSH session you captured earlier is to be submitted
- Take a scrrenshot of your webpage in your browser, showing the IP address
- Submit your work to the following [google form](https://docs.google.com/forms/d/e/1FAIpQLScSu_XY2bUksOdSnYicVS4u5RAyarcOo8V_XR0FhZ6pgLN75Q/viewform)
