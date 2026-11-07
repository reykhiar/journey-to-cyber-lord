# Linux System Hardening

Dokumentasi ini mencatat langkah-langkah praktis dan konsep keamanan sistem (*system hardening*) pada OS Linux untuk menerapkan prinsip **Least Privilege**.

---

## 1. Audit File Identitas Pengguna (`/etc/passwd`)

File `/etc/passwd` adalah basis data lokal yang memuat informasi akun pengguna di sistem Linux. Setiap baris dipisahkan oleh 7 kolom menggunakan tanda titik dua (`:`):

```text
username:x:UID:GID:GECOS:Home_Directory:Shell```