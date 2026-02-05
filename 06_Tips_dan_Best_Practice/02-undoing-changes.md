📄 Membatalkan Perubahan (Undoing Changes)

"Jangan panik! Salah satu kekuatan terbesar Git adalah kemampuannya untuk memutar balik waktu. Entah kamu salah ketik, salah hapus, atau salah commit, selalu ada jalan pulang."

🎯 Tujuan Pembelajaran

* Mampu membatalkan perubahan yang belum di-stage menggunakan git restore.
* Mengetahui cara membatalkan commit terakhir tanpa menghapus hasil kerja.
* Memahami perbedaan tingkat bahaya antara git reset soft, mixed, dan hard.

💡 Pembahasan Inti

1. Membatalkan Perubahan di File (Belum Add)
   Jika kamu sedang mengedit file (misalnya di Main.java) dan tiba-tiba kodenya berantakan, kamu bisa mengembalikannya ke kondisi terakhir yang stabil:

```bash
git restore nama-file.java
```

Perintah ini akan:

* Menghapus semua perubahan lokal pada file tersebut
* Mengembalikan file ke kondisi terakhir saat commit

⚠️ Catatan: Perubahan yang belum di-commit akan hilang.

---

2. Membatalkan Perintah Add (Unstaging)
   Jika kamu tidak sengaja mengetik `git add .` padahal ada file rahasia atau file yang belum siap ikut terbawa:

```bash
git restore --staged nama-file.java
```

Efeknya:

* File dikeluarkan dari staging area
* Perubahan di file tetap aman (tidak terhapus)

---

3. Membatalkan Commit (git reset)
   Ini adalah "mesin waktu" Git jika kamu sudah terlanjur melakukan commit tapi ada kesalahan.

🔹 git reset --soft
Membatalkan commit terakhir, tapi semua perubahan tetap berada di staging area.

```bash
git reset --soft HEAD~1
```

Cocok jika:

* Salah menulis pesan commit
* Ingin menggabungkan commit

🔹 git reset --mixed (Default)
Membatalkan commit dan staging, tapi file fisik tetap berubah.

```bash
git reset HEAD~1
```

🔹 git reset --hard (BAHAYA!)
Menghapus commit, staging, dan seluruh perubahan file.

```bash
git reset --hard HEAD~1
```

⚠️ Semua perubahan yang belum di-push akan hilang permanen.

---

🎭 Analogi Dunia Nyata: Menulis dengan Pensil vs Pulpen

* git restore: Seperti menghapus tulisan pensil sebelum dikumpulkan.
* git reset --soft: Tugas sudah dikumpulkan, tapi kamu ambil lagi untuk memperbaiki nama.
* git reset --hard: Kertas tugas dibakar dan kamu kembali ke draf lama.

---

📊 Tabel Penyelamat

| Situasi                     | Perintah                    | Risiko        |
| --------------------------- | --------------------------- | ------------- |
| Salah edit file (belum add) | git restore <file>          | Rendah        |
| Salah git add               | git restore --staged <file> | Rendah        |
| Salah pesan commit          | git commit --amend          | Rendah        |
| Hapus total perubahan       | git reset --hard HEAD~1     | SANGAT TINGGI |

---

❓ Pertanyaan Umum (Q&A)

T: Kapan saya harus pakai git reset --hard?
J: Hanya jika kamu benar-benar ingin membuang semua perubahan dan yakin tidak membutuhkannya lagi.

T: Apakah saya bisa membatalkan git push yang sudah masuk ke GitHub?
J: Bisa, tapi sangat tidak disarankan. Cara aman adalah menggunakan git revert agar riwayat tim tetap aman.

---

📌 Ringkasan Poin Penting

* Selalu jalankan git status sebelum membatalkan perubahan.
* Hindari git reset --hard kecuali benar-benar yakin.
* git restore adalah penyelamat harian yang paling aman.

⏭️ Next Step
Sebelum kamu terjun ke proyek besar, yuk pelajari jebakan-jebakan yang sering bikin mahasiswa stres.

👉 **Lanjut ke: [Kesalahan Umum Git](03-kesalahan-umum.md)**
