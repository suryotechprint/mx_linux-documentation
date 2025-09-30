# Perintah Terminal MX Linux Paling Gampang (Gen-Z Edition) 💻

Bingung sama terminal? Ini cheat-sheet biar keliatan pro di depan temen!

---

## 1. Update & Upgrade (Wajib Tiap Minggu!)
```bash
sudo apt update && sudo apt upgrade -y
```

---

## 2. Install Aplikasi
```bash
sudo apt install nama-aplikasi
# Contoh: sudo apt install vlc
```

---

## 3. Hapus Aplikasi
```bash
sudo apt remove nama-aplikasi
```

---

## 4. Cek Info Sistem
```bash
neofetch          # tampilkan info sistem keren
uname -a          # info kernel
lscpu             # info CPU
free -h           # cek RAM
df -h             # cek disk
```

---

## 5. Cek Koneksi Internet
```bash
ping google.com
```

---

## 6. Liat Daftar File/Folder
```bash
ls -lah
```

---

## 7. Shutdown/Restart VM
```bash
sudo shutdown -h now
sudo reboot
```

---

## 8. Permission & Eksekusi File
```bash
chmod +x namafile.sh   # biar file bisa di-eksekusi
./namafile.sh          # eksekusi script
```

---

## 9. Edit File Penting (Kayak sources.list.d/mx.list)
```bash
sudo nano /etc/apt/sources.list.d/mx.list
# Edit mirror repo, save dengan CTRL+O lalu CTRL+X
```

---

> **Tips:**  
> Ketik `history` buat liat perintah terakhir yang pernah lo jalankan.
