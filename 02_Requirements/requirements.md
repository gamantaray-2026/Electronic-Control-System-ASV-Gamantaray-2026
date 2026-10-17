# 📋 Spesifikasi Sistem & Kebutuhan Elektronika ASV Gamantaray

Dokumen ini mencakup spesifikasi komponen, tegangan kerja, dan perangkat keras yang digunakan pada sistem kontrol elektronik ASV Gamantaray berdasarkan desain sistem SAFINAH ONE 2026.

### 1. Spesifikasi Sumber Daya Utama
* **Baterai Utama:** LiPo 4S (14.8V, 10000 mAh, 25C).
* **Sistem Distribusi Daya:** Menggunakan Control Board pusat (PDB - Contol System) untuk regulasi ke 5 voltage rails utama (5V, 12V, 19V, 24V, dan internal 3.3V).

### 2. Daftar Komponen & Perangkat Keras Utama

| Kategori | Komponen / Device | Spesifikasi / Tipe | Peran Spesifik |
| :--- | :--- | :--- | :--- |
| **Controllers** | Flight Controller | Pixhawk 6C | Pengendali navigasi utama & otonom |
| | High-End SBC | Intel NUC Pro 12 i5 | Pemrosesan data berat (LiDAR & Visi) |
| | Low-End SBC | Raspberry Pi 4 Model B | Manajemen multi-kamera |
| | Microcontroller | STM32F4x1Cx (Black Pill) | Pemrosesan sensor jarak (TOF) |
| **Sensors** | LiDAR | RPLidarC1 | Pemetaan lingkungan sekitar & deteksi objek |
| | Vision / Camera | Logitech C922 (5 Units) | 4x pada RPi 4, 1x pada Intel NUC |
| | Distance Sensor | Sensor TOF VL53LXX (2 Units) | Sensor pendeteksi jarak dekat |
| | GNSS / GPS | UM980 | Modul navigasi satelit akurasi tinggi |
| **COMM / Network** | Remote Transmitter | RadioMaster Pocket Hall Sensor Gimbals Radio Transmitter ELRS | Remot kendali kapal manual dan command lainnya (OS EdgeTX, ELRS 2.4GHz, 250mW, 16 Ch) |
| | Remote Receiver | RadioMaster RP4TD 2.4GHz ExpressLRS ELRS Diversity Receiver RX | Receiver komunikasi manual RC (Dual chipset SX1280, True Diversity, 2.4GHz, CRSF) |
| | Router 1 | TP-Link Archer-MR400 | Jaringan lokal & internet kapal (12V) |
| | Router 2 | TP-Link EAP110 | Jaringan akses poin eksternal (24V) |
| **System Support** | Cooling System | Fan 12V (4 Units) | Sirkulasi udara & pendingin box elektronik |
