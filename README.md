# 🖥️ AWS Windows Server Lab

## 📄 Description

In this project, I demonstrate how to launch and configure a **Windows Server** instance using **Amazon Web Services (AWS)**. The goal is to build a foundational understanding of cloud infrastructure, virtual machine provisioning, and basic Windows Server administration in a secure, cloud-based environment.

This lab is a practical starting point for those pursuing roles in **cybersecurity**, **cloud administration**, or **IT infrastructure**.

---

## 🧰 Tools and Services Used

- **Amazon EC2** – for provisioning virtual machines  
- **Windows Server 2019 / 2022** – as the operating system  
- **RDP (Remote Desktop Protocol)** – for remote access  
- **AWS Identity and Access Management (IAM)** – for access control  
- **Amazon VPC** – for networking

---

## 💻 Environments Used

- AWS Management Console  
- Local Windows/macOS/Linux machine (with RDP client installed)  
- *(Optional)* Visual documentation or screenshots using Snipping Tool / Flameshot  

---

## 📋 Prerequisites

- AWS Free Tier account  
- Basic understanding of cloud concepts and Windows administration  
- Remote Desktop client (e.g., Remote Desktop Connection on Windows or Remmina on Linux)  

---

## 🚶‍♂️ Project Walk-through

### 1. 🧾 Create a Key Pair

Generate a key pair to securely access your instance:

- Go to **EC2 > Key Pairs**
- Create a new key pair (e.g., `aws-windows-key`) and download the `.pem` file  
- *(Convert to `.ppk` using PuTTYgen if on Windows and using PuTTY)*

### 2. 🏗️ Launch an EC2 Windows Server Instance

- Navigate to **EC2 > Instances > Launch Instance**
- Choose an Amazon Machine Image (AMI): `Microsoft Windows Server 2019 Base`
- Choose `t2.micro` for Free Tier
- Configure:
  - **Key Pair**: Select the one you created
  - **Network Settings**: Allow RDP (port 3389)
  - **Storage**: Accept default or expand (e.g., 30 GB)
- Launch the instance

### 3. 🌐 Configure Security Group

Ensure that your security group:
- Allows **inbound RDP (TCP 3389)** from your IP only
- Blocks all unnecessary inbound access

### 4. 🔑 Connect to the Instance

- After the instance starts, select it and click **Connect**
- Use the **Get Password** option (requires waiting ~4 minutes and uploading your `.pem` file)
- Use an RDP client with:
  - **Public IPv4 address**
  - **Username**: `Administrator`
  - **Password**: Decrypted from the key

### 5. 🛠 Initial Server Configuration

Once logged in via RDP:
- Rename the computer (optional)
- Install Windows updates
- *(Optional)* Enable and test services (e.g., IIS Web Server)

### 6. 🧯 Shutdown and Cost Control

To avoid unnecessary charges:
- Stop the instance when not in use
- Terminate when done (if no longer needed)

---

## 📸 Screenshots

Include screenshots of:

- EC2 instance launch wizard  
- Key pair creation  
- Security group settings  
- Successful RDP session  
- Installed roles/features (e.g., Server Manager with IIS)

---

## 📌 Conclusion

This lab demonstrates how to:

- Create and securely connect to a Windows Server instance on AWS  
- Configure basic network and access controls  
- Use RDP to perform administrative tasks remotely  
- Apply cloud best practices for resource and cost management
