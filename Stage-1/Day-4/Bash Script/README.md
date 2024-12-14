# Bash Script
Buatlah Bash Script untuk melakukan installasi webserver, dengan kebutuhan case: jika user menginputkan nomor 1 maka dia akan melakukan installasi WebServer Nginx dan jika user menginputkan nomor 2 maka akan melakukan installasi WebServer Apache2

Buatlah Bash Script untuk melakukan installasi webserver, dengan kebutuhan case: jika user menginputkan nomor 1 maka dia akan melakukan installasi WebServer Nginx dan jika user menginputkan nomor 2 maka akan melakukan installasi WebServer Apache2
 ```bash
#!/bin/bash

echo "Masukan Pilihan Anda!"
echo "1=Nginx"
echo "2=Apache" 
echo "3=exit"

read Pilihan
if [ "$Pilihan" = 1 ]; then
	echo "Melakukan Update"
	sudo apt update
	sudo apt upgrade
	echo "Update selesai"
	echo "--------Install Nginx--------"
	sudo apt install nginx
	echo "Install Selesai"
else

if [ "$Pilihan" = 2 ]; then
	echo "Melakukan Update"
	sudo apt update
	sudo apt upgrade
	echo "Update selesai"
	echo "---------Instal Appache--------"
	sudo apt install apache2
	echo "Install Selesai"
else
	echo "gagal"
fi
fi
```
