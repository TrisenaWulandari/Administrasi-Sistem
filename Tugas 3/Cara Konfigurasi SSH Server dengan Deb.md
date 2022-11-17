# Cara Konfigurasi SSH Server dengan Debian

1. Pertama tahap ini silahkan login sebagai user bisa klik su  
![1](https://user-images.githubusercontent.com/112459285/193229141-dd9c4207-51d0-4e91-9b33-f7fe018c3ae2.png)

2. Kedua Sebelumnya kita akan mengecek kembali, bahwa adapter 1 / eth0 ter bridge ke internet, karena pada saat ini koneksi internet saya menggunakan VirtualBox Host-Only Network #2 , maka disesuaikan dengan adapter nya, oleh karena itu saya menggunakan Intel(R) Wireless-AC 9560 160Mhz 
![adapter](https://user-images.githubusercontent.com/112459285/193231461-10a5eda4-6b36-4182-8734-dedf4c6da21d.png) 
Jika sudah, saat nya kita lakukan konfigurasi IP Address pada Linux Debian, tapi sebelum itu kita akan mengecek berapakah IP Address Internet yang kita dapatkan dari ISP.Untuk mengecek IP Address di windows, saya menggunakan CMD, lalu ketik ipconfig /all ![virtual](https://user-images.githubusercontent.com/112459285/193234601-f1e68ec2-9807-4209-9874-387361af8105.png)

3. ketiga jika sudah, berikutnya kita akan mengkonfigurasi IP Address pada Linux Debian caranya ketikan perintah nano /etc/network/interfaces , crtl+x dan ctrl+s  
![in](https://user-images.githubusercontent.com/112459285/193234999-8db64c12-7f0b-4df2-9cdf-2b9d0ecd1033.png)
![inter](https://user-images.githubusercontent.com/112459285/193235042-9f34d0e4-166e-48a7-904c-b127a507cd5f.png) Jika sudah, silahkan di save dengan cara ctrl+x lalu y lalu enter atau cara cepatnya ctrl+x y enter

4. Keempat ketikan ip a mengecek konfigurasi IP Address yang sudah kita buat 
![ip a](https://user-images.githubusercontent.com/112459285/193236071-ffdc9d9e-ddf6-49aa-ad53-45ad20da28c7.png)


Tahap berikutnya adalah, kita akan menginstall SSH atau openssh-server pada Linux Debian kita, Berikut ini adalah cara nya. 

5. Kelima jalankan ketik apt-get install openssh-server ![apt](https://user-images.githubusercontent.com/112459285/193236818-0374fb58-507f-4e64-bc9f-56f2db26edbc.png)

6. Keenam berikutnya kita akan diperintahkan, untuk memasukkan ISO DEBIAN Paket 1  dengan klik devices > optical disk > iso 
![de](https://user-images.githubusercontent.com/112459285/193237648-3af3a125-1b0d-46e6-95ab-c9a2c3375631.png)

7. Ketujuh silahkan tunggu beberapa saat, jika sudah selesai hal yang akan kita lakukan adalah, mengecek status dari SSH Server yang sudah kita install, dengan perintah ketikan /etc/init.d/ssh status
![init ](https://user-images.githubusercontent.com/112459285/193238480-62f405f2-cf3c-4e8a-b458-b6ae6a347fb6.png)

9. buka aplikasi futty masukkan ip 192.168.43.105
![4](https://user-images.githubusercontent.com/112459285/193229862-6fe73d63-fc30-475b-8623-52562db11c39.png)
6. dan akan muncul 
![3](https://user-images.githubusercontent.com/112459285/193229885-0b7800d9-2816-4b0a-87b0-0d49d0be62a2.png)
