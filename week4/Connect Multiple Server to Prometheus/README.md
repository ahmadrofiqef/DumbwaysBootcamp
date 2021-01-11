1. Selanjutnya karena seharusnya kita menginstall node exporter di tiap server akan memakan waktu yang cukup lama, disini saya menginstall docker dan menjalankan node exporter di docker untuk mempersingkat waktu.

<img src="/week4/assets/12.png">

2. Di dalam server Prometheus, di file Prometheus.yml kita isi konfigurasi seperti dibawah. Untuk bagian target isi IP dari tiap server yang ingin kita remote.

<img src="/week4/assets/13.png">

3. Selanjutnya kita buka domain monitoring.instructype.com, di bagian targets kita bisa melihat server mana saja yang sudah terhubung, jika statenya UP maka Prometheus sudah terhubung dengan server.

<img src="/week4/assets/14.png">

4. Jika sudah kita akan memonitoring server menggunakan grafana untuk tampilan yang lebih baik, disin kita wget package grafana terlebih dahulu

<img src="/week4/assets/15.png">

5. Proses Instalasi grafana

<img src="/week4/assets/16.png">

6. Cek status grafana server

<img src="/week4/assets/17.png">

7. Selanjutnya di dalam file monitoring.conf yang berada di public server, kita ubah port Prometheus 9090 menjadi port grafana 3000

<img src="/week4/assets/18.png">

8. Kemudian buka kembali domain monitoring.username.instructype.com, otomatis tampilan akan berubah menjadi tampilan login grafana

<img src="/week4/assets/19.png">

9. Selanjutnya masuk ke configuration > data source > pilih Prometheus. Kemudian masukkan URL menjadi localhost:9090 yaitu IP milik Prometheus. Kemudian save & test, jika outputnya adalah data source is working maka koneksi berhasil.

<img src="/week4/assets/20.png">

<img src="/week4/assets/21.png">

10. Yang terakhir kita bisa berkreasi menampilkan informasi dari server dengan grafik yang kita inginkan.

<img src="/week4/assets/22.png">


                              
                              
