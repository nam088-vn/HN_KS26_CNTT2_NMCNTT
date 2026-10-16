**Bài 5 : Xây dựng bộ tài liệu kỹ thuật cho dự án Smart Farm**

# **1\. Phân tích Hệ thống** 

* **Input :** Cảm biến DHT22 (Nhiệt độ & Độ ẩm không khí) \+ Cảm biến độ ẩm đất.  
* **Process:** Tiếp nhận dữ liệu, giải mã lệnh và ra quyết định kích hoạt Rơ-le.  
* **Output:** Rơ-le điều khiển bật/tắt máy bơm \+ Cảnh báo gửi tới người dùng.

# **2\. File README.md**

#  **Smart-Farm: Hệ Thống Tưới Lan Tự Động**

Hệ thống IoT thông minh giúp tự động hóa quy trình theo dõi và tưới nước cho vườn Lan, bảo vệ cây trồng và tiết kiệm năng lượng.

##  **Hướng dẫn Cài đặt**

\# Clone dự án về thiết bị  
git clone https\://github.com/smart-farm/orchid-system.git

\# Di chuyển vào thư mục và cài đặt  
cd orchid-system && npm install

\# Khởi chạy hệ thống  
npm start

##  **Tính năng Hệ thống**

* \[x\] Tự động đo nhiệt độ và độ ẩm vườn lan theo thời gian thực.  
* \[x\] Tự động kích hoạt máy bơm khi độ ẩm xuống thấp.  
* \[x\] Gửi cảnh báo về ứng dụng di động của người trồng.  
* \[ \] Tích hợp dự báo thời tiết để tối ưu lịch tưới.

##  **Bảng Thông số Kỹ thuật**

| Thành phần | Thông số Kỹ thuật | Ghi chú |
| ----- | ----- | ----- |
| **SoC Điều khiển** | ESP32 Dual-Core 240MHz, 520KB RAM | Xử lý trung tâm |
| **Cảm biến** | DHT22 (Nhiệt độ/Độ ẩm) | Sai số \$\\pm 0.5^\\circ\\text{C}\$ |
| **Nguồn cấp** | 5V DC / Adapter 220V | An toàn cho trang trại |
| **Kết nối** | Wi-Fi 802.11 b/g/n | Kết nối đám mây |

## **Chu kỳ Xử lý Lệnh**

## **Quá trình CPU xử lý lệnh tưới Lan:**

> 1. **Fetch:** CPU tải mã lệnh `CMD_WATER_ON` từ bộ nhớ RAM/Flash vào thanh ghi chỉ thị.  
> 2. **Decode:** Bộ giải mã xác định đây là lệnh xuất tín hiệu kích hoạt chân GPIO kết nối Rơ-le.  
> 3. **Execute:** CPU gửi tín hiệu mức cao (HIGH) ra chân GPIO21 để đóng Rơ-le, bật máy bơm.

   ##  **Mô hình Kim tự tháp DIKW**

   \[D\] Data: Dữ liệu thô từ cảm biến: Temp \= 36, Soil\_Humidity \= 30\.  
   \[I\] Information: Nhiệt độ hiện tại: 36°C, Độ ẩm đất: 30% (Cần tưới ngay)  
   \[K\] Knowledge: Khi Nhiệt độ \> 35°C & Độ ẩm \< 40%, gốc lan mất nước rất nhanh.  
   \[W\] Wisdom: Tự động điều chỉnh lịch tưới vào 6h sáng để tránh cháy lá.  
        
   **CẢNH BÁO XỬ LÝ TRÀN RAM :**

> Khi hệ thống ghi quá nhiều nhật ký (logs) làm bộ nhớ RAM 520KB bị đầy, thiết bị có thể bị treo.

> 

> 

> **Cách xử lý an toàn:**

> 1. Tự động xoá nhật ký đệm cũ khi dung lượng RAM trống dưới 15%.  
> 2. Tự động chuyển dữ liệu nhật ký sang thẻ nhớ SD/Cloud định kỳ 5 phút/lần.  
> 3. Trong trường hợp khẩn cấp , SoC sẽ tự động khởi động lại an toàn mà không làm ngắt kết nối trạng thái Rơ-le máy bơm.

# **3\. Kiểm thử**

* **Edge Case đã xử lý:** Tình huống RAM bị đầy do lưu nhật ký quá tải đã được cấu hình tự động giải phóng vùng nhớ đệm và kích hoạt khôi phục an toàn (Soft Reset) trong mục **Lưu ý Vận hành & Bảo trì**, đảm bảo máy bơm không bị mất kiểm soát khi SoC gặp sự cố bộ nhớ.

