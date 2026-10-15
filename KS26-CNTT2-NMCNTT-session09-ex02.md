**Bài 2 : Kiểm tra tài liệu trước khi xuất bản**

### **Phần 1\. Phân tích lỗi cú pháp**

1. **Thừa khoảng trắng trong cú pháp chèn ảnh:**  
- *Lỗi:* `[Logo PTIT] ([https://ptit.edu.vn/logo.png](https://ptit.edu.vn/logo.png))`  
- *Nguyên nhân:* Có khoảng trắng giữa ngoặc vuông `]` và ngoặc đơn `(`. Cú pháp chuẩn không được phép có khoảng trắng.  
- *Hậu quả:* Trình biên dịch hiểu đây là văn bản thường kèm ngoặc đơn, không render thành hình ảnh.  
2. **Nhảy cấp Tiêu đề (Heading) không hợp lệ:**  
- *Lỗi:* Sử dụng `# Tiêu đề 1` (H1) ngay lập tức xuống `### Giới thiệu dự án` (H3).  
- *Nguyên nhân:* Bỏ qua thẻ H2.  
- *Hậu quả:* Phá vỡ cấu trúc cây phân cấp (AST), khiến mục lục tự động (TOC) bị lỗi và giao diện hiển thị thụt lùi không đồng đều.  
3. **Sai quy tắc đệm dòng và khoảng trắng Heading:**  
- *Lỗi:* Đặt H1 rồi đến ngay H3 mà không có khoảng trống hoặc văn bản dẫn dắt, đồng thời vi phạm quy tắc "Mỗi tài liệu chỉ nên có 1 thẻ H1 duy nhất".  
- *Hậu quả:* Đưa nhiều thẻ H1 khiến trang bị loạn thứ bậc ưu tiên khi SEO hoặc render trên StackEdit.  
4. **Sai cú pháp in đậm:**  
- *Lỗi:* `Đây là đoạn văn bản in đậm.` (Thiếu cặp dấu `**` hoặc `__` bao quanh).  
- *Hậu quả:* Văn bản hiển thị dạng chữ thường.

**Phần 2\. Sửa lại mã Markdown** 

\# Giới thiệu Dự án Quản lý Đào tạo 

\!\[Logo PTIT\](https\://ptit.edu.vn/logo.png) 

\*\*Đây là đoạn văn bản in đậm.\*\* 

\#\# Mục tiêu dự án 

\- Quản lý sinh viên 

\- Quản lý môn học

