1. Untuk mengkonfigurasi SSL pada domain yang sudah dipasang kita dapat melakukan perintah dibawah ini di public server.
<pre>
<ul>
  <li><code>sudo apt-get install software-properties-common</code>
  <li><code>sudo add-apt-repository ppa:certbot/certbot</code>
  <li><code>sudo apt install certbot python-certbot-nginx python3-certbot-dns-cloudflare/certbot</code>
</ul>
</pre>

2. langkah selanjutnya kita bisa mulai memasang certbot pada domain yang sudah kita pasang dengan perintah.
<pre>
<ul>
Frontend :
  <li><code>sudo certbot --nginx -d ahmadrofiqef.instructype.com</code>
  
Backend :
  <li><code>sudo certbot --nginx -d api.ahmadrofiqef.instructype.com</code>
</ul>
</pre>
NB : Pastikan dalam proses instalasi certbot pada domain, pilih nomor 2 (Redirect) to HTTPS.

3. Jika semua proses sudah selesai, kita dapat mengecek apakah certification sudah terinstall atau belum didalam file <code>housybe.conf</code> & <code>housybe.conf</code> didalam folder <code>/etc/nginx/</code> yang berada di Public Server.

<img src="/week2/assets/27.png">

<img src="/week2/assets/28.png">


  
