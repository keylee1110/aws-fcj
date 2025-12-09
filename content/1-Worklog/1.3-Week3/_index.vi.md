---
title: "Week 3 Worklog"
date: "2025-10-20"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Tìm hiểu sâu về **Identity and Access Management (IAM)**.
* Khởi chạy và cấu hình **EC2 instances**.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Học về **IAM Policies** và Roles. <br> - Tạo IAM User và Group đầu tiên. | 15/09/2025 | 16/09/2025 | <AWS Documentation> |
| 3 | - Tìm hiểu các loại **EC2 instance** và giá cả. | 16/09/2025 | 17/09/2025 | <Youtube: AWS Study Group> |
| 4 | - Thực hành: Launch một **EC2 Linux instance**. <br> - SSH vào instance. | 17/09/2025 | 18/09/2025 | <AWS Lab 2> |
| 5 | - Phân biệt **Security Groups** và **NACLs**. <br> - Cấu hình Security Group cho Web Server. | 18/09/2025 | 19/09/2025 | <Youtube: AWS Study Group> |
| 6 | - Cài đặt Apache Web Server trên EC2. <br> - Tạo custom AMI. | 19/09/2025 | 20/09/2025 | <AWS Documentation> |

### Kết quả đạt được tuần 3

* **Thứ 2 (15/09/2025):**
    - Nắm vững các khái niệm cốt lõi của **IAM**: Users, Groups, Roles, Policies.
    - Đã thiết lập **MFA** để bảo vệ tài khoản root.

* **Thứ 3 (16/09/2025):**
    - Hiểu rõ các nhóm hình **EC2** (General Purpose, Compute Optimized,...).
    - Phân tích giá giữa On-Demand và Spot Instance.

* **Thứ 4 (17/09/2025):**
    - Khởi chạy thành công **EC2 instance** đầu tiên trong public subnet.
    - Kết nối thành công qua SSH sử dụng key pair.

* **Thứ 5 (18/09/2025):**
    - Cấu hình **Security Groups** cho phép traffic HTTP/HTTPS.
    - Phân biệt tường lửa stateful (SG) và stateless (NACL).

* **Thứ 6 (19/09/2025):**
    - Triển khai trang web tĩnh "Hello World" trên EC2.
    - Tạo **Amazon Machine Image (AMI)** từ instance đang chạy.
