---
title: "Week 6 Worklog"
date: "2025-11-10"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:

* Implement **Elastic Load Balancing (ELB)**.
* Configure **Auto Scaling Groups (ASG)**.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Understand ELB types (ALB, NLB, CLB). <br> - Create an **Application Load Balancer**. | 06/10/2025 | 07/10/2025 | <AWS Documentation> |
| 3 | - Configure **Target Groups** and Register Targets. | 07/10/2025 | 08/10/2025 | <Youtube: AWS Study Group> |
| 4 | - Introduction to **Auto Scaling**. <br> - Create Launch Template. | 08/10/2025 | 09/10/2025 | <AWS Lab 5> |
| 5 | - Configure **Auto Scaling Group** with ALB. <br> - Test scaling policies. | 09/10/2025 | 10/10/2025 | <Youtube: AWS Study Group> |
| 6 | - Stress test the architecture to trigger scaling. | 10/10/2025 | 11/10/2025 | <AWS Documentation> |

### Week 6 Achievements

* **Monday (06/10/2025):**
    - Differentiated between Application, Network, and Classic Load Balancers.
    - Deployed an **Application Load Balancer (ALB)** facing the internet.

* **Tuesday (07/10/2025):**
    - Configured Target Groups and health checks.
    - Verified traffic distribution across multiple EC2 instances.

* **Wednesday (08/10/2025):**
    - Created a **Launch Template** defining the configuration for new instances.

* **Thursday (09/10/2025):**
    - Set up an **Auto Scaling Group** spanning multiple Availability Zones.
    - Integrated ASG with the Load Balancer.

* **Friday (10/10/2025):**
    - Performed a stress test; observed new instances launching automatically as CPU load increased.
    - Verified instances terminating when load decreased.
