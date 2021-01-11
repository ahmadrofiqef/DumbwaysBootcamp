1. 
<ul>
<li>Download cms yang akan dideploy, dan ekstrak pada komputer lokal agar mempercepat proses deploy sehingga tidak perlu ekstrak didalam folder cPanel.
<li>Daftar ke cPanel dan pilih domain dan subdomain yang akan dipakai untuk mengakses CMS, pada kolom yang ada dikanan terdapat info yang bisa digunakan untuk mengakses ftp dan database
</ul>

<img src="/week4/assets/23.png">

2. Kemudian setelah kita download cms kita extract terlebih dahulu file cms di folder local, disini saya menggunakan filezila untuk melakukan transfer data karena lebih terstruktur dan bisa terlihat jika terdapat kegagalan saat ada perpindahan data 

<img src="/week4/assets/24.png">

3. Jika sudah kita bisa mengakses domain yang sudah didaftarkan, disini domain yang sudah saya daftarkan adalah ahmadr.epizy.com. Kemudian jalankan konfigurasinya.

<img src="/week4/assets/25.png">

4. Langkah selanjutnya next dan configure database, jika database belum dibuat, kita bisa buat terlebih dahulu di cPanel.

<img src="/week4/assets/26.png">

5. Kemudian di langkah ke-3 pilih default english kemudian install

<img src="/week4/assets/28.png">

6. Jika proses instalasi sudah selesai kita diharuskan untuk menghapus folder instalasinya

<img src="/week4/assets/29.png">

7. Kemudian kita bisa mengakses website dengan subdomain yang sudah didaftarkan

<img src="/week4/assets/30.png">

8. Untuk SSL disini saya menggunakan GoGetSSL

<img src="/week4/assets/31.png">

9. Untuk menambahkan SSL kita bisa mengisi data yang dibutuhkan dan tunggu proses sampai selesai.

<img src="/week4/assets/32.png">

10. Untuk menambahkan SSL kita bisa mengisi data yang dibutuhkan dan tunggu proses sampai selesai.

<img src="/week4/assets/33.png">

11. Selanjutnya kita perlu menunggu selama beberapa menit/jam untuk mendapatkan certificate untuk SSL. Jika sudah copy certificate tersebut

<img src="/week4/assets/34.png">

12. Kemudian di bagian SSL/TLS paste certificate yang sudah dicopy tadi.

<img src="/week4/assets/35.png">

13. Jika sudah status akan berubah menjadi validate certificate SSL installed

<img src="/week4/assets/36.png">

14. Kemudian kita bisa mengakses domain kembali dengan menambahkan https:// di urlnya. Selanjutnya kita bisa cek certificate domain tersebut.

<img src="/week4/assets/37.png">
