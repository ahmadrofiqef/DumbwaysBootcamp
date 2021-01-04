1. Kemudian kita install jenkins dari docker, pastikan buat private server baru untuk jenkins, kemudian jalankan perintah

<pre>
docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/usr/app jenkins/jenkins:lts
</pre>

docker akan secara otomatis mendownload jenkins yang ada pada docker hub

Keterangan: - digunakan port 8080 untuk akses gui jenkins dan 50000 untuk jenkins master/slave - perintah -v untuk membuat volume jenkins yang ada pada directory jenkins_home - lalu disini saya menggunakan versi jenkins lts karena lebih stabil.

<img src="/week3/assets/22.png">

2. Jika selesai menginstall jenkins di docker, selanjutnya lakukan reverse proxy, menambahkan sub-domain yang sudah didaftarkan dan memasang SSL.

<img src="/week3/assets/23.png">
       
