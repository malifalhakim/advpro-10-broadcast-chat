## 2.1. Original code of broadcast chat

![alt text](image.png) ![alt text](image-1.png) ![alt text](image-2.png) ![alt text](image-3.png)

Berdasarkan gambar-gambar diatas, dijalankan sebuah server dan tiga buah client. Server dijalankan dengan menggunakan perintah `cargo run --bin server`, sementara client dijalankan dengan perintah `cargo run --bin client`. Saat salah satu client mengirimkan pesan ke server, maka pesan tersebut akan diteruskan atau di-*broadcas* ke semua client yang terkoneksi pada server yang sama. Client yang menerima pesan broadcast akan menerima pesan dengan pola "From server: {isi pesan}". 

## 2.2. Modifying the websocket port

![alt text](image-4.png) ![alt text](image-5.png) ![alt text](image-6.png) ![alt text](image-7.png)

Pada gambar diatas, port pada client dan server diatur sama. Hasilnya program berjalan dengan normal seperti sebelumnya.

![alt text](image-9.png)![alt text](image-8.png)

Akan tetapi, jika port pada client dan server berbeda, misalnya hanya karena mengganti port pada client, maka akan terjadi error pada client. Hal ini karena tidak ada koneksi yang bisa dilakukan oleh client pada websocket connection yang telah ditetapkan. Hal ini akan menghasilkan program *crash* seperti gambar diatas.