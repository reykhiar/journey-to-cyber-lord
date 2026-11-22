# Client-Server Basics
- **Modul:** Computer Fundamentals (TryHackMe)
- **Fokus:** Model komunikasi client-server, protokol jaringan, DNS, port, dan struktur request-response pada HTTP

## 1. Konsep Inti
- **Client & Server:** Client (seperti browser) selalu memulai permintaan (request), sedangkan server melayani dan mengirimkan balasan (response).
- **Protocol:** Aturan dan bahasa komunikasi antara client dan server. Protokol mendefinisikan:
1) Perintah yang dipahami client dan server seperti GET
2) Struktur penyusunan permintaan (urutan perintah dan data yang diminta).
3) Sintaks atau format bahasa yang digunakan
4) Balasan standar untuk permintaan yang valid.
5) Pesan kesalahan (error response) jika permintaan tidak valid atau sumber daya tidak tersedia.
- **Port:** Identitas saluran/pintu spesifik untuk membedakan berbagai layanan yang berjalan bersamaan di dalam satu server.
- **DNS(Domain Name System):** Sistem yang menterjemahkan nama domain menjadi IP tujuan.

## 2. Protokol Web: HTTP & HTTPS
- **Sifat Stateless:** Setiap permintaan HTTP diproses secara independen tanpa meningat permintaan sebelumnya. Untuk menjaga status sesi (seperti status login), aplikasi web menggunakan pengenal sesi (session identifier) berupa cookie atau token yang dikirim ulang pada setiap permintaan berikutnya.
- **9 HTTP Methods (Perintah Utamanya):**
1) GET (mengambil data/sumber daya)
2) POST (mengirim data baru ke server)
3) PUT (memperbarui seluruh data yang ada)
4) PATCH (memperbarui sebagian data)
5) DELETE (menghapus data)
6) HEAD (mengambil header saja tanpa body)
7) OPTIONS (mengecek method yang didukung server)
8) CONNECT (membuka terowongan komunikasi/tunnel)
9) TRACE (melakukan uji pantul jalur permintaan)

## 3. Anatomi HTTP Request & Response (DevTools - Network)
- **Komponen Request:**
1) **Scheme:** Protokol yang digunakan (http atau https).
2) **Host:** Nama domain server tujuan.
3) **Filename:** Jalur/berkas yang diminta dari host.
4) **Address:** Alamat IP fisik dari server yang melayani permintaan.
5) **Status:** Kode hasil pemrosesan permintaan (contoh: 200 OK jika berhasil, 404 NotFound).
- **Bagian Response:**
1) **Response Header:** Metadata mengenai balasan server (tipe konten, ukuran berkas, waktu, jenis perangkat lunak server).
2) **Response Body:** Isi data utama yang diminta oleh client (misalnya kode HTML halaman web).

## 4. Keterkaitan dengan CySec
- Kemampuan membaca struktur URL (scheme, host, path), HTTP methods, headers, dan status code lewat Developer Tools menjadi dasar utama saat menganalisis lalu lintas web maupun mencari celah keamanan web.
- Pemahaman sifat stateless HTTP dan mekanisme cookie/token sangat krusial untuk memahami cara kerja autentikasi dan risiko pembajakan sesi (session hijacking).
