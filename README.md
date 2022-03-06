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

#### HTTP Method
* [GET](https://github.com/ekasaputrayogi/HTTP-Tutorial#get)
* [POST](https://github.com/ekasaputrayogi/HTTP-Tutorial#post)
* [PUT](https://github.com/ekasaputrayogi/HTTP-Tutorial#put)
* [DELETE](https://github.com/ekasaputrayogi/HTTP-Tutorial#delete)
* [PATCH](https://github.com/ekasaputrayogi/HTTP-Tutorial#patch)
* [HEAD](https://github.com/ekasaputrayogi/HTTP-Tutorial#head)
* [OPTION](https://github.com/ekasaputrayogi/HTTP-Tutorial#option)
* [TRACE](https://github.com/ekasaputrayogi/HTTP-Tutorial#trace)

#### HTTPS
* HTTPS merupakan HTTP yang ter-enkripsi
* Enkripsi dilakukan oleh SSL (Secure Sockets Layer)
* web yang menggunakan HTTP akan ditulis http:// sedangak web yang menggunakan HTTPS akan ditulis https://

#### HTTP Terminology
* TCP, untuk melakukan koneksi pada HTTP
* IP, adress untuk identitas jaringan
* URL (Uniform Resource Locator), alamat dari sebuah resource web
![mdn-url-all.png](https://github.com/ekasaputrayogi/HTTP-Tutorial/blob/master/Gambar/mdn-url-all.png)
* DNS (Domain Name Server), tempat untuk menyimpan katalog pemetaan antara nama domain di URL menuju lokasi IP komputer
* Web Server, untuk menerima request dari client dan mengirim informasi pada client.

## GET
GET digunakan untuk melakukan REQUEST data. REQUEST menggunakan GET hanya untuk menerima data, bukan untuk mengirim data
Contoh:
'''
GET http://www.example.com/customers/12345
GET http://www.example.com/customers/12345/orders
'''
## POST
POST digunakan untuk mengirim data ke server. POST biasanya digunakan untuk mengirim data baru sehingga biasanya memiliki request body
Contoh:
'''
POST http://www.example.com/customers
POST http://www.example.com/customers/12345/orders
'''

## PUT
PUT digunakan untuk mengganti semua data yang terdapat di server dengan data baru yang dikirim di request
Contoh:
'''
PUT http://www.example.com/customers/12345
PUT http://www.example.com/customers/12345/orders/98765
'''
## DELETE
DELETE digunakan untuk menghapus data
Contoh:
'''
DELETE http://www.example.com/customers/12345
'''

## PATCH
PATCH digunakan untuk mengubah sebagian data
Contoh:
'''
PATCH http://www.example.com/customers/12345
PATCH http://www.example.com/customers/12345/orders/98765
'''
## HEAD
HEAD digunakan seperti GET, tapi tanpa membutuhkan response body

## OPTION
OPTION digunakan untuk mendeskripsikan opsi komunikasi yang tersedia

## TRACE
TRACE digunakan untuk melakukan debugging, response TRACE akan mengembalikan seluruh informasi yang dikirim oleh client

## HTTP MESSAGE
```
POST /login HTTP/1.1
Host: example.com
Connection: keep-alive
accept: application/json
User-Agent: Mozzila/5.0 (Macintosh; Intel Mac OS X 10_15_7)
Content-Type: application/json
Content-Length: 51

{"password": "rahasia", "username": "yogi"}
```
#### START LINE
```
POST /login HTTP/1.1
```
#### HTTP HEADER
* Host: Authority pada URL
* Content-Type: Tipe data dari HTTP Body
* User-Agent: Informasi user agent (seperti browser dan OS)
* Accept: Tipe data yang diterima oleh Client
* Authorization: Credential untuk autentikasi (misal usernam + password)
```
Host: example.com
Connection: keep-alive
Accept: application/json
User-Agent: Mozzila/5.0 (Macintosh; Intel Mac OS X 10_15_7)
Content-Type: application/json
Content-Length: 51
```
#### HTTP BODY
```
{"password": "rahasia", "username": "yogi"}
```
#### HTTP STATUS
HTTP Status merupakan kode HTTP Response yang memberi informasi kepada client
* Informational Response (100-199)
* Succesfull Response (200-299)
* Redirect (300-399)
* Client Error (400-499)
* Server Error (500-599)

#### CARA MELIHAT HTTP REQUEST DAN RESPONSE PADA BROWSER
* Tekan ctrl + shift + C
* klik network
![browser1.png](https://github.com/ekasaputrayogi/HTTP-Tutorial/blob/master/Gambar/browser1.png)
