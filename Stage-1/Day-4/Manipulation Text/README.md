# Text Manipulation
Pada dasarnya kita bisa manipulasi pada sebuah file menggunakan terminal, tanpa menggunakan teks editor seperti nano

## Cat
Pada dasarna `cat` tidak hanya perintah untuk menampilkan isi dari sebuah file, tetapi juga bisa berfungsi sebagai perintah untuk manipulasi teks.
```bash
Cat file1
```
Perintah untuk menampilkan isi file1

```bash
cat > file1
```
Ketika kita mengetikan perintah ini maka selanjutnya kita bisa mengisi teks/pesan yang kita inginkan, ENter dan Ctrl C untuk mengakhiri perintah

```bash
cat >> file1
```
Perintah untuk menambahkan isi teks dari file1

```bash
cat file1 file2 > file3
```
Perintah untuk menggabungkan isi teks dari file1 dan file2 menjadi file3

## Sed
Stream editor, memanipulasi teks pada file dengan cepat
```bash
sed -i 's/Hello/Hai/g' file1
```
Mengganti kata `Hello` menjadi `Hai` pada file1, `s` search, `g` global.

## Sort
```bash
sort file1
```
Mengurutkan angka secara ascending

```bash
sort -r file1
```
Mengurutkan angka secara descending

## Tail
Melihat isi dari suatu file, melihat dan menghitung apa yang terjadi pada file tersebut / melihat log secara terstruktur
```bash
tail syslog
```
```bash
tail -f syslog
```
melihat secara realtime
```bash
tail -n 5 syslog
```
melihat 5 baris terkhir

## Head
Menampilkan isi dari suatu file sebanyak 10 baris, default
```bash
head file1
```
```bash
head -n 5 file1
```
menampilkan 5 baris
```bash
head -c 5 file5
```
akan menampilkan jumlah karakter/huruf

## Less
```bash
less file1
```
menampilkan seluruh isi dari file1 seperti menggunakan text editor.`q` untuk keluar

## Diff
```bash
diff file1 file2
```
untuk menampilkan isi yang bebeda dari 2 buah file, isi yang sama tidak akan di tampilkan

