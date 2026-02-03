# 📄 Push dan Pull ke Remote (push-pull-remote.md)

> "Menghubungkan folder di laptop dengan server di cloud itu seperti membangun **jembatan dua arah**. Kamu bisa mengirim hasil kerjamu (*push*) dan mengambil hasil kerja temanmu (*pull*) agar semuanya selalu sinkron."

---

## 🎯 Tujuan Pembelajaran

* Memahami konsep **Remote Repository**.
* Mampu menghubungkan repository lokal ke GitHub menggunakan perintah `git remote`.
* Menguasai perintah `git push` dan `git pull` untuk sinkronisasi data.

---

## 💡 Pembahasan Inti

### 1. Konsep Remote Repository

**Remote Repository** adalah salinan repository yang berada di server (GitHub), bukan di laptopmu.

Fungsinya:

* Menyimpan backup kode di cloud
* Menjadi titik temu kolaborasi tim
* Menjaga semua anggota tim bekerja di versi kode yang sama

Git menggunakan **alias** untuk menyebut remote, dan nama paling umum adalah **`origin`**.

---

### 2. Menghubungkan Repository Lokal ke Remote

Perintah ini **cukup dilakukan sekali di awal**:

```bash
git remote add origin https://github.com/username/nama-repo.git
```

Penjelasan:

* **origin** → Nama alias server utama
* **URL** → Alamat repository GitHub kamu

Untuk memastikan alamat remote sudah benar:

```bash
git remote -v
```

---

### 3. git push (Mengirim Kode ke Cloud)

Setelah kamu melakukan `commit` di lokal, perubahan tersebut **belum ada di GitHub**.

Gunakan perintah berikut untuk mengirimnya:

```bash
git push origin main
```

Artinya:

> Kirim semua commit dari branch `main` di laptop ke branch `main` di server `origin`.

💡 **Push pertama kali (disarankan):**

```bash
git push -u origin main
```

Setelah ini, kamu cukup mengetik `git push` saja.

---

### 4. git pull (Mengambil Kode dari Cloud)

Jika ada perubahan baru di GitHub (misalnya dari teman satu tim), kamu wajib menariknya ke laptop:

```bash
git pull origin main
```

Pull akan:

1. Mengambil commit terbaru dari GitHub
2. Menggabungkannya ke branch lokalmu

⚠️ Biasakan **pull sebelum mulai ngoding** untuk menghindari konflik besar.

---

## 🎭 Analogi Dunia Nyata: Galeri Foto Cloud

Bayangkan kamu mengelola album foto bersama:

* 📱 **Repository Lokal** → Galeri foto di HP-mu
* ☁️ **Remote (GitHub)** → Google Photos / iCloud

Tindakan:

* **git push** → Menekan tombol *Upload*
* **git pull** → Menekan tombol *Refresh*

Dengan dua tombol ini, semua perangkat selalu punya versi foto terbaru.

---

## 📊 Perbandingan Perintah Penting

| Tindakan      | Perintah                      | Frekuensi             |
| ------------- | ----------------------------- | --------------------- |
| Tambah Remote | `git remote add origin <url>` | Sekali di awal        |
| Kirim Kode    | `git push origin <branch>`    | Setelah selesai kerja |
| Ambil Kode    | `git pull origin <branch>`    | Sebelum mulai kerja   |
| Cek Remote    | `git remote -v`               | Saat verifikasi       |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Kenapa push saya ditolak (rejected)?**
**J:** Biasanya karena ada commit di GitHub yang belum ada di laptopmu. Solusinya:

1. Jalankan `git pull`
2. Selesaikan conflict (jika ada)
3. Lakukan `git push` kembali

**T: Apakah saya harus mengetik `origin main` setiap saat?**
**J:** Tidak. Setelah push pertama dengan `-u`, cukup gunakan `git push` dan `git pull`.

---

## 📌 Ringkasan Poin Penting

* Remote adalah **server cloud** proyekmu
* `git push` → Mengirim commit ke GitHub
* `git pull` → Mengambil commit dari GitHub
* Biasakan **pull → kerja → commit → push**

---

## ⏭️ Next Step

Bagaimana jika kamu ingin mengambil proyek orang lain dari GitHub ke laptopmu tanpa membuat repo dari nol?

👉 **Lanjut ke: [Clone Repository](04-clone.md)**
