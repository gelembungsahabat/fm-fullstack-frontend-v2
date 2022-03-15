# Frontend Masters : Fullstack Frontend v2

Repository ini adalah rangkuman dari course yang ada di Frontend Masters dengan judul Fullstack Frontend v2 
yang dibawakan oleh Jem Young. Jem Young adalah seorang Senior Software Engineer di Netflix.

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

