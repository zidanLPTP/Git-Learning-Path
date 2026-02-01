# 📄 Apa Itu Git?

> "Bayangkan Git sebagai mesin waktu dan tombol 'Undo' untuk setiap baris kode yang kamu tulis. Tanpanya, coding bareng teman bakal jadi hancur banget dan penuh file bernama `script_fix_v2_final_banget_FIXED.py`."

---

## 🎯 Tujuan Pembelajaran
* Memahami definisi Git sebagai *Version Control System* (VCS).
* Mengetahui alasan mengapa developer profesional wajib menggunakan Git.
* Membedakan alur kerja proyek manual vs menggunakan Git.

---

## 💡 Pembahasan Inti

### Apa Itu Version Control System (VCS)?
Dalam dunia Informatika, kita sering melakukan perubahan pada kode. Masalah muncul ketika kita ingin kembali ke versi kode dua hari yang lalu karena kode yang sekarang malah *error*. 

Git adalah sistem yang mencatat setiap perubahan pada file kamu. Setiap kali kamu melakukan perubahan besar, kamu mengambil **"Snapshot"** (potret) dari kondisi kodinganmu saat itu. Jika di masa depan terjadi kerusakan, kamu bisa "balik" kembali ke snapshot manapun dengan sempurna.

### Kenapa Kita Butuh Git?
1. **Track Changes:** Kamu bisa melihat siapa yang mengubah baris kode nomor 10, kapan diubahnya, dan apa alasannya.
2. **Collaboration:** Kamu dan tim bisa mengerjakan file yang sama secara bersamaan tanpa takut file saling tertimpa.
3. **Experimental:** Kamu bisa mencoba fitur baru yang aneh tanpa merusak kode utama yang sudah jalan. Kalau gagal? Tinggal balik ke versi sebelumnya seolah tidak pernah terjadi apa-apa.

---

## 🎭 Analogi : Game RPG

Agar lebih mudah, bayangkan kamu sedang bermain game RPG (seperti *Elden Ring*, *Genshin Impact*, atau *The Witcher*):

* **Repository:** Adalah slot save-an game kamu atau seluruh folder proyekmu.
* **Commit:** Adalah setiap kali kamu menekan tombol **"Save Game"**. Bedanya, di Git kamu wajib memberi catatan: *"Save setelah dapet pedang sakti"* atau *"Fix bug login"*.
* **Branching:** Bayangkan kamu di persimpangan jalan cerita. Kamu ragu mau jadi ksatria jahat atau baik. Kamu membuat "cabang" cerita. Jika ternyata menjadi jahat itu membosankan, kamu bisa kembali ke titik sebelum memilih tanpa harus mengulang game dari awal.
* **Merge:** Proses menggabungkan dua jalan cerita tadi menjadi satu akhir yang lengkap.

---

## 📊 Manual vs Git

| Fitur           | Cara Manual                              | Menggunakan Git                            |
| **Penyimpanan** | `tugas_v1.zip`, `tugas_v2_final.zip`     | Satu folder, banyak "Snapshot" tersembunyi |
| **Riwayat**     | Mengandalkan ingatan atau catatan manual | Otomatis tersimpan secara kronologis       |
| **Kolaborasi**  | Kirim file lewat WhatsApp / Flashdisk    | Sinkronisasi via Cloud (GitHub)            |
| **Keamanan**    | File hilang/corrupt = tamat              | Backup aman dan bisa dikembalikan          |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Apakah Git hanya untuk programmer?** **J:** Tidak! Penulis buku, desainer yang bekerja dengan teks (seperti file SVG), atau mahasiswa yang sedang menyusun skripsi juga bisa menggunakan Git untuk melacak revisi tulisan mereka.

**T: Apakah saya harus konek internet untuk pakai Git?** **J:** Tidak. Git bekerja sepenuhnya secara **lokal** di komputermu. Kamu baru butuh internet kalau mau mengirim (*push*) kodinganmu ke platform online seperti GitHub.

---

## 📌 Ringkasan Poin Penting
* **Git** adalah alat untuk mencatat setiap perubahan pada file (*Version Control*).
* **Snapshot** adalah istilah untuk rekaman kondisi kodinganmu di waktu tertentu.
* Git sangat krusial untuk **kolaborasi tim** dan menjaga keamanan kode dari kesalahan manusia (*human error*).

---

## ⏭️ Next Step
Sekarang kamu sudah tahu "Kenapa" harus pakai Git. Tapi, di mana kita menyimpan semua catatan itu agar bisa dilihat orang lain secara online dan aman?  

👉 **Lanjut ke: [Apa itu GitHub?](02-apa-itu-github.md)**