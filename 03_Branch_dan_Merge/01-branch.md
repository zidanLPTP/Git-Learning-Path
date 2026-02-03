# 📄 Mengenal Branch (Cabang)

> "Jangan takut merusak kodingan yang sudah jalan. Gunakan Branch untuk membuat cabang baru tempat kamu bisa bereksperimen dengan bebas tanpa mengganggu kode utama."

---

## 🎯 Tujuan Pembelajaran

* Memahami konsep **Branching** sebagai jalur pengembangan yang terpisah.
* Mampu membuat, melihat, dan berpindah antar branch.
* Mengetahui pentingnya branch `main` (atau `master`) dalam sebuah proyek.

---

## 💡 Pembahasan Inti

### 1. Apa itu Branch?

Secara default, saat kamu pertama kali melakukan `git init`, kamu berada di jalur utama yang biasanya bernama `main`.

**Branch** adalah salinan jalur pengembangan tersebut. Branch memungkinkan kamu bekerja di jalur terpisah tanpa mengganggu kode utama.

Jika eksperimenmu gagal, kamu cukup menghapus branch tersebut. Jika berhasil, hasilnya bisa digabungkan kembali ke `main`.

---

### 2. Perintah Dasar Branching

**Melihat daftar branch:**

```bash
git branch
```

**Membuat branch baru:**

```bash
git branch nama-fitur-baru
```

**Berpindah ke branch lain:**

```bash
git switch nama-fitur-baru
```

**Membuat sekaligus berpindah branch:**

```bash
git switch -c fitur-baru
```

---

## 🎭 Analogi Dunia Nyata: Film Avengers (Multiverse)

Bayangkan alur cerita utama film sebagai **branch `main`**.

Seorang penulis ingin mencoba ide ekstrem:

> "Bagaimana jika Thanos sebenarnya adalah orang baik?"

Maka dibuatlah **garis waktu alternatif** (branch eksperimen-thanos).

* Cerita utama tetap aman
* Eksperimen bebas dilakukan
* Jika idenya bagus → digabung
* Jika gagal → dihapus

Penonton tidak akan pernah tahu ada kekacauan di balik layar.

---

## 📊 Status Perintah Branch

| Kebutuhan                  | Perintah               |
| -------------------------- | ---------------------- |
| Cek posisi branch saat ini | `git branch`           |
| Membuat branch baru        | `git branch <nama>`    |
| Pindah branch              | `git switch <nama>`    |
| Hapus branch selesai       | `git branch -d <nama>` |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Apakah file di branch baru akan berbeda dengan branch `main`?**
J: Awalnya sama persis. Setelah kamu melakukan commit di branch baru, perubahan hanya akan ada di branch tersebut.

---

**T: Kenapa branch saya tidak muncul saat menjalankan `git branch`?**
J: Git memerlukan minimal satu commit awal. Pastikan kamu sudah melakukan commit pertama di `main`.

---

## 📌 Ringkasan Poin Penting

* Branch memungkinkan eksperimen tanpa risiko merusak kode utama
* Branch `main` harus selalu stabil dan siap dijalankan
* Gunakan nama branch yang deskriptif dan jelas

---

## ⏭️ Next Step

Eksperimen sudah selesai dan hasilnya mantap?

Sekarang saatnya membawa perubahan kembali ke jalur utama.

**Lanjut ke: [Menggabungkan Branch](02-merge.md)**
