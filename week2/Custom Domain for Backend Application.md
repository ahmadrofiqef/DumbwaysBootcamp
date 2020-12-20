1. Selanjutnya tambahkan domain baru di cloudflare dengan nama <code>api.ahmadrofiqef</code>dan juga ubah domain <code>ahmadrofiqef</code> kemudian matikan 
proxy status menjadi DNS Only.

<img src="/week2/assets/25.png">

2. Jika sudah, kita masuk ke Public Server & masuk kedalam folder /etc/nginx/ buka kedua file housybe.conf & housyfe.conf dengan perintah <code>sudo nano housybe.conf</code>
& <code>sudo nano housyfe.conf</code>

<img src="/week2/assets/23.jpg">

3. Kemudian ubah server_name yang berada pada file <code>housybe.conf</code> & <code>housyfe.conf</code> menjadi domain yang sudah didaftarkan kedalam cloudflare.
untuk backend ubah menjadi <code>api.ahmadrofiqef.instructype.com</code> sedangkan frontend menjadi <code>ahmadrofiqef.instructype.com</code>

<img src="/week2/assets/26.png">



