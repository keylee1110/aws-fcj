---
title: "Bản đề xuất"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Đề xuất – Trình phân tích Hồ sơ Thông minh
_Một giải pháp AWS Serverless hợp nhất để phân tích CV so với JD và tạo Điểm phù hợp_

---

## 1) Tóm tắt
**Trình phân tích Hồ sơ Thông minh** là một nền tảng web không máy chủ (serverless) đánh giá sự phù hợp giữa **CV** của ứng viên và **Mô tả công việc (JD)**. Nó tính toán **Điểm phù hợp**, phát hiện **lỗ hổng kỹ năng**, và cung cấp **gợi ý học tập cá nhân hóa**.
Giải pháp được thực hiện bởi một nhóm 5 thành viên trong **4 tuần** trên **AWS** sử dụng các dịch vụ được quản lý, trả tiền theo mức sử dụng để giữ chi phí gần bằng không cho một khối lượng công việc demo. Giao diện người dùng được xây dựng bằng **Next.js** và được lưu trữ trên **AWS Amplify**; backend sử dụng **API Gateway + Lambda** với **DynamoDB**, **S3**, **Comprehend**, **Textract**, và **Cognito**.

**Kết quả chính**
- Sàng lọc CV nhanh hơn 90% cho các kịch bản demo.
- Điểm phù hợp khách quan với báo cáo trực quan.
- Lộ trình học tập có thể hành động cho mỗi ứng viên.

---

## 2) Tuyên bố vấn đề
### 2.1 Vấn đề là gì?
- Nhà tuyển dụng dành nhiều thời gian để đọc CV và so sánh chúng với JD theo cách thủ công.
- Ứng viên thiếu thông tin về những kỹ năng họ còn thiếu và cách để cải thiện.
- Các công cụ hiện có đắt đỏ hoặc không được thiết kế riêng cho các trường hợp sử dụng ở Việt Nam/Đông Nam Á.

### 2.2 Giải pháp
- Tải lên CV (PDF/DOCX) và JD → trích xuất văn bản và NLP tự động.
- Phát hiện **kỹ năng, kinh nghiệm, học vấn**; tính toán **Điểm phù hợp** so với JD.
- Đề xuất **lộ trình kỹ năng** được ánh xạ từ một kho **SkillOntology** nhỏ.
- Đăng nhập an toàn với **Cognito**; kết quả được hiển thị trên một bảng điều khiển **Next.js** sạch sẽ.

---

## 3) Kiến trúc giải pháp (tổng quan)

![Sơ đồ kiến trúc giải pháp](https://i.ibb.co/ZR0VcspJ/Solution-Architecture.png)

Kiến trúc không máy chủ, hướng sự kiện trên AWS.

**Các thành phần chính**
- **Frontend**: Giao diện người dùng Next.js (Amplify Hosting) để tải lên và bảng điều khiển kết quả.
- **Lớp API**: Amazon API Gateway → các hàm AWS Lambda.
- **Xử lý**:
  - `parseResume` → Textract (nếu là PDF được quét) → văn bản được chuẩn hóa.
  - `nlpAnalyze` → Comprehend → các thực thể/kỹ năng/cụm từ.
  - `recommendSkills` → so sánh với JD + `SkillOntology` trong DynamoDB.
- **Dữ liệu**: DynamoDB (kết quả, ontology), S3 (CV/JD tạm thời).
- **Định danh**: Cognito (mã thông báo truy cập JWT).
- **Vận hành**: IaC với AWS SAM, CI/CD qua CodeBuild + CodePipeline, ghi log trong CloudWatch.

**(Một sơ đồ kiến trúc Mermaid được cung cấp riêng.)**

---

## 4) Triển khai kỹ thuật
### 4.1 Ngăn xếp công nghệ
- **Backend**: .NET 8 (C# Minimal API trên Lambda)
- **Frontend**: Next.js + TailwindCSS (Amplify Hosting)
- **AWS**: Lambda, API Gateway, DynamoDB, S3, Cognito, Comprehend, Textract
- **IaC**: AWS SAM
- **CI/CD**: CodeBuild + CodePipeline

### 4.2 Luồng từ đầu đến cuối
1. Người dùng xác thực qua **Cognito** và nhận JWT.
2. Frontend yêu cầu **URL đã ký trước** đến **S3** → tải lên CV/JD.
3. API Gateway gọi **Lambda `parseResume`**:
   - Nếu là bản quét PDF → **Textract** → trích xuất văn bản; nếu không thì phân tích trực tiếp.
   - Dọn dẹp và chuẩn hóa → lưu trữ các tạo phẩm tạm thời trên S3.
4. **Lambda `nlpAnalyze`** sử dụng **Comprehend** để phát hiện các thực thể/kỹ năng → ghi kết quả vào **DynamoDB**.
5. **Lambda `recommendSkills`** tải **SkillOntology** từ DynamoDB → so sánh CV với JD → tính toán **Điểm phù hợp** + các lỗ hổng.
6. Frontend truy vấn kết quả qua API → hiển thị biểu đồ/bảng.

### 4.3 Mô hình dữ liệu (DynamoDB – đơn giản hóa)
- **Bảng `Profiles`** (PK: `userId`, SK: `profileId`) – lưu trữ bản phân tích CV mới nhất.
- **Bảng `Analyses`** (PK: `analysisId`) – điểm phù hợp, lỗ hổng, dấu thời gian.
- **Bảng `SkillOntology`** (PK: `skillId`, thuộc tính: `name`, `tags`, `learningPath[]`).

### 4.4 API (cấp cao)
- `POST /upload-url` → ký trước cho CV/JD.
- `POST /analyze` → kích hoạt quy trình cho một cặp khóa S3 nhất định.
- `GET /analyses/{id}` → trả về Điểm phù hợp và các đề xuất.
- `GET /skills/{id}` → (tùy chọn) lấy lộ trình học tập của một kỹ năng.

---

## 5) Mốc thời gian và các cột mốc (4 tuần)
| Tuần | Cột mốc                      | Sản phẩm                                          |
| ---- | ---------------------------- | --------------------------------------------------- |
| 1    | Nền tảng                     | Mẫu SAM, bảng DynamoDB, Cognito, giao diện người dùng cơ bản |
| 2    | Phân tích & NLP              | `parseResume`, `nlpAnalyze`, phân tích JD, kiểm thử đơn vị |
| 3    | Tích hợp Recommender & FE   | `recommendSkills`, bảng điều khiển, biểu đồ         |
| 4    | Demo & hoàn thiện            | Kiểm thử E2E, ghi log, điều chỉnh chi phí, slide deck |

---

## 6) Ước tính ngân sách (quy mô demo)
_Chỉ định, giả sử < 500 yêu cầu/tháng_
- **Lambda**: ~$0.02
- **API Gateway**: ~$0.01
- **S3** (vài GB, yêu cầu thấp): ~$0.10
- **DynamoDB** (theo yêu cầu, R/W thấp): ~$0.05
- **Amplify Hosting**: ~$0.30
- **Comprehend + Textract (các trang nhỏ)**: ~$0.40
- **Cognito**: $0.00
**Tổng cộng ≈ $0.9 / tháng (~$10 / năm)**

---

## 7) Bảo mật, rủi ro và biện pháp giảm thiểu
**Bảo mật**
- Các bucket S3 riêng tư với **SSE‑KMS**; chỉ tải lên bằng URL đã ký trước.
- **IAM quyền tối thiểu**; API được bảo vệ bởi **Cognito JWT**.
- **Che dấu PII** cho các bản ghi log; cảnh báo **CloudWatch**.
- Tùy chọn: đặt quy tắc vòng đời để xóa CV/JD thô sau khi phân tích.

**Rủi ro và biện pháp giảm thiểu**
- _Độ chính xác của NLP_: Cung cấp các định dạng được hỗ trợ + dự phòng bằng các quy tắc từ khóa.
- _CV lớn/không sạch_: Xác thực kích thước/định dạng; làm sạch trước khi NLP.
- _Chi phí tăng đột biến_: Cảnh báo Ngân sách AWS; giới hạn số trang cho mỗi yêu cầu.

---

## 8) Kết quả mong đợi
- Tự động khớp CV‑JD với **Điểm phù hợp** minh bạch.
- Phân tích trực quan về **các kỹ năng khớp so với các lỗ hổng** và **lộ trình học tập**.
- Ngăn xếp không máy chủ, vận hành thấp, dễ dàng demo, mở rộng và bản địa hóa.

---

## 📄 Tài liệu đề xuất (Google Docs)


👉 **Xem lại đề xuất tại đây:**
[LIÊN KẾT GOOGLE DOC](https://docs.google.com/document/d/1ALFieRvZWl1Azg3C8a7L8Z-iL6-chpzS/edit?usp=sharing&ouid=100398969873071071371&rtpof=true&sd=true)
