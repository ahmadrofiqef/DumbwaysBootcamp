1. Pertama kita update & upgrade package OS di dalam server private kita dengan perintah <code>Sudo apt-get update && sudo apt-get upgrade</code>.

<img src="/week1/assets2/19.png">

2. Selanjutnya masukkan perintah <code>curl -sL http://deb.nodesource.com/setup_10.x | sudo -E bash -</code> untuk repository
nodejs versi 10.

<img src="/week1/assets2/20.png">

3. Lakukan perintah <code>Sudo apt install –y nodejs</code> untuk menginstall nodejs.

<img src="/week1/assets2/21.png">

4. Setelah proses instalasi nodejs selesai, jalankan perintah <code>git clone https://github.com/DumbwaysDotId/DW15WDTPH_housy.git</code>.
Kemudian masuk kedalam folder dengan perintah <code>cd DW15DWTPH_housy</code>, di dalam folder ini kita buat file bernama <code>ecosystem.config.js</code> 
dengan konfigurasi seperti dibawah.

<img src="/week1/assets2/22.1.png">

5. Selanjutnya install pm2 dengan <code>command sudo npm install -g pm2</code>

<img src="/week1/assets2/22.png">

6. Jalankan <code>pm2 start ecosystem.config.js</code>

<img src="/week1/assets2/23.png">
