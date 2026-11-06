# 01.Dasar Jaringan: Fisik, Identitas & Alamat 
> *"Komputer itu pada dasarnya bodoh. Mereka butuh identitas yang jelas dan jalur fisik yang pas untuk saling ngobrol tanpa tersesat*"

---

## 1. Anatomi Fisik & Media Transmisi (Layer 1)
Sebelum data bisa jalan-jalan, wujud aslinya di kabel atau udara itu cuma deretan bit `0` dan `1` yang diubah jadi:
* **Pulsa Listrik:** Lewat kabel tembaga (contoh: kabel UTP dengan konektor RJ45).
* **Kedipan Cahaya:** Lewat kabel Fiber Optic (kecepatannya tinggi antar kota atau bahkan negara).
* **Gelombang Radio:** Lewat udara (Wifi, Bluetooth, NFC).
* **Ancaman Fisik:** Kalau orang asing bisa nyelonong masuk ruang server dan colok perangkat ilegal, semua software keamanan canggih langsung tidak berguna (*physical security is the first line of defense*).

---

## 2. Identitas Perangkat: MAC Address vs IP Address (Layer 2 & 3)
Supaya tidak tertukar dengan komputer lain, setiap perangkat mempunyai dua identitas utama:
* **MAC Address (Media Access Control):**
  * KTP atau sidik jari fisik bawaan pabrik dari Network Interface Card (NIC)
  * Terdiri dari 12 karakter heksadesimal (contoh: `A1:B2:C3:D4:E5:F6`).
  * Bersifat permanen.
* **IP Address (Internet Protocol):**
  * Alamat rumah atau nomor kamar perangkat di dalam jaringan. Bersifat dinamis (bisa berubah tergantung tempat kita nyambung).

---

## 3. Pembagian IP: IPv4, IPv6, & Private vs Public IP
* **IPv4:** Format 4 oktet angka (rentang 0-255, contoh `192.168.1.1`). Total jatahnya hanya 4 miliar, yang sekarang sudah ludes.
* **IPv6:** Format kombinasi angka dan huruf yang sangat panjang, diciptakan karena IPv4 sudah habis.
* **Public IP vs Private IP:**
  * **Public IP:** Alamat asli perangkat kamu di mata internet global (diberikan oleh ISP/Internet Service Provider).
  * **Private IP:** Alamat lokal di dalam rumah.
  * **NAT (Network Address Translation):** Penjaga gerbang yang membuat ratusan device dirumah bisa sharing satu IP Publik yang sama untuk keluar ke internet.
  * **DHCP (Dynamic Host Configuration Protocol):** Bisa di ibaratkan sebagai ibu kos yang otomatis bagi-bagi kunci kamar (IP Address) ke HP atau laptop kita begitu nyambung ke wifi.

---

## 4. Perangkat Keras Jaringan (Network Hardware)
* **Hub:** Alat jadul yang "ember". Jika dapat data, dia akan teriak dan nyebar paket itu ke semua port. Jadi surga untuk packet sniffing.
* **Switch:** Alat cerdas di jaringan lokal (LAN) yang pakai MAC Address Table untuk ngirim data langsung ke tujuan spesifik tanpa bikin berisik perangkat lain.
* **Router:** Pusat distribusi paket antar jaringan (penghubung LAN lokal ke internet global/WAN). Target utama kalau mau nguasain satu wilayah jaringan.
* **Firewall**: Satpam galak yang ngecek daftar tamu (whitelist/blacklist) paket data yang boleh masuk atau keluar.