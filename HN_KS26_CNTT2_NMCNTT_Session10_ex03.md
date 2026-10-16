**Bài 3 : Giảm chi phí vận hành Chatbot AI**

## **Phần 1\. Phân tích bài toán (Góc nhìn Token AI)**

AI (LLM) không đọc chữ cái hay từ ngữ trực tiếp mà xử lý dữ liệu qua các **Token** (chuỗi ký tự được mã hóa).

* **HTML tiêu tốn quá nhiều Token thừa:** HTML dùng các cặp thẻ đóng/mở rườm rà như `<strong>Nông nghiệp</strong>` (chiếm $7-9$ token). Các ký tự kỹ thuật này không mang thêm thông tin ngữ cảnh thực sự cho câu trả lời.  
* **Markdown tối ưu Token:** Markdown dùng cú pháp tối giản như `**Nông nghiệp**` (chỉ khoảng $3-4$ token).  
* **Kết quả:** Giảm số lượng Token giúp AI **phản hồi nhanh hơn**, giảm độ trễ (latency) và **tiết kiệm** \$30\\% \- 50\\%\$**chi phí API** cho hệ thống GreenTech.

## **Phần 2\. So sánh & Đánh giá giải pháp**

### **Bảng so sánh Markdown vs HTML**

| Tiêu chí | Markdown | HTML |
| :---- | :---- | :---- |
| **Cú pháp in đậm** | `**Chăm sóc lan**` (17 ký tự) | `<strong>Chăm sóc lan</strong>` (31 ký tự) |
| **Số lượng Token** | Rất ít (Tối ưu) | Nhiều (Lãng phí) |
| **Độ dễ đọc (Human-readable)** | Rất cao (Đọc được ngay ở dạng thô) | Thấp (Bị rối bởi thẻ đóng/mở) |
| **Khả năng hiển thị** | Tự động render đẹp trên app/chat | Cần bộ duyệt web (Browser) đầy đủ |

### **Giải pháp tối ưu cho hệ thống GreenTech**

**Lựa chọn:** **Chỉ sử dụng Markdown** cho toàn bộ dữ liệu trao đổi giữa AI và Người nông dân.

**Lý do chọn:**

1. **Dễ đọc với người nông dân:** Người dùng có thể đọc trực tiếp tin nhắn dạng thô hoặc qua giao diện render đơn giản mà không bị nhiễu bởi thẻ mã lệnh.  
2. **Tiết kiệm chi phí & Tăng tốc độ:** Giảm lượng Token đầu ra (Output tokens) giúp AI phản hồi ngay lập tức trên các thiết bị di động có kết nối mạng yếu ở nông thôn.  
3. **Dễ bảo trì:** Đội ngũ phát triển dễ dàng cập nhật dữ liệu tri thức nông nghiệp mà không lo lỗi sai thẻ HTML.

