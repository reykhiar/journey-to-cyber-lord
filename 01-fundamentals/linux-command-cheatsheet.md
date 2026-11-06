# Linux Command Documentation & Security Reference Sheet

Dokumentasi ini mencatat perintah-perintah dasar hingga menengah pada Linux yang digunakan dalam aktivitas administrasi sistem, navigasi terminal, serta pengumpulan informasi awal (*reconnaissance*).

## 1. Navigasi & Operasi File

| Perintah | Deskripsi | Contoh Penggunaan |
| :--- | :--- | :--- |
| `pwd` | Menampilkan direktori kerja saat ini | `pwd` |
| `ls` | Menampilkan daftar file dan folder | `ls -la` *(tampilkan semua file termasuk file tersembunyi)* |
| `cd` | Berpindah direktori | `cd ~/Documents` |
| `mkdir` | Membuat direktori baru | `mkdir -p lab/subfolder` |
| `cp` | Menyalin file atau folder | `cp file.txt backup.txt` |
| `mv` | Memindahkan atau mengubah nama file | `mv old.txt new.txt` |
| `rm` | Menghapus file atau folder | `rm -rf test_dir` |

## 2. Pemeriksaan Sistem & Informasi Lingkungan

| Perintah | Deskripsi | Contoh Penggunaan |
| :--- | :--- | :--- |
| `uname` | Informasi arsitektur kernel dan sistem operasi | `uname -a` |
| `whoami` | Menampilkan nama pengguna yang aktif saat ini | `whoami` |
| `id` | Menampilkan User ID (UID) dan Group ID (GID) | `id` |
| `df` | Menampilkan penggunaan ruang sistem berkas (disk space) | `df -h` |
| `free` | Menampilkan penggunaan memori RAM | `free -h` |

## 3. Inspeksi Teks & Pengolahan Data

| Perintah | Deskripsi | Contoh Penggunaan |
| :--- | :--- | :--- |
| `cat` | Membaca dan menampilkan seluruh isi file | `cat file.txt` |
| `head` / `tail` | Membaca baris awal atau akhir dari sebuah file | `tail -n 20 /var/log/syslog` |
| `grep` | Mencari pola teks atau string tertentu | `grep -i "error" log.txt` |
| `jq` | Mengolah dan memfilter data format JSON | `cat data.json | jq .` |

---

> **Catatan Pembelajaran:** 
> Penguasaan navigasi CLI dan pengolahan teks dengan `grep` serta `jq` sangat penting saat melakukan analisis file *log* server maupun hasil keluaran dari alat *security scanner*.