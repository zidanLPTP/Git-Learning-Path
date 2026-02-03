# 📄 Pull Request (PR)

> "Pull Request bukan sekadar mengirim kode, tapi cara kamu bilang: *'Eh, saya punya perbaikan bagus nih, coba tolong dicek dan kalau oke tolong digabungkan ya!'* Ini adalah inti dari kolaborasi dan diskusi di GitHub."

---

## 🎯 Tujuan Pembelajaran

* Memahami apa itu **Pull Request** dan perannya dalam kolaborasi tim.
* Mampu membuat Pull Request dari repository hasil **fork** ke repository asli.
* Mengenal proses **Code Review** (peninjauan kode) sebelum kodingan resmi diterima.

---

## 💡 Pembahasan Inti

### 1. Apa itu Pull Request?

**Pull Request (PR)** adalah permintaan resmi yang kamu ajukan kepada pemilik repository (maintainer) agar mereka **menarik (pull)** perubahan yang sudah kamu buat ke dalam branch utama mereka (biasanya `main`).

PR menjadi tempat diskusi: membahas kualitas kode, logika program, performa, hingga kesesuaian dengan standar tim.

---

### 2. Alur Kerja Pull Request (Standard Workflow)

Berikut alur yang hampir selalu dipakai di proyek profesional:

1. **Fork & Clone**
   Ambil repository orang lain ke akun GitHub-mu, lalu clone ke laptop.

2. **Create Branch**
   Buat branch khusus untuk satu tujuan:

   ```bash
   git checkout -b fix-typo-landing-page
   ```

3. **Commit & Push**
   Setelah selesai memperbaiki kode:

   ```bash
   git add .
   git commit -m "fix: memperbaiki typo di landing page"
   git push origin fix-typo-landing-page
   ```

4. **Open Pull Request**
   Buka repository hasil fork di GitHub → klik **Compare & pull request**.

5. **Discussion & Review**
   Maintainer akan:

   * Menerima (Merge)
   * Meminta revisi
   * Atau menolak dengan alasan teknis

---

### 3. Kenapa Harus Pakai Pull Request?

Kenapa tidak langsung merge saja?

Karena PR berfungsi sebagai **gerbang keamanan kode**:

* Mencegah bug masuk ke branch `main`
* Menjaga konsistensi gaya penulisan kode
* Media belajar dari komentar reviewer
* Bukti kontribusi yang bisa dilihat publik

Di dunia profesional, **tidak ada yang boleh merge ke `main` tanpa PR**.

---

## 🎭 Analogi Dunia Nyata: Revisi Skripsi

Bayangkan proses bimbingan skripsi:

* **Naskah Dosen** → Repository utama
* **Salinan Mahasiswa** → Fork repository
* **Coretan & Perbaikan** → Commit di branch
* **Pull Request** → Mengajukan revisi ke dosen
* **Code Review** → Dosen membaca dan memberi komentar
* **Merge** → Revisi diterima dan masuk naskah final

Jika masih ada salah, dosen akan menyuruh revisi lagi — bukan langsung menolak total.

---

## 📊 Anatomi Sebuah Pull Request

| Bagian            | Fungsi             | Tips Praktis                             |
| ----------------- | ------------------ | ---------------------------------------- |
| **Title**         | Judul perubahan    | Gunakan format jelas: `Fix: error login` |
| **Description**   | Penjelasan detail  | Jelaskan *apa* dan *kenapa*              |
| **Commits**       | Riwayat perubahan  | Pastikan commit rapi & fokus             |
| **Files Changed** | Baris kode berubah | Cek ulang tidak ada file sampah          |
| **Reviewers**     | Peninjau kode      | Tag dosen / komting / senior             |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Apakah Pull Request bisa dibatalkan?**
J: Bisa. Kamu bisa menutup (Close) PR kapan saja jika merasa masih ada kesalahan besar.

**T: Bagaimana jika PR saya ditolak?**
J: Jangan baper 😄. Penolakan biasanya karena alasan teknis. Perbaiki kodenya di branch yang sama, lakukan `push` lagi, dan PR akan otomatis ter-update.

**T: Apakah satu PR boleh berisi banyak fitur?**
J: Sebaiknya tidak. Satu PR = satu tujuan. Ini memudahkan review dan mengurangi konflik.

---

## 📌 Ringkasan Poin Penting

* Pull Request adalah ajakan diskusi, bukan sekadar kirim kode.
* Code Review meningkatkan kualitas dan profesionalitas proyek.
* PR yang rapi mencerminkan developer yang rapi.
* Semua kontribusi open-source **dimulai dari PR**.

---

## ⏭️ Next Step

Sekarang kamu sudah paham *bagaimana* kontribusi dilakukan. Tapi…

> **Bagaimana cara tim profesional mengatur alur kerja Git agar rapi dari awal sampai rilis?**

👉 Lanjut ke: **[Strategi Workflow Git Git Flow](../05_Kolaborasi_Tim/01-workflow-git-flow.md)**
