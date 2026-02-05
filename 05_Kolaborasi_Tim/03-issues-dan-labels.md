# 📄 Issues dan Labels

> "Mengelola proyek tanpa daftar tugas yang jelas itu seperti mencari jalan di Pekanbaru tanpa Google Maps—bisa sampai, tapi banyak nyasarnya. GitHub Issues adalah asisten pribadimu untuk mencatat bug, ide, dan tugas yang harus diselesaikan."

---

## 🎯 Tujuan Pembelajaran

* Memahami fungsi **GitHub Issues** sebagai pusat pelaporan, diskusi, dan pelacakan tugas.
* Mampu menggunakan **Labels** untuk mengategorikan dan memprioritaskan pekerjaan.
* Mengetahui cara **menghubungkan Issue dengan Pull Request** agar alur kerja rapi dan terpantau.

---

## 💡 Pembahasan Inti

### 1. Apa itu GitHub Issues?

**Issues** adalah fitur GitHub yang berfungsi sebagai *task tracker*. Di sinilah semua ide, bug, request fitur, atau pekerjaan teknis dicatat secara terstruktur.

Dalam proyek tim (misalnya tugas kelompok PBO, RPL, atau website IEEE), Issues membantu:

* Mencegah tugas tercecer di chat WhatsApp
* Menentukan siapa mengerjakan apa
* Menyimpan diskusi teknis di tempat yang relevan

Satu masalah = **satu Issue**. Jangan digabung-gabung.

---

### 2. Anatomi Sebuah Issue

Sebuah Issue yang baik biasanya memiliki komponen berikut:

* **Title**
  Judul singkat, jelas, dan langsung ke masalah.
  Contoh: `Fix: Menu navigasi tidak muncul di mobile`

* **Description**
  Penjelasan detail tentang masalah atau fitur:

  * Apa yang terjadi?
  * Apa yang seharusnya terjadi?
  * Langkah untuk mereproduksi bug (jika ada)

* **Assignees**
  Menentukan siapa yang bertanggung jawab mengerjakan Issue tersebut agar tidak saling tunggu.

---

### 3. Menggunakan Labels (Kategorisasi & Prioritas)

**Labels** adalah penanda visual (warna + teks) yang membantu tim memahami kondisi proyek hanya dengan sekali lihat.

Label yang umum digunakan:

* `bug` → Ada yang rusak dan harus diperbaiki
* `enhancement` → Penambahan fitur atau peningkatan
* `documentation` → Perubahan di README, panduan, atau komentar
* `help wanted` → Butuh bantuan anggota lain
* `good first issue` → Cocok untuk pemula

Dengan label, kamu bisa memfilter Issue dengan cepat tanpa membaca satu per satu.

---

## 🎭 Analogi Dunia Nyata: Papan Pengumuman Sekretariat IEEE

Bayangkan di sekretariat IEEE UNRI ada papan tulis besar:

* **Issue:** Selembar kertas bertuliskan: "AC ruangan bocor"
* **Assignee:** Di pojok kertas tertulis nama: *Zidan*
* **Label:** Ditempeli stiker merah bertuliskan *URGENT*
* **Comment:** Coretan anggota lain: "Tukang AC dihubungi, datang besok jam 10"

Semua orang tahu statusnya tanpa harus tanya ke grup.

---

## 📊 Tips Menulis Issue yang Efektif

| Komponen    | Teknik Terbaik                             | Contoh                          |
| ----------- | ------------------------------------------ | ------------------------------- |
| Kejelasan   | Gunakan kata kerja di awal judul           | `Add: Filter harga hotel`       |
| Konteks     | Sertakan file, baris kode, atau screenshot | "Error di `Main.java` baris 45" |
| Keterkaitan | Hubungkan dengan Issue lain                | "Mirip dengan issue #12"        |

---

## 🔗 Menghubungkan Issue dengan Pull Request

GitHub punya fitur **Magic Words** untuk otomatis menutup Issue.

Contoh di deskripsi PR:

```
fixes #3
closes #7
```

Artinya: begitu PR di-*merge*, Issue tersebut akan otomatis ditutup.

Ini sangat membantu menjaga Issue tetap up-to-date tanpa perlu menutup manual.

---

## ❓ Pertanyaan Umum (Q&A)

**T: Siapa yang boleh menutup Issue?**
**J:** Biasanya orang yang mengerjakan tugas tersebut atau admin repository. Jangan menutup Issue sebelum benar-benar selesai dan terverifikasi.

**T: Apakah Issue harus selalu ada sebelum bikin Pull Request?**
**J:** Sangat disarankan. Issue memberi konteks kenapa PR itu dibuat dan memudahkan reviewer memahami tujuan perubahan.

---

## 📌 Ringkasan Poin Penting

* Issues adalah pusat manajemen tugas proyek
* Satu masalah sebaiknya dibuat satu Issue
* Labels membantu menentukan prioritas dan jenis pekerjaan
* Hubungkan PR dengan Issue agar alur kerja rapi dan transparan

---

## ⏭️ Next Step

Issue sudah rapi dan terklasifikasi. Tapi bagaimana melihat **gambaran besar progres proyek** dan menentukan mana yang harus dikerjakan dulu?

👉 **Lanjut ke: [Project Board](04-project-board.md)**
