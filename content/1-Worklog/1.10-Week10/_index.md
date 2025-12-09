---
title: "Week 10 Worklog"
date: "2025-12-08"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:

* Monitoring & Logging (**CloudWatch**, **CloudTrail**).
* Infrastructure as Code (**CloudFormation**).

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Configure **CloudWatch Alarms** and Dashboards. | 03/11/2025 | 04/11/2025 | <AWS Documentation> |
| 3 | - Analyze logs with **CloudWatch Logs** Insights. | 04/11/2025 | 05/11/2025 | <Youtube: AWS Study Group> |
| 4 | - Audit API calls using **CloudTrail**. | 05/11/2025 | 06/11/2025 | <AWS Lab 7> |
| 5 | - Introduction to **CloudFormation**. <br> - Write a simple YAML template. | 06/11/2025 | 07/11/2025 | <AWS Documentation> |
| 6 | - Deploy Project Infrastructure using CloudFormation. | 07/11/2025 | 08/11/2025 | <Project Work> |

### Week 10 Achievements

* **Monday (03/11/2025):**
    - Created a **CloudWatch Dashboard** to monitor EC2 CPU and Memory.
    - Set up an Alarm to send SNS notifications when CPU > 80%.

* **Tuesday (04/11/2025):**
    - Used Log Insights to query application logs.

* **Wednesday (05/11/2025):**
    - Enabled **CloudTrail** to track user activity and API usage for security auditing.

* **Thursday (06/11/2025):**
    - Learned the syntax of **CloudFormation** (Resources, Parameters, Outputs).
    - Deployed a simple S3 bucket stack via code.

* **Friday (07/11/2025):**
    - Started converting the manual project setup into CloudFormation templates for reproducibility.
