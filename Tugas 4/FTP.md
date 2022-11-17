# FTP
**1 Instalasi FTP :**

1) Langkah pertama buka Debian kemudian masuk ke super user dengan command **sudo su** dan masukkan password Linuxnya. Jika authentication failure silahkan menggunakan command su dan masukkan password Linuxnya.
![1](https://user-images.githubusercontent.com/112459285/200821387-cb4cb168-a3e9-49da-9d2f-9f6f7ae7bb1a.png)


2) Langkah kedua setelah berhasil masuk ke super user, silahkan install proftpd dengan menjalankan command **apt-get install proftpd** 
![2](https://user-images.githubusercontent.com/112459285/200821468-dd4d4cea-f6b2-41a7-9c5b-660a5075ee8d.png)


3) Langkah ketiga setelah berhasil masukan user command **nano /etc/apt/sources.list** 
![3](https://user-images.githubusercontent.com/112459285/200821621-851412ff-368b-42d6-b469-9a4a05ba8d88.png)


    kemudian tambahkan tanda # di depan deb cdrom baris ke -2 atau bisa juga text pada baris ke -2 tersebut dihapus. Simpan klik ctrl+s, ctrl+x 
![3 (1)](https://user-images.githubusercontent.com/112459285/200821733-31ebf8c0-e9e0-4cd5-9843-3e9f41142a39.png)


4) Langkah keempat simpan dan jalankan command **apt-get update** dan coba jalankan lagi command **apt-get install proftpd** untuk menginstall ulang. 
![4](https://user-images.githubusercontent.com/112459285/200822042-959975dd-5a51-4c03-b6da-82edec64017d.png)


5) Selanjutnya pengujian pada proftpd, kali ini saya lakukan dengan menggunakan aplikasi filezilla yang akan diinstall pada computer client. Untuk itu silahkan download aplikasi tersebut pada https://filezilla-project.org/download.php jika sudah diinstall jalankan, maka tampilannya akan sebagai berikut:
![5](https://user-images.githubusercontent.com/112459285/200823545-31b832c0-a4c7-45d2-b41f-f74cd1a63b8a.png)


**2 Testing**
1) Jalankan **filezilla** kemudian masukkan: Host : Isi dengan IP address dari debian Username : Nama user di debian Password : Password debian Port : 21
![5](https://user-images.githubusercontent.com/112459285/200823895-db635bd9-6217-4231-900a-a97b8099deb4.png)

  kemudian klik quickconnect, jika berhasil maka akan muncul seperti gambar dibawah ini. Perlu kalian ketahui bahwa sisi bagian kiri pada gambar dibawah merupakan sisi file local dari computer client kita sedangkan untuk sisi bagian kanan merupakan sisi server yaitu server yang menggunakan system operasi debian pada modul ini. 
![6](https://user-images.githubusercontent.com/112459285/200825492-1a4d9102-0aad-4d6d-9502-7c9e6e83af2a.png)

2) Lalu kita akan buat **file .txt**, untuk membuatnya jalankan command nano saya.txt kemudian isi ketik teks yang mau di masukkan. 
![7](https://user-images.githubusercontent.com/112459285/200825649-abc89166-e8a5-400b-b755-fec711f816ff.png)

kemudian simpan dan cek filenya apakah sudah ada dengan menggunakan command ls, atau bisa lihat di Remote site yang terdapat di Filezilla.
![6](https://user-images.githubusercontent.com/112459285/200825759-e1c73924-3083-4d29-92bc-35a6645a6fdb.png)


**Selesai**
