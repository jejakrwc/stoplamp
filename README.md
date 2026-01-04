# 🚦 STOP LAMP ESP8266 – Web Control Panel

Web-based **Control Panel untuk STOP LAMP LED Matrix berbasis ESP8266**, memungkinkan pengaturan teks, animasi, lampu belakang, WiFi, firmware, dan SPIFFS langsung melalui browser tanpa aplikasi tambahan.

---

## 📌 Fitur Utama

### 🖥️ Pengaturan Tampilan LED
- Input teks LED (custom text)
- Efek animasi teks (scroll, wipe, typing, dissolve, dll)
- Pengaturan:
  - Jenis font (Tipis / Tebal / Sangat Tebal)
  - Kecepatan animasi (0–15)
  - Kecerahan LED (0–15)
- Mode tampilan:
  - Teks saja
  - Animasi saja
  - Teks + Animasi

---

### 🎬 Manajemen Animasi
- Pemilihan animasi secara **multi-select**
- Kategori animasi:
  - Animasi Umum
  - Arah & Gerakan
  - Hewan
  - STOP / Rem
  - Hazard
  - Rambu Lalu Lintas
- Total animasi ditampilkan otomatis
- Accordion UI agar tetap rapi

---

### 🚗 Kontrol Lampu Belakang
- Lampu Sen Kiri
- Lampu Sen Kanan
- Lampu Rem (STOP)
- Lampu Hazard
- Setiap mode mendukung beberapa pola animasi

---

### 📡 Manajemen WiFi
- Ubah SSID & Password melalui Web UI
- Validasi password minimal 8 karakter
- Konfigurasi disimpan ke memori
- Restart Access Point otomatis setelah update

---

### ⚙️ Update Firmware OTA
- Upload firmware (`.bin`) langsung dari browser
- Progress bar real-time
- Proteksi UI selama proses upload
- Restart otomatis setelah selesai

---

### 💾 Upload SPIFFS
- Upload file filesystem (`.spiffs.bin`)
- Progress bar animasi
- Validasi file
- Restart otomatis setelah upload

---

### ℹ️ Informasi Sistem
- Penjelasan fungsi dan cara kerja sistem
- Panduan penggunaan
- Antarmuka mobile-friendly
- Modal informasi saat pertama kali dibuka

---

## 🧩 Teknologi yang Digunakan

| Komponen | Keterangan |
|--------|-----------|
| Mikrokontroler | ESP8266 (NodeMCU / ESP-12) |
| Web Server | ESP8266 Async Web Server |
| Frontend | HTML, CSS, JavaScript |
| Icon | Font Awesome |
| Penyimpanan | SPIFFS |
| OTA Update | HTTP OTA |

---

## 📂 Struktur Project

```text
project-root/
│
├── firmware/
│   ├── stop_lamp.ino
│   └── web_ui.h
│
├── web-ui/
│   ├── index.html
│   ├── css/
│   └── js/
│
├── tools/
│   └── build_webui.py
│
├── README.md
└── LICENSE
