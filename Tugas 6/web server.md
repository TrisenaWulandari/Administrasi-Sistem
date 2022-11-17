# WEB SERVER 

1. Langkah pertama buka Debian kemudia masuk ke super user dengan command **sudo su** dan masukkan password Linuxnya.
![1](https://user-images.githubusercontent.com/112459285/198181907-9c7d2814-81c5-4e28-9121-4347d7279889.png)


2. Langkah kedua silahkan install web server dengan mennjalankan command **apt-get install apache2**
![apt-get install apache2](https://user-images.githubusercontent.com/112459285/198181944-8c9fe916-f132-490b-83ec-8664065a4ad5.png)


3. Langkah ketiga jika sudah berhasil silahkan jalankan penginstalan bahasa pemprograman php dengan command **apt-get install php8.1**(php8.1 artinya php versi 8.1) jika gagak coba jalankan command **sudo apt -y install php8.1**
![sudo apt -y install php8 1](https://user-images.githubusercontent.com/112459285/198183112-cf5f3d5c-2429-4823-a81b-8db46d3d8040.png)


4. Langkah keempat selanjutnya konfigurasi, kita bisa melihat hasil dengan mengunjungi web browser dan mengetikkan alamat IP server kita (jalankan command **ip a** untuk melihat IP server) maka akan muncul seperti gambar dibawah ini.
![ip a](https://user-images.githubusercontent.com/112459285/198181985-b830246d-f9aa-4c53-83ac-f5695abd3366.png) 
![127 0 0 1](https://user-images.githubusercontent.com/112459285/198182282-10c652f6-d1fb-4db4-942d-412e5fa2f52c.png)



5. Langkah kelima selanjutnya kita akan menguji menggunakan script php untuk menampilkan info php pada server kita, Kita akan membuat skrip php pada folder **/var/www**  Jalankan command **nano /var/www/html/test/php** atau jika gagal **nano /var/www/test.php**. Setelah itu masukkan skrip seperti gambar dibawah ini 
![PHPP](https://user-images.githubusercontent.com/112459285/198182414-044328f0-e903-45ab-8fbf-ddb705c1e06f.png)

6. Langkah keenam yaitu yang langkah terakhir selanjutnya buka browser dalam linuxnya lalu ketik (**IP server kalian)/test.php.** Maka akan muncul laman tentang info dari php yang kita install pada server. 
![hasill](https://user-images.githubusercontent.com/112459285/198182948-cf185910-0a2d-48c6-8268-555c0578129e.png)


**SELESAI**
