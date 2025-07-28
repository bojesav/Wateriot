# Wateriot
Wateriot adalah sistem IoT berbasis ESP32 untuk memantau dan mengontrol kualitas air secara real-time. Sistem ini mengelola dua pompa (isi/kuras), reaktor, serta memantau   level air, pH, dan kekeruhan. Data dikirim ke Firebase untuk dipantau via aplikasi Android. Dilengkapi OTA update dan antarmuka web untuk konfigurasi mudah.

## Mode Kalibrasi Sensor pH

Untuk mengkalibrasi sensor pH, ikuti langkah-langkah berikut:

1. Upload sketch ke ESP32
2. Buka Serial Monitor
3. Reset ESP32 dan segera kirim karakter apa saja melalui Serial Monitor
4. Ikuti instruksi di Serial Monitor:
   - Langkah 1: Masukkan sensor ke dalam larutan buffer pH 7.0
   - Tunggu hingga nilai stabil, lalu kirim karakter apa saja melalui Serial Monitor
   - Langkah 2: Masukkan sensor ke dalam larutan buffer pH 4.0
   - Tunggu hingga nilai stabil, lalu kirim karakter apa saja melalui Serial Monitor
5. Setelah kalibrasi selesai, reset ulang ESP32 untuk keluar dari mode kalibrasi

## Sensor yang Digunakan

1. Sensor pH menggunakan library DFRobot_ESP_PH_BY_GREENPONIK
2. Sensor Turbidity (Kekeruhan) SEN0189

## Penggunaan Normal

Setelah kalibrasi selesai, sistem akan berjalan secara normal, membaca nilai pH dan kekeruhan serta mengirimkannya ke Firebase.
