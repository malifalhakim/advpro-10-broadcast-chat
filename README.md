## 2.1. Original code of broadcast chat

![alt text](image.png) ![alt text](image-1.png) ![alt text](image-2.png) ![alt text](image-3.png)

Berdasarkan gambar-gambar diatas, dijalankan sebuah server dan tiga buah client. Server dijalankan dengan menggunakan perintah `cargo run --bin server`, sementara client dijalankan dengan perintah `cargo run --bin client`. Saat salah satu client mengirimkan pesan ke server, maka pesan tersebut akan diteruskan atau di-*broadcas* ke semua client yang terkoneksi pada server yang sama. Client yang menerima pesan broadcast akan menerima pesan dengan pola "From server: {isi pesan}". 