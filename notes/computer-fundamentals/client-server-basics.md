# Client-Server Basics
- **Modul:** Computer Fundamentals (TryHackMe)
- **Fokus:** Model client-server, komponen dasar komunikasi jaringan, dan alur HTTP request-response

## 1. Konsep Inti
- **Client & Server:** Client (seperti browser) selalu memulai permintaan (request), sedangkan server melayani dan mengirimkan balasan (response).
- **Protocol:** Aturan dan format bahasa yang digunakan client dan server agar dapat saling memahami saat berkomunikasi.   
- **Port:** Identitas pintu/saluran layanan spesifik pada server sehingga client terhubung ke layanan yang tepat.   
- **DNS (Domain Name System):** Menerjemahkan nama domain menjadi alamat IP (Internet Protocol address) tujuan. 

## 2. Komunikasi Web & HTTP
- **HTTP / HTTPS:** Protokol stateless untuk komunikasi web; setiap request berdiri sendiri, sehingga aplikasi web memakai mekanisme seperti cookie atau token untuk menjaga status sesi (misalnya login).   
- **Method GET:** Digunakan untuk meminta/mengambil resource dari server.   
- **Inspeksi di Browser (DevTools - Network):** Memungkinkan melihat detail komunikasi seperti scheme (http/https), host, filename, address (IP server), status (misalnya 200 OK), headers, dan response body.

## 3. Keterkaitan dengan CySec
- Membaca request dan response di tab Network membantu memahami bagaimana data dikirim antara browser dan server.   
- Memahami port, DNS, dan stateless HTTP jadi fondasi awal sebelum masuk ke analisis jaringan dan keamanan web.