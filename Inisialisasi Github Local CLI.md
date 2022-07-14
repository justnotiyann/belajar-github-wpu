## Belajar Inisialisasi Github CLI Linux Ubuntu

---

#### **Instalasi**

Untuk instalasi Git CLI untuk linux (disini saya menggunakan ubuntu) dapat menggunakan sintaks berikut 

```bash
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh
```

Untuk dokumentasi resmi : [Dokumentasi Resmi Install Git](https://github.com/cli/cli/blob/trunk/docs/install_linux.md)



#### **Melakukan Remote Repository pada Github**

Sebelumnya kita dapat langsung remote pada github ke local menggunakan email dan password, akan tetapi kebijakkan baru dari github mengharuskan kita menggunakan PAT (**Personal Acces Token**) berita selengkapnya dapat dilihat [disini]([Token authentication requirements for Git operations | The GitHub Blog](https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/)). Efek dari penggunaan PAT maka kita harus menginisialisasi Token kita sendiri dengan cara sebagai berikut :

1. Verifikasi email terlebih dahulu

2. Lalu klik bagian profile kemudian masuk pada bagian setting

3. Pada sebelah kiri sidebar pilih menu **Developer Setting**

4. Lalu pada sebelah kiri sidebar pilih tab **Personal Acces Token**

5. Kemudian pilih **generate new token**

6. Berikan nama untuk token tersebut

7. Masukkan mau berapa lama aktif token tersebut

8. Pilih scope/jangkauan untuk token tersebut. Kalo disini saya centang semua 

9. Lalu jika selesai klik **generate token**

10. Oke token sudah dibuat harap simpan dengan hati-hati karena token tersebut password untuk melakukan remote pada repo kita



Dokumentasi Resmi : [Cara Membuat Token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)



**Menggunakan Token**

Setelah mendapatkan token kita bisa menggunakan untuk remote repo dengan sintaks sebagai berikut :

```bash
git clone https://github.com/username/repo.git
Username: your_username
Password: your_token
```

Referensi : [Dokumentasi Resmi](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)



Agar dapat otomatis tanpa harus mengulangi memasukkan username dan password terus menerus kita dapat menyimpan token tersebut dalam bentuk cache dengan menambahkan sintaks berikut 

```bash
git config --global credential.helper cache
```

Perlu diingat cache tersebut menyimpan token selama masa aktif token tersebut masih ada, apabila sudah habis masa berlaku kita dapat menghapus token tersebut dengan cara

```bash
git config --global --unset credential.helper
git config --system --unset credential.helper
```

referensi : [Referensi Menggunakan Token](https://itsmycode.com/support-for-password-authentication-was-removed-github/)



Cara cepat menggunakan bisa dengan sintaks berikut :

```bash
git clone https://<tokenhere>@github.com/<user>/<repo>.git
```

Referensi : [Referensi Stackoverflow](https://stackoverflow.com/questions/68775869/message-support-for-password-authentication-was-removed-please-use-a-personal)



Demikianlah tulisan singkat rangkuman instalisasi git pada device local kita.

Created by <mark>Muhammad Fitrian</mark>
