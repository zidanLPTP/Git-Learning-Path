# 📄 Membuat Repository di GitHub (membuat-repo.md)

> "Punya kode hebat di laptop itu bagus, tapi punya kode yang tersimpan aman di GitHub itu cerdas. **Repository** adalah *rumah* bagi proyekmu di dunia maya agar bisa diakses kapan saja dan (jika diizinkan) oleh siapa saja."

---

## 🎯 Tujuan Pembelajaran

* Mampu membuat **repository baru** melalui dashboard GitHub.
* Memahami perbedaan antara repository **Public** dan **Private**.
* Mengetahui fungsi file inisialisasi seperti **README**, **.gitignore**, dan **License**.

---

## 💡 Pembahasan Inti

### 1. Langkah Membuat Repository Baru

1. Login ke akun **GitHub**
2. Klik tombol **"+"** di pojok kanan atas
3. Pilih **New repository**

Isi form pembuatan repository:

* **Repository name**
  Gunakan nama singkat dan deskriptif
  Contoh: `portal-berita-unri`, `ieee-website-project`

* **Description (Optional)**
  Penjelasan singkat tentang tujuan proyek

---

### 2. Memilih Jenis Akses Repository

#### 🔹 Public Repository

* Bisa dilihat siapa saja di internet
* Cocok untuk:

  * Open-source
  * Portofolio pribadi
  * Proyek showcase

#### 🔹 Private Repository

* Hanya bisa diakses oleh kamu dan kolaborator yang diizinkan
* Cocok untuk:

  * Tugas kuliah (sebelum dikumpulkan)
  * Proyek internal tim
  * Kode yang masih rahasia

Pilih akses dengan bijak karena menyangkut **keamanan dan privasi kode**.

---

### 3. Opsi Inisialisasi Repository

Saat membuat repo, GitHub menyediakan beberapa opsi awal:

#### 🔹 Add a README file

* File dokumentasi utama
* Berisi penjelasan proyek, cara menjalankan, dan informasi penting lainnya
* Sangat disarankan jika memulai repo **langsung di GitHub**

#### 🔹 Add .gitignore

* Memilih template sesuai bahasa (Python, Java, Node, dll)
* Membantu menghindari file sampah ter-commit

#### 🔹 Choose a License

* Menentukan hak penggunaan kode oleh orang lain
* Contoh:

  * **MIT License** → bebas digunakan
  * **GPL** → wajib open-source turunan

Jika masih belajar, **MIT License** adalah pilihan paling aman.

---

## 🎭 Analogi Dunia Nyata: Menyewa Kavling Tanah

Membuat repository itu seperti menyewa kavling di perumahan GitHub:

* 🏠 **Nama Repo** → Alamat rumah
* 🔐 **Public / Private** → Pagar transparan atau pagar tertutup
* 🪧 **README** → Papan informasi di depan rumah
* 🗑️ **.gitignore** → Aturan barang apa yang tidak ikut pindahan

Semakin rapi rumahmu, semakin nyaman orang lain berkunjung.

---

## 📊 Checklist Pembuatan Repository

| Komponen   | Kegunaan           | Rekomendasi Mahasiswa                |
| ---------- | ------------------ | ------------------------------------ |
| Nama Repo  | Identitas proyek   | Gunakan *kebab-case*                 |
| Deskripsi  | Penjelasan singkat | Sertakan mata kuliah / divisi        |
| Visibility | Kontrol akses      | Private (tugas), Public (portofolio) |
| README     | Dokumentasi awal   | Selalu disarankan                    |
| .gitignore | Filter file        | Pilih sesuai bahasa                  |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Apakah repository Private bisa diubah jadi Public nanti?**
**J:** Bisa. Kamu dapat mengubahnya kapan saja melalui menu **Settings** repository.

**T: Saya sudah punya folder proyek di laptop. Haruskah centang "Initialize with README"?**
**J:** **JANGAN.** Jika kamu punya proyek lokal, buat repository **kosong** agar tidak terjadi konflik saat push pertama.

---

## 📌 Ringkasan Poin Penting

* Repository adalah rumah proyekmu di GitHub
* README sangat penting untuk dokumentasi
* Pilih Public atau Private sesuai kebutuhan
* Hati-hati jika kode mengandung data sensitif

---

## ⏭️ Next Step

Rumah sudah siap di cloud. Sekarang saatnya mengirim barang dari laptop ke rumah baru tersebut.

👉 **Lanjut ke: [Push dan Pull ke Remote](03-push-pull-remote.md)**
