1. Dalam mensetup monitoring server pastikan kita install node exporter dan prometheus di dalam server dengan perintah berikut.

<pre>
<ul>
<li>sudo apt update && sudo apt upgrade -y
<li>curl -LO https://github.com/prometheus/node_exporter/releases/download/v0.18.1/node_exporter-0.18.1.linux-amd64.tar.gz
<li>tar xzvf node_exporter-0.18.1.linux-amd64.tar.gz
<li>sudo cp node_exporter-0.18.1.linux-amd64/node_exporter /usr/local/bin
<li>sudo chown node_exporter:node_exporter /usr/local/bin/node_exporter
<li>sudo nano /etc/systemd/system/node_exporter.service
<ul>
</pre>

<pre>
<ul>
<li>sudo useradd --no-create-home --shell /bin/false prometheus
<li>sudo mkdir /etc/prometheus
<li>sudo mkdir /var/lib/prometheus
<li>sudo chown prometheus:prometheus /etc/prometheus
<li>sudo chown prometheus:prometheus /var/lib/prometheus
<li>curl -LO https://github.com/prometheus/prometheus/releases/download/v2.17.1/prometheus-2.17.1.linux-amd64.tar.gz
<li>tar xzvf prometheus-2.17.1.linux-amd64.tar.gz
<li>sudo cp prometheus-2.17.1.linux-amd64/prometheus /usr/local/bin
<li>sudo cp prometheus-2.17.1.linux-amd64/promtool /usr/local/bin
<li>sudo chown prometheus:prometheus /usr/local/bin/prometheus
<li>sudo chown prometheus:prometheus /usr/local/bin/promtool
<li>cp -r prometheus-2.17.1.linux-amd64/consoles /etc/prometheus
<li>cp -r prometheus-2.17.1.linux-amd64/console_libraries /etc/prometheus
<li>chown -R prometheus:prometheus /etc/prometheus/consoles
<li>chown -R prometheus:prometheus /etc/prometheus/console_libraries
<li>chown prometheus:prometheus /etc/prometheus/prometheus.yml
<li>sudo nano /etc/systemd/system/prometheus.service
</ul>
</pre>

2. Selanjutnya di ansible buat 4 buah reverse proxy yang nantinya akan dicopy melalui ansible ke folder nginx yang berada di public server 

<img src="/week4/assets/9.png">

3. Kemudian buat file yml ansible untuk mengcopy file-file tersebut ke folder nginx.

<img src="/week4/assets/10.png">

4. Selanjutnya lakukan SSL terhadap domain monitoring server. Disini saya masih melakukan instalasi certbot & pemasangan SSL secara manual tanpa menggunakan ansible.

<img src="/week4/assets/11.png">
