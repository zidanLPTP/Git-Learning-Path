# 📄 Cek Status dan Log (git status & git log)

> "Jangan menebak-nebak kondisi kodinganmu. Gunakan perintah pemantau untuk melihat apa yang sedang terjadi saat ini dan apa yang sudah terjadi di masa lalu."

---

## 🎯 Tujuan Pembelajaran

* Mampu memantau kondisi file (tracked vs untracked) menggunakan perintah `git status`.
* Mampu melihat riwayat perjalanan proyek (sejarah commit) menggunakan `git log`.
* Memahami perbedaan antara file yang sudah dimodifikasi, disiapkan, dan disimpan.

---

## 💡 Pembahasan Inti

### 1️⃣ `git status` (Cek Kondisi Sekarang)

Perintah ini adalah **perintah paling sering digunakan** oleh developer. Fungsinya untuk melihat kondisi repository secara *real-time*.

```bash
git status
```

Git akan menampilkan laporan penting, seperti:

* **Branch** → Cabang yang sedang aktif
* **Untracked** → File baru yang belum dipantau Git
* **Modified** → File lama yang berubah tapi belum masuk Staging Area
* **Staged** → File yang sudah siap untuk di-commit

---

### 2️⃣ `git log` (Cek Masa Lalu)

Untuk melihat riwayat atau "save-an" yang pernah kamu buat, gunakan:

```bash
git log
```

Perintah ini menampilkan daftar commit secara kronologis yang berisi:

* **Commit ID (SHA)** → Kode unik setiap perubahan
* **Author** → Nama & email pembuat commit
* **Date** → Waktu commit dibuat
* **Commit Message** → Catatan perubahan

#### Mode Ringkas

Jika log terlalu panjang, gunakan versi satu baris:

```bash
git log --oneline
```

---

## 🎭 Analogi Dunia Nyata: Laporan Inventaris Gudang

Bayangkan repository kamu adalah sebuah **gudang** yang sudah dipasangi sistem CCTV:

* **`git status`**
  Seperti mengecek barang yang ada di meja hari ini.
  Kamu tahu mana barang baru, mana yang sudah dipacking, dan mana yang belum dicatat.

* **`git log`**
  Seperti membuka **Buku Induk Laporan**.
  Semua aktivitas tercatat permanen: siapa, kapan, dan apa yang dikirim.

---

## 📊 Memahami Warna di Terminal

Saat menjalankan `git status`, perhatikan warna teks berikut:

| Warna         | Status               | Arti                                            |
| ------------- | -------------------- | ----------------------------------------------- |
| Merah         | Untracked / Modified | File baru atau berubah tapi belum masuk Staging |
| Hijau         | Staged               | File siap di-commit                             |
| Putih / Clean | Clean                | Tidak ada perubahan, repo aman                  |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Kenapa saat menjalankan `git log` terminal terasa "nyangkut"?**
**J:** Karena Git masuk ke mode pembaca (*less*). Tekan tombol **`q`** untuk keluar.

**T: Apakah ada cara melihat log yang lebih rapi?**
**J:** Ada. Gunakan `git log --oneline`, sangat cocok untuk proyek dengan banyak commit.

---

## 📌 Ringkasan Poin Penting

* `git status` → melihat kondisi file saat ini
* `git log` → melihat sejarah commit
* Cek `git status` secara rutin adalah kebiasaan developer profesional

---

## ⏭️ Next Step

Sekarang kamu sudah tahu kondisi file. Saatnya belajar cara **membungkus perubahan** dan menyimpannya secara permanen.

**Lanjut ke:[ Menyimpan Perubahan ](04-add-commit.md)**
