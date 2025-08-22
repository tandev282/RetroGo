# Retro-Go (ESP32-S3 + ST7789)

MOD của [Retro-Go](https://github.com/ducalex/retro-go) dành cho **ESP32-S3 DevKit** và màn hình **TFT LCD ST7789 240×320 (SPI)**.

> Retro-Go là firmware giả lập (NES, GB, GBC, SMS, GG, PCE, Doom, v.v.) cho ESP32. Repo này là bản **mod** để hỗ trợ **ESP32-S3 DevKit** cùng màn hình **ST7789 240×320**.

---

## ✨ Điểm khác biệt so với repo gốc
- Hỗ trợ build cho **ESP32-S3 DevKit** (N16R8).
- Thêm driver cho **màn hình ST7789/ST7789V SPI 240×320**.
- Cập nhật cấu hình chân SPI, backlight, nút bấm.
- Fix một số lỗi build với ESP-IDF 4.x / 5.x.
- Bổ sung font Unicode (có hỗ trợ tiếng Việt).

---

## ⬇️ Tải firmware
Vào mục [**Releases**](../../releases) để tải file `.img`.

---

## 🛠️ Nạp firmware

Dùng [esptool](https://github.com/espressif/esptool):

```bash
python -m esptool --chip esp32s3 -p COMx -b 921600 \
  --before default-reset --after hard-reset \
  write_flash --flash-size 16MB 0x0 retro-go_1.45-dirty_esp32s3-devkit-c.img
````
Thay COMx bằng cổng COM của ESP32-S3 trên máy tính.

# 📝 Ghi chú

Đây là bản mod, không chính thức từ tác giả Retro-Go.
Nếu có bug, vui lòng tạo Issues trong repo này.
Dựa trên Retro-Go v1.45.

# 📜 License
Retro-Go theo giấy phép GPLv3. Bản mod này phát hành theo cùng giấy phép.
