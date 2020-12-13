1. Disini kita akan membuat public dan private server untuk deployment menggunakan NAT Gateway. Langkah pertama yang dilakukan adalah kita
membuat VPC (Virtual Private Cloud) dengan nama myVPC dengan IPv4 CIDR 10.81.0.0/23

<img src="/week1/assets2/24.png">

2. Selanjutnya masuk ke subnet dan buat subnet public dengan nama PubSubnet dengan IPv4 CIDR 10.81.0.0/24

<img src="/week1/assets2/25.png">

3. Buat subnet private dengan IPv4 CIDR 10.81.1.0/24

<img src="/week1/assets2/26.png">

4. Berikutnya buat Internet Gateway dengan nama my-vpc-gw.

<img src="/week1/assets2/27.png">

5. attach internet gateway dengan myVPC yang sudah dibuat.

<img src="/week1/assets2/28.png">

6. Buat route table public dengan nama PublicRT dan sambungkan dengan myVPC.

<img src="/week1/assets2/29.png">

7. Selanjutnya buat kembali route table untuk private route table (PrivateRT) dan sambungkan dengan vpc yang sama.

<img src="/week1/assets2/30.png">

8. Kemudian pilih pilih PublicRT > routes > destination, add route dengan internet gateway yang sudah dibuat.

<img src="/week1/assets2/31.png">

9. Selanjutnya masuk ke Subnet Associations dan pilih PubSubnet.

<img src="/week1/assets2/32.png">

10. Pilih PrivateRT.

<img src="/week1/assets2/33.png">

11. Kemudian pilih subnet association dan pilih PvtSubnet.

<img src="/week1/assets2/34.png">

12. Selanjutnya buat NAT Gateway dengan nama my-NAT-GW dan gunakan subnet PubSubnet lalu Allocate Elastic IP.

<img src="/week1/assets2/35.png">

13. Setelah itu kembali ke Route table dan pilih PrivateRT lalu edit routes dan add route ke NAT gateway yang sudah dibuat.

<img src="/week1/assets2/36.png">

14. Selanjutnya kita  mulai membuat instance, kita akan membuat instance private terlebih dahulu dengan menggunakan
ubuntu server 18.04 LTS.

<img src="/week1/assets2/37.png">

15. Kemudian pilih spesifikasi instance yang akan dibuat, disini menggunakan Memory dan vCPU 1gb.

<img src="/week1/assets2/38.png">

16.	Configure instance dengan network : my-VPC, subnet : PvtSubnet, Auto-assign public IP : disable.

<img src="/week1/assets2/39.png">

17. Selanjutnya set storage yang akan digunakan, disini kita set 8gb.

<img src="/week1/assets2/40.png">

18.	Tambahkan name tag jika dirasa perlu.

<img src="/week1/assets2/41.png">

19.	Selanjutnya di configure security group pilih select an existing security group dan
centang security group yang sudah otomatis dibuat oleh VPC kita, kemudian review and launch.

<img src="/week1/assets2/42.png">

20.	Selanjutnya buat keypair jika belum mempunyai keypair, disini saya sudah mempunyai keypair maka saya
akan menggunakan keypair yang tersedia. Kemudian launch instances.

<img src="/week1/assets2/43.png">

21. Jika sudah membuat instance untuk private server selanjutnya  kita dapat membuat instance untuk public server dengan langkah yang hampir sama dengan membuat 
instance private, perbedaan yang ada adalah saat konfigurasi subnet. Pilih VPC yang sama yang sudah kita buat sebelumnya, lalu untuk subnet 
pilih PubSubnet dan assign IP disable (yang nanti akan dibuat elastic IPnya).

<img src="/week1/assets2/44.png">

22.	Jika langkah diatas sudah dilakukan, kita dapat membuat elastic IP untuk server public, dengan cara masuk ke elastic IP’s > allocate elastic IP address > allocate, 
selanjutnya elastic IP sudah otomatis terbuat. Kemudian pilih IP yang dibuat lalu akan muncul tampilan seperti dibawah, pilih associate elastic IP address.

<img src="/week1/assets2/45.png">

23.	Kemudian pilih instance yang diinginkan, kita pilih ahmadrofiqef-public-srv dari instance yang kita buat sebelumnya.

<img src="/week1/assets2/46.png">

24.	Kemudian choose a private ip address, lalu associate.

<img src="/week1/assets2/47.png">

25.	Kemudian kita bisa kembali ke security group, tambahkan beberapa port range seperti Custom TCP dan juga HTTPS sehingga tidak ada kendala saat proses deploying.

<img src="/week1/assets2/48.png">

26.	Jika semua langkah diatas telah dilakukan, kita dapat melakukan ssh, disini saya menggunakan command prompt windows, 
lakukan perintah dibawah dengan memasukkan keypair dan juga ubuntu@ip-address-public

<img src="/week1/assets2/49.png">

27.	Jika sudah masuk kita dapat membuat user, dengan perintah sudo adduser ahmadrofiqefpublic lalu information seperti full name, dll.
Setelah itu berikan usermod seperti dibawah.

<img src="/week1/assets2/50.png">

28.	Berikutnya kita masuk ke /etc/ssh/sshd_config dan ubah PasswordAuthentication menjadi Yes

<img src="/week1/assets2/51.png">

29.	Lalu kita restart service sshd dan kita bisa exit untuk mencoba ssh kembali.

<img src="/week1/assets2/52.png">

30.	Lakukan ssh seperti dibawah tanpa menggunakan keypair

<img src="/week1/assets2/53.png">

<img src="/week1/assets2/54.png">

31.	Dari langkah sebelumnya kita membuat user untuk public server, jika kita ingin membuat user untuk private kita dapat melakukan langkah yang sama seperti diatas 
dan perlu diingat kita hanya bisa melakukan ssh terhadap private server dari public server. Disini saya membuat private server dengan nama ahmadrofiqefprivate. 
Selanjutnya saya dapat melakukan ssh seperti dibawah.

<img src="/week1/assets2/55.png">

32.	Jika sudah masuk ke private server, kita dapat test apakah private server ini mendapatkan koneksi internet dengan command ping google.com

<img src="/week1/assets2/56.png">

