# 🔐 WiFi Penetration Testing Tool

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Language-Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Library-pywifi-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Type-CLI%20Tool-green?style=for-the-badge&logo=gnubash&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" />
</p>

<p align="center">
  Công cụ kiểm tra bảo mật mạng WiFi sử dụng <strong>Python + pywifi</strong>, hỗ trợ <strong>quét mạng</strong>, <strong>phân tích bảo mật</strong> và <strong>kiểm tra độ bền mật khẩu</strong> qua wordlist.
</p>

> ⚠️ **Tuyên bố miễn trừ trách nhiệm:** Dự án này được phát triển **chỉ phục vụ mục đích học tập và nghiên cứu bảo mật** trong môi trường kiểm soát. Chỉ sử dụng trên mạng mà bạn có quyền kiểm tra. Tác giả không chịu trách nhiệm về bất kỳ hành vi sử dụng trái phép nào.

---

## 📌 Giới thiệu

Dự án **WiFi Penetration Testing Tool** được phát triển nhằm mục đích **học tập về an ninh mạng không dây**.  
Công cụ mô phỏng quy trình kiểm tra bảo mật cơ bản: quét mạng → chọn mục tiêu → kiểm tra độ bền mật khẩu bằng wordlist, giúp người học hiểu cách thức hoạt động của các cuộc tấn công brute-force và cách phòng thủ hiệu quả.

---

## ⚙️ Chức năng chính

- **Quét mạng WiFi** tự động xung quanh thiết bị
- **Hiển thị thông tin chi tiết:** SSID, BSSID, cường độ tín hiệu, loại bảo mật
- **Wordlist-based testing** – kiểm tra độ bền mật khẩu với danh sách mật khẩu phổ biến
- **Giao diện CLI tương tác** – chọn mạng, xác nhận, huỷ hoặc quét lại dễ dàng
- **Hỗ trợ WPA/WPA2** – chuẩn bảo mật phổ biến nhất hiện nay

---

## 🧩 Sơ đồ hoạt động

<p align="center">
  <img src="https://github.com/khanhly-dn/WiFi_Penetration_Testing/blob/main/SDHD.png?raw=true" width="700" alt="Sơ đồ hoạt động" />
</p>

---

## 🛠️ Công nghệ sử dụng

| Thành phần | Chi tiết |
|---|---|
| **Ngôn ngữ** | Python 3.x |
| **Thư viện chính** | `pywifi` – giao tiếp với WiFi adapter |
| **Wordlist** | `rockyou.txt` – tùy chỉnh thêm từ điển tiếng Việt |
| **Giao diện** | CLI (Command Line Interface) |
| **Hệ điều hành** | Windows / Linux |

---

## 📊 Thông số kỹ thuật

| Thông số | Giá trị |
|---|---|
| Thời gian chờ mỗi lần thử | 2 giây |
| Loại bảo mật hỗ trợ | WPA2-PSK |
| Phương thức mã hoá | CCMP (AES) |
| Giao thức xác thực | Open Auth |
| Định dạng wordlist | `.txt` (mỗi dòng một mật khẩu) |

---

## 🚀 Hướng dẫn cài đặt & chạy

**1. Clone repository**
```bash
git clone https://github.com/your-username/wifi-pentest-tool.git
cd wifi-pentest-tool
```

**2. Cài đặt thư viện**
```bash
pip install pywifi
```

**3. Chuẩn bị wordlist**
```
Đặt file rockyou.txt vào cùng thư mục với WiFi_Penetration_Testing.py
```

**4. Chạy tool**
```bash
# Windows (chạy với quyền Administrator)
python WiFi_Penetration_Testing.py

# Linux (chạy với quyền root)
sudo python3 WiFi_Penetration_Testing.py
```

**5. Sử dụng**
```
1. Tool tự động quét và hiển thị danh sách mạng WiFi
2. Nhập Network ID của mạng cần kiểm tra
3. Xác nhận: y (tiếp tục) / n (huỷ) / r (quét lại)
4. Quan sát quá trình kiểm tra mật khẩu trên terminal
```

---

## 📋 Ví dụ đầu ra

```
###############################################################
Network ID: 1
  SSID: HomeWifi_2G
  BSSID: AA:BB:CC:DD:EE:FF
  Signal: -55
  Security: [2]

Network ID: 2
  SSID: CafeNet
  BSSID: 11:22:33:44:55:66
  Signal: -72
  Security: [2]

Enter the Network ID: 1
Confirm the WiFi HomeWifi_2G (y/n/r): y

Trying password: 123456
Trying password: password
Trying password: admin123
...
Successfully connected to HomeWifi_2G with password: admin123
```

---

## 📁 Cấu trúc thư mục

```
wifi-pentest-tool/
├── WiFi_Penetration_Testing.py   # Script chính
├── rockyou.txt                   # Wordlist mật khẩu
└── README.md
```

---

## 🚀 Hướng phát triển

- [ ] Thêm hỗ trợ **WPA3**
- [ ] Xuất kết quả kiểm tra ra file log `.txt`
- [ ] Thêm **tùy chọn timeout** linh hoạt cho mỗi lần thử
- [ ] Hỗ trợ **nhiều wordlist** cùng lúc
- [ ] Thêm giao diện **GUI đơn giản** bằng tkinter

---

## 👤 Thực hiện

**Lý Gia Khánh**  
Khoa: IoT - Công Nghệ Thông Tin

---

<p align="center">
  Made for learning purpose · Python · pywifi · Network Security
</p>
