# Deploy NodeJs
## Konfigurasi
```bash
mkdir json
```
```bash
cd json
```
pertama membuat folder dan masuk kedalamnya
```bash
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash
```
instal engine nodejs terlebih dahulu, Node Version Manager adalah command linux untuk memanage 2 versi node js yang berbeda, berpindah dari versi node ke versi node yang lain.

```bash
exec bash
```
eksekusi bash nya

```bash
nvm i 14
```
untuk menginstal nodejs versi 14

```bash
nvm use 14
```
untuk menggunakan nodejs versi 14
 
```bash
node -v
```
untuk mengecek versi nodejs yang digunakan

```bash
npm -v
```
untuk mengecek versi node paket manajer yang di gunakan

```bash
npm init -y
```
untuk menginisiasi folder json dan menghasilkan file package.json yang berisikan informasi dari aplikasi yang akan di buat

```bash
npm i express
```
menginstal framework dari express yang akan digunakan

```bash
nano index.js
```
```bash
const express = require("express");
const app = express();
const port = 3000;

app.get("/", (req, res) => {
  res.send("Hello TeguhJS!");
});

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`);
});
```
membuat file index.js dan mengisikan konfigurasinya untuk menampilkan ke we

```bash
node index.js
```
untuk menjalankan aplikasi yang kita buat, sekarang kita buka browser kita akses ip kita dengan port 3000





# Deploy Python
Pada dasarnya paket python sudah terinstal pada linux
## Konfigurasi
```bash
mkdir python
```
```bash
cd python
```
pertama membuat folder dan masuk kedalamanya

```bash
python3 -V
```
```bash
python3 --version
```
cek versi python yang digunakan

```bash
sudo apt install python3-pip
```
digunakan untuk menginstal pip, pip merupakan package manager untuk python digunakan untuk menginstal dan mengelola paket python seperti flask

```bash
pip install flask
```
menginstal paket flask

```bash
nano index.py
```
```bash
from flask import Flask
app = Flask(__name__)
@app.route('/')
def helloteguh():
    return "Hello Teguh!"
if __name__ == '__main__':
    app.run(host='10.19.162.188', port=5000)
```
membuat file dan isi konfigurasi untuk menampilkan pesan di web

```bash
python3 index.py
```
perintah untuk menjalankan python, sekrang kita buka browser dan akser ip kita dengan port 5000




# Deploy Golang
