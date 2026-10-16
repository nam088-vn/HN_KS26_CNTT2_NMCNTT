**Bài 6 : Sự cố tài liệu dự án trên GitHub**

# **Phân tích: Sai lầm của Nam và Ưu điểm Markdown**

### **2 sai lầm trong tư duy dùng Rich Text :**

1. **Dùng sai định dạng lưu trữ:** `.docx` là file nhị phân chứa nhiều mã định dạng ẩn, không phải văn bản thuần nên GitHub không thể đọc trực tiếp và gây xung đột toàn bộ file dù chỉ sửa 1 dấu phẩy.  
2. **Nguy cơ hỏng file cao:** File nhị phân nếu mất 1 byte dữ liệu do lỗi mạng sẽ bị lỗi cấu trúc và hỏng hoàn toàn, không mở được.

### **Tại sao Markdown an toàn & nhẹ hơn?**

* **An toàn :** Markdown là Plain Text, đọc được từng ký tự mã ASCII/UTF-8. Nếu mất vài byte, file chỉ mất vài chữ chứ không hỏng toàn bộ.  
* **Tương thích Git Diff & Nhẹ:** Git dễ dàng so sánh từng dòng thay đổi , hiển thị xem trực tiếp trên GitHub và dung lượng cực nhẹ.

# **Hoàn thiện: Chuyển đổi sang Markdown** 

# **GreenTech: Giải Pháp Nông Nghiệp Xanh**

Dự án ứng dụng công nghệ IoT vào quản lý và tự động hóa trang trại, giúp tối ưu nguồn tài nguyên và nâng cao năng suất cây trồng.

## **Mục tiêu Dự án**

* \[x\] Tự động hóa quy trình tưới tiêu và giám sát môi trường.  
* \[x\] Giảm tiêu thụ điện, nước trong sản xuất nông nghiệp.  
* \[ \] Tích hợp trí tuệ nhân tạo (AI) để dự báo sâu bệnh.

## **So sánh Giải pháp**

| Tiêu chí | Phương pháp Truyền thống | Giải pháp GreenTech |
| ----- | ----- | ----- |
| **Giám sát** | Thủ công tại vườn | Tự động qua Cảm biến và App |
| **Tối ưu nước** | Dựa trên kinh nghiệm | Tưới chính xác theo độ ẩm đất |
| **Hiệu quả** | Tốn chi phí nhân công | Tiết kiệm 40% tài nguyên |

