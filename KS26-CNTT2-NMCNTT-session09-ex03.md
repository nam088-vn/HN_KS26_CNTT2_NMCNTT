## **Bài 3 : Onboarding lập trình viên mới**

## 

## **1\. Báo cáo phân tích** 

| Tiêu chí | Input  | Output  |
| :---- | :---- | :---- |
| **Định dạng** | Chuỗi văn bản thuần (Plain Text) chứa các ký tự quy ước Markdown (\#, \*, \`, \` | , \- \[ \]\`). |
| **Hiển thị Mã nguồn** | Viết cú pháp khối \`\`\`python hoặc inline code \`var\`. | Đánh dấu màu sắc theo cú pháp và tách biệt font chữ đơn cách  |
| **Hiển thị Cấu trúc** | Căn chỉnh bằng các ký tự gạch ngang  | , \-, :hoặc dấu ngoặc vuông \[ \]. |
| **Ký tự đặc biệt** | Sử dụng ký tự thoát \\trước ký tự đặc biệt (ví dụ: \\\*, \\\#). | Hiển thị nguyên bản ký tự \* hoặc \# dạng văn bản thường mà không bị chuyển thành in đậm hay Header. |

## 

## **2\. Mã nguồn File Markdown** 

\# Hướng dẫn cài đặt và cấu hình VS Code:

Tài liệu này sử dụng ký tự \`\\\#\` để hiển thị dấu thăng và \`\\\*\` để hiển thị dấu sao mà không kích hoạt định dạng Heading hoặc In đậm của Markdown.

\#\# 1\. Kiểm tra môi trường Terminal:

Nhập các tên biến \`python\_version\` và \`user\_path\` vào câu lệnh Terminal để kiểm tra cấu hình:

\`\`\`bash  
\# Kiểm tra phiên bản Python hiện tại:  
python \--version

\# Kiểm tra đường dẫn thư mục biến môi trường:  
echo \$PATH

## **3: Đoạn mã Python chạy thử**

import sys

def verify\_environment(python\_version: str, user\_path: str) \-\> None:  
    """Kiểm tra và in ra thông số môi trường thực thi."""  
    print(f"Phiên bản Python: {python\_version}")  
    print(f"Đường dẫn hiện tại: {user\_path}")  
    print(f"Hệ điều hành: {sys.platform}")

if \_\_name\_\_ \== "\_\_main\_\_":  
    current\_ver \= sys.version  
    current\_path \= sys.prefix  
    verify\_environment(python\_version=current\_ver, user\_path=current\_path)

## **4: Bảng so sánh** 

| Tiêu chí so sánh | StackEdit | VS Code |
| :---- | :---- | :---- |
| **Mục đích chính** | Chỉnh sửa và xem trước văn bản Markdown | Môi trường phát triển tích hợp (IDE) đa ngôn ngữ |
| **Môi trường hoạt động** | Chạy trực tiếp trên Web Browser | Ứng dụng Desktop (Windows, macOS, Linux) |
| **Ưu điểm nổi bật** | Cấu hình nhẹ, đồng bộ Google Drive/Dropbox, Render tức thì | Hệ sinh thái Extension phong phú, tích hợp Terminal & Debugger |
| **Quản lý dự án** | Phù hợp với file đơn lẻ hoặc tài liệu nhẹ | Quản lý thư mục dự án lớn, hỗ trợ Git nâng cao |

## **4\. Danh sách công việc cài đặt**

* \[x\] Tải và cài đặt phiên bản VS Code mới nhất.

* \[x\] Cài đặt Extension **Python** và **Markdown All in One**.

* \[ \] Mở Terminal trong VS Code và kiểm tra biến python\_version.

* \[ \] Sao chép toàn bộ nội dung file này vào StackEdit để kiểm tra giao diện Render.

