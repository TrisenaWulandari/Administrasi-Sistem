# SSH (REMOTE ACCESS)

1. Pertama, jalankan mesin virtual Debian 11 Linux terlebih dahulu. Caranya klik mesin virtual Debian 11 kemudian klik tombol Mulai 
![1](https://user-images.githubusercontent.com/112459285/197339592-5e8aa31a-5513-42db-ba5a-0342589fe131.png)

2. Kedua setelah itu untuk melakukan konfigurasi kita harus login sebagai root.(sudo si). Karena di dalam sistem linux, 
root adalah hak akses yang paling tinggi (Super User). Jika kita login sebagai user biasa, kita tidak akan bisa melakukan konfigurasi. 
Caranya pada bagian user ketikkan root (sudo su) lalu tekan Enter, kemudian pada bagian password ketikkan password root yang kita buat pada saat instalasi 
![sudo su](https://user-images.githubusercontent.com/112459285/197339646-68ea0d61-98b9-4749-bc9b-467780c18877.png)

3. Ketiga ketikan apt-get install openssh-server dan jika berhasil akan tampil seperti gambar dibawah ini.
![image](https://user-images.githubusercontent.com/112459285/197339815-5be339b4-a067-42f7-883c-b238cc93a75b.png), karena saya sudah menginstall maka akan seperti itu 

4. Keempat kita cek ip addresnya dengan mengetikan "ip addr" ![ip addr](https://user-images.githubusercontent.com/112459285/197340337-1152cd32-90ce-4c7a-a089-b6f4655eae48.png)  dan mencek status ssh server yang sudah di install dengan mengetik " /etc/init.d/ssh status" 
![init d ssh](https://user-images.githubusercontent.com/112459285/197340360-5efd73de-fa92-429d-8084-e1be080077de.png)

5. Kelima masukkan ip address pada futty akan tetapi punya saya eror padahal ip yang saya ketikan sama dengan ip addr saya ![eror](https://user-images.githubusercontent.com/112459285/197342808-60e8f948-26cb-4e35-b958-d341baa832d0.png)


