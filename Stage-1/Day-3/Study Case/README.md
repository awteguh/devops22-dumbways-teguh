# Study Case
Ada 2 Developer yang sedang melakukan development aplikasi dari perusahaan A sebut saja Reyhan dan Teguh mereka kebetulan sedang mengerjakan suatu proyek yang sama, dan mereka sedang mengerjakan file yang sama index.html. Reyhan membuat perubahan pada file index.html dan melakukan commit: git add index.html; git commit -m "fix: Typo on Description". Teguh kebetulan juga membuat perubahan pada index.html dan melakukan commit: git add index.html ; git commit -m "feat: Header Adjustment". Kemudia disini ternyata Reyhan melakukan push ke repository. Teguh, yang belum melakukan push, mencoba untuk melakukan push ke repositori. Karena ternyata ada perubahan baru di remote yang belum dimiliki Teguh, Git menolak push Teguh dan memberi tahu bahwa ada konflik. Disini Teguh harus melakukan Fix Conflict tersebut agar perubahan yang di buat oleh Teguh dapat tersimpan ke dalam repositori app tersebut. lalu bagaimana cara menangani case yang dimiliki oleh Teguh?

## Installation
Siapkan dua buah server dan aplikasi/file yang akan dibua, untuk Reyhan dan Teguh

## Server Reyhan
1. Buat folder dan file index.html
    ```bash
    mkdir studycase
    ```
    ```bash
    cd studycase
    ```
    ```bash
    touch index.html
   ```
2. Inisiasikan dengan akun git
   ```bash
   git config --global user.name "your.github-user.name"
   ```
   ```bash
   git config --global user.email "your.github-user.email"
   ```
   ```bash
   git config --list
   ```
   cek status dan pastikan sudah terhubung
3. Generate ssh dan koneksikan ke github
   ```bash
   ssh-keygen
   ```
   ```bash
   cd ./ssh
   ```
   cari file `.pub` copy isinya dan tempel pada akun github di bagian profil seting, ssh, new ssh
   ```bash
   ssh -T git@github.com
5. Git init, inisiasikan folder studycase
   ```bash
   git init
   ```
6. Git add, menandai file indext.html seblum di commit
   ```bash
   git add .
   ```
7. Git commit
   ```bash
   git commit -m "add file"
   ```
   commit dengan pesan add file
8. New Repository pada akun github
9. Git remote
    ```bash
    git remote add origin git@github.com:nama repository/nama folder.git
10. Git push
   ```bash
   git push origin master
   ```

## Server Teguh
1. Cloning terselebih dahulu agar dari awal sama dengan Reyhan
   ```bash
   git clone https://github.com/awteguh/studycase
   ```
2. Copy isi dari ssh-key `id` dan `id.pub`dari Reyhan
3. Sesuaikan permision dari `id` dan `id.pub` dengan menggunakan `sudo chmod`
4. Inisiasikan dengan akun git
   ```bash
   git config --global user.name "your.github-user.name"
   ```
   ```bash
   git config --global user.email "your.github-user.email"
   ```
   ```bash
   git config --list
   ```
   cek status dan pastikan sudah terhubung

## Server Reyhan
1. Edit indext.html
   ```bash
   nano indext.html
   ```
   isikan hello teguh
2. Git add, menandai sebelum commit karena telah di edit
   ```bash
   git add .
   ```
3. Git commit dengan pesan
   ```bash
   git commit - m "fix: Typo on Description"
   ```
4. Push ke repository
   ```bash
   git push origin master
   ```

## Server Teguh
1. Edit indext.html
   ```bash
   nano indext.html
   ```
   isikan hello sanjaya
2. Git add, menandai sebelum commit karena telah di edit
   ```bash
   git add .
   ```
3. Git commit dengan pesan
   ```bash
   git commit - m "feat: Header Adjustment"
   ```
4. Push ke repository
   ```bash
   git push origin master
   ```
   maka akan muncul error/konflik, karena ada perubahan yang dilakukan/Reyhan sudah push terlebih dahulu
5. Git pull, untuk mengambil perubahan terbaru
   ```bash
   git pull origin master
   ```
   maka akan muncul sedikit error
   ```bash
   git config pull.rebase false
   ```
   untuk melakukan solve sesuai dengan step yg ada, untuk menggabungkan file tanpa menghapus riwayat yang ada
   ```bash
   git pull origin master
   ```
6. git push
   ```bash
   git push origin master
   ```
   
   
