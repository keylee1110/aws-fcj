---
title: "Event 5"
date: "2025-10-06"
weight: 4
chapter: false
pre: " <b> 4.5. </b> "
---

# EVENT REPORT: THE AWS WELL-ARCHITECTED SECURITY PILLAR

&emsp;**Event:** AWS Cloud Mastery Series #3: Following the AWS Well-Architected Security Pillar.

&emsp;**Date:** Saturday, November 29, 2025.

&emsp;**Time:** 8:30 AM – 12:00 PM (GMT+7).

&emsp;**Location:** AWS Vietnam Office, Bitexco Financial Tower, District 1, Ho Chi Minh City.

&emsp;**Event Objective:** To provide in-depth knowledge on the 5 pillars of the Security Pillar within the Well-Architected Framework, including core principles, services, and defense strategies.

---

## PROGRAM SUMMARY

| Time              | Topic                                            | Key Focus                                                                                                               |
|:------------------|:-------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| **8:30 – 8:50**   | **Opening & Security Foundation**                | Role of the Security Pillar, Shared Responsibility Model, and top cloud threats in Vietnam.                             |
| **8:50 – 9:30**   | **Pillar 1: Identity & Access Management (IAM)** | Modern IAM Architecture (Users, Roles, Policies), IAM Identity Center, SCP, MFA, and Access Analyzer Demo.              |
| **9:30 – 9:55**   | **Pillar 2: Detection**                          | Continuous monitoring with CloudTrail, GuardDuty, Security Hub, and the Detection-as-Code model.                        |
| **10:10 – 10:40** | **Pillar 3: Infrastructure Protection**          | Network security (VPC segmentation, SG vs NACL), WAF, Network Firewall, and Workload security.                          |
| **10:40 – 11:10** | **Pillar 4: Data Protection**                    | Encryption (at-rest & in-transit), Key Management (KMS), Secrets Management (Secrets Manager), and Data Classification. |
| **11:10 – 11:40** | **Pillar 5: Incident Response**                  | AWS IR lifecycle, Playbooks (Key Compromise, S3 Exposure), and automated response (Auto-response).                      |
| **11:40 – 12:00** | **Wrap-Up & Q&A**                                | Common pitfalls and the Security Specialty learning roadmap.                                                            |

---

## IN-DEPTH KNOWLEDGE BY THE 5 PILLARS

### 1. Security Foundation & Core Principles

* **Core Principles:** Emphasis on the necessity of **Least Privilege**, **Zero Trust** (never trust, always verify), and **Defense in Depth** (layered defense).

* **Shared Responsibility Model:** Clarifying the boundary of responsibility: AWS is responsible for the security **of the Cloud** (infrastructure, physical), while the Customer is responsible for security **in the Cloud** (data, IAM, configuration).

### 2. Pillar 1: Identity & Access Management (IAM)

* **Modern Architecture:** Avoid using **long-term credentials** (long-lived Access Keys) for users. Prioritize **Roles** for services and **IAM Identity Center** (SSO) for users.

* **Multi-Account Control:** Apply **Service Control Policies (SCPs)** at the AWS Organizations level and **Permission Boundaries** to set maximum limits for delegated permissions.

* **Mini Demo:** Demonstration of using **Access Analyzer** and the policy simulator tool to verify and validate access rights before deployment.

### 3. Pillar 2: Detection

* **Continuous Monitoring:** Utilize **CloudTrail** (at the Organization level) to log all API actions, **GuardDuty** for ML-powered abnormal threat detection, and **Security Hub** to aggregate findings.

* **Detection-as-Code:** Defining detection rules as code (e.g., Lambda, CloudFormation) to automate deployment and management.

### 4. Pillar 3: Infrastructure Protection

* **Network Segmentation:** Separate application tiers (Web, App, DB) using **VPC segmentation**. Clearly distinguish the roles of **Security Groups** (stateful) and **NACLs** (stateless).

* **Perimeter Defense:** Deploy **WAF** (Web Application Firewall) and **Shield** to protect applications against DDoS and Layer 7 attacks.

### 5. Pillar 4: Data Protection

* **Encryption:** Ensure data is encrypted both **at-rest** (stored in S3, EBS, RDS) and **in-transit** (transmitted via TLS/SSL).

* **Key and Secrets Management:** Use **KMS (Key Management Service)** to manage primary encryption keys, control key policies, and key rotation. Use **Secrets Manager** to store and automatically **rotate** secrets (database passwords, API keys).

### 6. Pillar 5: Incident Response

* **IR Lifecycle:** Guidance on adhering to the AWS standard lifecycle (Prepare, Detect, Respond, Recover).

* **Response Automation:** Develop automated **Playbooks** using **Lambda or Step Functions** for common incidents like compromised IAM keys or EC2 malware detection. Key steps include **Snapshot, isolation, and evidence collection**.

## Event Photos.

![c](/images/4-Events/Event5.1.jpg)  
![c](/images/4-Events/Event5.2.jpg)
![c](/images/4-Events/Event5.3.jpg)
![c](/images/4-Events/Event5.4.jpg)
![c](/images/4-Events/Event5.5.jpg)
![c](/images/4-Events/Event5.6.jpg) 

