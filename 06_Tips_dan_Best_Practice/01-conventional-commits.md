# 📄 Conventional Commits

> *"Pesan commit bukan cuma sekadar formalitas. Pesan yang jelas adalah surat cinta untuk dirimu di masa depan dan rekan timmu. Berhenti menulis `update`, `fix`, atau `asdf`, dan mulailah menulis sejarah yang bermakna."*

---

## 🎯 Tujuan Pembelajaran

* Mengenal standar penulisan pesan commit internasional (Conventional Commits)
* Mampu mengategorikan setiap perubahan kode dengan prefix yang tepat
* Mempermudah pencarian riwayat fitur atau perbaikan di masa depan

---

## 💡 Pembahasan Inti

**Conventional Commits** adalah aturan sederhana untuk menulis pesan commit agar mudah dibaca manusia maupun mesin (tools CI/CD, changelog generator, dll).

### Format Dasar

```
<type>: <description>
```

Contoh:

```
feat: tambah sistem login mahasiswa
```

---

## 1. Jenis-Jenis `type` yang Sering Digunakan

### `feat:` (Feature)

Digunakan saat kamu **menambah fitur baru**.

Contoh:

```
feat: tambah sistem login mahasiswa
```

---

### `fix:` (Bug Fix)

Digunakan saat kamu **memperbaiki error atau bug**.

Contoh:

```
fix: perbaiki error kalkulasi nilai di Java
```

---

### `docs:` (Documentation)

Digunakan saat kamu **mengubah dokumentasi**, seperti README atau komentar.

Contoh:

```
docs: update panduan instalasi di README
```

---

### `style:` (Formatting)

Mengubah **tampilan kode** tanpa mengubah logika program (spasi, indentasi, CSS).

Contoh:

```
style: rapikan indentasi file index.html
```

---

### `refactor:`

Mengubah struktur kode agar lebih bersih atau efisien **tanpa menambah fitur dan tanpa memperbaiki bug**.

Contoh:

```
refactor: sederhanakan fungsi validasi input
```

---

### `chore:`

Tugas rutin atau non-fitur seperti update dependency atau konfigurasi.

Contoh:

```
chore: update versi Node.js ke 20
```

---

## 🎭 Analogi Dunia Nyata: Label pada Kardus Pindahan

Bayangkan kamu pindah kos di Panam, Pekanbaru.

* ❌ **Buruk**: Semua kardus ditulis "Barang"
* ✅ **Baik**:

  * `DAPUR: Sendok dan Garpu`
  * `BUKU: Materi PBO`
  * `BAJU: Kemeja IEEE`

Conventional Commits adalah **label kardus untuk kode**. Tanpa dibuka, kamu langsung tahu isinya.

---

## 📊 Perbandingan Pesan Commit

| Sebelum (Berantakan) | Sesudah (Profesional)                   |
| -------------------- | --------------------------------------- |
| update lagi          | feat: tambah fungsi filter tanggal      |
| benerin bug          | fix: atasi crash saat input kosong      |
| ganti warna          | style: ubah warna button jadi biru UNRI |
| nambahin tulisan     | docs: tambah penjelasan alur aplikasi   |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Apakah saya harus pakai bahasa Inggris?**
J: Tidak wajib, tapi sangat disarankan agar terbiasa dengan standar industri. Yang paling penting adalah **konsisten dalam satu tim**.

---

**T: Bagaimana jika satu commit isinya macam-macam?**
J: Itu tanda kamu harus **lebih sering melakukan commit**. Idealnya, satu commit hanya punya satu tujuan.

---

## 📌 Ringkasan Poin Penting

* Pesan commit harus menjelaskan **apa yang berubah dan kenapa**
* Gunakan huruf kecil untuk prefix (`feat`, `fix`, dll)
* Jangan pakai titik di akhir pesan commit
* Pesan commit yang rapi memudahkan pembuatan **changelog otomatis**

---

## ⏭️ Next Step

Kadang kita khilaf dan melakukan kesalahan saat commit atau edit file. Jangan panik — Git punya tombol **undo rahasia** 🪄

👉 Lanjut ke:**[memundurkan perubahan](02-undoing-changes.md)**
