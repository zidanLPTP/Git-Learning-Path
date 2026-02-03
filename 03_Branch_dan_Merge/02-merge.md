# 📄 Menggabungkan Branch (git merge)

> "Setelah selesai bereksperimen di jalur aman (branch), saatnya membawa hasil karya terbaikmu kembali ke jalur utama (main). **Merge** adalah proses menyatukan ide-ide dari dua jalur pengembangan menjadi satu kesatuan yang utuh."

---

## 🎯 Tujuan Pembelajaran

* Memahami konsep **Merging** sebagai cara menyatukan riwayat pengembangan.
* Mampu menggabungkan perubahan dari satu branch ke branch lainnya secara teknis.
* Mengetahui perbedaan antara **Fast-Forward Merge** dan **Three-Way Merge**.
* Memahami praktik aman sebelum dan sesudah melakukan merge.

---

## 💡 Pembahasan Inti

### 1. Apa itu Merge?

**Merge** adalah proses mengambil seluruh riwayat commit dari sebuah branch (misalnya branch fitur) lalu menggabungkannya ke branch lain (biasanya `main`).

Merge dilakukan ketika:

* Fitur sudah selesai dikerjakan
* Kode sudah diuji dan berjalan dengan baik
* Siap digabungkan ke jalur utama (produksi)

Dengan merge, Git **tidak sekadar menyalin file**, tapi menyatukan *sejarah perubahan* dari dua jalur pengembangan.

---

### 2. Cara Melakukan Merge

Misalnya kamu ingin menggabungkan branch `fitur-keren` ke `main`.

**Langkah-langkahnya:**

1. Pindah ke branch tujuan (branch penerima hasil merge):

```bash
git switch main
```

2. Jalankan perintah merge dengan menyebutkan branch asal:

```bash
git merge fitur-keren
```

Jika tidak ada konflik, Git akan langsung menyelesaikan proses merge.

---

### 3. Tipe Penggabungan Dasar

#### 🔹 Fast-Forward Merge

Terjadi jika:

* Branch `main` **tidak memiliki commit baru** sejak branch fitur dibuat

Yang dilakukan Git:

* Penanda (`HEAD`) branch `main` langsung "maju" ke commit terakhir di branch fitur
* **Tidak ada commit merge baru** yang dibuat

Fast-forward adalah merge paling sederhana dan paling bersih.

---

#### 🔹 Three-Way Merge

Terjadi jika:

* Branch `main` **juga memiliki commit baru** saat kamu mengerjakan branch fitur

Yang dilakukan Git:

* Git membandingkan:

  1. Commit bersama terakhir
  2. Perubahan di branch `main`
  3. Perubahan di branch fitur
* Git membuat **commit merge baru** untuk menyatukan dua jalur tersebut

Commit ini menandai bahwa dua sejarah pengembangan telah bertemu.

---

## 🎭 Analogi Dunia Nyata: Memasak Sup Tim

Bayangkan sebuah dapur tim:

* **Panci besar** → Branch `main`
* **Mangkuk kecil** → Branch eksperimen

Kamu ingin mencoba bumbu rahasia, tapi takut sup utama rusak.

1. Kamu mengambil sup ke mangkuk kecil (membuat branch).
2. Kamu bereksperimen dengan bumbu di sana.
3. Rasanya ternyata enak dan disetujui tim.
4. Kamu menuangkan kembali isi mangkuk ke panci utama.

Proses menuangkan kembali itulah **Merge**.

Jika rasa sup utama juga berubah selama kamu bereksperimen, kamu perlu menyesuaikan rasa dengan hati-hati — inilah yang nanti disebut **Merge Conflict**.

---

## 📊 Langkah-Langkah Aman Saat Merge

1. Pastikan branch tujuan (`main`) dalam kondisi bersih:

```bash
git status
```

2. Pastikan semua perubahan sudah di-commit
3. Lakukan merge dari branch tujuan
4. Jalankan aplikasi / test ulang setelah merge
5. Hapus branch fitur jika sudah tidak dibutuhkan:

```bash
git branch -d fitur-keren
```

---

## ❓ Pertanyaan Umum (Q&A)

**T: Apa yang terjadi jika file yang sama diubah di kedua branch secara berbeda?**
**J:** Git akan menghentikan proses merge dan menandainya sebagai **Merge Conflict**. Kamu harus memilih atau menggabungkan perubahan tersebut secara manual.

**T: Apakah branch fitur akan terhapus setelah di-merge?**
**J:** Tidak otomatis. Branch tetap ada sampai kamu menghapusnya sendiri menggunakan `git branch -d`.

**T: Apakah merge bisa dibatalkan?**
**J:** Bisa, selama merge belum di-commit atau belum di-push. Git menyediakan mekanisme untuk membatalkan merge dengan aman.

---

## 📌 Ringkasan Poin Penting

* Merge menyatukan **riwayat commit**, bukan hanya file.
* Selalu pindah ke branch tujuan sebelum menjalankan `git merge`.
* **Fast-Forward Merge** tidak membuat commit baru.
* **Three-Way Merge** membuat commit merge khusus.
* Merge adalah langkah penting sebelum fitur masuk ke produksi.

---

## ⏭️ Next Step

Kadang proses merge tidak berjalan mulus karena ada kode yang bentrok di baris yang sama. Jangan panik — itu hal yang sangat normal.

👉 **Lanjut ke: [Menyelesaikan Merge Conflict](03-conflict.md)**
