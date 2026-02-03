# 📄 Mengabaikan File (.gitignore)

> "Tidak semua hal dalam folder proyekmu perlu masuk ke sejarah Git. Ada file rahasia, file sampah, atau folder besar yang sebaiknya dibiarkan tetap lokal dan tak terlihat oleh Git."

---

## 🎯 Tujuan Pembelajaran

* Memahami fungsi file `.gitignore` dalam mengelola repository.
* Mampu membuat dan mengelola daftar file yang harus diabaikan oleh Git.
* Mengetahui file-file standar yang biasanya tidak boleh masuk ke repository, terutama untuk ekosistem Python dan Java.

---

## 💡 Pembahasan Inti

### 1️⃣ Apa Itu `.gitignore`?

`.gitignore` adalah file teks khusus (tanpa nama depan, hanya ekstensi `.gitignore`) yang berfungsi memberi tahu Git untuk **mengabaikan** file atau folder tertentu.

File yang tercantum di dalam `.gitignore`:

* Tidak akan muncul saat menjalankan `git status`
* Tidak akan ikut saat menjalankan `git add .`
* Tidak akan pernah tercatat dalam riwayat commit

---

### 2️⃣ Kenapa Kita Harus Mengabaikan File?

Sebagai mahasiswa Informatika yang mengerjakan berbagai proyek, ada beberapa alasan krusial:

1. **Keamanan**
   Mencegah pengunggahan file berisi password, API key, atau token rahasia (contoh: `.env`).

2. **Kerapian Repository**
   File hasil kompilasi seperti `.class` (Java) atau `__pycache__` (Python) bisa dibuat ulang dan hanya mengotori riwayat commit.

3. **Efisiensi**
   Folder besar seperti virtual environment (`.venv/`) membuat proses *push* dan *pull* menjadi lambat.

---

### 3️⃣ Cara Membuat File `.gitignore`

Buat file baru bernama `.gitignore` di **root folder proyek**, lalu isi dengan daftar file atau pola yang ingin diabaikan.

Contoh isi `.gitignore` untuk proyek Python:

```gitignore
.venv/
__pycache__/
*.log
.env
```

Git akan langsung menerapkan aturan ini tanpa perlu perintah tambahan.

---

## 🎭 Analogi Dunia Nyata: Filter Sampah Saat Pindahan

Bayangkan kamu sedang **pindah rumah**:

* **Pakaian & Buku** → Kode program yang berharga
* **Sampah & Debu** → File sementara (*temporary files*)
* **Buku Diary Rahasia** → File konfigurasi berisi password

`.gitignore` adalah daftar instruksi untuk tukang angkut:

> "Angkut semua barang, **KECUALI** yang ada di daftar ini."

---

## 📊 Daftar File yang Umum Diabaikan

| Kategori | Contoh File / Folder     | Alasan                        |
| -------- | ------------------------ | ----------------------------- |
| Python   | `.venv/`, `__pycache__/` | Virtual env & cache kompilasi |
| Java     | `*.class`, `.settings/`  | Hasil build & konfigurasi IDE |
| Security | `.env`, `secrets.json`   | Data sensitif                 |
| Sistem   | `.DS_Store`, `Thumbs.db` | File sampah OS                |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Bagaimana jika file sudah terlanjur di-commit?**
**J:** Menambahkan file ke `.gitignore` tidak akan menghapusnya otomatis dari Git. Kamu harus menghapusnya dari indeks terlebih dahulu:

```bash
git rm --cached <nama_file>
```

**T: Apakah `.gitignore` mendukung wildcard?**
**J:** Ya. Contoh:

* `*.log` → mengabaikan semua file `.log`
* `folder/**/temp.txt` → mengabaikan file `temp.txt` di subfolder mana pun

---

## 📌 Ringkasan Poin Penting

* `.gitignore` mencegah file yang tidak perlu masuk ke repository
* Sangat penting untuk menjaga keamanan data sensitif
* Membantu menjaga ukuran repository tetap ringan
* Idealnya dibuat **setelah `git init` dan sebelum `git add .` pertama**

---

## ⏭️ Next Step

Selamat! Kamu sudah menguasai dasar manajemen file di lokal. Saatnya naik level ke fitur paling kuat Git: bekerja di jalur berbeda tanpa merusak kode utama.

 **Lanjut ke: [Mengenal Branching](../03_Branch_dan_Merge/01-branch.md)**
