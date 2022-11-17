# DATABASE SERVER

1. - Login ke debian dengan menggunakan user root dengan cara menjalankan command su atau sudo -i setelah itu jalankan command **apt-get install mysql-server** untuk menginstall database pada server kita, jika ada keterangan "Package 'mysql-server' has no installation candidate" coba jalankan command **apt-get install default-mysql-server**.
![apt-get install default-mysql-server](https://user-images.githubusercontent.com/112459285/201567283-c1692588-e263-4f7f-9c72-179e020a19f9.png)


2. - Jika sudah selanjutnya adalah menginstall phpmyadmin, aplikasi ini digunakan untuk memudahkan user yang tidak terbiasa dengan command line karena aplikasi ini menggunakan GUI. Untuk menginstallnya silahkan jalankan command **apt-get install phpmyadmin**. Pilih apache2 sebagai web server yang digunakan.
![apt-get install phpmyadmin](https://user-images.githubusercontent.com/112459285/201567301-8a131830-3b7d-473e-bf29-0e148946ad76.png)

![apt-get install phpmyadmin (2)](https://user-images.githubusercontent.com/112459285/201567337-5681b2ad-9d46-4ece-95a8-c4567891a689.png)

    - Pada form di bawah ini pilih **Yes**
![apt-get install phpmyadmin (3)](https://user-images.githubusercontent.com/112459285/201567369-aa916e08-e17c-4135-b119-a7f531d83a47.png)


3. - Setelah itu kalian akan diminta untuk memasukkan root password dan konfirmasi password pada saat installasinya berjalan, saran saya buat semudah mungkin agar kalian tidak lupa pada saat ingin menggunakannya. 
![apt-get install phpmyadmin (4)](https://user-images.githubusercontent.com/112459285/201567401-80260524-fff2-418c-886c-206444f3101b.png)


4. - Selanjutnya adalah pengujian, Silahkan kalian buka browser dalam linuxnya lalu ketikkan alamat (IP server kalian)/**phpmyadmin**. 
![apt-get install phpmyadmin (5) TIDAK BERHASIL](https://user-images.githubusercontent.com/112459285/201567445-f2dfa4f7-7a4e-4278-a585-893d313d8c6d.png)

Isi dengan Username = root, Password = (password yang kalian masukkan pada saat installasi)
