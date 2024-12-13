# Installation git
```bash
sudo apt install git
```
pada dasarnya git sudah terinstal pada linux, jika belum bisa menggunakan command ini

## Git Config
```bash
git config --global user.name "your.github-user.name"
```
```
git config --global user.email "your.github-user.email"
```
meng inisiasi github, pastikaan user dan email sesuai dengan akun github

```bash
git config --list
```
untuk melihat nama user dan email yang terhubung

## SSS Keygen
```bash
ssh-keygen
```
untuk mendapatkan kunci ssh pada server kalian
```bash
cat .ssh/id_rsa.pub
```
ketika sudah menggenerate kunci ssh maka akan terdapat kunci unik yang berada pada folder `.ssh`, dan isi dari kunci tersebut yang berakhiran `.pub` di salin di masukan ke akun github di bagian profil setting, ssh & gpg key, klik new ssh key dan tempel isi dari `id_rsa.pub`

## Cek koneksi
```bash
ssh -T git@github.com
```
untuk mengecek koneksi local kita sudah terkoneksi dengan github atau belum

## Repository
ini akan membuat nama folder yang akan di gunakan di local
```bash
git init namarepository
```
atau bisa membuat folder terlebih dahulu lalu `git init` untuk meninisiasi folder tersebut
```bash
mkdir namarepository
```
```bash
cd namarepository
```
```bash
git init
```

## Git Ignore
`.gitignore` sebuah file yang berisi file dan directory yang diasingkan /abaikan oleh git. Perubahan apapun yang kita lakukan terhadap file dan direktori yang sudah masuk ke dalam daftar .gitignore tidak akan dicatat oleh git.

*Pertama membuat beberapa file
```bash
touch file1 file2 file3
```
Cek status file yang terbuat
```bash
git status
```
Membuat file ignore terlebih dahulu untuk menampung file yang akan di abaikan
```bash
touch .gitignore
```
Untuk mengabaikan file3, masukan `file3` kedalam file .gitignore menggunakan teks editor nano
```bash
sudo nano .gitignore
```
Jika sudah maka file3 tidak terbaca
```bash
git status
```
Maka file3 ketika dipush kegithub tidak terbaca tetapi masih ada dalam lokal kita

## Git add / Stage
Perintah untuk menandai/menyimpan file sebelum melakukan commit
```bash
git add file1
```
Hanya menandai file1
```bash
git add *.html
```
Menandai file semua file berakhiran `.html` sebelum di commit
```bash
git add .
```
Menandai semua file sebelum comit

## Git Commit
``` bash 
git commit -m "pesan yang akan di tulis/commit"
```
perintah untuk menyimpan file kedalam data base git dengan menggunakan pesan commit

## Git remote
Login github lalu pilih new repository, pilih ssh dan salin url. Pada `git remote` ini dimana kita memilih lokasi untuk mengunggah file yang akan kita upload
```bash
git remote add origin git@github.com:nama repository/nama folder.git
```
copy link tersebut dari github pada bagian ssh

```bash
git remote -v
```
untuk melihat lokasi remote yang kita gunakan

## Push
proses upload data local kita ke github
```bash
git push origin master
```
master merupakan branch default yang ada di local kita, sekarang file local kita sudah terupload pada github

## Git Branch
```bash
git branch namabranch
```
perintah untuk membuat namabranch baru + mengcloning isi dari repository yang ada
```bash
git checkout namabranch
```
untuk pindah branch
```bash
git branch -m (name branch)
```
untuk membuat nama branch serta pindah langsung ke dalam branch tersebut
```bash
git branch - a
```
untuk melihat daftar nama branch
```bash
git branch -d namabranch
```
untuk menghapus branch

## Pull
```bash
git pull origin namabrach
```
perintah untuk menyamakan perubahan yang terjadi pada branch yang dituju

## Merge
```bash
git merge master
```
untuk menggabungkan file yang ada di branch master kedalam branch development (`git checkout development` posisi di branch development)



