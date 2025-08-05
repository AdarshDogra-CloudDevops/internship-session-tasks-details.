# Cloud Learning Timeline

---

## WEEK -1 [23/06/2025 — 29/06/2025]

### 25 JUNE  
**Basics of Cloud:**
- What is cloud computing  
- Shared responsibility model  
- Deployment models:
  - Private Cloud
  - Public Cloud
  - Hybrid Cloud
  - Multi Cloud  
- Benefits of cloud services:
  - Scalability
    - Horizontal scaling
    - Vertical scaling
  - High availability
  - Reliability and predictability
  - Security and governance
  - Manageability  
- Service models:
  - IaaS
  - PaaS
  - SaaS  
- Azure physical infrastructure:
  - Regions
  - Availability Zones
  - Data Centres
  - Resource Groups
  - Subscriptions

---

## WEEK -2 [30/06/2025 — 06/07/2025]

### 30 JUNE  
- Azure Scopes (Entra ID, Management Groups, Subscription, RG)  
- Entra ID Introduction (Directory)  
- How Licensing Works (Entra ID P2)  
- App Registration / Enterprise Application  
- Roles & Administrators at Entra ID  
- Subscription (RBAC, Custom RBAC, Control/Data Plane, Policy, Subs Management)  
- Resource Locks, Managed RGs  
- Virtual Network Overview  
- NSG, Subnetting  
- IPv4 Classes, Decimal to Binary conversion for IPs  

### 01 JULY  
**AZURE TASK:**  
**ARM Template with Custom Script Extension (CSE)**  
Create an ARM template to:

1. **Resource Deployment via ARM:**
   - Deploy a Windows Server 2022 VM and required resources
   - Use CSE for post-deployment configuration

2. **Custom Script Extension Tasks:**
   - Disable Windows Defender Firewall
   - Install:
     - Google Chrome
     - Visual Studio Code
     - Power BI Desktop

3. **Desktop Customization:**
   - Shortcuts for Chrome, VS Code, Power BI
   - Browser shortcut to: [https://portal.azure.com](https://portal.azure.com)
   - `VMDetails.txt` file with:
     - Username
     - Admin Password

**File Naming Conventions:**
- ARM Template: `azuredeploy.json`
- Parameters File: `azuredeploy.parameters.json`
- PowerShell Script for CSE: `vm-setup.ps1`

**Expected Outcome:**  
The VM should be fully configured post-deployment with all specified desktop shortcuts and files.

### 02 JULY  
Explored the above task for a **Linux VM**

### 03 JULY  
_**NO ONE CONNECTED – REVISED FROM DOCUMENTATION**_  
- Load Balancer, Network Watcher, Traffic Manager  
- Routing methods, Routing protocols  
- Configure port forwarding in Azure Load Balancer via portal  
- Configure Traffic Manager with different routing methods  
- VPN, Virtual Network Gateway, Local Gateways  
- Connections (Point-to-site, Site-to-site), VNet Peering

### 04 JULY  
**AWS Topics:**
- AWS Organization and Account Structure  
- VPC  
- Public and Private Subnets  
- Gateway Attachments  
- Public and Private IP CIDR ranges  

**Tasks:**

- **Task 1:**  
  - Create a VPC (any range) with 1 subnet  
  - Launch 2 Linux EC2 instances  
  - Ensure both instances can ping each other  

- **Task 2:**  
  - Create a VPC (any range) with 2 subnets (Public and Private)  
  - Launch 1 EC2 in the public subnet, 1 in the private subnet  
  - From the public instance, SSH into the private instance and ping each other  

---

## WEEK -3 [07/07/2025 — 13/07/2025]

### 07 JULY  
**AWS Tasks:**

- **Task 1:**  
  - Use Windows Server 2022 AMI (30 GB disk)  
  - Attach an additional 1 GB volume  
  - Store data and create files on it  
  - Detach volume, attach to a new instance and verify contents

- **Task 2:**  
  - Explore NAT Gateway / NAT Instance  
  - Architecture:
    - Public Subnet
    - Private Subnet
    - NAT Gateway / Instance  
  - Ensure private subnet instances can access the internet via NAT  

### 08 JULY  
**AWS Task:**  
- Create a specialized image of Windows EC2  
- Installed Software:
  - VS Code
  - Git Bash
  - IIS Web Server with sample web page  
- Share AMI with given AWS account ID

### 09 JULY  
**Topics:**
- Security Groups vs Network ACL  
- Auto Scaling Group  
- Load Balancer (Application / Network)

### 10 JULY  
**AWS Task:**  
- Create a **Highly Available Architecture**
  - Use Application Load Balancer
  - 2 EC2 instances in a target group across 2 AZs
  - Auto Scaling should replace a terminated instance within 5 minutes

### 11 JULY  
**CloudFormation Concepts (Self-study)**

**Task:**  
- Create a simple EC2 instance using CFT

---

## WEEK -4 [14/07/2025 — 20/07/2025]

### 14 JULY  
**CloudFormation Concepts SESSION**

**Task:**  
Create a CFT which deploys following resources:
VPC 
Subnet
LINUX EC2 Instance
Key
Outputs: EC2 Name, ID, Public ip address of ec2 instance 
-> ENABLED PASSWORD BASED LOGIN TOO, WITH BOTH PASS OR KEY

### 15 JULY  

**Task:**  
-Create a CFT which deploys following resources:
-VPC 
-Subnet
-WINDOWS EC2 Instance
-Key
-Outputs: EC2 Name, ID, Public ip address of ec2 instance 
-> ENABLED PASSWORD BASED LOGIN ONLY WITHOUT KEY .

**Task:**

-public subnet windows machine.
-private subnet linux machine.
-login from windows machine into linux machine using password.


### 16 JULY 

 **Task:**
create a aws cft which satisfy below conditions:
 
-Take input from the user regarding OS he wants to deploy
-If user chooses windows then it should only deploy windows server 2022 base image with IIS role installed and should host any webpage from 60+ Free HTML Website Templates Responsive & Mobile Ready
-If user chooses linux then it should only deploy linux machine with apache/httpd installed and should host any webpage from 60+ Free HTML Website Templates - Responsive & Mobile Ready
-If user chooses both then it should deploy both the machine with respective server role installed and should host any webpage from 60+ Free HTML Website Templates - Responsive & Mobile Ready
-CFT should work in us-east-1, us-east-2 region.


 ### 17 JULY
 
RDS - DID IT FROM DOCUMENTATION

 ### 18 JULY
 
**Task:**

-Connect ec2 machine with rds db mysql database first try manually and then automate everything using cft
-Note: there should not be any public endpoint available for database
-Connectivity between rds nd ec2 must be private

## WEEK -5 [21/07/2025 — 27/07/2025]

 ### 21 JULY

Manually create - ECS Cluster, Task definition, service to host simple hello world application
 
After that do everything cft
 
Host docker image on docker hub


### 22 JULY

REVISION FOR THE ASSESMENT

### 23 JULY

AWS IAM SESSION
     
### 24 JULY

IAM -Session
-permission boundary
**Task:** 
Create an IAM Policy which allows s3 bucket list, create, put objects permissions but denies everything apart from that, allows access to ec2 services in us-east-1, us-east-2 also he should be able to create, start, stop instances and delete the instances.

### 25 JULY

**ASSESMENT**
+ IAM Connect

## WEEK -6 [28/07/2025 — 03/08/2025]

### 28 JULY

**Task:**  S3
 
Bucket policy enforce - to deny access to user - test user
Enable static website - Host any simple website
Replication rules - Enable replication and try out how it works

### 29 JULY

**Task:** AWS LABS ASSIGNED COMPLETED THEM

### 30 JULY

**Task:** AZURE LABS ASSIGNED COMPLETED THEM
  

### 31 JULY

Session on azure introductory.

### 1 AUGUST

Session on azure IAM + SUBSCRIPTIONS.

## WEEK -7 [04/08/2025 — 10/08/2025 ]

### 4 AUGUST

Asked to do pending labs of azure

### 5 AUGUST

### 6 AUGUST


### 7 AUGUST


### 8 AUGUST
