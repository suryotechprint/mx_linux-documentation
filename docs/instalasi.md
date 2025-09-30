# Cara Instalasi MX Linux di VirtualBox 🚀

Yuk, kita mulai perjalanan jadi hacker sejati (atau minimal ngoding tanpa drama 😎) dengan MX Linux di VirtualBox!

---

## 1. Bahan yang Harus Disiapin
- File ISO MX Linux (download di [sini](https://mxlinux.org/download-links/))
- VirtualBox (install versi terbaru dari [sini](https://www.virtualbox.org/wiki/Downloads))
- Space kosong di HDD/SSD (minimal 20GB biar lega)

---

## 2. Setting VirtualBox (Anti Lemot)
1. **Bikin VM Baru**  
   - Klik "New", kasih nama misal “mxlinux-genz”
   - Type: Linux | Version: Debian (64-bit)
2. **RAM**  
   - Min: 2048 MB (2GB), Recommended: 4096 MB (4GB) biar smooth
3. **CPU**  
   - Naikkin core CPU ke 2 atau lebih (kalau PC kuat)
4. **Storage**  
   - Create Virtual Hard Disk, minimal 20GB (kalau mau ngembangin, bisa 40GB)
5. **ISO Boot**  
   - Attach ISO MX Linux ke optical drive VM

---

## 3. Install MX Linux (Step by Step)
1. Start VM, pilih boot dari ISO
2. Pilih "Install MX Linux" (bukan Live)
3. Ikuti wizard:  
   - Pilih bahasa (Indonesia recommended)
   - Zona waktu: Asia/Jakarta
   - Keyboard: US atau sesuai selera
4. Partition:  
   - Pilih "Auto Install" buat pemula
5. Masukkan username & password  
   - Username: genz (atau terserah lo)
   - Password: [rahasia lo sendiri]

---

## 4. Reboot dan Happy MX-ing!
- Setelah selesai, cabut ISO dari VM (biar ga ngulang install)
- Boot ke MX Linux, login, dan siap lanjut konfigurasi!

---

## ⚠️ NOTE: Install VirtualBox Guest Additions!
Biar resolusi VM auto-fit, clipboard sharing, dan drag n drop aktif:
- Lihat [Troubleshooting Guest Additions](../troubleshooting.md#kendala-guest-additions)
