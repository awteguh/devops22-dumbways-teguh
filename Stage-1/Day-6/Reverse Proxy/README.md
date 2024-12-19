# Reverse Proxy

## Konfigurasi 
siapkan server untuk web server
```bash
sudo apt install nginx
```
pertama siapkan web server nginx terlebih dahulu

```bash
cd /etc nginx
```
```bash
sudo mkdir appdumbflix
```
```bash
cd appdumbflix
```
```bash
sudo nano appdumbflix.conf
```
```bash
server { 
    server_name teguhjr.xyz; 
  
    location / { 
             proxy_pass http://10.19.162.188:3000;
    }
}
```
buat folder dan file untuk konfigurasi reverse proxy nya

```bash
cd ..
```
keluar dari folder, atau masuk pada bagian /etc nginx

```bash
sudo nano nginx.conf
```
tambahkan inisiasi folder appdumbflix agar terbaca oleh nginx pada bagian include `include /etc/nginx/appdumbflix/*;`

```bash
sudo nginx -t
```
cek konfigurasi nginx sukses atau masih terdapat error

## Local
```bash
sudo nano /etc/hosts
```
di locakserver, tambahkan ip web server dan domain `teguhjr.xyz` tadi agar terbaca ketika dijalankan. Selanjutnya cek `teguhjr.xyz` menggunakan browser

```bash
sudo systemctl reload nginx
```
reload jika belum terbaca
