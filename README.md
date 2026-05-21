# Identity & Access Management(Active Directory)

## Overview

This project demonstrates the deployment and management of an Active Directory environment hosted on Google Cloud Platform (GCP). The goal was to simulate a real-world IT infrastructure, focusing on cloud networking, automated user provisioning, and hierarchical security management.

---
## Technical Stack

    Cloud Provider: Google Cloud Platform (GCP)

    Region: africa-south1 (Johannesburg, ZA)

    Operating System: Windows Server 2022 Datacenter

    Automation: PowerShell

    Services: Active Directory Domain Services (ADDS), DNS, Remote Desktop (RDP)

---
## Key Features & Achievements
### 1. Cloud Infrastructure

    Provisioned a Windows Server instance with a custom VPC network and firewall rules.

    Configured static internal IP addressing and optimized network latency by selecting the local Johannesburg region.

### 2. Active Directory Architecture

    Promoted the server to a Forest Root Domain Controller for wandile.local.

    Designed a structured Organizational Unit (OU) hierarchy (IT, Sales, Accounting) to implement departmental security boundaries.

### 3. PowerShell Automation

    Developed a custom script to automate bulk user onboarding.

    Implemented secure string encryption for passwords and enforced mandatory password resets on first login (ChangePasswordAtLogon).

    Reduced manual configuration time through CLI-first administration.

## Troubleshooting & Resolution

During the deployment, several "real-world" challenges were encountered and resolved:

    DNS Resolution Errors: Resolved Non-existent domain errors by diagnosing mismatched subnet masks and manually re-configuring IPv4 DNS priority.

    ADDS Promotion Hurdles: Fixed prerequisite failures related to the local Administrator account security requirements using the net user CLI.

    Connectivity: Utilized Test-NetConnection to diagnose cross-subnet communication gaps and validate firewall integrity
