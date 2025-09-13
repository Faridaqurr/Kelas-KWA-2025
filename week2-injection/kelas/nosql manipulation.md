# nosql manipulation - OWASP Juice Shop

>Kategori = Injection☠️

[nosql manipulation](http://localhost:3000/#/score-board?categories=Injection)

---

## Langkah-langkah pengerjaan
1. Memasukkan review random ke item random
![alt text](./gambar/nm-1.png)

2. Ternyata review yang sudah di submit dapat di edit
![alt text](./gambar/nm-2.png)

3. Saat mengecek endpoint yang muncul di burp suite terdapat endpoint menggunakan **PATCH** untuk mengupdate review nya
![alt text](./gambar/nm-3.png)

4. Saat di repeater dapat langsung mengupdate massagenya, disini saya update jadi `cihuyyy` dan setelah di send review berhasil terupdate
![alt text](./gambar/nm-4.png)

## Find and Fix
1.
![alt text](./gambar/nm-5.png)

2.
![alt text](./gambar/nm-6.png)