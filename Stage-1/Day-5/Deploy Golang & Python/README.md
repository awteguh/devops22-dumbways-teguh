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
`
from flask import Flask
app = Flask(__name__)
@app.route('/')
def helloteguh():
    return "Hello Teguh!"
if __name__ == '__main__':
    app.run(host='10.19.162.188', port=5000)
`
membuat file dan isi konfigurasi untuk menampilkan pesan di web

```bash
python3 index.py
```
perintah untuk menjalankan python




# Deploy Golang
