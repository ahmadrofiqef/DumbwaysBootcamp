1. Tambahkan DNS dari CloudFlare dengan memasukkan domain dari elastic IP server public milik kita.

<img src="/week1/assets2/8.png">

2. Di dalam file nginx dapat kita lihat server_name dengan address public milik kita.

<img src="/week1/assets2/9.png">

3. Lalu ubah server_name menjadi subdomain ahmadrofiqef.instructype.com

<img src="/week1/assets2/10.png">

4. Jika sudah, masuk ke server private milik kita lalu masuk ke direktori source code dan jalankan <code>npm start</code>. Kemudian masukkan subdomain yang sudah didaftarkan ke dalam browser.

<img src="/week1/assets2/11.png">
