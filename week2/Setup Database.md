1. Masuk ke dalam server database dan jalankan command dibawah.

<img src="/week2/assets/6.png">

<img src="/week2/assets/7.png">

2. Kemudian jalankan instalasi menggunakan perintah <code>sudo apt-get install mysql-server mysql-client</code> tunggu hingga selesai.

<img src="/week2/assets/8.png">

3. Selanjutnya akan masuk ke dalam proses instalasi mysql, pilih nomor 1 terlebih dahulu, kemudian ubah versi mysql, disini saya menggunakan mysql
versi 5.7 dan selesaikan proses instalasinya.

<img src="/week2/assets/9.png">

<img src="/week2/assets/10.png">

4. Jika instalasi sudah selesai, kita dapat login dari server database menggunakan perintah <code>mysql -u root -p</code> umumnya user default yang ada adalah
root dan tanpa menggunakan password.

<img src="/week2/assets/12.png">

5. Kemudian jika kita ingin menambahkan keamanan dalam database kita dengan menambahkan password, kita dapat menjalankan perintah
<code>ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'root'</code> disini saya ubah passwordnya menjadi 'root'.

<img src="/week2/assets/13.png">
  
