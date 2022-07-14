# Git Merge Conflict & Cara kembali ke commit Terdahulu

---

#### Pengertian Merge Conflict

**Merge Conflict** terjadi apabila terdapat kesamaan antara baris tertentu dalam code/file kita. Jadi kita harus fix secara manual untuk memilih mau menggunakan baris code yang mana.

#### Cara Kembali ke Commit terdahulu

Kita cek dahulu commit yang sudah dibuat dengan menggunakan perintah 

```bash
git log
```

Kemudian pilih salah satu commit dan ambil 7 digit angka awalan checkoutnya. Sebagai contoh

![](/home/iyan/.config/marktext/images/2022-07-14-17-46-43-image.png)

Lalu apabila sudah diketahui digit angkanya kita bisa langsung melakukan checkout dengan cara

```bash
git checkout '7 digit awal'
```

Apabila kita tetap berada pada commit tersebut dan ingin menambahkan branch baru maka kita harus melakukan checkout dan commit 

```bash
git checkout '7 digit awal'
git branch 'nama branch baru'
```

Lalu tinggal checkout ke branch yang baru dibuat dengan cara

```bash
git checkout 'nama branch baru'
```

Created by @justnotiyann
