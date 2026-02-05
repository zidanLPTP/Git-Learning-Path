📄 **Kesalahan Umum (Common Mistakes)**

"Orang pintar belajar dari kesalahannya sendiri, tapi orang yang jauh lebih pintar belajar dari kesalahan orang lain. Inilah daftar lubang yang sering bikin mahasiswa *terperosok* saat menggunakan Git."

---

## 🎯 Tujuan Pembelajaran

* Mengenali kesalahan teknis yang sering terjadi bagi pemula.
* Memahami bahaya menyimpan data sensitif di repository publik.
* Mengetahui cara menghindari conflict yang sebenarnya tidak perlu terjadi.

---

## 💡 Pembahasan Inti

### 1. Lupa `.gitignore` (Sampah Masuk ke Cloud)

Banyak mahasiswa langsung `git add .` tanpa filter. Akibatnya, file hasil kompilasi (seperti `.class` di Java, `node_modules`, atau file `.exe`) ikut terunggah ke GitHub.

**Dampak:**

* Repository jadi berat dan kotor.

**Solusi:**

* Selalu buat file `.gitignore` di awal proyek sesuai dengan bahasa pemrograman yang kamu pakai (Java, Python, Flutter, dll).

---

### 2. Mengunggah Data Sensitif (Password & API Key)

Karena terlalu semangat, kadang file konfigurasi database atau token API ikut ter-push ke repository **Public**.

**Dampak:**

* Akunmu bisa dibajak orang lain dalam hitungan detik.

**Solusi:**

* Jangan pernah tulis password langsung di kode.
* Gunakan *Environment Variables* (`.env`) dan masukkan file tersebut ke `.gitignore`.

---

### 3. Commit Terlalu Besar (Giant Commits)

Mengerjakan tugas seharian, lalu baru melakukan satu kali commit di akhir dengan pesan "Selesai".

**Dampak:**

* Sulit melacak perubahan.
* Sulit membatalkan sebagian perubahan jika terjadi error.

**Solusi:**

* Lakukan *commit kecil tapi sering* (atomic commits).
* Satu fitur, satu commit.

---

### 4. Bekerja Langsung di Branch `main`

Mengerjakan fitur baru atau eksperimen langsung di jalur utama tanpa membuat branch baru.

**Dampak:**

* Jika kodenya error, tidak ada versi stabil untuk dikumpulkan ke dosen atau di-*deploy*.

**Solusi:**

* Selalu buat branch fitur, misalnya `feature/rpg-combat` atau `feature/login-page`.

---

## 🎭 Analogi Dunia Nyata: Membawa Sampah ke Dalam Rumah

Mengerjakan proyek tanpa `.gitignore` itu seperti kamu pulang ke rumah (GitHub):

* Masuk tanpa melepas sepatu berlumpur.
* Membawa plastik sampah ke dalam kamar.

Hasilnya, rumah yang harusnya rapi malah jadi kotor — padahal yang kamu butuhkan di rumah itu cuma dirimu sendiri (kode inti).

---

## 📊 Checklist "Anti-Gagal" Sebelum Push

| Apa yang Dicek? | Cara Memastikan                         |
| --------------- | --------------------------------------- |
| Status File     | Jalankan `git status`                   |
| Data Sensitif   | Pastikan tidak ada password / token API |
| Kompilasi       | Pastikan program bisa di-run            |
| Pesan Commit    | Gunakan format *Conventional Commits*   |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Saya terlanjur push password ke GitHub Public, apa yang harus saya lakukan?**
**J:** Segera ganti/hapus password tersebut. Anggap password itu sudah bocor. Menghapus commit tidak menjamin data aman karena riwayat bisa saja sudah di-*clone* orang lain.

**T: Kenapa teman saya tidak melihat perubahan terbaru?**
**J:** Pastikan kamu push ke branch yang benar dan temanmu melakukan `git pull` dari branch yang sama.

---

## 📌 Ringkasan Poin Penting

* `.gitignore` adalah **wajib**, bukan pilihan.
* Keamanan data adalah prioritas utama saat repository bersifat Public.
* Gunakan branch agar kolaborasi tim berjalan aman dan rapi.

---

🎉 **Selamat!** Dengan ini, modul Git & GitHub dasar–menengah kamu sudah **lengkap dan siap dipakai** untuk praktikum, kerja tim, maupun portofolio pribadi.
