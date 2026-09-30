\# Project 001 — Secure AWS Account Foundation



\## Overview



This project documents the process of securing and preparing an AWS account for future cloud projects.



The goal was to apply basic cloud security and governance practices before deploying workloads. This included securing the root account, creating a dedicated IAM administrator, enabling MFA, managing permissions through an IAM group, investigating unexpected AWS charges, removing unused resources, and configuring cost monitoring.



This project forms part of my AWS and Cloud Security learning portfolio.



\---



\## Objectives



The objectives of this project were to:



\- Secure the AWS root account.

\- Enable Multi-Factor Authentication (MFA).

\- Avoid using the root account for daily administration.

\- Create a dedicated IAM administrator user.

\- Manage administrator permissions through an IAM group.

\- Avoid unnecessary long-term access keys.

\- Investigate AWS billing and unexpected charges.

\- Remove unused AWS resources.

\- Configure AWS Budgets for cost monitoring.

\- Verify that recurring charges stopped.



\---



\## AWS Services Used



\- AWS Identity and Access Management (IAM)

\- Amazon EC2

\- Amazon EBS

\- Amazon VPC

\- AWS Billing and Cost Management

\- AWS Cost Explorer

\- AWS Budgets



\---



\## IAM Architecture



The final IAM structure is:



```text

AWS Account

│

├── Root User

│   ├── MFA Enabled

│   ├── No Active Access Keys

│   └── Reserved for account-level tasks

│

└── IAM

&#x20;   └── Project001-Administrators

&#x20;       └── AdministratorAccess

&#x20;           └── don-admin

&#x20;               ├── Console Access

&#x20;               ├── MFA Enabled

&#x20;               └── No Access Key

