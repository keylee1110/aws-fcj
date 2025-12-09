---
title: "Week 4 Worklog"
date: "2025-10-27"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Làm chủ **S3 (Simple Storage Service)**.
* Hiểu về các lớp lưu trữ (Storage Classes) và chính sách vòng đời (Lifecycle).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Giới thiệu khái niệm **S3** (Buckets, Objects). <br> - Tạo S3 bucket đầu tiên. | 22/09/2025 | 23/09/2025 | <AWS Documentation> |
| 3 | - Tìm hiểu các **S3 Storage Classes** (Standard, IA, Glacier). | 23/09/2025 | 24/09/2025 | <Youtube: AWS Study Group> |
| 4 | - Cấu hình **Versioning** và **Encryption** trên S3. | 24/09/2025 | 25/09/2025 | <AWS Lab 3> |
| 5 | - Triển khai **Lifecycle Policies** để chuyển dữ liệu sang Glacier. | 25/09/2025 | 26/09/2025 | <Youtube: AWS Study Group> |
| 6 | - Host một **Static Website** trên S3. | 26/09/2025 | 27/09/2025 | <AWS Documentation> |

### Kết quả đạt được tuần 4

* **Thứ 2 (22/09/2025):**
    - Tạo nhiều **S3 Buckets** thông qua Console và CLI.
    - Upload và quản lý các file object.

* **Thứ 3 (23/09/2025):**
    - Phân tích sự khác biệt chi phí giữa S3 Standard, Intelligent-Tiering và Glacier.

* **Thứ 4 (24/09/2025):**
    - Bật tính năng **Versioning** để bảo vệ dữ liệu khỏi xóa nhầm.
    - Bật mã hóa Server-Side Encryption (SSE-S3).

* **Thứ 5 (25/09/2025):**
    - Tạo quy tắc Lifecycle để tự động chuyển object sang **Glacier** sau 30 ngày.

* **Thứ 6 (26/09/2025):**
    - Host thành công website tĩnh cá nhân sử dụng S3.
    - Cấu hình Bucket Policy cho phép truy cập công khai (public read).
