# Database Schema - OWASP Juice Shop

>Kategori = Injection☠️

[database schema](http://localhost:3000/#/score-board?categories=Injection)

---

## Langkah-langkah pengerjaan
1. Menguji untuk menemukan skema databasenya, disini melakukan pencarian bebas yang kemudian di inspect
![Alt text](./gambar/ds-1.png)

2. Setelah dicari muncul bagian network yaitu `/search?q=` yang berisi endpoint `/rest/products/search?q=` untuk ditelusuri lebih lanjut
![Alt text](./gambar/ds-2.png)

3. Kemudian dilanjutkan dengan menjalankan url `http://localhost:3000/rest/products/search?q=` dengan ditambahkan `carrot'))--` untuk menjalankan query nya
![Alt text](./gambar/ds-3.png)

4. Dari hasil itu menambahkan payload `carrot')) UNION SELECT 1,2,3,4,5,6,7,8,9 FROM sqlite_master --` yang bisa digunakan untuk mengembalikan skema databasenya 
![Alt text](./gambar/ds-4.png)

5. Hasil dari pengembalian skema databasenya dan ditambahkan payload `carrot')) UNION SELECT sql,2,3,4,5,6,7,8,9 FROM sqlite_master --` untuk menampilkan isi databasenya
![Alt text](./gambar/ds-5.png)

6. Soal berhasil untuk diselesaikan
![Alt text](./gambar/ds-6.png)

## Find and Fix
1. Ditemukan pada baris ke 5 dimana query dibentuk langsung dari input user tanpa replacements/binding, sehingga rawan SQL injection dan bisa menyebabkan kebocoran data
![Alt text](./gambar/ds-7.png)

2. Perbaikan dilakukan dengan memanfaatkan fitur replacements agar input user tidak langsung dimasukkan ke query dengan begitu serangan SQL injection bisa dicegah dan akses ke database tetap aman
![Alt text](./gambar/ds-8.png)