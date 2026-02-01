# 📄 Konfigurasi Git (git config)

> "Git adalah asisten yang sangat patuh, tapi dia perlu tahu bagaimana kamu ingin dia bekerja. Dengan konfigurasi yang tepat, pengalaman ngodingmu akan jauh lebih personal dan efisien."

---

## 🎯 Tujuan Pembelajaran

* Memahami cara melihat dan mengubah pengaturan Git.
* Mengetahui perbedaan level konfigurasi (System, Global, dan Local).
* Mampu mengatur editor teks default dan alias untuk mempercepat alur kerja.

---

## 💡 Pembahasan Inti

Meskipun kamu sudah melakukan setup nama dan email di awal, Git masih punya banyak pengaturan lain yang bisa disesuaikan agar cocok dengan gaya kerjamu.

---

### 1️⃣ Level Konfigurasi

Git memiliki tiga tingkat penyimpanan pengaturan:

* **`--system`**
  Berlaku untuk seluruh pengguna di komputer tersebut.

* **`--global`**
  Berlaku untuk pengguna saat ini (paling sering digunakan).

* **`--local`**
  Hanya berlaku untuk satu repository tertentu.

---

### 2️⃣ Melihat Daftar Pengaturan

Untuk melihat semua konfigurasi yang sedang aktif:

```bash
git config --list
```

Git akan menampilkan seluruh pengaturan yang berlaku, digabung dari level system, global, dan local.

---

### 3️⃣ Mengatur Editor Default

Secara default, Git sering menggunakan **Vim**, yang cukup membingungkan untuk pemula. Kamu bisa menggantinya ke **VS Code**:

```bash
git config --global core.editor "code --wait"
```

Sekarang setiap kali Git membutuhkan editor (misalnya saat commit tanpa `-m`), VS Code akan terbuka.

---

### 4️⃣ Membuat Alias (Singkatan Perintah)

Jika kamu sering mengetik perintah yang sama, alias bisa menghemat banyak waktu.

```bash
git config --global alias.st status
git config --global alias.cm "commit -m"
```

Contoh penggunaan:

```bash
git st
git cm "perbaiki bug login"
```

---

## 🎭 Analogi Dunia Nyata: Mengatur Dashboard Mobil

Bayangkan Git adalah sebuah **mobil baru**:

* **Setup Awal** → Mengatur spion & kursi agar nyaman (Nama & Email)
* **Alias** → Tombol pintas di setir agar tidak perlu menjangkau dashboard
* **Local Config** → Mengatur AC sangat dingin hanya di daerah tertentu (Pengaturan khusus satu repo)

---

## 📊 Ringkasan Level Konfigurasi

| Level  | Perintah              | Cakupan                  |
| ------ | --------------------- | ------------------------ |
| System | `git config --system` | Seluruh user di komputer |
| Global | `git config --global` | User kamu (semua repo)   |
| Local  | `git config --local`  | Hanya repo ini           |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Mana yang diprioritaskan jika Global dan Local berbeda?**
**J:** Local akan selalu menang karena lebih spesifik ke repository tersebut.

**T: Di mana file konfigurasi Git disimpan?**
**J:** Untuk level Global, file biasanya berada di `~/.gitconfig`.

---

## 📌 Ringkasan Poin Penting

* Gunakan `git config --list` untuk melihat pengaturan aktif
* Level Global paling umum untuk konfigurasi harian
* Alias sangat meningkatkan produktivitas

---

## ⏭️ Next Step

Konfigurasi sudah siap. Sekarang saatnya memastikan repository tetap bersih dari file-file yang tidak perlu.

👉 **Lanjut ke:[Mengabaikan File](06-ignore-file.md)**
