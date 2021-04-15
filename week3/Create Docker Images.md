1. Jika kita sudah berhasil menginstall docker, kita dapat mencoba membuat sebuah dockerfile, dimana dockerfile ini merupakan kumpulan instruksi yang nanti akan dieksekusi secara berurutan untuk membangun sebuah image docker. Dan pastikan buat 2 buah dockerfile di masing-masing server yang terinstall docker

<img src="/week3/assets/7.png">

<img src="/week3/assets/15.png">

2. Selanjutnya lakukan <code>docker build -t <nama-image>:<tag> .</code> yang otomatis akan mengeksekusi dockerfile yang sudah kita buat tadi

<img src="/week3/assets/8.png">

3. Ketik <code>docker images</code> untuk melihat images yang sudah pernah kita buat

<img src="/week3/assets/9.png">

4. Selanjutnya kita akan membuat sebuah docker container dengan image yang sudah dibuat dengan perintah <code>docker container create --name nama-container -p port-aplikasi:port nama-image:tag</code>
  
<img src="/week3/assets/10.png">

5. Jika sudah berhasil membuat docker container, kemudian jalankan container tersebut dengan perintah <code>docker start container nama-container</code>

<img src="/week3/assets/11.png">

6. Selanjutnya jika kita ingin membuild dan push ke repository docker, kita bisa lakukan langkah yang sama dengan perintah build sebelumnya, tapi tambahkan username dockerhub di depan repository kita. Dan pastikan kita harus login docker terlebih dahulu.
  
<img src="/week3/assets/12.png">

7. Lakukan perintah build dengan username seperti dibawah.

<img src="/week3/assets/13.png">

8. Jika sudah lakukan docker push repository seperti dibawah.

<img src="/week3/assets/14.png">


  
