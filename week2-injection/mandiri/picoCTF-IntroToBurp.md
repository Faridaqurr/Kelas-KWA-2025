# IntroToBurp - PicoCTF

### Detail Informasi
Kategori = Web Exploitation🖥️

Level = Easy🟢

[IntroToBurp](https://play.picoctf.org/practice/challenge/419?category=1&page=1)

![Alt text](./gambar/ITB-1.png)
## Langkah-langkah pengerjaan
1. Menuju web yang terdapat di link challange nya dan isi seperti pada gambar ini untuk mencoba masuk
![Alt text](./gambar/ITB-2.png)

2. Masukkan random kode OTP
![Alt text](./gambar/ITB-3.png)

3. Hasilnya nanti akan invalid dan bisa beralih ke burp suite untuk cek endpoint yang muncul
![Alt text](./gambar/ITB-4.png)

4. Muncul endpoint /dashboard dengan metode **POST** pada burp suite nya
![Alt text](./gambar/ITB-5.png)

5. Hapus bagian `otp` dan send, maka akan muncul response yang menampilkan flag nya
![Alt text](./gambar/ITB-6.png)