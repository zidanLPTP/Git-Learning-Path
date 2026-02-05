📄 Project Board (GitHub Projects)

"Punya daftar tugas (Issues) itu bagus, tapi melihat bagaimana tugas-tugas itu bergerak dari 'Rencana' hingga 'Selesai' adalah kunci manajemen proyek yang sukses. Project Board adalah pusat kendali visual untuk seluruh tim."

---

🎯 Tujuan Pembelajaran

* Memahami konsep Kanban Board dalam pengembangan perangkat lunak.
* Mampu membuat dan mengelola kolom status tugas (To Do, In Progress, Done).
* Mengetahui cara memantau beban kerja tim secara visual.

---

💡 Pembahasan Inti

### 1. Apa itu Project Board?

Project Board adalah fitur GitHub yang menggunakan metodologi **Kanban**. Kamu bisa membayangkan ini sebagai papan tulis dengan kartu-kartu tugas (Issues) yang bisa digeser-geser sesuai progres pengerjaannya.

Dengan Project Board, ketua tim atau anggota tim bisa langsung melihat:

* Tugas apa saja yang belum dikerjakan
* Tugas mana yang sedang dikerjakan
* Tugas mana yang sudah selesai

Ini sangat membantu untuk proyek tim agar tidak ada pekerjaan yang terlupakan.

---

### 2. Kolom Standar Kanban

Secara umum, sebuah papan proyek memiliki minimal tiga kolom utama:

* **To Do (Rencana)**
  Semua Issue yang sudah dibuat tapi belum ada yang mulai mengerjakan.

* **In Progress (Sedang Dikerjakan)**
  Tugas yang sedang dikerjakan oleh anggota tim. Kolom ini penting agar tidak ada dua orang yang mengerjakan hal yang sama.

* **Done (Selesai)**
  Semua tugas yang sudah selesai, di-merge, dan sudah dites.

Dalam proyek yang lebih besar, kamu juga bisa menambahkan kolom tambahan seperti:

* Review
* Testing
* Blocked

---

### 3. Otomatisasi (Automation)

GitHub Projects versi terbaru mendukung otomatisasi yang sangat membantu. Contohnya:

* Issue otomatis masuk ke kolom **To Do** saat dibuat
* Kartu otomatis pindah ke **In Progress** saat Pull Request dibuka
* Kartu otomatis pindah ke **Done** saat PR di-merge

Dengan otomatisasi ini, tim tidak perlu memindahkan kartu secara manual setiap saat.

---

🎭 Analogi Dunia Nyata: Alur Produksi Video Kelompok

Ingat proyek video peran komputer kamu yang dikerjakan bareng 4 orang anggota?

Bayangkan kamu punya papan fisik di dinding:

* **To Do**: "Cari referensi komedi Saiki Kusuo", "Tulis naskah", "Sewa kamera"
* **In Progress**: Saat temanmu mulai menulis naskah, kartu "Tulis naskah" dipindahkan ke sini
* **Review**: Naskah sudah jadi tapi perlu dicek bareng-bareng
* **Done**: Naskah final siap syuting

Dengan satu lihat papan, semua orang langsung paham kondisi proyek.

---

📊 Manfaat Menggunakan Project Board

| Manfaat      | Penjelasan untuk Mahasiswa                                       |
| ------------ | ---------------------------------------------------------------- |
| Transparansi | Semua anggota tim tahu siapa sedang mengerjakan apa              |
| Fokus        | Tim bisa melihat tugas mana yang menjadi penghambat (bottleneck) |
| Motivasi     | Kolom "Done" yang makin penuh bikin semangat                     |
| Organisasi   | Menghindari tumpang tindih pekerjaan                             |

---

❓ Pertanyaan Umum (Q&A)

**T: Apakah Project Board hanya untuk kodingan saja?**
J: Tidak. Project Board bisa dipakai untuk tugas non-teknis, seperti pembagian konten media sosial, desain poster, atau pengaturan event.

**T: Apa bedanya Project Board dengan Issues?**
J: Issues adalah unit tugasnya, sedangkan Project Board adalah alat untuk mengatur status dan alur pengerjaan tugas-tugas tersebut.

---

📌 Ringkasan Poin Penting

* Project Board membantu melihat progres proyek secara menyeluruh.
* Gunakan kolom **In Progress** dengan disiplin agar tidak ada tugas yang terbengkalai.
* Hubungkan Issues dengan Project Board agar semua pekerjaan terdokumentasi dengan rapi.

---

⏭️ Next Step
Proyek sudah rapi, tugas sudah terpantau. Sekarang bagaimana cara menjaga kualitas kode dan riwayat perubahan agar tetap bersih?
👉 Lanjut ke: **[Strategi Workflow Git Git Flow](../06_Tips_dan_Best_Practice/01-conventional-commits.md)**