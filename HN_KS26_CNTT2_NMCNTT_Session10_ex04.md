**Bài 4 : Thiết kế Prompt tối ưu cho AI Assistant**

### **1\. Thiết kế Prompt (Bản hoàn chỉnh)**

Markdown  
\# Bối cảnh  
Tôi là sinh viên năm nhất ngành Công nghệ Thông tin, chưa có kinh nghiệm thực tế về nông nghiệp công nghệ cao. Tôi đang làm quen với các khái niệm hệ thống cơ bản và muốn hiểu rõ cách hoạt động của một mô hình trang trại thông minh.

\# Nội dung  
Hãy đóng vai một gia sư công nghệ thân thiện, giải thích cho tôi về "Mô hình IPO (Input \- Process \- Output) áp dụng trong Trang trại thông minh (Smart Farm)".

\# Yêu cầu  
\- \[ \] Giải thích khái niệm IPO qua ví dụ thực tế trong trang trại (ví dụ: hệ thống tưới nước hoặc nhà kính tự động).  
\- \[ \] Phân tích rõ 3 thành phần: Input (Đầu vào là gì?), Process (Xử lý ra sao?), Output (Đầu ra nhận được gì?).  
\- \[ \] Giữ độ dài câu trả lời dưới 300 từ, trình bày ngắn gọn, dễ hiểu.  
\- \[ \] Chỉ dùng từ ngữ phổ thông, giải thích ngay nếu có thuật ngữ cơ bản.

\#\# Không cần  
\- Không cần đi sâu vào mã nguồn (code), mạch điện tử hoặc cấu hình phần cứng chi tiết.  
\- Không cần dùng các thuật ngữ tiếng Anh chuyên ngành phức tạp (như machine learning models, edge computing, protocols...).  
\- Không cần trình bày dài dòng hoặc lan man sang các chủ đề khác.

### **2\. Giải quyết Edge Case (Ngăn AI quá dài/nhiều thuật ngữ)**

Để kiểm soát độ khó và độ dài khi AI vi phạm Edge Case, Prompt đã cắm sẵn các ràng buộc cụ thể:

* **Về độ dài:** Đặt định lượng rõ ràng trong Task List: \- \[ \] Giữ độ dài câu trả lời dưới 300 từ, trình bày ngắn gọn, dễ hiểu.

* **Về thuật ngữ:** Cài đặt trực tiếp tại phần \#\# Không cần: Không cần dùng các thuật ngữ tiếng Anh chuyên ngành phức tạp và trong Task List: Chỉ dùng từ ngữ phổ thông, giải thích ngay nếu có thuật ngữ cơ bản.

### **3\. Sản phẩm: Mẫu File .md AI trả về sau khi áp dụng Prompt**

Markdown  
\# Tìm hiểu Mô hình IPO trong Trang trại Thống minh

Mô hình \*\*IPO\*\* là viết tắt của \*\*Input (Đầu vào) \- Process (Xử lý) \- Output (Đầu ra)\*\*. Đây là cách tư duy cơ bản để hiểu cách một hệ thống tự động vận hành.

\---

\#\# Ví dụ thực tế: Hệ thống tưới cây tự động

Hãy hình dung một nhà kính trồng dâu tây thông minh. Mô hình IPO sẽ hoạt động như sau:

\#\#\# 1\. Input (Đầu vào)  
Là các thông tin thu thập từ môi trường thông qua cảm biến:  
\*   Độ ẩm của đất (đất đang khô hay ẩm).  
\*   Nhiệt độ không khí trong nhà kính.

\#\#\# 2\. Process (Xử lý)  
Bộ điều khiển trung tâm (đóng vai trò như bộ não) nhận dữ liệu và phân tích:  
\*   \*So sánh:\* Độ ẩm đất hiện tại là 30%, trong khi mức chuẩn cần là 60%.  
\*   \*Ra quyết định:\* Đất quá khô, cần bật máy bơm để tưới nước.

\#\#\# 3\. Output (Đầu ra)  
Là hành động thực tế được kích hoạt dựa trên quyết định ở bước xử lý:  
\*   Máy bơm tự động bật và phun nước.  
\*   Gửi thông báo "Đã tưới nước cho dâu tây" về điện thoại của người quản lý

\#\# Tóm lại Mô hình IPO giúp trang trại thông minh \*\*"nghe/nhìn"\*\* môi trường (Input), \*\*"suy nghĩ"\*\* để đưa ra quyết định (Process), và \*\*"hành động"\*\* chính xác mà không cần con người can thiệp thủ công (Output).