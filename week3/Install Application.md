1. Berikutnya kita akan membuat docker compose dan pastikan kita harus menginstallnya terlebih dahulu karena docker dan docker compose merupakan 2 aplikasi yang berbeda kita dapat menggunakan perintah

<pre>
<code>sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose</code>

sudo chmod +x /usr/local/bin/docker-compose

docker-compose --version
</pre>

Buat file <code>docker-compose.yml</code> dengan isi seperti berikut untuk backend & frontend

<img src="/week3/assets/16.png">

<img src="/week3/assets/17.png">

2. Selanjutnya <code>jalankan docker-compose up -d</code>

<img src="/week3/assets/18.png">

<img src="/week3/assets/19.png">

3. Jika sudah berhasil kita dapat mengecek status docker dengan menggunakan <code>docker ps</code>

<img src="/week3/assets/20.png">

<img src="/week3/assets/21.png">
