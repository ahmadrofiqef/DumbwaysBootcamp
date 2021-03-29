1. Pertama pastikan kita menginstall docker dikedua server milik kita yaitu server frontend & backend, tambahkan dependency-dependency untuk menginstall docker

<code>sudo apt-get install curl apt-transport-https ca-certificates software-properties-common</code>

<pre>
- apt-transport-https = tansfer file dan data melalui https.
- ca-certificates = untuk cek sertifikat keamanan
- curl = transfer data
- software-properties-common = script untuk mengelola software.
</pre>

<img src="/week3/assets/1.png">

<pre>
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt update
apt-cache policy docker-ce
</pre>

<img src="/week3/assets/2.png">

install docker 
<pre>
sudo apt install docker-ce
</pre>

<img src="/week3/assets/3.png">

2. Selanjutnya kita bisa mulai menginstall docker dengan perintah <code>sudo apt install docker-ce</code>

<img src="/week3/assets/4.png">

3. Jika dependency dan instalasi docker sudah berhasil, kemudian kita bisa mengecek status docker yang sudah kita install dengan perintah <code>sudo systemctl status docker</code>

<img src="/week3/assets/5.png">

4. Kemudian test membuat sebuah docker images dengan menjalankan perintah <code>docker run hello-world</code>

<img src="/week3/assets/6.png">
