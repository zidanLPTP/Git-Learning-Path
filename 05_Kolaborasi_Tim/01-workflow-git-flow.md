# 📄 Workflow Git Flow

> "Jangan biarkan branch utama (`main`) menjadi medan perang. Git Flow adalah sistem lalu lintas yang memastikan fitur baru, perbaikan bug, dan rilis aplikasi berjalan di jalurnya masing-masing tanpa saling tabrak."

---

## 🎯 Tujuan Pembelajaran

* Memahami struktur **branch permanen** dan **branch sementara** dalam Git Flow.
* Mampu membedakan fungsi antara branch `main`, `develop`, dan branch pendukung.
* Mengetahui **kapan dan ke mana** sebuah branch harus di-merge agar alur kerja tetap rapi.

---

## 💡 Pembahasan Inti

**Git Flow** adalah salah satu strategi branching paling populer di dunia profesional. Model ini sangat cocok untuk proyek tim jangka menengah hingga panjang, misalnya website divisi IEEE, aplikasi kampus, atau proyek skripsi berbasis tim.

Intinya: **tidak semua orang dan tidak semua fitur boleh menyentuh `main` secara langsung**.

---

### 1. Branch Permanen (The Core)

Branch ini selalu ada sejak awal proyek dan **tidak boleh sembarangan dihapus**.

* **`main`**

  * Jalur produksi / rilis
  * Hanya berisi kode yang **siap dipakai user**
  * Setiap commit di sini idealnya merepresentasikan versi aplikasi (v1.0, v1.1, dst)

* **`develop`**

  * Jalur integrasi
  * Tempat semua fitur yang sudah selesai digabungkan
  * Masih boleh ada bug kecil, tapi **secara umum stabil**

> 📌 Aturan emas: **Tidak ada development langsung di `main`.**

---

### 2. Branch Pendukung (Temporary)

Branch ini dibuat sesuai kebutuhan dan **boleh dihapus setelah selesai**.

* **`feature/<nama-fitur>`**

  * Dibuat dari `develop`
  * Digunakan untuk mengerjakan satu tugas spesifik
  * Contoh:

    * `feature/login-page`
    * `feature/form-pendaftaran`

* **`release/<versi>`**

  * Dibuat dari `develop`
  * Digunakan untuk pengetesan akhir (QA), perbaikan kecil, dan dokumentasi
  * Setelah rilis:

    * Di-merge ke `main`
    * Juga di-merge kembali ke `develop`

* **`hotfix/<nama-bug>`**

  * Dibuat langsung dari `main`
  * Digunakan jika ada **bug kritis di produksi**
  * Setelah selesai:

    * Di-merge ke `main`
    * Juga di-merge ke `develop`

---

## 🎭 Analogi Dunia Nyata: Dapur Restoran Bintang Lima

* **Piring Saji (`main`)**
  Makanan yang sudah sampai ke pelanggan. Tidak boleh salah rasa atau kotor.

* **Meja Persiapan (`develop`)**
  Semua masakan yang hampir siap dikumpulkan dan dicicipi ulang.

* **Kompor Masing-masing Koki (`feature/`)**
  Setiap koki mengerjakan satu menu. Kalau gagal, tidak merusak hidangan lain.

* **Pemadam Kebakaran (`hotfix/`)**
  Jika ada kesalahan fatal di makanan pelanggan, perbaikan dilakukan secepat mungkin tanpa menunggu menu baru.

---

## 📊 Aturan Alur Git Flow

| Jenis Branch      | Prefix     | Dibuat dari | Tujuan Merge       |
| ----------------- | ---------- | ----------- | ------------------ |
| Fitur             | `feature/` | `develop`   | `develop`          |
| Persiapan Rilis   | `release/` | `develop`   | `main` & `develop` |
| Perbaikan Darurat | `hotfix/`  | `main`      | `main` & `develop` |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Apakah Git Flow tidak terlalu ribet untuk proyek kuliah?**
J: Untuk tugas individu, iya. Tapi untuk kerja kelompok (3–5 orang), Git Flow justru **menghemat waktu dan emosi** karena konflik bisa ditekan sejak awal.

**T: Kapan branch `feature` harus dihapus?**
J: Segera setelah berhasil di-merge ke `develop` dan dipastikan tidak ada error. Branch yang menumpuk hanya akan membingungkan tim.

---

## 📌 Ringkasan Poin Penting

* `main` = kode siap rilis, **jangan disentuh sembarangan**.
* Semua fitur dikerjakan di branch terpisah.
* Git Flow membuat kerja tim terasa seperti sistem, bukan chaos.

---

## ⏭️ Next Step

Alur kerja sudah rapi, branch sudah tertib. Tapi satu hal penting belum dibahas:

👉 **Bagaimana cara memberi komentar ke kode teman tanpa bikin suasana tim panas?**
Lanjut ke: **[Etiket Code Review](02-code-review-etiket.md)**
