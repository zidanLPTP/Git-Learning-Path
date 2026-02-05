# 📑 Git Cheat Sheet

> *"Jangan dihafal, tapi dipahami. Simpan file ini di tempat yang mudah dijangkau saat kamu sedang ngoding di lab atau di sekretariat IEEE."*

---

## 🛠️ Inisialisasi & Persiapan

| Perintah                                        | Kegunaan                                     |
| ----------------------------------------------- | -------------------------------------------- |
| `git init`                                      | Membuat repository Git baru di folder lokal. |
| `git clone <url>`                               | Menyalin proyek dari GitHub ke laptopmu.     |
| `git config --global user.name "Zidan"`         | Mengatur namamu sebagai identitas commit.    |
| `git config --global user.email "email@mu.com"` | Mengatur email sebagai identitas commit.     |

---

## 📝 Siklus Kerja Harian (The Basics)

| Perintah                | Kegunaan                                                |
| ----------------------- | ------------------------------------------------------- |
| `git status`            | Mengecek kondisi file (mana yang berubah/belum di-add). |
| `git add <nama-file>`   | Menandai file tertentu untuk disimpan.                  |
| `git add .`             | Menandai semua perubahan file di folder tersebut.       |
| `git commit -m "pesan"` | Menyimpan perubahan secara permanen dengan catatan.     |
| `git log`               | Melihat riwayat semua commit yang pernah dilakukan.     |

---

## 🌿 Percabangan (Branching)

| Perintah                 | Kegunaan                                                  |
| ------------------------ | --------------------------------------------------------- |
| `git branch`             | Melihat daftar branch yang ada.                           |
| `git branch <nama>`      | Membuat branch baru (misal: `feature/rpg-combat`).        |
| `git checkout <nama>`    | Berpindah ke branch lain.                                 |
| `git checkout -b <nama>` | Membuat branch baru sekaligus langsung berpindah.         |
| `git merge <asal>`       | Menggabungkan perubahan dari branch asal ke branch aktif. |
| `git branch -d <nama>`   | Menghapus branch yang sudah tidak digunakan.              |

---

## ☁️ Bekerja dengan GitHub (Remote)

| Perintah                      | Kegunaan                                                       |
| ----------------------------- | -------------------------------------------------------------- |
| `git remote add origin <url>` | Menghubungkan folder lokal dengan repository GitHub.           |
| `git push origin <branch>`    | Mengirim commit dari lokal ke GitHub.                          |
| `git pull origin <branch>`    | Mengambil dan menggabungkan update terbaru dari GitHub.        |
| `git fetch upstream`          | Mengambil update dari repository asli (untuk repo hasil fork). |

---

## 🚑 Tombol Penyelamat (Undo)

| Perintah                      | Kegunaan                                                            |
| ----------------------------- | ------------------------------------------------------------------- |
| `git restore <file>`          | Membatalkan perubahan file (sebelum di-add).                        |
| `git restore --staged <file>` | Membatalkan git add (unstaging).                                    |
| `git reset --soft HEAD~1`     | Membatalkan commit terakhir (file tetap aman).                      |
| `git reset --hard HEAD~1`     | **BAHAYA!** Kembali ke versi lama dan menghapus semua kerjaan baru. |

---

## 💡 Tips Cepat

* 🔄 **Selalu Pull di Awal**
  Biasakan `git pull` sebelum mulai ngoding biar nggak kena conflict sama tim.

* 🧹 **Gunakan `.gitignore`**
  Pastikan file `.class` (Java), `node_modules`, atau folder `build` tidak ikut ter-push.

* 👔 **Identitas Profesional**
  Gunakan email **[zidanlptp@gmail.com](mailto:zidanlptp@gmail.com)** dan username GitHub **zidanLPTP** agar konsisten dengan CV dan portofolio.

---

> 📌 **Catatan Akhir**
> Cheat sheet ini bukan buat dihafal. Pakai, ulangi, dan lama-lama otot tanganmu yang akan ingat sendiri perintah Git-nya 😄
