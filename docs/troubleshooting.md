# 🚨 Troubleshooting & Galat MX Linux VirtualBox (Gen-Z Edition)

Yuk, cek solusi buat masalah-masalah yang sering muncul waktu ngoprek MX Linux di VirtualBox. Jangan panik, semua bisa diatasi asal niat! 💪

---

## 1. Guest Additions Error (Resolusi Gak Bisa Fullscreen / Copy-paste Nyangkut)

### Gejala:
- Layar VM stuck di resolusi kecil
- Drag n Drop/Clipboard ga jalan

### Solusi:
1. **Cek Kernel Headers**
   - Buka terminal:
   ```bash
   sudo apt install build-essential linux-headers-$(uname -r)
   ```
2. **Reinstall Guest Additions**
   - Insert Guest Additions dari menu VirtualBox
   - Jalankan:
   ```bash
   sudo mount /dev/cdrom /media/cdrom
   cd /media/cdrom
   sudo sh VBoxLinuxAdditions.run
   ```
   - Restart VM

3. **Cek Modul Kernel**
   - Pastikan modul `vboxguest` udah jalan:
   ```bash
   lsmod | grep vboxguest
   ```
   - Kalau nggak muncul, coba reboot dan install ulang Guest Additions

---

## 2. Error Update: "Repository ... does not have a Release file" (sources.list.d/mx.list)

### Gejala:
- Waktu update muncul error repo gak valid

### Solusi:
1. **Edit Repo Mirror**
   - Buka:
   ```bash
   sudo nano /etc/apt/sources.list.d/mx.list
   ```
   - Ganti server repo, misal pilih mirror Indonesia:
   ```
   deb http://kartolo.sby.datautama.net.id/mxlinux/mx/repo/ bookworm main non-free
   ```
   - Save (CTRL+O, ENTER, CTRL+X)
2. **Update Lagi**
   ```bash
   sudo apt update
   ```
3. **Cek Koneksi Internet**
   - Pastikan koneksi stabil, kadang repo error karena internet putus-nyambung

---

## 3. Gagal Booting Setelah Install

- Pastikan boot order di VirtualBox: Hard Disk di atas Optical
- Cek setting Storage, jangan ada ISO nyangkut
- Kalau masih gagal: Reinstall, pastikan semua step diikuti

---

## 4. WiFi VirtualBox Ga Muncul

- VirtualBox by default cuma kasih jaringan “Wired”
- Pakai “Bridged Adapter” di setting Network VM biar dapet IP dari router

---

## 5. Audio/Mic Ga Jalan

- Cek setting audio di VirtualBox: pilih “ALSA” atau “PulseAudio”
- Di MX Linux, cek di **Pengaturan > Audio** dan pastikan output device sesuai

---

## 6. Lain-lain

- Cek log system:
  ```bash
  journalctl -xe
  ```
- Cek space disk:
  ```bash
  df -h
  ```

---

> **Masih error juga?**  
> Jangan sungkan tanya di forum MX Linux, Discord komunitas, atau DM admin repo ini.  
> Ingat, error hari ini adalah pengalaman besok! 🚀
