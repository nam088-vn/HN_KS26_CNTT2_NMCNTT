## **Bài 1 : Chuẩn hóa tài liệu Markdown cho dự án**

## **Phần 1\. Phân tích lỗi cú pháp**

1. **Nhảy cấp tiêu đề (`###`):**  
   * **Lỗi:** Tiêu đề nhảy trực tiếp từ `H1` xuống `H3` (bỏ qua `H2`).  
   * **Nguyên nhân:** Làm mất cấu trúc phân cấp cây thư mục, khiến giao diện render bị lệch kích thước và thiếu tính logic.  
2. **Cú pháp chèn ảnh sai:**  
   * **Lỗi:** Thừa khoảng trắng giữa `]` và `(`, đồng thời thiếu dấu `!` ở đầu (`[Logo Dự án] (...)`).  
   * **Nguyên nhân:** Markdown hiểu đây là một đường link văn bản bị lỗi cú pháp chứ không phải lệnh chèn ảnh, dẫn đến **ảnh không hiển thị**.  
3. **Cú pháp in đậm sai:**  
   * **Lỗi:** Chỉ dùng $1$ dấu sao hai đầu (`*Rất quan trọng*`).  
   * **Nguyên nhân:** $1$ dấu sao tạo chữ *in nghiêng*. Để **in đậm**, bắt buộc phải dùng $2$ dấu sao (`**Rất quan trọng**`).  
4. **Khoảng cách sau ký tự `#` :**  
   * **Quy tắc:** Cần giữ nguyên tắc **mỗi bài chỉ có** $1$ **H1 duy nhất** và bắt buộc phải có $1$ **khoảng trắng** sau dấu `#` để trình dịch nhận diện đúng tiêu đề.

## **Phần 2\. Mã Markdown hoàn thiện**

\# Lợi ích của rau sạch

\#\# Danh sách các loại rau

\!\[Logo Dự án\](https\://greentech.vn/logo.png)

\*\*Rất quan trọng\*\*

