# Terraform AWS EC2 Deployment

Deploy AWS infrastructure using Terraform from scratch.

---

## Project Overview

This project demonstrates how to provision AWS infrastructure using Terraform Infrastructure as Code (IaC).

The infrastructure includes:

- Custom VPC
- Public Subnet
- Internet Gateway
- Route Table
- Security Group
- EC2 Instance
- Terraform Outputs

---

## Technologies Used

- Terraform
- AWS EC2
- AWS VPC
- Ubuntu 24.04
- Linux
- AWS CLI

---

## Architecture

Internet
    │
    ▼
Internet Gateway
    │
    ▼
Public Route Table
    │
    ▼
Public Subnet
    │
    ▼
EC2 Instance

---

## Project Files

| File | Purpose |
|-------|----------|
| provider.tf | AWS Provider Configuration |
| variables.tf | Input Variables |
| terraform.tfvars | Variable Values |
| main.tf | AWS Resources |
| outputs.tf | Terraform Outputs |

---

## Resources Created

- VPC
- Public Subnet
- Internet Gateway
- Route Table
- Route Table Association
- Security Group
- EC2 Instance

---

## Terraform Commands

Initialize Terraform

```bash
terraform init
```

Validate configuration

```bash
terraform validate
```

Preview infrastructure

```bash
terraform plan
```

Deploy infrastructure

```bash
terraform apply
```

Destroy infrastructure

```bash
terraform destroy
```

---

## Outputs

Example:

```
instance_id
public_ip
public_dns
vpc_id
```

---

## Lessons Learned

During this project I learned:

- Infrastructure as Code (IaC)
- Terraform Providers
- Variables
- Outputs
- AWS Authentication
- Terraform State
- Terraform Plan
- Terraform Apply
- Terraform Destroy
- AWS Networking Basics
- Security Groups
- VPC Architecture

---

## Challenges Faced

### AWS Signature Error

Issue:

```
Signature expired
```

Solution:

Synchronize system time using:

```bash
sudo timedatectl set-ntp true
```

---

### No Default VPC

Issue:

```
No default VPC
```

Solution:

Created a custom VPC using Terraform.

---

### Free Tier Instance Type Error

Issue:

```
Instance type not eligible
```

Solution:

Changed instance type to:

```
t3.micro
```

---

## Author

Mohamed Naseeb

GitHub:
https://github.com/YOUR_USERNAME
