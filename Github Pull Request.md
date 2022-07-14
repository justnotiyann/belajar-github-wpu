# Pull Request / Remote Branch

---

**Pendahuluan**

**Pull request** => Suatu kejadian dimana kita memberikan masukkan atau code kedalam repo seseorang. Jadi intinya disini proses kolaborasi code berlangsung

Pada Rangkuman kali ini kita akan berfokus pada bagaimana proses pull request dari repo/branch yang kita miliki

Pull request sendiri merupakan fitur dari github

**Isi**

Untuk melakukan sinkronisasi antara repo local dan repo cloud kita bisa gunakan perintah git fetch, sintaksnya

```bash
git fetch
```

Jadi skenario saat ini adalah kita mempunyai 3 repo

1. Repo master kita

2. Repo local

3. Repo fork / Code orang lain



**Catatan :**

- Untuk membuat pull request sebaiknya kita membuat branch baru, jadi bukan master branch yang kita pull request. Jadi yang menerima pull request menerima branch kita

- Branch master akan selalu sinkron dengan repo asli pemilik. Jadi kita lakukan experimental dalam branch baru


