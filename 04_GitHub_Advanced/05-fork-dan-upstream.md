# 📄 Fork dan Upstream

> "Fork adalah cara sopan untuk *menyalin* proyek orang lain ke akunmu sendiri agar kamu bisa bebas mengutak-atiknya tanpa merusak aslinya. Sementara **Upstream** adalah tali pengaman yang menjaga kamu tetap terhubung dengan sumber asli agar tidak ketinggalan perkembangan."

---

## 🎯 Tujuan Pembelajaran

* Memahami konsep **Forking** dan perbedaannya dengan `git clone`.
* Mampu melakukan sinkronisasi antara repository hasil fork dengan repository asli menggunakan konsep **Upstream**.
* Mengetahui alur kerja standar saat berkontribusi ke proyek publik / open-source.

---

## 💡 Pembahasan Inti

### 1. Apa itu Fork?

**Fork** bukanlah perintah Git, melainkan fitur dari platform seperti **GitHub**.

Saat kamu menekan tombol **Fork** di sebuah repository:

* GitHub akan membuat **salinan penuh repository tersebut ke akun GitHub-mu**.
* Repository hasil fork **berdiri sendiri** dan sepenuhnya berada di bawah kendalimu.
* Kamu punya **hak penuh untuk push, membuat branch, dan eksperimen bebas**.

> Fork sangat umum digunakan saat kamu ingin berkontribusi ke proyek besar, tapi tidak punya akses langsung ke repository aslinya.

---

### 2. Apa itu Upstream?

Setelah melakukan fork dan `git clone` ke laptop, secara default kamu hanya punya satu remote:

* **origin** → repository hasil fork di akun GitHub-mu

Agar repo fork-mu tidak ketinggalan update dari sumber asli, kamu perlu menambahkan remote kedua:

* **upstream** → repository asli milik pemilik awal

📌 Dengan kata lain:

* **origin** → tempat kamu *mengirim* kode
* **upstream** → tempat kamu *mengambil* pembaruan resmi

---

### 3. Cara Sinkronisasi Fork dengan Upstream

Jika repository asli mengalami update, repo fork **tidak akan otomatis ikut berubah**. Sinkronisasi dilakukan manual dengan langkah aman berikut:

```bash
# 1. Tambahkan repository asli sebagai upstream (cukup sekali)
git remote add upstream https://github.com/pemilik-asli/nama-repo.git

# 2. Ambil seluruh perubahan terbaru dari upstream
git fetch upstream

# 3. Gabungkan ke branch lokalmu (biasanya main)
git merge upstream/main
```

💡 Tips penting:

* Lakukan sinkronisasi **sebelum mulai mengerjakan fitur baru**.
* Jika terjadi conflict, selesaikan seperti materi *Merge Conflict* sebelumnya.

---

## 🎭 Analogi Dunia Nyata: Membuka Cabang Restoran

* **Repository Asli (Pusat):** Restoran terkenal milik koki hebat.
* **Fork (Cabangmu):** Kamu membuka cabang restoran tersebut dengan nama dan manajemen sendiri.
* **Upstream:** Jalur komunikasi dari pusat ke cabang untuk mengirim resep dan standar terbaru.

Tanpa upstream, restoran cabangmu lama-lama akan **ketinggalan tren**. Dengan upstream, kualitas tetap terjaga.

---

## 📊 Perbedaan Clone vs Fork

| Fitur              | Git Clone              | GitHub Fork                     |
| ------------------ | ---------------------- | ------------------------------- |
| Lokasi Salinan     | Laptop / Lokal         | Akun GitHub-mu (Cloud)          |
| Tujuan Utama       | Mengerjakan proyek     | Berkontribusi / eksperimen      |
| Hak Akses Push     | Harus jadi kolaborator | Bebas (repo milikmu)            |
| Remote Default     | origin                 | origin + upstream               |
| Umum Dipakai Untuk | Proyek pribadi / tim   | Open-source & kontribusi publik |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Kapan saya harus melakukan Fork?**
J: Saat kamu ingin berkontribusi ke proyek publik (open-source) di mana kamu **tidak punya izin push langsung** ke repository utama.

**T: Apakah Fork akan memakan kuota storage GitHub saya?**
J: Tidak signifikan. GitHub mengelola fork secara efisien dan tidak membebani akun personal secara nyata.

**T: Apakah saya tetap perlu clone setelah fork?**
J: Ya. Fork hanya menyalin repo ke akun GitHub-mu. Untuk bekerja di laptop, kamu tetap harus melakukan `git clone`.

---

## 📌 Ringkasan Poin Penting

* **Fork** menyalin repository ke akun GitHub-mu.
* **Clone** menyalin repository ke laptopmu.
* **Upstream** wajib ditambahkan agar fork tidak ketinggalan update.
* Sinkronisasi rutin adalah kebiasaan penting sebelum kontribusi.

---

## ⏭️ Next Step

Fork sudah rapi dan up-to-date. Kamu sudah menambahkan fitur atau memperbaiki bug.

Sekarang, bagaimana cara **mengirim perubahanmu kembali ke pemilik asli agar bisa direview dan digabungkan secara resmi?**

👉 Lanjut ke: **[Pull Request](06-pull-request.md)**
