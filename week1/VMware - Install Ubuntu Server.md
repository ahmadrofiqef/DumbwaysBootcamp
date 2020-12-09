1. pertama-tama kita membuat operating system dengan nama UbuntuServer, pilih type : Linux, Version : 64 bit.

<img src="/week1/assets/1.png">

2. selanjutnya buat jumlah memory ram yang akan digunakan, disini sebanyak 2gb atau 2048mb

<img src="/week1/assets/2.png">

3. Pilih Create a Virtual Hard disk

<img src="/week1/assets/3.png">

4. Pilih VDI (Virtual Box Disk Image)

<img src="/week1/assets/4.png">

5. Selanjutnya pilih Dynamic Allocated

<img src="/week1/assets/5.png">

6. Selanjutnya buka setting pada VM, lalu pilih Settings > Storage > Controller: IDE > Empty > pilih gambar disk, lalu pilih direktori dimana file iso ubuntu server disimpan.
kemudian pilih.

<img src="/week1/assets/6.png">

7. Set ukuran harddisk yang dibutuhkan, disini sebanyak 10gb > create.

<img src="/week1/assets/7.png">

8. Jika sudah create maka tampilannya akan seperti dibawah ini.

<img src="/week1/assets/8.png">

9. Start ubuntu server.

<img src="/week1/assets/9.png">

10. Tampilan dibawah merupakan tampilan utama instalasi ubuntu server.

<img src="/week1/assets/10.png">

<img src="/week1/assets/11.png">

<img src="/week1/assets/12.png">

11. karena kita ingin membuat IP static nantinya, untuk langkah ini tidak perlu diubah.

<img src="/week1/assets/13.png">

<img src="/week1/assets/14.png">

12. Pilih custom storage layout.

<img src="/week1/assets/15.png">

13. Selanjutnya pilih harddisk yang sudah dibuat sebelumnya saat instalasi yang berukuran 10gb > Add GPT Partition.

<img src="/week1/assets/16.png">

14. Masukkan 1G dengan format swap.

<img src="/week1/assets/17.png">

15. Pilih Add GPT Partition.

<img src="/week1/assets/18.png">

16. Kemudian pilih kembali harddisk, lalu masukkan size yang masih tersisa, disini 8,997G dengan format ext4.

<img src="/week1/assets/19.png">

17. Kemudian Continue.

<img src="/week1/assets/20.png">

18. Selanjutnya masukkan name, server name, username & password.

<img src="/week1/assets/21.png">

19. Ceklist install Open SSH Server.

<img src="/week1/assets/22.png">

20. Pilih done.

<img src="/week1/assets/23.png">

21. Proses instalasi ubuntu server sedang berjalan.

<img src="/week1/assets/24.png">

22. Selesai proses instalasi ubuntu server.

<img src="/week1/assets/25.png">
