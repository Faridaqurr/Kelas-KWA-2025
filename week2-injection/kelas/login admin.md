# Login Admin - OWASP Juice Shop

>Kategori = Injection☠️

[login admin](http://localhost:3000/#/score-board?categories=Injection)

---

## Langkah-langkah pengerjaan
1. Mencari bagian menu **Login** untuk masuk ke akun
![Alt text](./gambar/admin-1.png)

2. Saat memasuki menu loginnya, kita diminta untuk melakukan SQL Injection dan disini saya menggunakan `' or 1=1 --` untuk dapat bypass login dan bebas untuk bagian passwordnya
![Alt text](./gambar/admin-2.png)

3. Setelah berhasil masuk ke akunnya, kita diminta untuk melanjutkan soalnya
![Alt text](./gambar/admin-3.png)

## Find and Fix

1. Disini menemukan bagian yang salah pada baris ke 15 di bagian input sql user nya karena rentan terkena injection sehingga memungkinkan adanya bypass seperti `' or 1=1 --`
![Alt text](./gambar/admin-4.png)

2. Disini membenarkan bagian yang salah dengan penambahan bagian **$1 dan $2** dengan tujuan memberikan tempat untuk inputan agar tidak langsung tergabung ke querynya
![Alt text](./gambar/admin-5.png)