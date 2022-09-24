# Cara Menghubungkan client-server dengan Windows 

1. Buka VirtualBox, kemudian buka kembali Terminal pada VirtualBoxnya.
   
2. Setelah itu untuk melakukan konfigurasi kita harus login sebagai root ketikan *sudo nano /etc/network/interfaces*. Kemudian pada bagian password ketikkan password *root* yang kita buat pada saat instalasi.
   ![Step 2](/Tugas2/gambar/Screenshot%20(5).png)
   
3. Langkah selanjutnya kita akan ke file interface. Edit file dengan menambahkan konfigurasi IP Address server, sebagai contohnya IP Address Server pada *eth0* adalah *192.168.7.1*
Setelah selesai, tekan *ctrl+s* lalu Enter untuk menyimpan yang kita buat tadi, kemudian *ctrl+x* untuk keluar dari editor.
![Step 3](/Tugas2/gambar/Screenshot%20(6).png)

4. Setelah selesai melakukan konfigurasi IP Address, kemudian restart service dari networking pada komputer server kita. Caranya ketikkan perintah */etc/init.d/networking* restart lalu tekan Enter.
   ![Step 4](/Tugas2/gambar/Screenshot%20(9).png)
   
5.  Langkah selanjutnya kita harus memastikan dulu apakah IP Address kita berhasil atau tidak. Caranya dengan mengetikkan perintah *ifconfig* lalu Enter 
   ![Step 5](/Tugas2/gambar/Screenshot%20(11).png)


6.  Setelah itu, buka *Control Panel -> Network and Internet Connections -> Network Connections*. di situ akan terdapat Local Are Connections. 
   ![step6](/Tugas2/gambar/Screenshot%20(22).png)

7.  Klik kanan pada Local Area Connections lalu pilih Properties. Klik pada Internet Protocol (TCP/IP) kemudian klik Properties, akan muncul Jendela Internet Protocol (TCP/IP) Properties.
   ![step7](/Tugas2/gambar/Screenshot%20(18).png)
   
8.  Pada Internet Protocol (TCP/IP) Properties pilih *Use the following IP address*, kemudian masukkan IP Address pada network yang sama. Sebagai contoh IP Address untuk komputer client tidak bolah sama dengan yang sebelumnya *192.168.1.4*, kemudian pada bagian *Subnet mask* biasanya akan terisi *255.255.255.0* secara otomatis. Setelah itu tekan Ok.
Setelah selesai buka cmd dan ping ip address.
   ![step8](/Tugas2/gambar/Screenshot%20(20).png)
