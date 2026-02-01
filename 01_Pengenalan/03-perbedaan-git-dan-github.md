# 📄 Perbedaan Git dan GitHub

> "Jangan sampai tertukar: Git adalah **alatnya**, sedangkan GitHub adalah **tempat penyimpanannya**. Seperti punya kamera (Git) tapi tidak punya galeri online (GitHub) untuk memamerkan fotonya."

---

## 🎯 Tujuan Pembelajaran
* Mampu membedakan peran spesifik antara Git dan GitHub.
* Memahami hubungan ketergantungan antara keduanya.
* Mengetahui bahwa Git bisa digunakan tanpa GitHub, tapi tidak sebaliknya.

---

## 💡 Pembahasan Inti

### Analogi Paling Gampang
Untuk membedakan keduanya secara instan, gunakan analogi benda yang kita pakai sehari-hari:

1. **Video Editor (Git) vs YouTube (GitHub)**
   Kamu bisa mengedit video di laptopmu pakai aplikasi (Git) tanpa butuh internet. Tapi kalau mau orang lain menonton videomu, kamu harus mengunggahnya ke platform online (GitHub).
2. **Kamera (Git) vs Instagram (GitHub)**
   Kamera berfungsi memotret momen (snapshot). Instagram berfungsi menyimpan foto tersebut agar bisa dilihat, di-like, dan dikomentari orang lain.

### Kenapa Orang Sering Bingung?
Kebingungan terjadi karena saat kita menggunakan GitHub, kita **wajib** menggunakan perintah Git. GitHub hanyalah sebuah "bungkus" visual yang cantik agar perintah-perintah Git yang rumit di terminal jadi lebih mudah dikelola secara tim.

---

## 📊 Tabel Perbandingan Head-to-Head

| Poin Perbedaan       | Git                              | GitHub                        |
| **Jenis**            | Software (VCS)                   | Layanan Berbasis Web          |
| **Instalasi**        | Harus diinstal di komputer lokal | Cukup akses lewat browser     |
| **Koneksi Internet** | **Offline** (Tidak butuh)        | **Online** (Wajib butuh)      |
| **Fungsi Utama**     | Mencatat riwayat perubahan file  | Hosting repo & kolaborasi tim |
| **Antarmuka**        | Command Line (Terminal/CLI)      | GUI (Web Dashboard)           |
| **Kompetitor**       | SVN, Mercurial                   | GitLab, Bitbucket             |

---

## 🎭 Skenario Penggunaan

### Kapan Kamu Hanya Butuh Git?
* Kamu mengerjakan proyek pribadi yang tidak ingin dibagikan ke siapa pun.
* Kamu hanya ingin punya cadangan (backup) jika suatu saat kodinganmu *error* dan ingin kembali ke versi sebelumnya.

### Kapan Kamu Butuh Keduanya?
* Kamu mengerjakan tugas kelompok (misal: proyek IEEE atau tugas kuliah).
* Kamu ingin membangun **Portfolio** agar bisa dilirik oleh HRD perusahaan IT.
* Kamu ingin berkontribusi ke proyek orang lain (*Open Source*).

---

## ❓ Pertanyaan Umum (Q&A)

**T: Bisakah saya pakai GitHub tanpa Git?**
**J:** Secara teknis, kamu bisa upload file manual lewat web GitHub (seperti Google Drive), tapi itu sangat tidak disarankan karena kamu kehilangan esensi "mesin waktu" dan fitur kolaborasi otomatisnya.

**T: Kalau saya hapus folder Git di laptop, apakah di GitHub juga hilang?**
**J:** Tidak. Itulah gunanya GitHub sebagai **Cloud Backup**. Apa yang kamu hapus di lokal tidak akan mempengaruhi apa yang sudah kamu "Push" ke GitHub.

---

## 📌 Ringkasan Poin Penting
* **Git** adalah software yang berjalan di komputermu (Mesinnya).
* **GitHub** adalah platform hosting yang ada di internet (Rumahnya).
* Kamu bisa pakai Git tanpa GitHub, tapi hampir mustahil pakai GitHub secara profesional tanpa paham Git.

---

## ⏭️ Next Step
Sudah paham teorinya? Sekarang saatnya kita "mengotori" tangan. Ayo kita mulai dari langkah paling awal: instalasi dan konfigurasi identitasmu di Git!

👉 **Lanjut ke: [Instalasi dan Setup Awal]()**