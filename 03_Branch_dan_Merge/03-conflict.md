# 📄 Menangani Konflik (Merge Conflict)

> "Jangan panik saat terjadi tabrakan kode! **Merge Conflict** hanyalah cara Git meminta bantuanmu untuk memutuskan: *'Versi mana yang ingin kamu simpan?'* Ini adalah bagian **normal dan sehat** dari kolaborasi tim."

---

## 🎯 Tujuan Pembelajaran

* Memahami penyebab terjadinya **Merge Conflict**.
* Mampu membaca dan mengenali **indikator konflik** di dalam file teks.
* Mampu menyelesaikan konflik secara manual dengan aman.
* Menyelesaikan proses merge dengan **commit hasil perbaikan**.

---

## 💡 Pembahasan Inti

### 1. Apa itu Merge Conflict?

**Merge Conflict** terjadi ketika Git **tidak bisa memutuskan secara otomatis** perubahan mana yang harus digabungkan.

Kondisi paling umum penyebab konflik:

* Dua branch mengubah **baris yang sama** pada file yang sama secara berbeda
* Satu branch menghapus file, sementara branch lain masih mengeditnya
* Branch fitur terlalu lama tidak digabungkan ke `main`

Penting untuk diingat:

> ❗ Merge Conflict **bukan error** dan **bukan kesalahanmu** — ini hanyalah titik diskusi yang diminta Git.

---

### 2. Cara Membaca Konflik di Dalam File

Saat konflik terjadi:

* Proses merge akan **berhenti sementara**
* `git status` akan menandai file sebagai **unmerged**
* Git menambahkan **penanda konflik** langsung ke dalam file

Contoh isi file yang mengalami konflik:

```text
<<<<<<< HEAD
Git itu sangat mudah.
=======
Git itu sangat seru.
>>>>>>> fitur-deskripsi
```

Arti simbol konflik:

* **`<<<<<<< HEAD`** → Perubahan di branch tempat kamu berada sekarang
* **`=======`** → Garis pemisah dua versi yang bentrok
* **`>>>>>>> nama-branch`** → Perubahan dari branch yang ingin digabungkan

Tugasmu adalah **mengedit isi file** dan menghapus seluruh penanda tersebut.

---

### 3. Cara Menyelesaikan Konflik (Langkah Demi Langkah)

1. Buka file yang bermasalah (biasanya berwarna merah di VS Code)
2. Tentukan solusi:

   * Gunakan versi milikmu
   * Gunakan versi milik branch lain
   * Gabungkan keduanya secara manual (opsi terbaik)
3. Hapus semua penanda konflik (`<<<<<<<`, `=======`, `>>>>>>>`)
4. Simpan file
5. Tandai konflik sudah selesai dan akhiri merge:

```bash
git add .
git commit -m "fix: menyelesaikan merge conflict pada index.html"
```

> Merge **belum selesai** sampai commit ini dibuat.

---

## 🎭 Analogi Dunia Nyata: Edit Dokumen Tugas Kelompok

Bayangkan kamu dan temanmu mengedit **paragraf yang sama** di satu dokumen:

* Kamu menulis: *"Git itu sangat mudah."*
* Temanmu menulis: *"Git itu sangat seru."*

Saat digabungkan, muncul kebingungan.

Solusi terbaik bukan memilih salah satu, tapi menulis ulang:

> **"Git itu sangat mudah dan seru."**

Proses diskusi dan penentuan kalimat akhir inilah yang disebut **Resolving Conflict**.

---

## 📊 Indikator Status Saat Konflik

| Status di Git | Arti                                        |
| ------------- | ------------------------------------------- |
| Unmerged      | Ada konflik yang belum diselesaikan         |
| Modified      | File sedang kamu perbaiki                   |
| Staged        | Konflik pada file tersebut sudah dibereskan |

Gunakan `git status` sebagai kompas utama saat menyelesaikan konflik.

---

## ❓ Pertanyaan Umum (Q&A)

**T: Apakah saya harus pakai terminal untuk menyelesaikan konflik?**
**J:** Tidak wajib. VS Code menyediakan tombol visual seperti *Accept Current*, *Accept Incoming*, dan *Accept Both* yang sangat membantu pemula.

**T: Kenapa saya sering mengalami konflik?**
**J:** Biasanya karena jarang melakukan `git pull` atau branch fitur dibiarkan terlalu lama. Semakin sering sinkronisasi, semakin kecil potensi konflik besar.

**T: Apakah merge conflict bisa dicegah 100%?**
**J:** Tidak. Tapi bisa **diperkecil** dengan komunikasi tim, commit kecil, dan merge yang rutin.

---

## 📌 Ringkasan Poin Penting

* Merge Conflict adalah **permintaan konfirmasi**, bukan kegagalan
* Konflik harus diselesaikan langsung di dalam file
* Semua penanda konflik **wajib dihapus** sebelum commit
* Merge dianggap selesai **setelah add dan commit dilakukan**

---

## ⏭️ Next Step

Lokal sudah beres, konflik sudah ditaklukkan. Sekarang saatnya membawa proyekmu ke level kolaborasi global.

👉 **Lanjut ke: [Strategi Branching Tim](04-strategi-branching.md)**
