# Retro-Go (ESP32-S3 + ST7789)

Đây là **bản mod Retro-Go** cho **ESP32-S3 DevKit** và màn hình **TFT LCD ST7789 240×320 (SPI)**.  
Repo này chỉ công khai **file firmware `.img`** để nạp trực tiếp cho ESP32-S3, không chứa source code.

---

## 🔥 Tính năng
- Chạy Retro-Go 1.45 trên ESP32-S3 (N16R8).
- Hỗ trợ màn hình TFT ST7789/7789V 240×320 SPI.
- Hỗ trợ các giả lập: NES, GB, GBC, SMS, GG, PCE, Doom, v.v.
- Hỗ trợ font và ngôn ngữ tiếng Việt.

---

## ⬇️ Tải firmware
Vào mục [**Releases**](../../releases) để tải file `.img`.

---

## 🛠️ Nạp firmware

Dùng [esptool](https://github.com/espressif/esptool):

```bash
python -m esptool --chip esp32s3 -p COMx -b 460800 \
  --before default-reset --after hard-reset \
  write_flash --flash-size 16MB 0x0 retro-go_esp32s3-st7789.img
````
Thay COMx bằng cổng COM của ESP32-S3 trên máy tính.

# 📝 Ghi chú

Đây là bản mod, không chính thức từ tác giả Retro-Go.
Nếu có bug, vui lòng tạo Issues trong repo này.
Dựa trên Retro-Go v1.45.

# 📜 License
Retro-Go theo giấy phép GPLv3. Bản mod này phát hành theo cùng giấy phép.
