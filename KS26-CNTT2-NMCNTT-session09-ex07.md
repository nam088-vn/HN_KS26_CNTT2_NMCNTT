## **Bài 7: Gỡ Lỗi Trang Hướng Dẫn Nộp Bài Của Giảng Viên**

## **Phần 1: Phân tích lỗi**

### **Liệt kê lỗi và Hậu quả khi Render**

| Vị trí | Đoạn bị lỗi | Nguyên nhân | Hậu quả khi Render |
| :---- | :---- | :---- | :---- |
| **Dòng 3** | \#\#\#Lưu ý quan trọng | Thiếu dấu cách sau \#\#\#. | Không tạo thành tiêu đề (\<h3\>), hiển thị dạng văn bản thường chứa nguyên chuỗi \#\#\#. |
| **Dòng 6** | \[GitHub\](github.com) | Thiếu giao thức https\:// ở đầu URL. | Trình duyệt hiểu lầm là đường dẫn tương đối (Relative Link) dẫn đến lỗi **404 Not Found** khi bấm vào. |
| **Dòng 6–9** | \-Bước 1:... đến \-Bước 4:... | Thiếu dấu cách sau dấu gạch ngang \-. | Không tạo thành danh sách (\<ul\>/\<li\>), các dòng bị hiển thị như đoạn văn bản dính liền. |
| **Dòng 7** | \*\*HNKS25CNTT1\_IT101... | Thiếu cặp dấu đóng in đậm \*\* ở cuối. | Từ từ đó trở đi bị lỗi định dạng, không in đậm đúng đoạn văn bản mong muốn. |
| **Dòng 11** | \*Nộp muộn sẽ bị trừ 50% điểm\!\*\* | Bắt đầu bằng 1 dấu \*(Nghiêng) nhưng kết thúc bằng 2 dấu \*\* (Đậm). | Lỗi bất đồng bộ cú pháp, ký tự \* và \*\*sẽ bị lộ ra giao diện thay vì đổi định dạng. |

## 

## **Phần 2: Sửa lỗi**

### **1\. Sửa lại đoạn Markdown** 

\#\# Hướng Dẫn Nộp Bài Tập \- Session 08

\#\#\# Lưu ý quan trọng

Các bước nộp bài:  
\- Bước 1: Tạo tài khoản GitHub tại \[GitHub\](https\://github.com)  
\- Bước 2: Tạo repository mới đặt tên theo định dạng \*\*HNKS25CNTT1\_IT101\_Session08\*\*  
\- Bước 3: Upload file .md của bài làm lên repository  
\- Bước 4: Copy đường dẫn và nộp lên Portal

\> Deadline: Chủ nhật 23:59 — \*\*\*Nộp muộn sẽ bị trừ 50% điểm\!\*\*\*

### **2\. Giải thích bẫy dữ liệu**

### Nếu không có https\://, Markdown sẽ hiểu đó là **Đường dẫn tương đối (Relative URL)** thuộc trang web hiện tại.

* **Hiện tượng:** Khi sinh viên nhấp vào liên kết, trình duyệt sẽ chuyển hướng đến địa chỉ dạng \[https\://ten-mien-hien-tai.com/github.com\](https\://ten-mien-hien-tai.com/github.com).

* **Kết quả:** Trang báo lỗi **404 Not Found** do địa chỉ trên không tồn tại trên hệ thống.

