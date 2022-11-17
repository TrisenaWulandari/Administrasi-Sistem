# **DNS**

**1 Install DNS**

1) Langkah pertama buka debian kemudian masukkan ke super user dengan command **sudo su** dan masukkan password Linuxnya. Jika authentication failure silahkan menggunakan command su dan masukkan password Linuxnya. 
![1](https://user-images.githubusercontent.com/112459285/200841408-65c637c1-1180-41d7-836d-8e4a1212d704.png)


2) Langkah kedua ketikan command **nano /etc/network/interfaces**
![2](https://user-images.githubusercontent.com/112459285/200841490-dfbbbbcd-2d63-46a5-ae67-b59c2b8cf22e.png)


3) Langkah ketiga lalu ketikkan :  
- auto enp0s3,  
- iface enp0s8 inet static, 
address 192.168.50.1, 
netmask 255.255.255.0

![3](https://user-images.githubusercontent.com/112459285/200841609-24c13aab-0474-4ec1-8e48-73195f153b44.png) Setelah itu ctrl+x, y dan enter

4) Langkah keempat ketikkan command **systemctl restrt networking** untuk merestart 
![4](https://user-images.githubusercontent.com/112459285/200841719-623bdeda-ca64-4857-bff0-35bb17ea399a.png)


5) Langkah kelima ketikkan command **nano /etc/apt/sources.list** untuk menentukan sumber download dari mana saja
![5](https://user-images.githubusercontent.com/112459285/200841866-a1e73a6c-d649-462e-999d-cb5138afb3c4.png)


6) Setelah selesai, langkah keenam install bind9 dengan ketikkan command **apt-get install bind9 dnsutils** . 
![6](https://user-images.githubusercontent.com/112459285/200841972-091b61fe-edbf-4b58-907c-f53c7bf04ae3.png) 
Ketikkan Y lalu muncul seperti gambar dibawah ini 
![6 (1)](https://user-images.githubusercontent.com/112459285/200842033-f65b72ac-ca17-4260-9d5c-3bd166797c43.png)

7) Langkah ketuju ketikah command 
- cd /etc/bind/, 
- cp db 127.db.192, 
- cp db.local db.maria dan 
- nano named.conf.local
![7](https://user-images.githubusercontent.com/112459285/200842173-91fe4485-9c4c-4b1f-bc2f-c8268efe0efb.png)


8) Langkah kedelapan selanjutnya masuk ke direktori nano **named.conf.local**, dan saya tambahkan isinya  sebagai berikut:
![8](https://user-images.githubusercontent.com/112459285/200842351-f8d4e440-8e8d-4686-b71d-cb30ffe24df0.png)
Jika sudah, simpan dengan menekan ctrl+x lalu y lalu tekan enter.

9) Langkah kesembilan selanjutnya  itu masuk ke direktori db.maria dengan mengetikkan command **nano nameed.conf.local**
![9](https://user-images.githubusercontent.com/112459285/200842500-6c69e812-8087-4e48-b13f-330751a6f173.png)
Selanjutnya di dalam di rektori nano db.maria ketikkan ctrl+\ untuk replace lalu  ketikkan localhost lalu enter lalu ketikkan nama domain, disini nama domain saya  maria.com lalu enter. Untuk mengganti nama localhost yang ada menjadi nama domain kita ketikkan A. Lalu ganti ip sesuai dengan ip kita (127.0.0.1 menjadi 192.168.1.1). Bagian  bawahnya juga diganti menjadi ip kita dan AAA diganti menjadi CNAME dan  simbol @ diganti menjadi www. Selanjutnya tambahkan pada baris baru mail IN CNAME @. Lalu simpan

10) Selanjutnya masuk ke direktori 192 dengan mengetikkan command **nano db.192** pertama-tama kita replace dengan mengetikkan ctrl+\ lalu ketikkan localhost  ganti sesuai domain kita (maria.com) lalu tekan A. Selanjutnya ganti 1.0.0 menjadi @, pada nama domain tambahkan www lalu pada baris baru buat 1 IN PTR mail.maria.com.
Lalu simpan
![10](https://user-images.githubusercontent.com/112459285/200843303-6f56d3c6-02f2-4444-a466-a655e11dea7e.png)

![11](https://user-images.githubusercontent.com/112459285/200843286-883a9719-fd71-41fa-8436-d3180985a8dd.png)

![11(1)](https://user-images.githubusercontent.com/112459285/200843241-6f344126-c91c-464a-bda0-a367f19fdf1f.png)



11) Lalu ketikkan **nano /etc/resolv.conf** Tambahkan didalam di rektori ini pada bagian atas ketikkan : 
- domain maria.com
- search maria.com
- nameserver 192.168.500.1 Lalu simpan
![12](https://user-images.githubusercontent.com/112459285/200843489-3616a6ce-0481-4544-9adb-3cc50c17106d.png)


12) Lalu kita akan merestart bindnya dengan mengetikkan **systemctml restart bind9**
![13](https://user-images.githubusercontent.com/112459285/200843592-a08e5006-b75b-4067-8ab1-c4e0cda7afb5.png)

14) Terakhhir kita ketikkan command **nslookup maria.com**
![14](https://user-images.githubusercontent.com/112459285/200843611-1da9af32-9470-4ae7-9ac2-c5bf84ddfbf7.png)

