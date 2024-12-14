# Soal Case
Anda bekerja di sebuah tim data analis untuk sebuah situs web yang menampilkan data pembalap Formula 1. Data pembalap disimpan dalam sebuah file teks md yang bernama formula-one-drivers.md, dengan format sebagai berikut: ID,Nama,Tim,Posisi,Gaji 001,Lewis Hamilton,Mercedes,1,70000000 002,Max Verstappen,Red Bull Racing,2,50000000 003,Sergio Perez,Red Bull Racing,3,25000000 004,Charles Leclerc,Ferrari,4,15000000 005,Lando Norris,Mclaren,5,10000000 006,Daniel Ricciardo,AlphaTauri,6,8000000 Tugas kalian adalah melakukan beberapa manipulasi text menggunakan perintah sed di Linux. Berikut adalah beberapa hal yang harus kalian lakukan.
- Mengganti kata "Red Bull Racing" dengan "Red Bull Racing Honda" pada kolom Tim.
- Menghapus seluruh baris yang berisi pembalap dengan posisi lebih dari 3

## Konfigurasi
```bash
touch formula-one-drivers.md
```
membuat file terlebih dahulu

```bash
nano formula-one-drivers.md
```
edit file dan isi dengan daftar nama pembalap

```bash
sed -i 's/Red Bull Racing/Red Bull Racing Honda/g' formula-one-drivers.md
```
menganti nama Red Bull Racingmenjadi Red Bull Racing Honda 

```bash
sed -i '/,[4-6],/d' formula-one-drivers.md
```
mencari dan menghapus baris ke 4 sampai 6
