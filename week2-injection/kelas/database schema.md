# Database Schema - OWASP Juice Shop

### Detail Informasi
---
Kategori = Injection☠️

[Database Schema](http://localhost:3000/#/score-board?categories=Injection)

## Langkah-langkah pengerjaan
1. Menguji untuk menemukan skema databasenya, disini melakukan pencarian bebas yang kemudian di inspect
![Alt text](./gambar/ds-1.png)

2. Setelah dicari muncul bagian network yaitu `/search?q=` yang berisi endpoint `/rest/products/search?q=` untuk ditelusuri lebih lanjut
![Alt text](./gambar/ds-2.png)

3. Kemudian dilanjutkan dengan menjalankan url `http://localhost:3000/rest/products/search?q=` dengan ditambahkan `carrot'))--` untuk menjalankan query nya
![Alt text](./gambar/ds-3.png)

4. Dari hasil itu bisa disiapkan payload yang bisa digunakan untuk mengembalikan skema databasenya 
![Alt text](./gambar/ds-4.png)

5. Hasil dari pengembalian skema databasenya
![Alt text](./gambar/ds-5.png)

6. Soal berhasil untuk diselesaikan (solve)
![Alt text](./gambar/ds-6.png)

## Find and Fix
1. 
![Alt text](./gambar/ds-7.png)

2.
![Alt text](./gambar/ds-8.png)