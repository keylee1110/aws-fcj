---
title: "Worklog Tuần 2"
date: 2025-09-15
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu Tuần 2:

Mục tiêu của tuần này là áp dụng kiến thức đã học để **xây dựng và triển khai** một ứng dụng đơn giản trên AWS, bao gồm:
* Cấp quyền truy cập dịch vụ AWS cho ứng dụng thông qua IAM Role.
* Thực hành tích hợp ứng dụng với dịch vụ lưu trữ (S3).
* Làm quen với cơ sở dữ liệu trên AWS (RDS/DynamoDB) để lưu trữ và quản lý dữ liệu.
* Hoàn thiện quy trình triển khai ứng dụng cơ bản từ **EC2 → IAM → Storage → Database**.

---

### Các công việc thực hiện trong tuần:

| Ngày | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo                                                                                                                                                                                                           |
| ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | - Thiết lập môi trường thử nghiệm (EC2 và S3) để kiểm tra quyền truy cập <br> - Thử cấp quyền cho ứng dụng bằng IAM user và access key, kiểm tra kết nối thành công <br> - Chuyển sang sử dụng IAM Role gắn trực tiếp cho EC2 để cấp quyền tạm thời, an toàn hơn <br> - Xác nhận ứng dụng có thể truy cập dịch vụ AWS mà không cần quản lý khóa tĩnh <br> - Dọn dẹp các tài nguyên đã tạo để tránh phát sinh chi phí                                                                                     | 09/15/2025   | 09/16/2025      | <ul><li><a href="cloudjourney.awsstudygroup.com">AWS Study Group</a></li><li><a href="https://youtube.com/playlist?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i&si=WUiw02xGd5n35cao">First Cloud Journey Bootcamp - 2025</a></li></ul>                                                                                                                                                                      |
