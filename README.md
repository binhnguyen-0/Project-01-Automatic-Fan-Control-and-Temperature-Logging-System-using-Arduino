# 🔧 Hệ thống hiển thị, lưu log, cảnh báo nhiệt độ và điều khiển quạt tự động  
**Automatic Fan Control and Temperature Logging System using Arduino**

<img width="933" height="834" alt="image" src="https://github.com/user-attachments/assets/f2b59ddb-1d8e-4e48-8439-6cec565cf014" />


---

## 🚀 Giới thiệu | Introduction

Dự án này sử dụng **Arduino Uno** để tạo ra một hệ thống theo dõi nhiệt độ, hiển thị thông tin lên **LCD**, lưu log vào **thẻ nhớ SD**, và tự động **bật quạt** khi nhiệt độ vượt quá ngưỡng cài đặt.

This project uses an **Arduino Uno** to build a temperature monitoring system that displays data on an **LCD**, logs readings to an **SD card**, and automatically **controls a fan** when overheating is detected.

---

## ⚙️ Phần cứng sử dụng | Hardware Used

| Thiết bị / Component        | Mô tả / Description              |
|-----------------------------|----------------------------------|
| Arduino Uno                 | Vi điều khiển chính              |
| LM35                        | Cảm biến nhiệt độ analog         |
| LCD 2004 I2C                | Màn hình hiển thị 20x4           |
| SD Card Module              | Lưu log dữ liệu nhiệt độ         |
| Module Relay 5V             | Điều khiển bật/tắt quạt          |
| Quạt 5V                     | Làm mát tự động                  |
| Nguồn ngoài 5V              | Cấp nguồn cho relay và quạt      |

---

## 🔋 Sơ đồ nối dây | Wiring Diagram

> 📷 Xem sơ đồ mạch phía trên để hiểu cách kết nối phần cứng  
(See the circuit diagram above for hardware connections)

### Một số chân quan trọng | Key pin mappings:

| Module             | Arduino UNO Pin |
|--------------------|------------------|
| LM35               | A0               |
| LCD SDA/SCL        | A4 / A5          |
| Relay IN           | D3               |
| SD Card Module     | D10 (CS), D11-D13|
| Quạt 5V            | Nguồn ngoài qua relay |
| Nút nhấn (nếu có)  | D2 (tùy chọn)    |

---

## 🧠 Tính năng chính | Key Features

- 🌡️ Đọc nhiệt độ từ cảm biến LM35  
- 🖥️ Hiển thị nhiệt độ hiện tại trên LCD 2004 I2C  
- 💾 Ghi log nhiệt độ + thời gian vào thẻ SD  
- 🚨 Cảnh báo khi nhiệt độ vượt **50°C**  
- 🌬️ Tự động bật quạt qua **relay** khi quá nhiệt  
- ✅ Hệ thống có thể hoạt động liên tục, ổn định

---

## 🛠️ Cài đặt | Setup

### 1. Clone project
```bash
git clone https://github.com/your_username/your_repo.git
