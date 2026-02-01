# 📄 Menyimpan Perubahan (git add & git commit)

> "Di dunia Git, menekan Ctrl+S saja tidak cukup. Kamu perlu melakukan dua langkah: memasukkan ke dalam keranjang (Add), lalu mengunci pintunya secara permanen (Commit)."

---

## 🎯 Tujuan Pembelajaran

* Memahami alur kerja pemindahan file dari Working Directory ke Staging Area.
* Mampu menggunakan perintah `git add` untuk memilih perubahan.
* Mampu menggunakan `git commit` untuk menyimpan snapshot proyek dengan pesan yang deskriptif.

---

## 💡 Pembahasan Inti

Setelah kamu melakukan perubahan kode di **Working Directory**, ada dua tahap krusial agar perubahan tersebut tercatat dalam sejarah Git: **Add** dan **Commit**.

---

### 1️⃣ `git add` (Menyiapkan Perubahan)

Perintah `git add` memindahkan file dari Working Directory ke **Staging Area**. Di sinilah kamu memilih perubahan mana yang sudah siap disimpan.

#### Menambahkan satu file

```bash
git add nama_file.py
```

#### Menambahkan semua file sekaligus

```bash
git add .
```

Setelah perintah ini dijalankan, status file akan berubah menjadi **Staged** (biasanya berwarna hijau saat dicek dengan `git status`).

---

### 2️⃣ `git commit` (Menyimpan Secara Permanen)

Jika file sudah berada di Staging Area, langkah selanjutnya adalah menyimpannya sebagai **snapshot permanen** di Repository.

```bash
git commit -m "fitur: menambahkan fungsi hitung luas"
```

Keterangan:

* `-m` → *message*, yaitu catatan singkat tentang perubahan yang kamu lakukan
* Pesan commit **wajib jelas dan spesifik** agar mudah dipahami di masa depan

Setelah commit berhasil, status file menjadi **Committed** dan aman tersimpan di sejarah proyek.

---

## 🎭 Analogi Dunia Nyata: Packing Barang di Gudang

Bayangkan kamu sedang mengelola gudang logistik:

* **Working Directory (Lantai Gudang)**
  Barang-barang masih berserakan dan sedang diperiksa atau diperbaiki.

* **Staging Area (Kardus)**
  Barang dimasukkan ke dalam kardus. Kardus belum dilakban, kamu masih bisa menambah atau mengurangi isinya (`git add`).

* **Repository (Seal & Kirim)**
  Kardus dilakban dan diberi label pengiriman. Barang resmi tercatat dan tidak bisa diubah tanpa prosedur baru. Inilah **Commit**.

---

## 📊 Alur Kerja Perintah

| Langkah         | Perintah                      | Status File            |
| --------------- | ----------------------------- | ---------------------- |
| Pilih perubahan | `git add <file>`              | Staged (Siap disimpan) |
| Simpan permanen | `git commit -m "pesan"`       | Committed (Aman)       |
| Batal staging   | `git restore --staged <file>` | Kembali ke Modified    |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Kenapa harus dua langkah? Kenapa tidak satu perintah saja?**
**J:** Agar kamu punya kontrol penuh. Kamu bisa memilih perubahan tertentu untuk disimpan tanpa mencampur perubahan lain yang belum siap.

**T: Apa yang terjadi jika saya lupa memberi pesan commit (`-m`)?**
**J:** Git akan membuka editor teks (seperti Vim atau Nano) dan meminta kamu menulis pesan commit. Untuk pemula, ini sering membingungkan, jadi biasakan selalu menggunakan `-m`.

---

## 📌 Ringkasan Poin Penting

* `git add` → memasukkan perubahan ke Staging Area
* `git commit` → menyimpan perubahan secara permanen ke Repository
* Pesan commit yang jelas membuat `git log` mudah dipahami

---

## ⏭️ Next Step

Perubahan sudah tersimpan dengan aman. Tapi bagaimana jika ada file-file tertentu yang **tidak ingin** kita masukkan ke dalam Git?

👉 **[Lanjut ke: Mengabaikan File](05-config-git.md)**
