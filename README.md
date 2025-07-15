# 🔧 Hệ thống hiển thị, lưu log, cảnh báo nhiệt độ và điều khiển quạt tự động  
**Automatic Fan Control and Temperature Logging System using Arduino**

![Circuit]([./path/to/your/image.png](https://private-user-images.githubusercontent.com/181681048/466431246-c56b3779-456e-4fdc-9c89-f55ad3678795.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NTI1NzQyMzksIm5iZiI6MTc1MjU3MzkzOSwicGF0aCI6Ii8xODE2ODEwNDgvNDY2NDMxMjQ2LWM1NmIzNzc5LTQ1NmUtNGZkYy05Yzg5LWY1NWFkMzY3ODc5NS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwNzE1JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDcxNVQxMDA1MzlaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1lYzc1NjBlNTBiZDM2ODk0ZTZiMDQyNzgzN2RjMDc0MjMzN2RlOTgzYzQ2YjE4ZmRhMDEzYzI0MzQ1MTAxN2JkJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.xwiOeiYhwBEW2zSuF30dIVfJ8ejgo7CpAQkQ0oAzj9g)) <!-- Đổi path nếu bạn upload ảnh khác -->

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
