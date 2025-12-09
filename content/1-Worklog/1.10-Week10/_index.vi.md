---
title: "Week 10 Worklog"
date: "2025-12-08"
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Giám sát & Ghi log (**CloudWatch**, **CloudTrail**).
* Cơ sở hạ tầng dưới dạng mã (**CloudFormation**).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Cấu hình **CloudWatch Alarms** và Dashboards. | 03/11/2025 | 04/11/2025 | <AWS Documentation> |
| 3 | - Phân tích log với **CloudWatch Logs** Insights. | 04/11/2025 | 05/11/2025 | <Youtube: AWS Study Group> |
| 4 | - Kiểm tra các gọi API sử dụng **CloudTrail**. | 05/11/2025 | 06/11/2025 | <AWS Lab 7> |
| 5 | - Giới thiệu về **CloudFormation**. <br> - Viết một template YAML đơn giản. | 06/11/2025 | 07/11/2025 | <AWS Documentation> |
| 6 | - Triển khai hạ tầng dự án bằng CloudFormation. | 07/11/2025 | 08/11/2025 | <Project Work> |

### Kết quả đạt được tuần 10

* **Thứ 2 (03/11/2025):**
    - Tạo **CloudWatch Dashboard** để theo dõi CPU và Memory của EC2.
    - Thiết lập Alarm gửi thông báo SNS khi CPU > 80%.

* **Thứ 3 (04/11/2025):**
    - Sử dụng Log Insights để truy vấn log ứng dụng.

* **Thứ 4 (05/11/2025):**
    - Bật **CloudTrail** để theo dõi hoạt động người dùng và sử dụng API phục vụ kiểm toán an ninh.

* **Thứ 5 (06/11/2025):**
    - Học cú pháp **CloudFormation** (Resources, Parameters, Outputs).
    - Triển khai một stack S3 bucket đơn giản bằng code.

* **Thứ 6 (07/11/2025):**
    - Bắt đầu chuyển đổi các thiết lập thủ công của dự án thành CloudFormation templates để có thể tái sử dụng.
