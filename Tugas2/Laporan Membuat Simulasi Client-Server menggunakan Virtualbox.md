# Cara Menghubungkan client-server dengan Windows 

1. Buka VirtualBox, kemudian buka kembali Terminal pada VirtualBoxnya.
   
2. Setelah itu untuk melakukan konfigurasi kita harus login sebagai root ketikan *sudo nano /etc/network/interfaces*. Kemudian pada bagian password ketikkan password *root* yang kita buat pada saat instalasi.
   
3. Langkah selanjutnya kita akan ke file interface. Edit file dengan menambahkan konfigurasi IP Address server, sebagai contohnya IP Address Server pada *eth0* adalah *192.168.7.1*
Setelah selesai, tekan *ctrl+s* lalu Enter untuk menyimpan yang kita buat tadi, kemudian *ctrl+x* untuk keluar dari editor.

4. Setelah selesai melakukan konfigurasi IP Address, kemudian restart service dari networking pada komputer server kita. Caranya ketikkan perintah */etc/init.d/networking* restart lalu tekan Enter.
   
5.  Langkah selanjutnya kita harus memastikan dulu apakah IP Address kita berhasil atau tidak. Caranya dengan mengetikkan perintah *ifconfig* lalu Enter
   
6.  Setelah itu, buka *Control Panel -> Network and Internet Connections -> Network Connections*. di situ akan terdapat Local Are Connections.
   
7.  Klik kanan pada Local Area Connections lalu pilih Properties. Klik pada Internet Protocol (TCP/IP) kemudian klik Properties, akan muncul Jendela Internet Protocol (TCP/IP) Properties.
   
8.  Pada Internet Protocol (TCP/IP) Properties pilih *Use the following IP address*, kemudian masukkan IP Address pada network yang sama. Sebagai contoh IP Address untuk komputer client tidak bolah sama dengan yang sebelumnya *192.168.1.7*, kemudian pada bagian *Subnet mask* biasanya akan terisi *255.255.255.0* secara otomatis. Setelah itu tekan Ok.