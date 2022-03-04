## DEFINISI
* HTTP merupakan singkatan dari Hypertext Transfer Protocol
* HTTP merupakan protokol untuk melakukan transmisi hypermedia document seperti HTML, Javascript, CSS, Image, Audio, dll.

#### CLIENT & SERVER
* HTTP mengikuti arsitektur client dan server
* CLIENT mengirim HTTP REQUEST untuk meminta atau mengirim informasi ke server
* SERVER membalas dengan HTTP RESPONSE dari HTTP Request yang diterima
#### STATELESS
* HTTP Request merupakan request yang independent, tidak terikar dengan request sebelum atau sesudahnya
* HTTP Request tidak harus dilakukan dalam sequence, artinya client dapat melakukan request secara bebas tanpa ada aturan harus mulai dari mana
#### Session
* HTTP memiliki fitur bernama HTTP Cookie
* HTTP Cookie berfungsi untuk menyimpan informasi yang diberikan oleh server
#### HTTP Version
###### HTTP/1.1 vs HTTP/2
* HTTP/1.1 merupakan fallback protocol, Web Browser secara default akan menggunakan HTTP/2. Jika Web Server tidak mendukung HTTP/2, makan Web Browser akan menggunakan HTTP/1.1
* HTTP/1.1 dan HTTP/2 secara garis besar sama, hanya pada HTTP/2 Request yang dikirimkan dalam bentuk text diubah menjadi binary sehinggan lebih cepat dibandingkan HTTP/1.1
* HTTP/2 menggunakan algoritma kompresi sehingga request menjadi lebih ringan dan HTTP/2 mendukung multiplexing sehingga dapat mengirim beberapa request dalam satu connection yang sama

#### SYNTAX
* [GET]
* [POST]
* [PUT]
* [DELETE]
* [HEAD]
* [OPTION]

#### HTTPS
* HTTPS merupakan HTTP yang ter-enkripsi
* Enkripsi dilakukan oleh SSL (Secure Sockets Layer)
* web yang menggunakan HTTP akan ditulis http:// sedangak web yang menggunakan HTTPS akan ditulis https://

#### HTTP Terminology
* TCP, untuk melakukan koneksi pada HTTP
* IP, adress untuk identitas jaringan
* URL (Uniform Resource Locator), alamat dari sebuah resource web
* DNS (Domain Name Server), tempat untuk menyimpan katalog pemetaan antara nama domain di URL menuju lokasi IP komputer
* Web Server, untuk menerima request dari client dan mengirim informasi pada client.