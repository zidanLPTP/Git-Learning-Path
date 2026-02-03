# 📄 SSH vs HTTPS (Koneksi ke GitHub)

> "Pernah gagal melakukan `git push` karena ditolak oleh GitHub? Itu tandanya kamu perlu cara yang lebih aman untuk mengenalkan komputermu ke server. **Pilih pintu yang tepat** agar alur kerjamu lancar tanpa gangguan."

---

## 🎯 Tujuan Pembelajaran

* Memahami perbedaan antara protokol **HTTPS** dan **SSH** dalam ekosistem GitHub.
* Mengetahui alasan kenapa **HTTPS kini mewajibkan Personal Access Token (PAT)**.
* Mampu memilih metode koneksi yang **paling efisien dan aman** untuk penggunaan jangka panjang.

---

## 💡 Pembahasan Inti

Saat Git lokal ingin berkomunikasi dengan GitHub (push, pull, clone), dibutuhkan **jalur koneksi + autentikasi**. Ada dua metode utama yang disediakan GitHub: HTTPS dan SSH.

---

### 1. HTTPS (Hypertext Transfer Protocol Secure)

Ini adalah metode **paling mudah** dan biasanya digunakan oleh pemula.

**Ciri utama:**

* URL repository diawali dengan `https://github.com/...`
* Tidak memerlukan konfigurasi awal yang rumit

**Perubahan penting (sejak 2021):**
GitHub **tidak lagi menerima password akun** untuk autentikasi melalui terminal.

**Solusinya:**
Kamu wajib membuat **Personal Access Token (PAT)** melalui:

```
Settings → Developer Settings → Personal Access Tokens
```

Token ini digunakan **sebagai pengganti password** saat melakukan push atau pull.
Juga ini hanya berlaku untuk private repositori

**Karakteristik HTTPS:**

* ✅ Mudah digunakan
* ❌ Harus memasukkan token saat autentikasi
* ❌ Token bisa kadaluwarsa atau perlu diganti

HTTPS cocok untuk **komputer umum atau sementara**.

---

### 2. SSH (Secure Shell)

SSH menggunakan **sepasang kunci digital**:

* **Public Key** → disimpan di GitHub
* **Private Key** → disimpan di laptop kamu

Setelah dikonfigurasi **sekali saja**, GitHub akan mengenali laptopmu secara otomatis.
tetapi hal ini tidak perlu di rincikan sekarang

**Kelebihan utama SSH:**

* Tidak perlu username, password, atau token
* Autentikasi otomatis (passwordless)
* Sangat aman untuk penggunaan jangka panjang

**Catatan penting:**
Private Key adalah **identitas digitalmu**. Jangan pernah dibagikan atau diunggah ke repository.

SSH sangat direkomendasikan untuk **laptop pribadi dan kerja profesional**.

---

## 🎭 Analogi Dunia Nyata: Kunci vs Kartu Akses

Bayangkan kamu ingin masuk ke sebuah gedung:

### 🔹 HTTPS — Kartu Akses Tamu

* Kamu masuk menggunakan kartu sementara
* Jika kartu kadaluwarsa, kamu harus minta yang baru
* Setiap masuk, identitasmu diperiksa ulang

### 🔹 SSH — Kunci Pribadi

* Kamu punya kunci fisik sendiri
* Sidik jarimu sudah terdaftar di sistem
* Selama membawa kunci itu, pintu akan terbuka otomatis

SSH membuat GitHub **percaya penuh pada perangkatmu**.

---

## 📊 Perbandingan Singkat

| Fitur       | HTTPS                    | SSH                          |
| ----------- | ------------------------ | ---------------------------- |
| Setup Awal  | Sangat mudah             | Sedikit teknis (sekali saja) |
| Autentikasi | Personal Access Token    | SSH Key Pair                 |
| Kenyamanan  | Sering login ulang       | Otomatis                     |
| Keamanan    | Aman, tergantung token   | Sangat aman                  |
| Rekomendasi | PC Lab / Laptop Pinjaman | Laptop Pribadi               |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Kenapa password GitHub saya ditolak saat push?**
**J:** GitHub sudah menghapus autentikasi password di terminal. Kamu wajib menggunakan **Personal Access Token (PAT)**.

**T: Apakah saya bisa pindah dari HTTPS ke SSH di tengah jalan?**
**J:** Bisa. Kamu hanya perlu mengganti URL remote:

```bash
git remote set-url origin <url-ssh>
```

**T: Apakah SSH benar-benar aman?**
**J:** Ya, selama Private Key dijaga dengan baik dan tidak dibagikan.

---

## 📌 Ringkasan Poin Penting

* HTTPS sekarang **tidak lagi menggunakan password**, tapi PAT
* SSH adalah pilihan **terbaik dan paling praktis** untuk laptop pribadi
* Jangan pernah membagikan **PAT atau Private Key**
* Pilih metode sesuai konteks penggunaan

---

## ⏭️ Next Step

Koneksi sudah dipahami. Sekarang saatnya membuat rumah pertama proyekmu di cloud.

👉 **Lanjut ke: [Membuat Repository di GitHub](02-membuat-repo.md)**
