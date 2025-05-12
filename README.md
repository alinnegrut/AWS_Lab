# 🖥️ AWS Windows Server Lab

## 📄 Description

In this project, I demonstrate how to launch and configure a **Windows Server** instance using **Amazon Web Services (AWS)**. The goal is to build a foundational understanding of cloud infrastructure, virtual machine provisioning, and basic Windows Server administration in a secure, cloud-based environment.

---

## 🧰 Tools and Services Used

- **Amazon EC2** – for provisioning virtual machines  
- **Windows Server 2019 / 2022** – as the operating system  
- **RDP (Remote Desktop Protocol)** – for remote access  
- **AWS Identity and Access Management (IAM)** – for access control  

---

## 💻 Environments Used

- AWS Management Console  
- Local Windows machine (with RDP client installed)  

---

## 📋 Prerequisites

- AWS Free Tier account  
- Basic understanding of cloud concepts and Windows administration  
- Remote Desktop client (e.g., Remote Desktop Connection on Windows)  

---

## 🚶‍♂️ Project Walk-through

### 1. 🧾 Create a Key Pair

Generate a key pair to securely access the instance:

- Go to **EC2 > Key Pairs**
- Create a new key pair  and download the `.pem` file  

### 2. 🏗️ Launch an EC2 Windows Server Instance

- Navigate to **EC2 > Instances > Launch Instance**
- Choose an Amazon Machine Image (AMI): `Microsoft Windows Server 2025 Base`
- Choose `t3.micro` for Free Tier
- Configure:
  - **Key Pair**: Select the one you created
  - **Network Settings**: Allow RDP (port 3389)
  - **Storage**: Accept default or expand (e.g., 30 GB)
- Launch the instance

### 3. 🔑 Connect to the Instance

- After the instance starts, select it and click **Connect**
- Use the **Get Password** option (requires waiting ~4 minutes and uploading your `.pem` file)
- Use an RDP client with:
  - **Public IPv4 address**
  - **Username**: `Administrator`
  - **Password**: Decrypted from the key

### 4. 🛠 Initial Server Configuration

Once logged in via RDP:
- Rename the computer (optional)
- Install Windows updates
- *(Optional)* Enable and test services (e.g., IIS Web Server)

### 5. 🧯 Shutdown and Cost Control

To avoid unnecessary charges:
- Stop the instance when not in use
- Terminate when done (if no longer needed)

---

## 📸 Screenshots

- EC2 instance launch wizard

![image](https://github.com/user-attachments/assets/8485a8fa-f6b4-4e0a-b5cf-e95eba4d4ebd)
![image](https://github.com/user-attachments/assets/a6dca98e-2ece-4549-8d24-01b0d5d2c88e)

- Key pair creation

![image](https://github.com/user-attachments/assets/ebfb5192-df53-45e9-baf1-134573d7a1a6)

- Security group settings

![image](https://github.com/user-attachments/assets/7f928bcb-3f71-4d2d-a826-a4f861a7f42c)

- Successful RDP session

![image](https://github.com/user-attachments/assets/bf9b3743-54ed-4d97-ab3e-5e06a4c2e9f6)
![image](https://github.com/user-attachments/assets/fb54c0dc-519f-42d5-847c-22e20c21da03)
![image](https://github.com/user-attachments/assets/de813b9e-0807-4b74-8d88-96f5267f4c26)
![image](https://github.com/user-attachments/assets/a3a63e9c-a32b-47ca-8e30-102f3d676580)
![image](https://github.com/user-attachments/assets/97314ea7-f085-48a1-a1e5-b452a8884f4f)

---

## 📌 Conclusion

This lab demonstrates how to:

- Create and securely connect to a Windows Server instance on AWS  
- Configure basic network and access controls  
- Use RDP to perform administrative tasks remotely  
- Apply cloud best practices for resource and cost management
