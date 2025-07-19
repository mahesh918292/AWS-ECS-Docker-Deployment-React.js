# Deploy Dockerized Application on AWS ECS

Step-by-step guide to push a Docker image to Amazon ECR and deploy it on ECS.

---

## Step 1: Create an IAM Role for ECR Push

Create an IAM role to allow pushing Docker images from your local machine to Amazon ECR.

![Step 1 - IAM Role Creation](https://github.com/user-attachments/assets/6a9e40d3-85dc-4101-a33d-677796bf7c66)

---

## Step 2: Create a Repository in Amazon ECR

Create a repository to store your Docker image.

![Step 2 - Create ECR Repository](https://github.com/user-attachments/assets/6d72660f-a4de-4959-818e-dd8ea3e7d1cc)

---

## Step 3: Create a Task Definition

Configure your task with required resources, networking (VPC, subnets, security groups), Docker image URL, ports, and other settings.

![Step 3 - Task Definition Part 1](https://github.com/user-attachments/assets/c061efea-335c-4dd0-9a7a-44c52b55fe0d)  
![Step 3 - Task Definition Part 2](https://github.com/user-attachments/assets/2b42d15d-a20c-49cf-9186-7cd54cf132b8)  
![Step 3 - Task Definition Part 3](https://github.com/user-attachments/assets/78a80d76-6f10-46a0-8f5d-87c8e6ee9c6b)

---

## Step 4: Create an ECS Cluster

Create a cluster where your container tasks will run.

![Step 4 - Create ECS Cluster](https://github.com/user-attachments/assets/daa4491c-8a58-4c7d-b849-a146486d9007)

---

## Step 5: Create a Service and Attach Task Definition

Create a service to manage task deployment and scaling. Attach your task definition and specify the service name.

![Step 5 - Create ECS Service](https://github.com/user-attachments/assets/9c373211-ada6-419b-a236-7140f2e0a174)  
![Step 5 - Attach Task to Service](https://github.com/user-attachments/assets/0e04f8d1-427f-49f2-b3f1-b19fc19edce1)  
![Step 5 - Configure Service Settings](https://github.com/user-attachments/assets/d2141c31-ef39-4de9-b2df-ac3a27c4aae5)

---

## Final Step: Verify Network Mappings

After creating the service, select the running task inside the service and check the **Network Mappings** to verify port configuration.

---

> **Tip:**  
> Ensure your security groups and load balancers (if any) allow inbound traffic on the mapped ports.

---

If you want, I can help you add code snippets, automation scripts, or AWS CLI commands to this README. Just ask!
