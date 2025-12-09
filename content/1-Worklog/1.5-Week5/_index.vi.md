---
title: "Week 5 Worklog"
date: "2025-11-03"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Khám phá **Cơ sở dữ liệu quan hệ (RDS)**.
* Khám phá **Cơ sở dữ liệu NoSQL (DynamoDB)**.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Giới thiệu về **RDS** (MySQL/PostgreSQL). <br> - Tạo một RDS instance. | 29/09/2025 | 30/09/2025 | <AWS Documentation> |
| 3 | - Kết nối EC2 tới RDS. <br> - Hiểu về **Multi-AZ** và Read Replicas. | 30/09/2025 | 01/10/2025 | <Youtube: AWS Study Group> |
| 4 | - Giới thiệu về **DynamoDB**. <br> - Tạo bảng DynamoDB. | 01/10/2025 | 02/10/2025 | <AWS Lab 4> |
| 5 | - Thực hiện thao tác CRUD trên DynamoDB dùng CLI. | 02/10/2025 | 03/10/2025 | <Youtube: AWS Study Group> |
| 6 | - So sánh use case giữa SQL và NoSQL. | 03/10/2025 | 04/10/2025 | <AWS Documentation> |

### Kết quả đạt được tuần 5

* **Thứ 2 (29/09/2025):**
    - Khởi tạo **MySQL RDS** instance trong private subnet.
    - Cấu hình Security Groups để bảo vệ truy cập database.

* **Thứ 3 (30/09/2025):**
    - Kết nối thành công web server (EC2) tới RDS database.
    - Bật tính năng **Multi-AZ** để đảm bảo tính sẵn sàng cao.

* **Thứ 4 (01/10/2025):**
    - Tạo bảng **DynamoDB** với Partition Key và Sort Key.
    - Hiểu về đơn vị dung lượng Đọc/Ghi (RCU/WCU).

* **Thứ 5 (02/10/2025):**
    - Thêm và truy vấn dữ liệu trong DynamoDB sử dụng **AWS CLI**.

* **Thứ 6 (03/10/2025):**
    - Phân tích các kịch bản phù hợp cho Database Quan hệ so với NoSQL.
    - Dọn dẹp tài nguyên để tránh phát sinh chi phí.
