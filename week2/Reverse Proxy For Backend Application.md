1.<ul>
<li> Clone repository dengan perintah <code>git clone git@github.com:ahmadrofiqef/housy-backend.git</code> dan masuk ke directory housy-backend lalu jalankan perintah <code>npm install</code>.

<li> install library pendukung seperti nodejs dan pm2 seperti pada minggu pertama dan install sequelize dengan perintah <code>sudo npm install -g sequelize-cli</code> untuk kebutuhan migrasi database.

<li> Selanjutnya dalam folder housy-backend/config Edit file <code>config.json</code> dan isi username, password serta host sesuai seperti yang sudah dibuat pada sesi instalasi database
</ul>

<img src="/week2/assets/17.png">

2. Selanjutnya langkah yang saya lakukan adalah install mysql 5.7 didalam server backend dengan perintah <code>sudo apt install mysql-client-core-5.7</code>
jika proses instalasi sudah selesai kita dapat mengecek versi sql yang sudah kita install dengan perintah <code>mysql-V</code>

<img src="/week2/assets/18.png">

3. Masuk ke mysql server database dengan perintah <code> mysql -u 'username' -h 'ip-server-db' -p </code> dan coba lihat database yang ada dengan perintah <code>show databases;</code>

<img src="/week2/assets/19.png">

4. Berikutnya kita bisa melakukan migrasi database dengan perintah <code>sequelize db:migrate all</code>, dan pastikan berada pada directory housy-backend. Jika proses migrate
berhasil, kurang lebih akan seperti dibawah. Jika dalam proses migrate mendapatkan kegagalan, kita dapat menginstall mysql2 dengan perintah <code>sudo npm install -g mysql2</code>
dan coba kembali untuk melakukan migrasi.

<img src="/week2/assets/20.png">

5. Jika sebelumnya kita sudah menginstall pm2, kita dapat mengkonfigurasi pm2 dengan membuat file bernama <code>ecosystem.config.js</code> dengan konfigurasi seperti dibawah.

<img src="/week2/assets/21.png">

6. Selanjutnya kita dapat menjalankan file <code>ecosystem.config.js</code> dengan perintah pm2 start, jika hasilnya seperti dibawah maka proses dalam backend sudah berjalan.
untuk mengecek apakah service pm2 masih berjalan atau tidak, kita dapat menggunakan perintah <code>pm2 status</code>

<img src="/week2/assets/22.png">
