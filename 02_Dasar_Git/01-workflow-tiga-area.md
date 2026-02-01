# 📄 Alur Kerja Git: Three States (Tiga Area)

> "Memahami Git bukan sekadar menghafal perintah, tapi memahami 'perjalanan' sebuah file. Ada tempat untuk mengedit, ada tempat untuk mengemas, dan ada tempat untuk menyimpan selamanya."

---

## 🎯 Tujuan Pembelajaran
* Memahami konsep **Three States** (Working Directory, Staging Area, dan Repository).
* Mengenal siklus hidup file di dalam Git.
* Mengetahui kapan sebuah file dianggap "aman" oleh Git.

---

## 💡 Pembahasan Inti

Dalam Git, sebuah file akan melewati tiga area utama sebelum akhirnya tersimpan secara permanen dalam sejarah proyek. Memahami alur ini akan mencegahmu dari kebingungan seperti: *"Kenapa file saya sudah diedit tapi tidak muncul di daftar commit?"*

### 1. Working Directory (Area Kerja)
Ini adalah folder proyek yang kamu lihat di File Explorer atau VS Code. Di sini kamu bebas menambah, mengedit, atau menghapus kode. Status file di sini disebut sebagai **Modified** (sudah diubah tapi belum ditandai untuk disimpan).

### 2. Staging Area / Index (Area Persiapan)
Anggap saja ini sebagai "keranjang belanja". Kamu memilih file mana saja dari Working Directory yang ingin kamu masukkan ke dalam daftar simpan. Kamu menggunakan perintah `git add` untuk memindahkan file ke area ini. Statusnya berubah menjadi **Staged**.

### 3. Local Repository / .git (Area Penyimpanan)
Setelah yakin dengan daftar file di Staging Area, kamu melakukan "Checkout" atau penguncian dengan perintah `git commit`. Git akan mengambil potret (snapshot) dari file-file tersebut dan menyimpannya secara permanen di folder `.git`. Status filenya menjadi **Committed**.

---

## 🎭 Analogi Dunia Nyata: Sesi Pemotretan (Photoshoot)

Agar lebih mudah dibayangkan, mari gunakan analogi seorang fotografer:

1.  **Working Directory (Ruang Ganti):** Model sedang mencoba berbagai baju, berganti gaya, dan merias diri. Banyak perubahan terjadi, tapi belum ada foto yang diambil.
2.  **Staging Area (Panggung):** Fotografer memanggil model untuk berdiri di depan latar belakang. Hanya model yang berdiri di panggung inilah yang akan masuk ke dalam frame foto.
3.  **Repository (Hasil Foto):** Fotografer menekan tombol *shutter* (Klik!). Gambar tersimpan di kartu memori. Itulah **Commit**. Kamu punya bukti permanen tentang kondisi model pada saat itu.

---

## ❓ Pertanyaan Umum (Q&A)

**T: Kenapa harus ada Staging Area? Kenapa tidak langsung simpan saja?**
**J:** Agar kamu punya kendali penuh. Kadang kamu mengedit 5 file, tapi hanya ingin menyimpan 2 file dulu karena yang 3 lainnya belum selesai. Staging Area memungkinkan kamu memilih perubahan secara spesifik.

**T: Apakah saya bisa membatalkan file yang sudah masuk Staging Area?**
**J:** Bisa banget. Git menyediakan perintah untuk mengeluarkan file dari keranjang (Unstage) tanpa menghapus perubahan kodenya.

---

## 📌 Ringkasan Poin Penting
* **Working Directory:** Tempat kamu mengetik kode (status: *Modified*).
* **Staging Area:** Tempat kamu memilih kode (status: *Staged*).
* **Repository:** Tempat kode tersimpan aman (status: *Committed*).
* Alur standarnya adalah: **Edit** -> `git add` -> `git commit`.

---

## ⏭️ Next Step
Sekarang kamu sudah paham konsep areanya. Yuk, kita mulai praktek dengan membuat "Gudang" pertama kita menggunakan perintah inisialisasi!

👉 **Lanjut ke: [Inisialisasi Repository (git init)](02-init-repo.md)**