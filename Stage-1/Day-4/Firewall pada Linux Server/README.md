## Implementasikan Firewall pada linux server kalian.
- Buatlah 2 buah Virtual Machine.
-Study case nya adalah agar hanya server A yang hanya dapat mengakses WebServer yang ada pada server B.
-Carilah cara agar UFW dapat memblokir ataupun mengizinkan specific protocol jaringan seperti TCP dan UDP.
-Jelaskan perbedaan protocol Jaringan TCP serta UDP.
- 10.10.10.254 Ip local
- 10.19.162.191 B
- 10.19.162.14 A

## ufw instal (konfigurasi pada server B)
langkah pertama melakukan instalasi ufw
```bash
sudo apt instal ufw -y
```

## ufw deny incoming
```bash
sudo ufw default deny incoming
```
memblokir semua akses yang masuk

## ufw allow outgoing
```bash
sudo ufw default allow outgoing
```
membuka semua akses yang keluar

## sudo ufw enable
```bash
sudo ufw enable
```
untuk menghidupkan firewalll 

## konfigurasi 
```bash
sudo ufw allow from 10.19.162.14 to any port 80
```
mengijinkan dari ip 10.19.162.14/server a ke server di port 80
```bash
sudo ufw allow from 10.19.162.14 to any port 443
```
mengijinkan dari ip 10.19.162.14/server a ke server  di port 80

```bash
sudo ufw deny 80
```
memblokir semua akses ke port 80 dari alamat lain
```bash
sudo ufw deny 443
```
memblokir semua akses ke port 443 dari alamat lain

```bash
sudo ufw allow 80/tcp
```
membuka akses untuk port 80 dengan koneksi tcp

# Tambahan
## ufw app list
```bash
sudo ufw app list
```
untuk menampilkan aplikasi yang di dukung ufw

## status verbose
```bash
sudo ufw status verbose
```
untuk melihat status firewall apa saja yang ada

## delete
```bash
sudo ufw delete deny 80
```
menghapus konfigurasi, harus sama dengan perintah
```bash 
sudo ufw status numbered
```
untuk melihat status firewall yang aktif berdasarkan number
```bash
sudo ufw delete 1
```
untuk menghapus urutan pertama firewall

# Perbedaan TCP dan UDP
## Tcp
Transmission Control Protocol adalah protokol berorientasi koneksi, yang berarti ia menetapkan koneksi antara pengirim dan penerima sebelum data dikirim.
Menjamin pengiriman data secara urut dan benar. 
TCP digunakan untuk aplikasi di mana keandalan dan urutan data penting, seperti HTTP/HTTPS (web browsing), FTP (file transfer), dan SMTP (email)
## Udp
User Datagram Protocol adalah protokol tanpa orientasi koneksi, yang berarti tidak ada sesi atau koneksi yang dibuat sebelum data dikirim. Data dikirimkan secara langsung.
UDP lebih cepat dibandingkan TCP karena tidak ada mekanisme untuk pengaturan koneksi, pengurutan, atau kontrol aliran.
UDP digunakan untuk aplikasi di mana kecepatan lebih penting daripada keandalan, seperti streaming video/audio, game online.

