# NetPro7 - Tugas 7 Networking Programming
## Anggota Kelompok:
#### Meilyand Evriyan Timor  1301161769
#### Reyhan Rahmansyah       1301160805
#### Reno Butar Butar        1301164724


## Secure Web Server Design
### Finite State Machine Web Server
<p align="center">
  <img src="https://github.com/Meilyand/NetPro7/blob/master/fsmHTTPS.png">
</p>

### Cara Kerja
Berdasarkan dari diagram FSM diatas. Berikut cara kerja dari web server yang kami rancang:

* Browser meminta data web page kepada server, maka instruksi permintaan data oleh
browser tersebut akan dikemas di dalam TCP yang merupakan protokol transport dan dikirim
ke alamat yang dalam hal ini merupakan protokol berikutnya yaitu HTTPS.

* Data yang diminta dari browser ke web server disebut dengan HTTPS request kemudian akan
dicarikan oleh web server di dalam data server. Jika ditemukan, data tersebut akan dikemas
oleh web server dalam TCP dan dikirim kembali ke browser untuk ditampilkan.

* Data yang dikirim dari server ke browser disebut dengan HTTPS response. Jika data yang
diminta oleh browser tersebut tidak ditemukan oleh web server, maka web server akan
menolak permintaan tersebut dan browser akan menampilkan notifikasi Page Not Found atau
Error 404.


## Secure Web Server Implementation
### Jalankan File main.go dengan command: _sudo go run main.go_
<p align="center">
  <img src="https://github.com/Meilyand/NetPro7/blob/master/implementasi_terminal.png">
</p>

### Ketik _https://localhost_ pada browser
<p align="center">
  <img src="https://github.com/Meilyand/NetPro7/blob/master/implementasi_browser.png">
</p>

Warning NET::ERR_CERT_AUTHORITY_INVALID muncul karena mengakses sebuah website
menggunakan protokol https yang dimana website ini menggunakan self-signed certificate, bukan
menggunakan certificate yang sudah diverifikasi oleh CA.
