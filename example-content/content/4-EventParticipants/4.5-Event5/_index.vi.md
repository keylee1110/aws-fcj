---
title: "Event 5"
date: "2025-10-06"
weight: 4
chapter: false
pre: " <b> 4.5. </b> "
---

# BÀI BÁO CÁO SỰ KIỆN: SECURITY PILLAR TRONG AWS WELL-ARCHITECTED FRAMEWORK

&emsp;**Sự kiện:** AWS Cloud Mastery Series #3: Theo AWS Well-Architected Security Pillar.

&emsp;**Ngày:** Thứ Bảy, 29 tháng 11, 2025.

&emsp;**Thời gian:** 8:30 AM – 12:00 PM (GMT+7).

&emsp;**Địa điểm:** Văn phòng AWS Vietnam, Tòa nhà Bitexco Financial Tower, Quận 1, TP.HCM.

&emsp;**Mục tiêu sự kiện:** Cung cấp kiến thức chuyên sâu về 5 trụ cột của Security Pillar trong Well-Architected Framework, bao gồm các dịch vụ, nguyên tắc cốt lõi và chiến lược phòng thủ.

---

## TÓM TẮT CHƯƠNG TRÌNH

| Thời gian         | Chủ đề                                           | Trọng tâm Chính                                                                                                                |
|:------------------|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| **8:30 – 8:50**   |  **Khai mạc & Nền tảng Bảo mật**                 | Vai trò của Security Pillar, Mô hình Trách nhiệm Chung (Shared Responsibility Model), và các mối đe dọa hàng đầu tại Việt Nam. |
| **8:50 – 9:30**   | **Pillar 1: Identity & Access Management (IAM)** | Kiến trúc IAM hiện đại (Users, Roles, Policies), IAM Identity Center, SCP, MFA và Demo Access Analyzer.                        |
| **9:30 – 9:55**   | **Pillar 2: Detection**                          | Giám sát liên tục với CloudTrail, GuardDuty, Security Hub, và mô hình Detection-as-Code.                                       |
| **10:10 – 10:40** | **Pillar 3: Infrastructure Protection**          | Bảo vệ mạng (VPC segmentation, SG vs NACL), WAF, Network Firewall, và bảo mật Workload.                                        |
| **10:40 – 11:10** | **Pillar 4: Data Protection**                    | Mã hóa (at-rest & in-transit), Quản lý khóa (KMS), Quản lý Bí mật (Secrets Manager) và Phân loại dữ liệu.                      |
| **11:10 – 11:40** | **Pillar 5: Incident Response**                  | Chu kỳ IR theo AWS, các Playbook (Key Compromise, S3 Public Exposure) và tự động hóa ứng phó (Auto-response).                  |
| **11:40 – 12:00** | **Tổng kết & Q&A**                               | Common pitfalls và lộ trình học tập Security Specialty.                                                                        |

---

## KIẾN THỨC CHUYÊN SÂU THEO 5 TRỤ CỘT

### 1. Nền tảng Bảo mật & Nguyên tắc Cốt lõi

* **Nguyên tắc Cốt lõi:** Nhấn mạnh sự cần thiết của **Least Privilege** (quyền tối thiểu), **Zero Trust** (không tin tưởng bất kỳ ai/thứ gì theo mặc định), và **Defense in Depth** (phòng thủ đa tầng).

* **Mô hình Trách nhiệm Chung (Shared Responsibility Model):** Làm rõ ranh giới trách nhiệm: AWS chịu trách nhiệm bảo mật **Cloud** (hạ tầng, vật lý), Khách hàng chịu trách nhiệm bảo mật **trong Cloud** (dữ liệu, IAM, cấu hình).

### 2. Pillar 1: Identity & Access Management (IAM)

* **Kiến trúc Hiện đại:** Tránh sử dụng **long-term credentials** (key Access Key lâu dài) cho người dùng. Ưu tiên sử dụng **Roles** cho các dịch vụ và **IAM Identity Center** (SSO) cho người dùng.

* **Kiểm soát Đa tài khoản:** Áp dụng **Service Control Policies (SCPs)** ở cấp độ AWS Organizations và **Permission Boundaries** để đặt giới hạn tối đa cho quyền được ủy thác.

* **Mini Demo:** Trình diễn cách sử dụng **Access Analyzer** và công cụ giả lập chính sách để kiểm tra và xác thực quyền truy cập trước khi triển khai.

### 3. Pillar 2: Detection (Phát hiện)

* **Giám sát Liên tục:** Sử dụng **CloudTrail** (ở cấp độ Tổ chức) để ghi lại tất cả hành động API, **GuardDuty** để phát hiện các mối đe dọa bất thường bằng Machine Learning, và **Security Hub** để tổng hợp kết quả.

* **Detection-as-Code:** Định nghĩa các quy tắc phát hiện dưới dạng code (ví dụ: Lambda, CloudFormation) để tự động hóa việc triển khai và quản lý.

### 4. Pillar 3: Infrastructure Protection (Bảo vệ Hạ tầng)

* **Network Segmentation:** Tách biệt các tầng ứng dụng (Web, App, DB) bằng **VPC segmentation**. Phân biệt rõ vai trò của **Security Groups** (stateful) và **NACLs** (stateless).

* **Bảo vệ Vùng biên:** Triển khai **WAF** (Web Application Firewall) và **Shield** để bảo vệ ứng dụng khỏi các cuộc tấn công DDoS và lớp 7.

### 5. Pillar 4: Data Protection (Bảo vệ Dữ liệu)

* **Mã hóa:** Đảm bảo dữ liệu được mã hóa cả khi **at-rest** (lưu trữ trên S3, EBS, RDS) và **in-transit** (truyền qua TLS/SSL).

* **Quản lý Khóa và Bí mật:** Sử dụng **KMS (Key Management Service)** để quản lý các khóa mã hóa chính, kiểm soát chính sách khóa và luân chuyển khóa. Sử dụng **Secrets Manager** để lưu trữ và tự động **rotation** các bí mật (mật khẩu database, API key).

### 6. Pillar 5: Incident Response (Ứng phó Sự cố)

* **Chu kỳ IR:** Hướng dẫn tuân thủ chu kỳ chuẩn của AWS (Prepare, Detect, Respond, Recover).

* **Tự động hóa Ứng phó:** Phát triển các **Playbook** (kịch bản ứng phó) tự động bằng **Lambda hoặc Step Functions** cho các sự cố phổ biến như khóa IAM bị lộ hoặc phát hiện malware trên EC2. Các bước quan trọng bao gồm **Snapshot, isolation (cách ly), và evidence collection (thu thập bằng chứng)**.

## Một số hình ảnh khi tham gia sự kiện.

![c](/images/4-Events/Event5.1.jpg)  
![c](/images/4-Events/Event5.2.jpg)
![c](/images/4-Events/Event5.3.jpg)
![c](/images/4-Events/Event5.4.jpg)
![c](/images/4-Events/Event5.5.jpg)
![c](/images/4-Events/Event5.6.jpg) 

