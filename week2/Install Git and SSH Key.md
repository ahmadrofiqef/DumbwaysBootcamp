1. Pertama kita melakukan fork repository pada git project yang sudah diberikan.

<img src ="/week2/assets/0.png">

2. Jika sudah melakukan fork, di bagian server backend saya membuat keygen dengan perintah <code>ssh-keygen</code> kemudian isi passphrase apabila
dirasa perlu, jika tidak dapat dikosongkan saja dengan mengklik enter.

<img src ="/week2/assets/1.png">

3. Selanjutnya jika sudah melakukan ssh-keygen diatas, kita masuk ke dalam folder /.ssh dengan perintah <code>cd /.ssh</code> dan gunakan perintah
<code>cat id_rsa.pub</code> untuk melihat isi file tersebut, kemudian copy isi file.

<img src ="/week2/assets/2.png">

4. Kemudian masuk ke dalam github > settings > SSH and GPG keys > new SSH key lalu paste isi file yang berasal dari id_rsa.pub

<img src ="/week2/assets/3.png">

5. Selanjutnya jalankan perintah SSH -T git@github, jika sudah, lakukan git clone dengan perintah <code>git clone git@github.com:ahmadrofiqef/housy-backend.git</code>
untuk mengambil repository private dari akun github.

<img src ="/week2/assets/4.png">

6. Kemudian kita bisa melakukan perintah seperti <code>git add .</code> , <code>git commit -m ""</code> , <code>git push</code>

<img src ="/week2/assets/5.png">
