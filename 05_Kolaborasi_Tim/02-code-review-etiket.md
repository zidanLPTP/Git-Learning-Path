# 📄 Etiket Code Review (Cara Berkomentar di Pull Request)

> "Code Review bukan ajang untuk menjatuhkan teman, melainkan proses belajar bersama. Ingat: kita sedang menyerang *bug* atau *kode yang bermasalah*, bukan menyerang orang yang menulisnya."

---

## 🎯 Tujuan Pembelajaran

* Memahami pentingnya **Code Review** dalam menjaga kualitas dan konsistensi proyek.
* Mampu memberikan kritik yang **konstruktif dan profesional** di GitHub Pull Request.
* Mengetahui etika **menerima masukan** tanpa defensif atau emosi.

---

## 💡 Pembahasan Inti

### 1. Apa itu Code Review?

**Code Review** adalah proses di mana satu atau beberapa anggota tim meninjau perubahan kode yang diajukan melalui Pull Request (PR) sebelum digabungkan ke branch utama (`main` atau `develop`).

Tujuannya bukan mencari kesalahan semata, melainkan:

* Menemukan bug atau kesalahan logika sejak dini
* Menjaga standar penulisan kode (coding style)
* Memastikan kode mudah dibaca dan dirawat oleh orang lain
* Menjadi sarana belajar bersama dalam tim

Dalam proyek tim (seperti tugas besar, praktikum, atau proyek IEEE), Code Review adalah *quality gate* sebelum kode masuk ke jalur utama.

---

### 2. Prinsip Utama: Kritik Kodenya, Bukan Orangnya

Ini adalah aturan emas yang **tidak boleh dilanggar**.

❌ **Buruk (Menyerang Pribadi):**

> "Kodinganmu berantakan, susah dibaca."

✅ **Baik (Fokus ke Kode):**

> "Bagian fungsi ini mungkin bisa dirapikan agar lebih mudah dipahami oleh anggota tim lain."

Gunakan bahasa yang:

* Objektif
* Netral
* Tidak menghakimi

Ingat: semua orang pernah menulis kode yang buruk, termasuk reviewer itu sendiri 😄

---

### 3. Berikan Solusi, Bukan Hanya Keluhan

Komentar terbaik adalah komentar yang **membantu**, bukan hanya menunjukkan kesalahan.

❌ **Kurang Membantu:**

> "Penamaan variabelnya jelek."

✅ **Konstruktif:**

> "Agar konsisten dengan file lain, mungkin variabel ini bisa menggunakan camelCase. Contoh: `user_input` → `userInput`."

Jika memungkinkan:

* Sertakan contoh kode
* Sertakan alasan teknis
* Sertakan referensi (jika ada)

---

### 4. Gunakan Pertanyaan, Bukan Perintah

Mengubah perintah menjadi pertanyaan akan membuka ruang diskusi dan menghindari kesan sok menggurui.

❌ **Terlalu Memerintah:**

> "Ganti looping ini pakai map."

✅ **Lebih Elegan:**

> "Apakah ada alasan khusus menggunakan looping ini? Sepertinya `map()` bisa membuat kodenya lebih ringkas dan readable."

Diskusi teknis > adu ego.

---

## 🎭 Analogi Dunia Nyata: Mengoreksi Naskah Presentasi

Bayangkan kamu membantu teman sekelompokmu mengecek naskah presentasi (misalnya mata kuliah PBO atau RPL):

* **Code Review:** Menandai typo, kalimat bertele-tele, atau slide yang kurang jelas
* **Etiket:** Kamu tidak bilang "Presentasimu jelek", tapi "Bagian ini mungkin lebih jelas kalau dipindah ke slide awal"
* **Hasil:** Presentasi jadi lebih kuat, nilainya bagus, dan hubungan tim tetap sehat

Itulah esensi Code Review yang benar.

---

## 📊 Checklist Komentar Code Review yang Baik

| Aspek     | Lakukan                       | Hindari                    |
| --------- | ----------------------------- | -------------------------- |
| Bahasa    | Sopan, jelas, objektif        | Sarkas, kasar, merendahkan |
| Fokus     | Logika, keamanan, keterbacaan | Nitpicking tanpa alasan    |
| Sikap     | Mengajak diskusi              | Menggurui                  |
| Apresiasi | Puji bagian kode yang bagus   | Hanya fokus ke kesalahan   |
| Respon    | Terima masukan dengan terbuka | Defensif atau emosional    |

---

## ❓ Pertanyaan Umum (Q&A)

**T: Bagaimana jika saya tidak setuju dengan komentar reviewer?**
**J:** Sampaikan alasan teknismu dengan sopan di kolom komentar. Perbedaan pendapat itu normal. Jika diskusi buntu, libatkan anggota tim ketiga sebagai penengah.

**T: Apakah semua Pull Request harus di-review?**
**J:** Idealnya iya, terutama di proyek tim. Ini mencegah adanya "kode ajaib" yang hanya dipahami oleh satu orang dan meningkatkan kualitas keseluruhan proyek.

---

## 📌 Ringkasan Poin Penting

* Code Review adalah proses kolaborasi, bukan ajang pamer kemampuan
* Kritiklah **kode**, bukan **orangnya**
* Komentar terbaik selalu disertai solusi atau alasan teknis
* Gunakan Code Review sebagai sarana belajar dan mentoring
* Akhiri PR dengan status yang jelas: **Approve** atau **Request Changes**

---

## ⏭️ Next Step

Kode sudah rapi, diskusi sehat, dan tim solid. Sekarang bagaimana cara mengatur pekerjaan agar tidak ada tugas yang terlewat dan semua orang tahu apa yang harus dikerjakan?

👉 **[Lanjut ke: Issues dan Labels](03-issues-dan-labels.md)**
