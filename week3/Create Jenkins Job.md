1. Saat kita sudah selesai menginstall jenkins, kita menambahkan plugins seperti Publish Over SSH untuk melakukan Remote terhadap server yang kita inginkan.

<img src="/week3/assets/24.2.png">

2. Jika proses instalasi selesai, kemudian restart.

<img src="/week3/assets/24.png">

3. Selanjutnya kita tambahkan credentials yaitu menggunakan private key milik server yang kita miliki.

<img src="/week3/assets/24a.png">

4. Selanjutnya kita bisa melakukan configure system, kemudian cari Publish Over SSH > SSH Server. Kemudian berikan nama server, isi hostname dengan ip milik server, kemudian isi username sesuai dengan username server dan remote directory di folder /home/username-server. selanjutnya untuk server kita bisa menggunakan password milik server kita dan set timeout menjadi 0. Kemudian klik Test Configuration untuk mengecek apakah konfigurasi success. Jika success maka konfigurasi berhasil. Lakukan untuk server yang lainnya.

<img src="/week3/assets/25.png">

<img src="/week3/assets/26.png">

5. Jika kita sudah selesai mengkonfigurasi, kita bisa membuat jobs di jenkins, isi nama dan pilih freestyle project.

<img src="/week3/assets/27.png">

6. Selanjutnya pilih source code management, pilih git, kemudian masukkan url repository git yang ingin kita remote, kemudian pilih credentials yang sudah dibuat

<img src="/week3/assets/28.png">

7. Kemudian scroll kebawah, pilih github hook trigger for GITScm polling.

<img src="/week3/assets/29.png">

8. Kemudian pilih build > send files or execute command over ssh, masukkan konfigurasi seperti dibawah. dibagian exec command masukkan perintah untuk automation jika seandainya terjadi perubahan maka otomatis akan mengeksekusi command-command tersebut.

<img src="/week3/assets/30.png">

9. Jika konfigurasi sudah selesai, kita masuk ke Settings di repository github kita, masuk ke bagian webhooks, tambahkan URL sub-domain dan tambahkan /github-webhook/ di bagian belakang URLnya.

<img src="/week3/assets/31.png">

10. Selanjutnya saya mencoba melakukan perubahan pada file yang berada di dalam repository kemudian save.

<img src="/week3/assets/32.png">

11. Kemudian jenkins otomatis akan mengecek dan membuild perubahan tersebut, jika berhasil akan muncul notifikasi successful dan kemudian kita bisa cek console output untuk melihat logs dari perubahan tersebut.

<img src="/week3/assets/33.png">

12. Pastikan kita sudah membuat jobs untuk server frontend & backend, lalu kita coba test lakukan perubahan.

<img src="/week3/assets/34.png">

13. Berikutnya untuk notifier disini saya menggunakan discord notifier, pertama kita dapat menginstall pluginsnya terlebih dahulu di manage plugins. Jika sudah, kemudian buat sebuah channel di discord, klik settings di bagian text-channel > integrations > create webhooks. selanjutnya copy url webhook tersebut.

<img src="/week3/assets/35.png">

14. Selanjutnya di bagian post build actions, tambahkan discord notifier > masukkan link yang kita copy tadi dan paste di webhook URL, lalu save

<img src="/week3/assets/35.5.png">

15. Jika selanjutnya terjadi perubahan, secara otomatis bot di discord akan memberikan notifikasi kedalam channel.

<img src="/week3/assets/36.png">



