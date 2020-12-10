1. Selanjutnya kita akan memulai menginstall beberapa aplikasi seperti nginX dan nodejs, disini kita akan menggunakan SSH yang dijalankan melalui
command prompt dengan perintah seperti dibawah dan gunakan ip address static yang sudah disetup sebelumnya.

<img src="/week1/assets/29.png">

2. Jika sudah kita install nginX dengan perintah sudo apt install nginX

<img src="/week1/assets/30.png">

3. Selanjutnya jika instalasi dirasa sudah berhasil, kita bisa mengecek status dari nginx dengan perintah sudo systemctl status nginx
atau kita dapat mencoba langsung memasukkan address ke dalam browser kita, jika berhasil maka tampilan akan seperti dibawah.

<img src="/week1/assets/31.png">

4. Langkah berikutnya kita akan menginstall nodejs dengan melakukan perintah dibawah terlebih dahulu agar package nodejs yang terinstall
adalah versi ke-10.

<img src="/week1/assets/32.png">

5. Jika proses sudah selesai kita dapat menginstall nodejs dengan perintah sudo apt-get install -y nodejs

<img src="/week1/assets/33.png">

6. Berikutnya kita dapat melakukan git clone dari source yang sudah disediakan. Kemudian lakukan perintah dibawah.

<img src="/week1/assets/34.png">

7. Jika perintah git clone sudah berhasil dijalankan, kita dapat memulai service dengan perintah npm start seperti dibawah.

<img src="/week1/assets/35.png">

8.Jika service sudah berjalan akan muncul tampilan seperti dibawah.

<img src="/week1/assets/36.png">

9. Test langsung ke halaman browser menggunakan port default yaitu 3000.

<img src="/week1/assets/37.png">
