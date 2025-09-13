# Christmas Spesial - OWASP Juice Shop

>Kategori = Injection☠️

[christmas spesial](http://localhost:3000/#/score-board?categories=Injection)

---

## Langkah-langkah pengerjaan
1. Dari endpoint yang di dapat dari challange sebelumnya saya mencoba bypass dengan menambahkan `%'))+--` setelah endpoint `/rest/products/search?q=`
![Alt text](./gambar/cs-2.png)
![Alt text](./gambar/cs-3.png)

2. Dari response yang muncul, cari keyword **"Christmas"** dengan id nya 10
![Alt text](./gambar/cs-4.png)

3. Lalu pada halaman juice-shop nya bisa menambahkan item random dan cek bucket ikon-nya maka di request nya akan muncul endpoint dan send to repeater
![Alt text](./gambar/cs-5.png)

4. Pada bagian productid ganti menjadi 10
![Alt text](./gambar/cs-6.png)

5. Item christmas akan muncul di bucket dan bisa di checkout untuk solve challange nya
![Alt text](./gambar/cs-7.png)

6. Brhasil solve challange
![Alt text](./gambar/cs-8.png)