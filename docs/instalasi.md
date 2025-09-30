# Panduan Instalasi MX Linux di VirtualBox

Halo, selamat datang di panduan instalasi MX Linux khusus buat kamu yang mau nyobain MX Linux di VirtualBox! 🎉  
Panduan ini cocok banget buat yang pengen belajar, ngoprek, atau sekadar penasaran sama MX Linux tanpa harus instal langsung di laptop/PC.

Gak usah takut ribet, semua langkah bakal dijelasin dengan bahasa santai dan gampang dipahami. Yuk, langsung cek step by step-nya!

**Apa aja yang bakal lo temuin di sini?**
- Cara siapin VirtualBox & file ISO MX Linux
- Bikin mesin virtual baru (VM) biar siap install
- Langkah instalasi MX Linux di dalam VirtualBox
- Setting awal biar MX Linux makin cus
- Tips & trik troubleshooting kalau ada kendala

Jangan sungkan buat tanya atau diskusi kalau ada yang kurang jelas—kita belajar bareng di sini.  
Ayo mulai petualangannya! 🚀

---

## 1. Persiapan Sebelum Instalasi

Sebelum mulai, cek dulu beberapa hal penting di bawah ini:

### 1.1 Install VirtualBox

Download dan install VirtualBox versi terbaru di laptop atau PC kamu.  
Bisa langsung ke website resminya: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)  
> **Tips:** VirtualBox support di Windows, Linux, dan macOS, tinggal pilih sesuai OS kamu.

### 1.2 Download ISO MX Linux

Download file ISO MX Linux terbaru di situs resminya: [https://mxlinux.org/download-links/](https://mxlinux.org/download-links/)  
Pilih edisi yang sesuai kebutuhan, misal “MX Linux Xfce” buat yang ringan, atau “KDE” kalau mau tampilan lebih kece.

> **Tips:**  
> - Cek hash file (MD5/SHA256) biar yakin file-nya gak corrupt.
> - Pakai koneksi internet yang stabil, jangan sampai gagal di tengah jalan.

---

## 2. Membuat Mesin Virtual di VirtualBox

Setelah VirtualBox dan ISO siap, lanjut ke tahap bikin mesin virtual:

1. Buka VirtualBox, klik **New** atau **Baru**.
2. Isi nama VM, misal: `MX Linux` dan pilih tipe **Linux**, versi **Debian (64-bit)**.
3. Atur RAM minimal 2GB (rekomendasi 4GB biar lancar jaya).
4. Buat hard disk virtual baru, pilih VDI/VHD, dynamic allocation, dan size minimal 15GB (biar lega).
5. Setelah VM jadi, klik **Settings** (Pengaturan):
   - Masuk ke **Storage**, pilih empty optical drive, lalu attach file ISO MX Linux yang udah didownload.
   - (Opsional) Cek **System > Processor** buat nambah core CPU, makin banyak makin ngebut (asal hardware support).

> **Tips:**  
> - Aktifin juga **Enable 3D Acceleration** di Display kalau mau tampilan lebih smooth.
> - Jangan lupa save pengaturan sebelum lanjut.

---

## 3. Proses Instalasi MX Linux di VirtualBox

1. Start atau Jalankan VM yang baru dibuat.
2. Pilih opsi **Boot MX Linux** di menu awal.
3. Tunggu hingga masuk ke tampilan live session MX Linux.
4. Klik **Install MX Linux** di desktop.
5. Ikuti wizard instalasi, pilih partisi default (biasanya sudah otomatis), atur username & password sesuai keinginan.
6. Selesaikan instalasi, lalu restart VM.

> **Catatan:**  
> Setelah restart, eject file ISO dari “Optical Drive” biar gak balik ke menu installer lagi.

---

## 4. Konfigurasi Awal Setelah Instalasi

Setelah berhasil boot ke MX Linux:

- Update sistem:  
  Buka Terminal & ketik:  
  ```bash
  sudo apt update && sudo apt upgrade
  ```
- Install Guest Additions (biar VM fullscreen & copy-paste lancar):  
  Di menu VirtualBox, klik Devices > Insert Guest Additions CD Image, lalu ikuti petunjuk instalasi di dalam VM.
- Setting user, keyboard, timezone, dan preferensi lain sesuai kebutuhan.

---

## 5. Troubleshooting & FAQ

Kalau ada masalah (gak bisa fullscreen, suara gak keluar, atau error lain), cek tips berikut:

- Cek Guest Additions sudah terinstall dengan benar.
- Pastikan setting RAM/CPU cukup, jangan terlalu kecil.
- Lihat log error di VirtualBox kalau VM gak bisa start.

Masih bingung atau nemu error aneh? Jangan sungkan buat diskusi di repo ini. Sharing is caring! 😁

---

Selamat mencoba!  
Kalau ada saran, pertanyaan, atau mau share pengalaman, feel free buat buka issue atau pull request di repo ini.  
Semangat belajar Linux & happy virtual lab! 💻✨
(Tuliskan langkah-langkah instalasi MX Linux di sini)
