---
title: "Week 6 Worklog"
date: "2025-11-10"
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Triển khai **Elastic Load Balancing (ELB)**.
* Cấu hình **Auto Scaling Groups (ASG)**.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Hiểu các loại ELB (ALB, NLB, CLB). <br> - Tạo một **Application Load Balancer**. | 06/10/2025 | 07/10/2025 | <AWS Documentation> |
| 3 | - Cấu hình **Target Groups** và đăng ký Targets. | 07/10/2025 | 08/10/2025 | <Youtube: AWS Study Group> |
| 4 | - Giới thiệu về **Auto Scaling**. <br> - Tạo Launch Template. | 08/10/2025 | 09/10/2025 | <AWS Lab 5> |
| 5 | - Cấu hình **Auto Scaling Group** với ALB. <br> - Test chính sách mở rộng. | 09/10/2025 | 10/10/2025 | <Youtube: AWS Study Group> |
| 6 | - Stress test kiến trúc để kích hoạt scaling. | 10/10/2025 | 11/10/2025 | <AWS Documentation> |

### Kết quả đạt được tuần 6

* **Thứ 2 (06/10/2025):**
    - Phân biệt được Application, Network, và Classic Load Balancers.
    - Triển khai một **Application Load Balancer (ALB)** public.

* **Thứ 3 (07/10/2025):**
    - Cấu hình Target Groups và Health Checks.
    - Kiểm tra việc phân phối traffic giữa nhiều EC2 instances.

* **Thứ 4 (08/10/2025):**
    - Tạo **Launch Template** định nghĩa cấu hình cho các instance mới.

* **Thứ 5 (09/10/2025):**
    - Thiết lập **Auto Scaling Group** trải dài trên nhiều Availability Zones.
    - Tích hợp ASG với Load Balancer.

* **Thứ 6 (10/10/2025):**
    - Thực hiện stress test; quan sát instance mới tự động được tạo khi CPU tăng cao.
    - Xác nhận instance tự hủy khi tải giảm.
