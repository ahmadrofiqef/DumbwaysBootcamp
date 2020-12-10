1. Untuk melakukan setup network mengubah ip dynamic ke static kita lakukan sudo nano /etc/netplan/00-installer-config.yaml kemudian ubah seperti 
gambar dibawah, disini saya menggunakan address 192.168.0.108/24 dengan DNS google [8.8.8.8, 8.8.4.4]

<img src="/week1/assets/26.png">

2. Jika kita tidak mengetahui gateway yang kita punya, kita dapat mengecek gateway dengan perintah berikut

<img src="/week1/assets/27.png">

3. Selanjutnya jika langkah diatas sudah selesai kita dapat menulis sudo netplan apply, jika tidak terdapat error atau semacamnya, 
artinya langkah diatas berhasil

<img src="/week1/assets/28.png">
