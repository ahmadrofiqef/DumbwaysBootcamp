1. Pertama update package dengan command sudo <code>apt-get update && sudo apt-get upgrade</code> setelah itu
install nginx di public server dengan perintah <code>sudo apt install -y nginx</code>.

<img src="/week1/assets2/15.png">

2. Berikutnya masuk ke folder nginx dari server public dengan command <code>cd /etc/nginx/</code> kemudian buat folder baru,
disini saya membuat folder bernama <code>ahmadrofiqef</code> di dalam folder saya membuat sebuah file dengan nama <code>housy.conf</code> 
dengan konfigurasi seperti dibawah, dimana <code>server_name 52.23.84.89</code> merupakan elastic IP server public yang sudah dibuat, sedangkan untuk 
<code>proxy_pass http://10.81.1.191:3000</code> merupakan IP dari private server.

<img src="/week1/assets2/16.png">

3. Selanjutnya masuk ke dalam folder nginx.conf dengan perintah <code>sudo nano /etc/nginx/nginx.conf</code> tambahkan lokasi direktori dari file
conf yang sudah dibuat sebelumnya dan masukkan dengan command <code>include /etc/nginx/ahmadrofiqef/*</code> di dalam file nginx.conf. Setelah semua
langkah dilakukan, restart nginx services dengan perintah <code>sudo systemctl restart nginx</code>.

<img src="/week1/assets2/17.png">

4. Masukkan <code>52.23.84.89</code> IP server public ke dalam browser.

<img src="/week1/assets2/18.png">
