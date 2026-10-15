## **Bài 8: Hoàn Thiện file README Dự Án Của Nhóm**

## **Phần 1: Điền khuyết**

| Vị trí \_\_\_\_ | Giá trị điền | Giải thích lý do |
| :---- | :---- | :---- |
| **Dòng 1** (\# \_\_\_\_ 📅) | *(Khoảng trắng)* | Cú pháp H1 cần dấu \# theo sau bởi 1 khoảng trắng. |
| **Dòng 5** (\_\_\_\_bash) | \`\`\` | Mở khối mã nguồn (Code Block) với cú pháp highlight bash. |
| **Dòng 8** (cuối phần Cài đặt) | \`\`\` | Đóng khối mã nguồn (Code Block). |
| **Dòng 12, 13, 14** (\_\_\_\_ \[ \]) | \- | Dấu gạch ngang để khởi tạo danh sách công việc (Task List). |
| **Dòng 18** (| \_\_\_\_ |...) | :--- (hoặc \---) | Tạo hàng phân cách tiêu đề cột trong Bảng (Table). |

## **Phần 2: Hoàn thiện**

### **1\. File README.md hoàn chỉnh**

Markdown  
\# Ứng dụng Quản lý Lịch Học Cá nhân

Ứng dụng giúp sinh viên \*\*lên kế hoạch học tập\*\* hiệu quả.

\#\# Hướng dẫn Cài đặt

\`\`\`bash  
git clone \[https\://github.com/nhom5/lich-hoc-app\](https\://github.com/nhom5/lich-hoc-app)  
cd lich-hoc-app

## **Tính năng đã hoàn thành**

* \[x\] Đăng ký / Đăng nhập tài khoản

* \[ \] Nhắc nhở lịch học qua email

* \[x\] Xuất lịch ra file PDF

## **Bảng So sánh** 

| Công nghệ | Mục đích | Phiên bản |
| :---- | :---- | :---- |
| Python | Backend xử lý dữ liệu | 3.11 |
| Markdown | Viết tài liệu README | \- |

\#\#\# 2\. Bẫy dữ liệu (Xóa hàng phân cách bảng)

\* \*\*Hiện tượng:\*\* Toàn bộ bảng sẽ bị vỡ định dạng và hiển thị dưới dạng \*\*văn bản thô (Plain Text)\*\* chứa các dấu \`|\`.  
\* \*\*Lý do:\*\* Hàng phân cách \`| \--- |\` là ký tự bắt buộc để Trình biên dịch Markdown (Markdown Parser) nhận diện cấu trúc và render thành thẻ HTML \`\<table\>\`. Khuyết hàng này, parser sẽ coi các dòng trên và dưới chỉ là các đoạn văn bản thường.

