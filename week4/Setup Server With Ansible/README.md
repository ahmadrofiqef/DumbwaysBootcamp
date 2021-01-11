1. Install ansible secara manual tanpa bantuan docker

<pre>
apt install python
sudo apt-add-repository ppa:ansible/ansible
apt update
apt install ansible
</pre>

2. Setelah ansible terinstall, buat list inventory yang berisikan informasi host server yang ingin kita remote.

<img src="/week4/assets/1.png">

3. Jika proses instalasi ansible sudah selesai, kita bisa membuat file bernama Inventory didalam direktori ansible yang kita buat dan isi server apa saja yang ingin kita remote.

<img src="/week4/assets/2.png">

4. Lalu di dalam folder yang sama kita bisa membuat file ansible.cfg yang merupakan file default konfigurasi untuk ansible.

<img src="/week4/assets/3.png">

5. Selanjutnya kita bisa test koneksi apakah ansible sudah terhubung dengan server remote dengan perintah dibawah.

<img src="/week4/assets/4.png">

6. Selanjutnya buat sebuah file dengan format .yml yang nantinya akan dijalankan melalui ansible-playbook. Disini merupakan install nginx di public server, jika sudah kita bisa mengecek nginx di public server apakah sudah terinstall atau belum


<img src="/week4/assets/5.png">

<img src="/week4/assets/6.png">

  
  
  
  
