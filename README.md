# Frontend Masters : Fullstack Frontend v2

Repository ini adalah rangkuman dari course Frontend Masters dengan judul Fullstack Frontend v2 
yang dibawakan oleh Jem Young https://frontendmasters.com/courses/fullstack-v2/. Jem Young adalah seorang Senior Software Engineer di Netflix.

<br/><br/>

## BAB 1: Pengenalan
### Apa itu Fullstack ?
Arti `fullstack` sendiri sampai sekarang masih dapat diperdebatkan, karena realitanya adalah manusia punya kelebihan dan punya kekurangan masing-masing. Ada yang lebih jago di Frontend, atau lebih jago di Backend, atau database, dan seterusnya. Sampai ada meme dari Bryan Holt (salah satu mentor di FrontendMasters juga), yang seperti ini : <br/>
![Screenshot from 2022-03-15 19-38-43](https://user-images.githubusercontent.com/26225791/158379386-6ebb3f68-f034-47e8-bc20-9a40fe70c449.png) 

Di gambar tersebut ada gambar kuda yang bagus di sebagian saja, namun bagian lainnya kurang bagus. <br/> <br/>
Namun, arti Fullstack yang sebenarnya adalah `Seseorang (Engineer/Programmer) yang dapat membuat aplikasi dari awal hingga akhir`.<br/><br/>

### Kenapa harus belajar Fullstack ?
Alasan dari belajar untuk menjadi Fullstack Engineer adalah untuk menjadi seorang engineer yang lebih baik lagi, karena kita akan paham cara kerja aplikasi dari awal hingga akhir.
<br/><br/>

### Pengenalan Command Line
Command Line adalah `perintah` yang kita inputkan ke terminal/cmd untuk mendapatkan suatu output yang kita inginkan. Command Line sangat bermanfaat untuk kita, bahkan kita bisa membuang mouse dari hadapan kita dan hanya mengandalkan Command Line saja. Command Line juga memiliki beberapa kelebihan lainnya, yaitu :
- Cepat
- Konsisten
- Mudah diautomasi

<br/>Berikut adalah Command Line yang paling sering digunakan di kehidupan sehari-hari: <br>
![Getting Started](https://cdn.discordapp.com/attachments/831441947549499406/953283939408158740/Screenshot_from_2022-03-15_20-29-39.png)


<br/>

### Shell
Shell atau Bash adalah aplikasi untuk menjalankan Command Line. di Linux, secara default terminal sudah menjalankan Bash atau Shell. Lalu, apa perbedaan Shell atau Bash dengan Terminal/cmd? perbedaannya, Terminal/cmd adalah aplikasi untuk menjalankan Bash, dan Bash adalah aplikasi untuk menjalankan Command Line yang akan dikirim ke sistem. <br/><br/>

## BAB 2: Memahami Internet
### Bagaimana Cara Kerja Internet ?
Pada dasarnya, internet adalah sebuah sistem yang terhubung secara global dan dapat berinteraksi satu sama lain dengan `request` dan `response`. Jadi sehari-hari, kita saling terhubung satu sama lain tanpa kita sadari. 

### IP Address & Protocol

- IP Address adalah sebuah label dari perangkat yang terhubung dengan internet, dan bertujuan untuk mengenali perangkat yang terhubung dengan internet. ada beberapa versi IP Address, beberapa versinya yaitu IPv4 dan IPv6. 
- Protocol yang digunakan untuk saling terhubung dari satu perangkat dengan perangkat yang lain ada 2 jenis, yaitu UDP (User Datagram Protocol) dan TCP (Transmission Control Protocol). Perbedaan mendasar dari TCP dan UDP adalah TCP membutuhkan ACK (Acknowledge) dan UDP tidak ada ACK, jadi UDP hanya mengirim data dari client ke server tanpa mengetahui apakah data yang diterima client sudah sesuai atau belum.

### Packets
Packet adalah sebuah informasi yang paling kecil yang dapat dikirim. Packet dapat diumpamakan seperti sebuah amplop yang berisi `beberapa data` yang akan dikirim.

### Penekanan Cara Kerja Internet
Internet berjalan menggunakan Protocol `TCP/IP`, lalu Internet mengirimkan `Packet` yang berisi data yang akan dikirim dari IP Address pengirim ke IP Address penerima, dan semua berjalan dengan `kepercayaan`. 

<br><br>

## BAB 3: Server
### VIM (Vi Improved) & Modes
- Vim adalah sebuah text editor yang biasa digunakan untuk menulis program. Vim sering digunakan programmer untuk mengedit file yang ada di Server, karena lebih baik dari Nano (text editor sejenis Vim). <br>
- Vim ada 3 jenis Mode: Insert Mode (Text Editing), Command Mode (Primary Mode), Last Line Mode (Searching, Saving, Editing). cara untuk masuk kedalam tiap mode adalah dengan menekan huruf `i` pada keyboard untuk Insert Mode, kemudian `ESC` untuk Command Mode, dan `:` untuk Last Line Mode.

### Apa Tugas dari Server ?
Tugas server adalah sederhana, yaitu menyajikan konten. Setiap ada request data dari Client (pengguna atau user), maka Server akan langsung menyajikan data sesuai dengan request dari Client. Semua perangkat yang bisa terhubung ke internet bisa dijadikan server (Laptop, HP, IoT Device, dll.). <br>

### Data Center & The Cloud
Data Center tempat dari beberapa server yang ditumpuk agar dapat meng-handle request dengan efisien. `Cloud Computing` sebenarnya hanyalah panggilan untuk menyewa server dari penyedia layanan server, karena servernya tidak bisa kita lihat secara langsung dan berjalan layaknya di awan, maka dari itu disebut `Cloud`.

### VPS (Virtual Private Server)
Virtual Private Server adalah Server virtual yang bisa kita gunakan dari penyedia layanan Cloud. VPS sebenarnya adalah sebuah potongan dari sebuah sistem Server, namun dapat kita gunakan `layaknya` Server biasa.

### OS (Operating System) <br>
OS pada server mempunyai dua tipe, yaitu Linux dan Windows. berikut adalah diagram turunan dari tiap OS :
![Getting Started](https://cdn.discordapp.com/attachments/831441947549499406/953345899327803392/Screenshot_from_2022-03-16_00-36-01.png)

<br>
berikut adalah prinsip kerja dari Linux : <br>

![Diagram Linux](https://cdn.discordapp.com/attachments/831441947549499406/953349781852401695/Screenshot_from_2022-03-16_00-51-06.png) <br>
Kernel adalah layer yang berkomunikasi dengan hardware (CPU, RAM, dll.), kemudian Utilities adalah aplikasi kecil yang dibuat untuk menjalankan satu tugas saja. Karena Utilities adalah app kecil, maka Utilities dapat diupdate tanpa membuat kernel bermasalah. 
Semua Utilities yang ada, nantinya akan berkomunikasi dengan kernel untuk menjalankan tugas yang diinginkan. 

<br>
berbeda dengan Windows yang tidak mempunyai Utilities dan membuat semuanya menjadi satu kesatuan. itulah sebabnya Windows update sangatlah menyebalkan. 

### SSH 
SSH adalah bagian dari keamanan, dan keamanan sangatlah penting untuk menghindari kejadian yang tidak diinginkan (dihack misalnya). Jem Young menjelaskan bahwa keamanan yang basic itu ada 2 cara, yaitu menggunakan SSH key, atau menggunakan username password. SSH adalah singkatan dari Secure Socket Shell, yang merupakan `key` yang sangat besar dan susah untuk dipecahkan, dan itu adalah cara yang lebih aman untuk login ke server. <br> 
SSH terdiri dari 2 bagian, yaitu `public key` dan `private key`. <br>
![ssh](https://cdn.discordapp.com/attachments/831441947549499406/953415343408287844/Screenshot_from_2022-03-16_05-11-41.png)

<br>
<br>
cara kerjanya adalah sebagai berikut : <br>
private key akan menetap di local (komputer atau perangkat user), dan public key akan dikirim ke server. data yang dikirim ke server, semuanya akan ter-enkripsi dengan private key, jadi ketika ada data yang dikirim ke server, tidak ada yang tahu apa yang terjadi karena datanya telah terenkripsi dan hanya bisa didekripsi mengunakan private key dari user.

![carakerja ssh](https://cdn.discordapp.com/attachments/831441947549499406/953416369318285372/Screenshot_from_2022-03-16_05-16-04.png)

<br>
Walaupun tidak sepenuhnya aman, namun SSH adalah sistem keamanan terkuat untuk saat ini. Karena dapat mencegah terjadinya Man Of The Middle (atau disadap).

## BAB 4: Setup Server
### Membeli Domain
kita bisa membeli Domain dari manapun, Jem Young menyarankan untuk membeli di namecheap.com

### Setup Domain
Untuk setup domain, kita bisa menggunakan DigitalOcean untuk menambahkan domain yang telah dibeli, kemudian mengupdate nama server di penyedia Domain. <br>
![domain](https://cdn.discordapp.com/attachments/831441947549499406/953427678176886855/Screenshot_from_2022-03-16_06-01-00.png) <br>

### Setup Server
Hal yang perlu dilakukan untuk menyetup sebuah server adalah sebagai berikut: <br>
![setupserver](https://cdn.discordapp.com/attachments/831441947549499406/953428807354826812/Screenshot_from_2022-03-16_06-05-30.png) <br>

### Update & Upgrade Software 
caranya mudah, kita hanya perlu memasukkan command line berupa: <br>
```sudo apt update``` <br>
kemudian <br>
```sudo apt upgrade```  <br>
selesai. <br>
Tujuan dari mengupdate dan mengupgrade software sistem adalah untuk mencegah adanya vulnerability.

### Menambahkan User Baru
Untuk menambahkan user baru, kita hanya perlu memasukkan Command Line seperti ini : <br>
```add user {username yang ingin dibuat}```
<br> Tujuan dari menambahkan user baru adalah agar kita dapat mencegah untuk mengakses server menggunakan akses `root`.

### Menambahkan User Permission
berikut adalah langkah untuk menambahkan user permission di server <br>
![userpermission](https://cdn.discordapp.com/attachments/831441947549499406/953432203562450954/Screenshot_from_2022-03-16_06-18-17.png)

### Menonaktifkan Root User
Setelah menambahkan public key di server, kita harus logout dulu dari server menggunakan perintah `exit` yang diinputkan di command line. kemudian, login dengan User baru yang telah kita buat.
![nonaktifuser](https://cdn.discordapp.com/attachments/831441947549499406/953433017999851520/Screenshot_from_2022-03-16_06-22-14.png) <br>
Kemudian, kita tinggal mengubah hak akses dari file Public Key, lalu menonaktifkan login menggunakan akses root. <br>
![nonaktifroot](https://cdn.discordapp.com/attachments/831441947549499406/953433383327899658/Screenshot_from_2022-03-16_06-23-42.png)
<br>
untuk menonaktifkan login menggunakan root, kita perlu mengedit file `sshd_config` menjadi seperti ini : <br>

![sshdconfig](https://cdn.discordapp.com/attachments/831441947549499406/953433951815471134/Screenshot_from_2022-03-16_06-25-53.png) <br>

### Pengenalan Nginx
Nginx adalah salah satu web server yang cukup popular karena dapat dibilang salah satu web server yang cukup ringan dan cepat. Nginx dapat melakukan banyak hal, reverse proxy, web server, proxy server, caching, dan lain-lain. dan Jem Young (pemateri) sangat suka dengan software ini.

### Pengenalan NodeJS
NodeJS adalah sebuah engine untuk menjalankan Javascript, dan berjalan diatas V8 yang dikembangkan oleh google chrome. NodeJS bisa menghandle asynchronous dengan sangat baik. Untuk menginstall NodeJS sangatlah mudah, yaitu dengan cara: <br>
```sudo apt install nodejs npm```

### Version Control dengan Git
Git adalah alat yang digunakan untuk mengontrol versi dari sebuah aplikasi, bahkan kita bisa berkolaborasi untuk membangun sebuah aplikasi bersama orang banyak.

### Install Fail2ban
Fail2ban adalah aplikasi untuk mencegah orang yang hendak melakukan bruteforce (login secara paksa). cara kerjanya, Fail2ban akan mem-blacklist IP Address yang gagal login sebanyak 5x. Cara installnya ada di link berikut https://www.techrepublic.com/article/how-to-install-fail2ban-on-ubuntu-server-18-04/


## BAB 5: Dasar Penggunaan Bash
Jem Young pada bab ini menjelaskan tentang dasar-dasar penggunaan Bash, namun hanya beberapa saja. Saya menyarankan untuk melihat artikel yang lebih lengkap disini: <br> https://educative.io/blog/bash-shell-command-cheat-sheet

## BAB 6: Dasar Configurasi Nginx 
### Nginx Redirect
Nginx dapat melakukan redirect dari link domain kita, ke domain yang kita inginkan. caranya adalah buka file nginx.conf, lalu tambahkan command sebagai berikut: <br>
![redirect](https://cdn.discordapp.com/attachments/831441947549499406/953458722204712980/Screenshot_from_2022-03-16_08-03-24.png) <br>
perintah diatas adalah untuk me-redirect route /help ke link https://developer.mozilla.org/en-US

### Nginx Subdomain
Nginx juga dapat membuat subdomain, dengan menambahkan perintah di file nginx.conf : <br>
![subdomain](https://cdn.discordapp.com/attachments/831441947549499406/953459926334832650/Screenshot_from_2022-03-16_08-09-11.png)

### Kompresi File di Nginx
Nginx menggunakan jenis kompresi file berupa gzip.

## BAB 7: Keamanan

### Checklist Keamanan
Keamanan adalah hal yang penting dalam sebuah sistem aplikasi. maka dari itu, kita dapat meningkatkan keamanan dengan beberapa cara : <br>
- Selalu login ke server dengan menggunakan SSH
- menambahkan Firewall
- mengupdate software sistem
- 2 Factor Authentication
- VPN (Virtual Private Network)

### Unattended Upgrades
Unattended Upgrades adalah untuk mengupgrade software sistem. caranya adalah sebagai berikut: <br>
```sudo apt install unattended-upgrades```

### Firewall
Firewall adalah sebuah perangkat jaringan keamanan yang memonitor komunikasi yang masuk dan keluar, dan menentukan antara mengizinkan atau menolak traffic tersebut berdasarkan aturan keamanan yang telah diatur.

### Uncomplicated Firewall
Uncomplicated Firewall adalah aplikasi yang menyederhanakan command line dari `iptable`. beberapa contoh command line Uncomplicated Firewall adalah sebagai berikut : <br>
![ufw](https://cdn.discordapp.com/attachments/831441947549499406/953468361055035433/Screenshot_from_2022-03-16_08-41-07.png) <br>

## BAB 8: HTTP
### Pengertian HTTP
HTTP adalah singkatan dari Hypertext Transport Protocol, dan HTTP berjalan dengan menggunakan TCP/IP. 

### HTTP Headers & Cookies
HTTP Headers adalah informasi yang digunakan untuk mengirim informasi dari payload atau data yang dikirim atau diterima, berikut adalah contoh dari HTTP Headers:
![header](https://cdn.discordapp.com/attachments/831441947549499406/953472070010961940/Screenshot_from_2022-03-16_08-56-38.png)

<br>
Struktur Headers : <br>

![struktur](https://cdn.discordapp.com/attachments/831441947549499406/953475425395408966/Screenshot_from_2022-03-16_09-10-44.png)
<br><br>
Cookies adalah beberapa data berupa text yang akan bertahan di browser. Biasanya Cookie digunakan untuk mengambil data untuk meningkatkan User Experience dari suatu Website.

### HTTPS 
HTTPS adalah versi lebih aman dari HTTP. HTTPS menambahkan SSL (Secure Socket Layer) diatas HTTP, agar komunikasi bisa lebih aman.

### HTTP/2
HTTP/2 adalah versi HTTP yang telah support multiplexing, dan HTTP Headersnya telah dicompress untuk menghasilkan komunikasi yang lebih cepat. Versi HTTP ini adalah yang digunakan oleh banyak aplikasi di dunia saat ini.

### HTTP/3
HTTP/3 masih belum rilis secara resmi, namun ada beberapa perusahaan (google contohnya) sudah menerapkan teknologi ini. 
perbedaan yang paling mencolok dari HTTP/3 adalah, HTTP/3 berjalan menggunakan protocol UDP.

## BAB 9: Dasar Container
### Containers & Microservices
- Container adalah sebuah sistem sangat kecil yang hanya berisi library yang dapat menjalankan suatu aplikasi.
- Microservices adalah sebuah Service yang hanya dapat menangani satu tugas saja.

### Docker & Orchestration
Docker adalah aplikasi yang biasa digunakan untuk membuat Container, sedangkan Orchestration adalah sebuah sistem untuk mengendalikan banyak container dalam suatu Server, contoh Orchestration: Kubernetes, Docker Swarm, Amazon EKS, dll.

### Load Balancer
Load Balancer bertugas untuk mengatur resource yang dibutuhkan untuk mencegah server down. Nginx dapat digunakan juga sebagai load balancer, caranya adalah sebagai berikut: <br>
https://docs.nginx.com/nginx/admin-guide/load-balancer/http-load-balancer/


## BAB 10: Menyimpan Data
Cara sederhana untuk menyimpan data adalah dengan menyimpannya ke sebuah file. Namun, ketika kita mempunyai banyak transaksi dengan banyak perangkat, mengirim file sangatlah tidak efisien. Maka dari itu ada yang namanya DBMS (Database Management System) untuk menyimpan data secara efisien. <br>
### Tipe Database
Database memiliki dua tipe, relational (SQL) dan non-relational (No-SQL). tiap jenis mempunyai kelebihan dan kekurangannya masing-masing. Untuk relational database, kelebihannya adalah kita dapat mengatur struktur datanya seperti apa, jadi kita tidak perlu khawatir data yang disimpan tidak
sesuai dengan yang kita inginkan. Sebaliknya, Non-relational database tidak mempunyai struktur yang tetap, jadi kita bisa bebas menyimpan data dengan sesuka hati. 

### Redis 
Redis adalah aplikasi untuk Caching (menyimpan data sementara). cara installnya adalah sebagai berikut : <br>
![installredis](https://cdn.discordapp.com/attachments/831441947549499406/953503421430906971/Screenshot_from_2022-03-16_11-01-57.png)

### WebSockets
WebSockets bertugas untuk menjaga koneksi antar perangkat yang terhubung oleh internet agar tidak terganggu oleh apapun. WebSockets mendukung koneksi dua arah, dan multiplexed.

## BAB 11: Penutup
Kita telah belajar banyak hal dari apa yang dijelaskan oleh Jem Young dalam course Fullstack Frontend v2 ini, dari cara kerja internet hingga menyimpan data di server. Saya harap rangkuman dari course ini dapat bermanfaat untuk kita semua.. <br>
Terima kasih telah membaca! see you next time ^^