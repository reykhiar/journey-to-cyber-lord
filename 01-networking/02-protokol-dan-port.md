# 02. Protokol, TCP/UDP, & Ports (Fase 3)

> *"Punya alamat rumah saja tidak cukup. Kita harus tahu lewat pintu mana tamu boleh masuk dan bagaimana cara kurir mengantar barangnya."*

---

## 1. Model OSI & TCP/IP (Peta Standar Komunikasi)
Komunikasi jaringan dibagi ke dalam beberapa lapisan atau bisa disebut *layer* agar standarnya jelas secara global:
- **Layer Bawah (Fisik & Data Link):** Urusan kabel, sinyal, dan MAC Address.
- **Layer Tengah (Network & Transport):** Urusan IP Address, rute pengiriman, dan kepastian data sampai (TCP/UDP).
- **Layer Atas (Session, Presentation, Application): Urusan aplikasi yang langsung berinteraksi dengan pengguna (browser, web server).

---

## 2. Cara Kirim Paket: TCP vs UDP (Transport Layer)
Saat data dikirim, ada dua metode utama yang dipakai:
- **TCP (Transmission Control Protocol):**
  - Pengiriman yang **andal, resmi, dan dijamin sampai**.
  - Menggunakan mekanisme **3-Way Handshake**:
    1. `SYN` (Kirim sinyal kenalan/minta sambung)
    2. `SYN-ACK` (Server terima dan balas siap)
    3. `ACK` (Klien konfirmasi balik, koneksi terbuka)
  - Cocok untuk *browsing*, transfer file, dan *login* data penting.
- **UDP (User Datagram Protocol):**
  - Pengiriman cepat **tanpa basa-basi dan tanpa peduli ada paket yang hilang** (asal lempar).
  - Cocok untuk *streaming* video atau *gaming* online, di mana kecepatan jauh lebih penting daripada sedikit data yang korup.

---

## 3. Ports: Pintu Masuk Rumah & Layanan Server 
Kalau IP Address adalah alamat gedung/rumah, maka **Port** adalah nomor kamar atau pintu spesifik tempat layanan berjalan:
- **Port 80 (HTTP):** Pintu depan untuk *web server* biasa (tanpa pengaman).
- **Port 443 (HTTPS):** Pintu web aman yang sudah dilapisi enkripsi.
- **Port 21 (FTP):** Pintu gudang untuk transfer file ukuran besar.
- **Port 22 (SSH):** Pintu rahasia terminal jarak jauh yang dijaga ketat kodenya.
- **Port 53 (DNS):** Pintu khusus untuk penerjemahan nama domain.

---

## 4. Enkripsi Dasar: HTTP vs HTTPS
- **HTTP:** Ibarat mengirim surat terbuka tanpa amplop. Siapa saja yang lewat di jalur yang sama bisa membaca isinya mentah-mentah (*plaintext*).
- **HTTPS:** HTTP yang dibungkus dalam brankas baja berenkripsi menggunakan **TLS (Transport Layer Security)**, sehingga data tetap aman meskipun disadap di tengah jalan.