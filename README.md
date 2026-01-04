🚦 STOP LAMP ESP8266 – Web Control Panel

Web-based Control Panel untuk STOP LAMP LED Matrix berbasis ESP8266, dirancang untuk mengatur teks, animasi, lampu belakang, WiFi, firmware, dan SPIFFS langsung melalui browser tanpa aplikasi tambahan.

📌 Fitur Utama
🖥️ Pengaturan Tampilan LED

Input teks LED (custom text)

Efek animasi teks (scroll, wipe, typing, dissolve, dll)

Pengaturan:

Jenis font (Tipis / Tebal / Sangat Tebal)

Kecepatan animasi (0–15)

Kecerahan LED (0–15)

Mode tampilan:

Teks saja

Animasi saja

Teks + Animasi

🎬 Manajemen Animasi

Pemilihan animasi secara multi-select

Kategori animasi:

Animasi Umum

Arah & Gerakan

Hewan

STOP / Rem

Hazard

Rambu Lalu Lintas

Total animasi ditampilkan otomatis

UI accordion (expand / collapse) agar tetap rapi

🚗 Kontrol Lampu Belakang

Lampu Sen Kiri & Kanan

Lampu Rem (STOP)

Lampu Hazard

Setiap mode memiliki banyak pilihan animasi dinamis

📡 Manajemen WiFi

Ubah SSID dan Password langsung dari Web UI

Validasi password minimal 8 karakter

Konfigurasi tersimpan ke memori

Access Point restart otomatis setelah update

⚙️ Update Firmware OTA

Upload firmware melalui browser (.bin)

Progress bar real-time

Proteksi UI saat upload (anti double click)

Restart otomatis setelah update

Peringatan keamanan selama proses update

💾 Upload SPIFFS

Upload filesystem SPIFFS (.spiffs.bin)

Progress bar animasi

Validasi file otomatis

Restart otomatis setelah upload selesai

ℹ️ Informasi Sistem

Penjelasan fitur dan alur kerja sistem

Informasi teknis perangkat

Antarmuka ramah pengguna (mobile-friendly)

Modal panduan wajib dibaca saat pertama membuka halaman

🧩 Teknologi yang Digunakan
Komponen	Keterangan
Mikrokontroler	ESP8266 (NodeMCU / ESP-12)
Web Server	ESP8266 Async Web Server
Frontend	HTML, CSS, JavaScript
Icon	Font Awesome
Penyimpanan	SPIFFS
Update OTA	HTTP POST
📂 Struktur File (Disarankan)
project-root/
│
├── firmware/
│   ├── stop_lamp.ino
│   └── web_ui.h
│
├── web-ui/
│   ├── index.html   ← file ini
│   ├── css/
│   └── js/
│
├── tools/
│   └── build_webui.py
│
├── README.md
└── LICENSE


💡 Catatan:
File HTML ini bisa:

Disimpan langsung di SPIFFS

Atau digenerate ke PROGMEM melalui header (web_ui.h)

🔄 Alur Kerja Sistem

Pengguna membuka Web UI melalui browser

Mengatur teks, animasi, dan lampu belakang

Data dikirim ke ESP8266 via HTTP

ESP memproses dan menyimpan konfigurasi

Perubahan diterapkan secara real-time

🛡️ Keamanan & Catatan Penting

⚠️ Peringatan Firmware Update

Jangan mematikan perangkat saat upload

Jangan menutup browser saat proses berjalan

Gagal upload dapat menyebabkan firmware rusak

⚠️ SPIFFS

Gunakan file .spiffs.bin yang sesuai

Salah file dapat menyebabkan sistem tidak stabil

🌐 Akses Web UI

Biasanya dapat diakses melalui:

http://192.168.4.1


atau IP lokal ESP8266 setelah terhubung ke WiFi.

📸 Tampilan Antarmuka

Responsive (Mobile & Desktop)

Tab-based navigation

Animasi halus

Custom alert & modal system

🧑‍💻 Pengembang

ESP8266 STOP LAMP System
Web UI & Firmware by JEJAKRWC

📄 Lisensi

Proyek ini bersifat custom / internal project.
Silakan sesuaikan lisensi sesuai kebutuhan (MIT / Private / Commercial).
