# Git Branch dan Merge Pada CLI

---

#### Git Branch & Merge

Sebelum belajar lebih jauh kita rekap sebentar dari istilah git yang sudah dipelajari yakni :

- **Branch** => Merupakan cabang bebas dari cabang utama/master. Hal ini bertujuan membuat cabang baru tanpa mempengaruhi cabang utama

- **Merge** => Menggabungkan branch kedalam salah satu cabang ataupun cabang utama

#### Command CLI Git Branch

Rekap sejenak //

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

#### Git Merge

Lalu bagaimana kita menggabungkan branch bebas kedalam branch utama ?. Maka dalam hal kita bisa melakukannya dengan sintaks sebagai berikut

```bash
git merge 'nama branch'
```

Dan sebelum melakukan merge kita harus checkout/pindah kedalam branch master/utama

Sebelum melakukan merge kita harus tau dulu jenis-jenis merge, Diantaranya yakni :

1. **Fast Forward** => Terjadi ketika branch yang ingin dimerge berada dijalur langsung / *direct path*

2. **Three-way Merge** => Terjadi ketika ingin melakukan merge branch kedalam master akan tetapi tidak ada *direct path*. Jadi saat di merge ia juga melakukan commit sendiri.

Untuk mengetahui branch mana yang sudah di merge kita bisa menambahkan sintaks berikut :

```bash
git branch --merged
```

Lalu untuk menghapus branch bisa menggunakan sintaks berikut

```bash
git branch -d 'nama branch'
```

script diatas akan berfungsi apabila status branch terkait sudah dimerge, namun apabila ingin menghapus secara paksa walau belum di merge bisa menggunakan sintaks berikut :

```bash
git branch -D 'nama branch'
```

Letak perbedaan ada di parameter terkait.

Created by justnotiyann
