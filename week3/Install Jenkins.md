1. Kemudian kita install jenkins dari docker, pastikan buat private server baru untuk jenkins, kemudian jalankan perintah

<pre>
docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/usr/app jenkins/jenkins:lts
</pre>

docker akan secara otomatis mendownload jenkins yang ada pada docker hub

Keterangan: - digunakan port 8080 untuk akses gui jenkins dan 50000 untuk jenkins master/slave - perintah -v untuk membuat volume jenkins yang ada pada directory jenkins_home - lalu disini saya menggunakan versi jenkins lts karena lebih stabil.

<img src="/week3/assets/22.png">

2. Jika selesai menginstall jenkins di docker, selanjutnya lakukan reverse proxy, menambahkan sub-domain yang sudah didaftarkan dan memasang SSL.

<img src="/week3/assets/23.png">

3. Selanjutnya kita bisa mulai mengakses domain yang sudah terpasang ke browser local kita.

<img src="/week3/assets/23.1.png">

4. Karena kita menginstall jenkins di docker, maka untuk menampilkan security password untuk menginstall jenkins kita dapat menggunakan perintah <code>docker logs jenkins-container</code> kemudian copy dan paste.

<img src="/week3/assets/23.2.png">

5. Selanjutnya pilih install suggested plugins.

<img src="/week3/assets/23.3.png">

6. Buat user untuk jenkins.

<img src="/week3/assets/23.4.png">

7. Untuk jenkins url, pastikan domain yang ada adalah domain yang sudah kita pasang.

<img src="/week3/assets/23.5.png">
       
