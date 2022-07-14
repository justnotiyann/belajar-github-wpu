# Git Branch dan Merge Pada CLI

---

#### Git Branch & Merge

Sebelum belajar lebih jauh kita rekap sebentar dari istilah git yang sudah dipelajari yakni :

- **Branch** => Merupakan cabang bebas dari cabang utama/master. Hal ini bertujuan membuat cabang baru tanpa mempengaruhi cabang utama

- **Merge** => Menggabungkan branch kedalam salah satu cabang ataupun cabang utama

#### Command CLI Git Branch dan Merge

Rekap sebenetar //

 Apabila status dari file tersebut *modified* kita dapat melakukan commit secara langsung dengan menambahkan parameter -a, sintaksnya sebagai berikut

```bash
git commit -am 'pesan commit'
```

Lalu bagaimana dengan sintaks membuat branch dalam CLI ?.Kita dapat melakukan dengan sebagai berikut :

```bash
git branch 'nama branch'
```

Setelah membuat branch kita dapat melihat daftar branch yang ada dengan sintaks sebagai berikut :

```bash
git branch
```

Kemudian apabila ingin berpindah kesalah satu branch kita bisa menggunakan perintah **checkout** :

```bash
git checkout 'nama branch'
```

Catatan

- **git checkout** => Biasanya digunakan untuk berpindah dari satu branch ke branch lainnya. Perintah ini juga bisa digunakan untuk berpindah ke commit sebelumnya.



Untuk melihat kita berada dalam branch mana, kita bisa melihat posisi **HEAD** ada disebelah mana. Contohnya sebagai berikut :

![](/home/iyan/.config/marktext/images/2022-07-14-12-04-11-image.png)

Pada gambar diatas saya berada dalam brach dev. dan dev branch ini berada dalam satu jalur dengan branch utama/master branch.


