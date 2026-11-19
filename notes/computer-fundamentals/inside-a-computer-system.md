# Inside a Computer System

- **Modul:** Computer Fundamentals (TryHackMe)
- **Fokus:** Komponen dasar perangkat keras dan urutan proses booting

## 1. Komponen Utama Hardware
Ringkasan fungsi komponen utama yang menyusun sistem komputer:

- **Motherboard:** Papan sirkuit utama yang menampung dan menghubungkan seluruh komponen agar dapat saling berkomunikasi.
- **CPU (Central Processing Unit):** Komponen pemrosesan utama yang mengeksekusi berbagai instruksi di dalam komputer.
- **RAM (Random Access Memory):** Memori penyimpanan sementara berkecepatan tinggi untuk data dan program yang sedang aktif dijalankan. Bersifat *volatile* (seluruh isinya hilang saat aliran listrik terputus).
- **Storage (SSD/HDD):** Media penyimpanan permanen (*non-volatile*) untuk OS, apk, dan data pengguna nya itu sendiri. SSD menggunakan chip memori tanpa komponen mekanis sehingga jauh lebih cepat dibandingkan HDD.
- **Network Adapter:** Komponen yang bisa membuat komputer itu sendiri menjadi terhubung dan bertukar data melalui jaringan (kabel maupun nirkabel).
- **Power Supply (PSU):** Komponen yang menyuplai dan mendistribusikan daya listrik ke seluruh komponen komputer.
- **Graphics Card (GPU):** Komponen yang memproses data grafis dan menghasilkan output tampilan ke monitor/layar laptop.
- **Input/Output (I/O):** Perangkat dan antarmuka untuk menerima input dari pengguna (keyboard, mouse) serta menampilkan atau mengeluarkan hasil pemrosesan (monitor, speaker, printer, dll).

## 2. Urutan Proses Booting (Boot Sequence)
Tahapan yang berlangsung sejak tombol power ditekan hingga OS siap digunakan:

- **Press Power Button:** Tombol power ditekan dan mengirim sinyal ke PSU agar mulai mengalirkan daya listrik ke komponen sistem.
- **Firmware Starts (UEFI/BIOS):** Firmware tingkat awal menyala untuk menginisialisasi dan mengkoordinasikan perangkat keras sebelum OS berjalan.
- **Power-On Self Test (POST):** UEFI menjalankan pengujian mandiri untuk memastikan komponen perangkat keras utama terpasang, terkonfigurasi, dan berfungsi dengan normal.
- **Select Boot Device:** UEFI memeriksa daftar urutan prioritas boot untuk menentukan perangkat penyimpanan tempat OS berada.
- **Initiate Bootloader: Bootloader memuat OS dari storage ke dalam RAM, kemudian UEFI menyerahkan kendali penuh sistem kepada OS.

## 3. Keterkaitannya dengan CySec

- **Memori Volatile (RAM):** Data aktivitas yang sedang berjalan berada di RAM dan akan hilang jika listrik terputus, sehingga analisis memori (*memori forensics*) sangat krusial dilakukan sebelum perangkat dimatikan.
- **Lapisan Awal Booting (Firmware & Bootloader):** Berjalan sebelum sistem operasi dan mekanisme pertahanan di level OS aktif, sehingga memiliki hak akses tingkat tinggi dan menjadi titik sensitif dalam keamanan sistem.