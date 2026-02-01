# 📄 Instalasi dan Setup Awal

> "Sebelum mulai balapan, kita harus punya mobilnya (Instalasi) dan mendaftarkan identitas pengemudinya (Konfigurasi). Tanpa identitas, Git tidak akan tahu siapa yang bertanggung jawab atas setiap baris kode yang ditulis."

---

## 🎯 Tujuan Pembelajaran
* Berhasil menginstal Git di berbagai sistem operasi (Windows, macOS, Linux).
* Mampu melakukan verifikasi apakah Git sudah terpasang dengan benar melalui terminal.
* Melakukan konfigurasi identitas global (`user.name` & `user.email`) sebagai tanda tangan digital.

---

## 💡 Pembahasan Inti

### 1. Cara Instalasi Git
Pilih metode instalasi sesuai dengan sistem operasi yang kamu gunakan saat ini:

* **Windows:** 1. Kunjungi [git-scm.com/downloads](https://git-scm.com/downloads).
    2. Download installer dan jalankan.
    3. Klik `Next` pada pilihan default (pilihan default sudah sangat optimal untuk pemula).
    4. Setelah selesai, kamu akan mendapatkan aplikasi bernama **Git Bash**.
* **macOS:**
    1. Buka Terminal bawaan Mac.
    2. Ketik `git --version`.
    3. Jika belum ada, sistem akan otomatis menawarkan instalasi *Xcode Command Line Tools*. Klik **Install**.
* **Linux (Ubuntu/Debian):**
    1. Buka Terminal.
    2. Ketik perintah: `sudo apt update && sudo apt install git -y`.

### 2. Verifikasi Instalasi
Setelah proses instalasi selesai, kita harus memastikan Git sudah "hidup" di dalam sistem. Buka Terminal atau Git Bash, lalu ketik:

```bash
git --version

```

Jika muncul teks seperti git version 2.x.x, berarti instalasimu sukses!

### 3. Konfigurasi Identitas
Ini adalah langkah paling krusial setelah instalasi. Git perlu tahu siapa yang membuat perubahan kode. Gunakan perintah berikut (ganti teks di dalam kutipan dengan datamu):

```Bash
git config --global user.name "Nama Lengkapmu"
git config --global user.email "emailkamu@example.com"
```

> "Tips: Gunakan email yang sama dengan yang kamu gunakan untuk mendaftar akun GitHub agar profilmu bisa menampilkan statistik kontribusi dengan benar."

## 🎭 Analogi Dunia Nyata: Tanda Tangan Kontrak
Bayangkan kamu sedang mengerjakan proyek pembangunan gedung (proyek kodingan). Setiap kali kamu memasang batu bata atau mengubah desain, kamu wajib membubuhkan stempel atau tanda tangan:

* **`user.name`**: Adalah nama terangmu agar teman setim tahu siapa yang bekerja.
* **`user.email`**: Adalah ID unikmu agar sistem tidak tertukar dengan orang lain yang namanya mungkin mirip.

Tanpa konfigurasi ini, Git akan "menolak" ketika kamu mau menyimpan hasil kerjamu karena dia tidak tahu siapa yang bertanggung jawab atas perubahan tersebut.

---

## 📊 Cek Hasil Konfigurasi
Untuk memastikan datamu sudah tersimpan di sistem Git, gunakan tabel perintah berikut:

| Perintah                | Fungsi                                      |
| `git config --list`     | Melihat semua pengaturan Git yang aktif     |
| `git config user.name`  | Memastikan nama yang tersimpan sudah benar  |
| `git config user.email` | Memastikan email yang tersimpan sudah benar |

---

## ❓ Pertanyaan Umum (Q&A)
**T: Apa maksud dari flag `--global`?** **J:** Itu artinya pengaturan ini berlaku untuk **seluruh** proyek kodingan di laptopmu. Kamu tidak perlu mengetikkan nama dan email lagi setiap kali membuat folder proyek baru.

**T: Saya salah ketik nama, apakah bisa diubah?** **J:** Sangat bisa. Cukup ketik ulang perintah yang sama dengan nama yang benar. Git akan otomatis menimpa (*overwrite*) pengaturan yang lama.

---

## 📌 Ringkasan Poin Penting
* Gunakan `git --version` untuk mengecek keberhasilan instalasi.
* Konfigurasi `user.name` dan `user.email` adalah langkah wajib yang dilakukan satu kali setelah instalasi.
* Identitas ini akan melekat pada setiap "snapshot" (*commit*) yang kamu buat selamanya.

---

## ⏭️ Next Step
Sekarang mobil sudah siap dan driver sudah terdaftar secara resmi. Ayo kita mulai masuk ke babak praktek dan belajar cara membuat "Gudang" (Repository) pertama kita!

👉 **Lanjut ke folder Dasar Git: [Inisialisasi Repository (git init)](../02_Dasar_Git/01-workflow-tiga-area.md)**