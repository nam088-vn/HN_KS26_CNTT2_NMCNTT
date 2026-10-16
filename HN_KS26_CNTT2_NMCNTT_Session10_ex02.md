## **Bài 2 : Chuẩn hóa tài liệu cài đặt hệ thống**

## **I. Báo cáo Phân tích (Input / Output)**

1. **Input:** Chuỗi ký tự thô chứa câu lệnh, đoạn mã điều khiển và bảng thông số chưa qua định dạng, dễ gây nhầm lẫn giữa hướng dẫn và lệnh thực thi.  
     
2. **Output:** Tài liệu kĩ thuật hiển thị trực quan:  
- Tên câu lệnh/biến nổi bật nhờ **Inline Code** (`...`).  
- Mã nguồn Python có **Syntax Highlighting** (màu sắc rõ ràng theo ngôn ngữ).  
- **Bảng (Table)** so sánh trực quan và **Task List** dễ dàng theo dõi tiến độ.  
- Ký tự đặc biệt như `\*` hay `\#` hiển thị chính xác nhờ ký tự thoát (Escape `\`).

## **II. Source Code**

## **1\. Code** 

import time

HUMIDITY\_THRESHOLD \= 40  \# Khai báo ngưỡng độ ẩm

def control\_pump(current\_humidity):  
    if current\_humidity \< HUMIDITY\_THRESHOLD:  
        print("Độ ẩm thấp\! Bật máy bơm...")  
    else:  
        print("Độ ẩm đủ. Tắt máy bơm.")

\# Giả lập đọc dữ liệu  
control\_pump(35)

#### **2\. Bảng so sánh Cảm biến**

| Tiêu chí | Cảm biến Cũ (DHT11) | Cảm biến Mới (Capacitive v1.2) |
| ----- | ----- | ----- |
| **Độ bền**  | Thấp (Dễ ăn mòn) | Cao (Chống ăn mòn) |
| **Độ chính xác** | \$\\pm 5\\%\$ | \$\\pm 2\\%\$ |
| **Giao tiếp** | Digital | Analog |

#### **3\. Danh sách công việc kiểm tra (Task List)**

* \[x\] Lắp đặt cảm biến vào chậu lan  
* \[x\] Kết nối dây tín hiệu với Raspberry Pi / Arduino  
* \[ \] Chạy đoạn code Python kiểm tra máy bơm  
* \[ \] Cấu hình cảnh báo qua Telegram

