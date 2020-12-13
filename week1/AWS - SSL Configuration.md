1. Dalam mengkonfigurasi SSL pertama kita lakukan <code>sudo apt-get install software-properties-common</code>
lalu add repository dari certbot dengan perintah <code>sudo add-apt-repository ppa:certbot/certbot</code>

<img src="/week1/assets2/1.png">

2. Selanjutnya install dengan perintah <code>sudo apt install certbot python-certbot-nginx python3-certbot-dns-cloudflare</code>

<img src="/week1/assets2/2.png">

3. Masukkan domain milik kita dengan perintah <code>sudo certbot --nginx -d ahmadrofiqef.instructype.com</code> jika terdapat 
pertanyaan pilih Agree/Yes.

<img src="/week1/assets2/3.png">

4. Selanjutnya akan ada prompt question seperti dibawah, pilih nomor 2 (redirect).

<img src="/week1/assets2/4.png">

5. Jika semua proses instalasi certbot sudah selesai dilakukan, kita dapat mengecek konfigurasi didalam nginx yang sudah kita buat sebelumnya,
jika isi didalam file.conf kita sudah seperti ini artinya SSL berhasil dilakukan.

<img src="/week1/assets2/5.png">

6. Dan satu hal yang perlu diingat adalah di konfigurasi AWS yang kita buat apakah <code>HTTPS</code> sudah terdaftar atau belum, jika belum
maka nantinya akan mendapati error.

<img src="/week1/assets2/6.png">

7. Hasil domain yang sudah terpasang SSL akan terdapat logo gembok di samping domainnya yang artinya website sudah terpasang SSL (Secured).

<img src="/week1/assets2/7.png">
