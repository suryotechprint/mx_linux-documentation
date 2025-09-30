# Konfigurasi Awal MX Linux (Gen-Z Style) 🛠️

Abis install, jangan langsung dipake! Biar makin optimal, lakukan konfigurasi berikut. Trust me, hidup lo bakal lebih mudah.

---

## 1. Update MX Linux (Jangan Gaptek!)
Buka terminal dan ketik:
```bash
sudo apt update && sudo apt upgrade -y
```

---

## 2. Setting Bahasa Indonesia (Biar Indo Banget)
- Buka **MX Tools > MX Package Installer**
- Cari “language pack” Indonesia, install deh
- Setting di “Pengaturan > Bahasa & Wilayah”

---

## 3. Setting Waktu & Zona  
- Buka **Pengaturan > Waktu & Tanggal**
- Pilih zona waktu Asia/Jakarta

---

## 4. Install Guest Additions (Wajib VirtualBox Bro!)
Guest Additions bikin VM makin comfy!
- Klik menu VirtualBox: **Devices > Insert Guest Additions CD image…**
- Buka terminal:
```bash
sudo mount /dev/cdrom /media/cdrom
cd /media/cdrom
sudo sh VBoxLinuxAdditions.run
```
- Restart VM

**Kalau error, cek [Troubleshooting Guest Additions](../troubleshooting.md#kendala-guest-additions)**

---

## 5. Aktifkan Clipboard & Drag n Drop
- VM: **Settings > General > Advanced**
- Set both ke “Bidirectional”

---

## 6. Tweak Tampilan (Biar Gak Bosen)
- Ganti wallpaper, tema, atau icon pack
- Explore di **MX Tweaks**!

---

## 7. Cek & Edit Repo List (sources.list.d/mx.list)
Kadang update error gara-gara repo mirror.  
- Edit file:  
```bash
sudo nano /etc/apt/sources.list.d/mx.list
```
- Pilih mirror Indo/terdekat, save, lalu update lagi

---

## 8. Install Software Favorit
Lanjut ke [Daftar Software](../software/software-umum.md) buat rekomendasi app kece!
