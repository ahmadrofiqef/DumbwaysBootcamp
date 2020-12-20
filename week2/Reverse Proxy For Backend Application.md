1. Didalam public server, masuk kedalam folder <code>/etc/nginx/</code> disini saya membuat file bernama <code>housybe.conf</code> untuk reverse proxy backend & <code>housyfe.conf</code>untuk reverse proxy frontend dengan konfigurasi <code>server_name 'ip-server-public'</code> dan location adalah masing-masing IP dari Server
Backend & Frontend dimana <code>10.82.1.223:5000</code>milik backend sedangkan <code>10.82.3.112:3000</code> milik frontend.

<img src="/week2/assets/23.jpg">

2.
<ul>

  <li> Sebelumnya didalam frontend kita juga melakukan langkah yang sama yaitu melakukan fork repository, membuat SSH-keygen dan melakukan clone dengan perintah <code>git clone git@github.com:ahmadrofiqef/housy-frontend.git</code> sama halnya seperti saat mengkonfigurasi untuk backend.
  
  <li>Jika semua langkah sudah dilakukan kita dapat masuk ke dalam folder <code>/housy-frontend</code> dan lakukan instalasi nodejs, pm2 & npm install.
  
  <li>Selanjutnya masuk kedalam file <code>api.js</code> didalam folder <code>/housy-frontend/src/</code> dan ubah baseURL ke IP Server Backend, kemudian save.

</ul>

<img src="/week2/assets/24.png">
