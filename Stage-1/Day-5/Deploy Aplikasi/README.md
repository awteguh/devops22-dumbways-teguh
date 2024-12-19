# Deploy Aplikasi Dumbflix
## Konfigurasi 

```bash
git clone https://github.com/dumbwaysdev/dumbflix-frontend
```
```bash
cd dumbflix-frontend
```
siapkan aplikasi yang akan di deploy, clone dari github dan masuk kedalam foldernya

```bash
nvm 14
```
menggunakan node versi 14

```bash
npm i
```
menginsatal dependensi yang ada

```bash
npm start
```
menjalankan script aplikasi

## PM2
```bash
pm2 start npm -- start
```
untuk menjalankan aplikasi berjalan di background

```bash
pm2 stop npm
```
untuk menyetop aplikasi agar tidak berjalan di background

```bash
pm2 delete npm
```
untuk menghapus konfigurasi yang dijalankan
