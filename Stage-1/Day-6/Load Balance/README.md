# Load Balance
Load balancing adalah teknik distribusi lalu lintas jaringan atau beban kerja di beberapa server untuk memastikan bahwa tidak ada satu server yang terlalu terbebani.
![loadbalancing](https://github.com/user-attachments/assets/49f50bb4-d543-423d-b4c6-fe7c0e0cb740)

## konfigurasi
* untuk membuat suatu Load Balancing harus membuat server baru lagi dan aplikasi yang sama seperti sebelumnya
* sekarang sudah ada 2 buah server aplikasi dan 1 server web
* selanjutnya masuk kedalam konfigurasi reverse proxy yang dibuat sebelumnya di server web
```bash
sudo nano /etc/nginx/appdumbflix/appdumbflix.conf
```

```bash
upstream appdumflix {
        server 10.19.162.188:3000;
        server 10.19.162.81:3000;
}
server {
        server_name teguhjr.xyz;

        location / {
             proxy_pass http://appdumflix;
    }
}
```
lalu masuk ke folder dan file, ganti/tambahkan konfigurasi sebelumnya menjadi ini

```bash
sudo nginx -t
```
cek ada error atau tidak di bagian konfigurasi

```bash
sudo systemctl reload nginx
```
selanjutnya jalankan aplikasi yang ada pada server

* untuk make sure load balancing sudah berjalan atau belum, bisa menggunakan cara hidupkan dan matikan salah satu aplikasi atau semuanya





