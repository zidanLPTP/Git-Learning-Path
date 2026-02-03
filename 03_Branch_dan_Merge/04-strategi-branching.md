# 📄 Strategi Branching (Workflows)

> "Pernah bayangkan tim besar seperti Google atau Facebook mengedit satu basis kode yang sama secara bersamaan? Tanpa strategi, kode mereka akan hancur dalam sehari. **Strategi branching** adalah aturan main agar semua orang bisa ngoding bareng dengan rapi dan aman."

---

## 🎯 Tujuan Pembelajaran

* Memahami pentingnya memiliki **aturan standar** dalam penggunaan branch.
* Mengenal **model Git Flow** yang populer di dunia profesional.
* Mampu menerapkan **alur kerja sederhana** untuk proyek skala kecil hingga menengah (mahasiswa & tim kecil).

---

## 💡 Pembahasan Inti

Dalam kerja tim, kita **tidak boleh asal membuat branch** atau sembarang merge ke `main`. Tanpa aturan, konflik akan sering terjadi dan kode utama menjadi tidak stabil.

Berikut adalah pembagian branch yang umum dan terbukti efektif.

---

### 1. Branch Utama (Production Branch)

**`main` / `master`**

* Berisi kode yang **100% stabil**
* Siap dijalankan dan dipresentasikan ke pengguna atau dosen
* ❌ Tidak boleh ngoding langsung di sini

Branch ini adalah **pintu utama aplikasi** — harus selalu bisa dibuka.

---

### 2. Branch Pengembangan (Development Branch)

**`develop`**

* Tempat berkumpulnya semua fitur baru
* Digunakan untuk integrasi dan testing sebelum masuk ke `main`
* Bisa saja masih ada bug kecil

Jika `main` adalah produk jadi, maka `develop` adalah **ruang perakitan**.

---

### 3. Branch Pendukung (Supporting Branches)

#### 🔹 Feature Branch

**`feature/nama-fitur`**
Contoh: `feature/login-page`

* Dibuat untuk satu tugas atau fitur spesifik
* Aman untuk eksperimen
* Setelah selesai → merge ke `develop` (atau `main` untuk tim kecil)
* Setelah itu **wajib dihapus**

---

#### 🔹 Hotfix Branch

**`hotfix/nama-bug`**

* Dibuat langsung dari `main`
* Untuk bug **kritis** di versi produksi
* Setelah diperbaiki → merge ke `main` dan `develop`

Hotfix itu seperti **pemadam kebakaran** — cepat, fokus, dan mendesak.

---

## 🎭 Analogi Dunia Nyata: Redaksi Berita Online

Bayangkan alur kerja di kantor berita:

* 📰 **Website Utama (`main`)**
  Berita sudah tayang dan dibaca publik. Tidak boleh salah.

* 📝 **Draf Editor (`develop`)**
  Kumpulan artikel dari wartawan yang sedang disunting.

* ✍️ **Catatan Wartawan (`feature/*`)**
  Tempat wartawan menulis bebas tanpa takut merusak berita utama.

* 🚨 **Ralat Mendesak (`hotfix/*`)**
  Jika ada kesalahan fatal, langsung diperbaiki di website utama.

---

## 📊 Contoh Alur Kerja Sederhana (Mahasiswa)

Untuk tugas kelompok atau proyek kampus, gunakan versi ringan berikut:

* **`main`** → Kode final yang siap dikumpulkan
* **`feature/nama-mahasiswa`** → Jalur kerja masing-masing anggota

Contoh:

| Jenis Tugas   | Nama Branch               | Tujuan Akhir             |
| ------------- | ------------------------- | ------------------------ |
| Fitur Baru    | `feature/crud-database`   | Merge ke `main`          |
| Perbaikan Bug | `bugfix/salah-hitung`     | Merge ke `main`          |
| Eksperimen    | `experiment/library-baru` | Boleh dihapus jika gagal |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Kenapa harus ribet bagi-bagi branch? Bukannya bisa langsung di `main`?**
**J:** Saat kerja tim, satu kesalahan di `main` bisa menghentikan seluruh kelompok. Strategi branching menjaga agar jalur utama selalu aman.

**T: Kapan branch fitur harus dihapus?**
**J:** Segera setelah berhasil di-merge dan dipastikan tidak ada error. Branch yang menumpuk akan membingungkan.

---

## 📌 Ringkasan Poin Penting

* Jangan pernah melakukan eksperimen langsung di `main`
* Gunakan prefix jelas: `feature/`, `bugfix/`, `hotfix/`
* Strategi branching membuat **riwayat Git rapi dan mudah dibaca**
* Semakin besar tim, semakin wajib strateginya

---

## ⏭️ Next Step

Strategi di lokal sudah mantap. Sekarang saatnya benar-benar pindah ke cloud dan menghubungkan Git lokal dengan GitHub.

👉 **Lanjut ke: [SSH vs HTTPS](../04_GitHub_Advanced/01-ssh-vs-https.md)**
