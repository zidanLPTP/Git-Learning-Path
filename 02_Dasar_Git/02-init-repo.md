# 📄 Inisialisasi Repository (git init)

> "Setiap perjalanan seribu mil dimulai dengan satu langkah. Di dunia Git, langkah itu adalah `git init`. Perintah ini mengubah folder biasa menjadi markas besar yang memiliki mesin waktu."

---

## 🎯 Tujuan Pembelajaran

* Memahami cara mengubah folder proyek biasa menjadi repository Git.
* Mengetahui fungsi dan pentingnya folder rahasia `.git`.
* Mampu memulai manajemen versi pada proyek lokal secara mandiri.

---

## 💡 Pembahasan Inti

### 1️. Apa Itu `git init`?

`git init` adalah perintah pertama yang dijalankan saat memulai sebuah proyek baru menggunakan Git. Perintah ini memberi tahu Git untuk mulai memantau setiap perubahan yang terjadi di dalam folder tersebut.

Tanpa proses inisialisasi ini, sebuah folder hanyalah folder biasa yang **tidak memiliki kemampuan version control**.

---

### 2️. Cara Eksekusi `git init`

Masuk ke folder proyek menggunakan **Terminal** atau **Git Bash**, lalu jalankan perintah berikut:

```bash
git init
```

Jika berhasil, Git akan menampilkan pesan bahwa sebuah repository baru telah dibuat.

---

### 3️. Folder Rahasia `.git`

Setelah perintah `git init` dijalankan, Git akan membuat sebuah folder tersembunyi bernama:

```
.git
```

#### Isi Folder `.git`

Folder ini adalah **jantung repository Git**, yang berisi:

* Database internal Git
* Konfigurasi repository
* Seluruh riwayat *snapshot* (commit)

#### ⚠️ Aturan Emas

* **Jangan pernah** mengedit isi folder `.git` secara manual
* **Jangan menghapus** folder `.git`

Jika folder ini terhapus, maka:

> Seluruh riwayat commit dan mesin waktu Git akan **hilang permanen**

---

## 🎭 Analogi Dunia Nyata: Memasang Sistem CCTV

Bayangkan folder proyekmu adalah sebuah **gudang penyimpanan**.

Sebelum `git init`:

* Barang bisa keluar-masuk
* Tidak ada catatan perubahan
* Jika terjadi kehilangan, sulit dilacak

Setelah `git init`:

* Gudang dipasangi **sistem CCTV**
* Setiap pergerakan barang (perubahan kode) tercatat
* Ada ruang kontrol khusus (folder `.git`)
* Kamu bisa memutar ulang rekaman jika terjadi kesalahan

---

## ❓ Pertanyaan Umum (Q&A)

**T: Apakah saya harus menjalankan `git init` setiap kali menambah file baru?**
**J:** Tidak. `git init` hanya dijalankan **satu kali** di awal pembuatan proyek. Setelah itu, Git otomatis memantau semua file di dalam folder tersebut.

**T: Bolehkah menjalankan `git init` di folder yang sudah berisi file?**
**J:** Boleh. Semua file yang sudah ada akan dianggap sebagai **untracked files** dan siap untuk mulai dikelola oleh Git.

---

## 📌 Ringkasan Poin Penting

* `git init` mengubah folder biasa menjadi **Git Repository**
* Perintah ini membuat folder `.git` sebagai pusat data Git
* Dilakukan **satu kali** di awal proyek

---

## ⏭️ Next Step

Repository sudah siap, tapi bagaimana cara melihat kondisi file dan perubahan yang terjadi?

 **Lanjut ke:[Cek Status dan Log ](03-status-log.md)**

