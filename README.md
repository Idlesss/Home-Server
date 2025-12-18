# Panduan Membangun Home Server Mandiri 🚀

Repository ini berisi dokumentasi lengkap cara membangun home server menggunakan hardware bekas (Mini PC/STB) untuk keperluan hosting website dan cloud storage pribadi.

## 🛠️ Hardware yang Digunakan
* **Device:** HP EliteDesk 800 G3 Mini
* **RAM:** 8GB / 16GB
* **Storage:** SSD 256GB NVMe
* **OS:** Ubuntu Server 22.04 LTS / Debian 11

## 📦 Software Stack
* **Panel:** HestiaCP
* **Apps:** Nextcloud, 
* **Tunneling/DNS:** Cloudflare

## 1. Persiapan Awal
Pastikan Anda sudah memiliki:
1.  Flashdisk (min 8GB) berisi installer OS (gunakan Rufus/BalenaEtcher).
2.  Koneksi internet via kabel LAN.
3.  Domain aktif (bisa beli di Hostinger/Namecheap).

## 2. Instalasi OS
Lakukan instalasi Ubuntu Server standar. Pastikan untuk mengaktifkan SSH Server saat instalasi.
Setelah selesai, update sistem:
```bash
sudo apt update && sudo apt upgrade -y
```

## 3. Instalasi HestiaCP
Masuk ke server via SSH (PuTTY/Terminal):
```bash
ssh root@192.168.1.xx
```
Login sebagai root via SSH, lalu jalankan installer:
```bash
wget [https://raw.githubusercontent.com/hestiacp/hestiacp/release/install/hst-install.sh](https://raw.githubusercontent.com/hestiacp/hestiacp/release/install/hst-install.sh)
bash hst-install.sh
```
Note: Simpan sandi admin yang muncul di akhir instalasi
## 4.  Konfigurasi Nextcloud

 * Masuk ke dashboard HestiaCP (Port 8083).
 * Buat Web Domain baru (misal: cloud.domainanda.com).
 * Aktifkan SSL (Let's Encrypt).
 * Install Nextcloud menggunakan fitur "Quick Install App" di HestiaCP atau manual via terminal.
