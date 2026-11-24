# Virtualization

* **Modul:** Computer Fundamentals (TryHackMe)
* **Fokus:** Efisiensi perangkat keras, arsitektur virtualisasi (Hypervisor, VM, Container), serta pengelolaan VM dan host

## 1. Alasan Menggunakan Virtualisasi
* Pola lama *"one server = one application"* sering boros biaya (hardware, listrik, pendinginan, tempat), kapasitas server sering menganggur, lambat saat butuh mesin baru, dan sulit di-scale.
* **Virtualisasi** memungkinkan satu komputer fisik dibagi/dimanfaatkan seperti beberapa sistem terpisah secara efisien dan aman.

## 2. Komponen Utama
* **Hypervisor:** Management Software yang membuat, membagi resource, menjaga isolasi, dan mengelola siklus hidup virtual machine.
  * **Type 1:** Berjalan langsung di atas hardware fisik, keuntungannya cepat dan efisien untuk server, database, maupun data center.
  * **Type 2:** Berjalan di atas sistem operasi yang sudah ada. cocok untuk belajar, testing, menjalankan lab/Kali Linux, atau menguji file berbahaya.
* **Virtual Machine (VM / Mesin Laboratorium):** Komputer virtual lengkap dengan CPU, RAM, storage, jaringan, dan sistem operasi sendiri (contoh: VirtualBox, VMware Workstation). Terisolasi dari VM lain dan host (dengan konfigurasi/isolasi yang tepat).
* **Container (Wadah):** Lingkungan terisolasi yang ringan untuk menjalankan aplikasi beserta dependensinya dengan berbagi **kernel** dari sistem operasi host. Lebih cepat nyala dan hemat resource dibanding VM penuh, tetapi harus sesuai dengan tipe kernel host. Contoh platform: **Docker**.
* **Container Image (Gambar Wadah):** Template/paket yang sudah dikemas sebelumnya untuk membuat container.

## 3. Praktik Pengelolaan VM & Host
* **Status & Perbaikan VM:** Memantau status VM (seperti `Running`, `Stopped`, atau `Error`) dan melakukan restart/rerun saat layanan bermasalah.
* **Pembuatan VM:** Menentukan alokasi resource seperti nama, CPU cores, memory, dan disk size sesuai kebutuhan layanan.
* **Monitoring Host Fisik:** Mengecek penggunaan CPU, memori, storage, dan status koneksi tiap host agar tidak overload serta tahu kapasitas yang masih tersedia.

## 4. Manfaat & Keterkaitan dengan CySec
* **Manfaat:** Hemat biaya, pemanfaatan resource optimal, deployment lebih cepat, fleksibel, portable, scalable, dan terpusat.
* **Keamanan Siber:** Memberi ruang latihan terisolasi (seperti VM lab atau pengujian file mencurigakan) tanpa membahayakan sistem utama/host, sekaligus menjadi dasar untuk memahami infrastruktur modern dan cloud.
