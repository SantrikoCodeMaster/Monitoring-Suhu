# Monitoring-Suhu
Monitor Suhu Arduino dengan Modul Ethernet ENC28J60
Proyek Arduino ini menggunakan modul Ethernet ENC28J60 untuk membuat server web yang memonitor suhu dan menampilkan informasi tersebut pada halaman web. Suhu diukur menggunakan sensor suhu LM35 yang terhubung ke Arduino.

Komponen yang Dibutuhkan
Arduino (Uno, Mega, atau varian lainnya)
Modul Ethernet ENC28J60
Sensor Suhu LM35
Kabel Jumper
Kabel Ethernet
Sumber daya untuk Arduino dan ENC28J60
Persyaratan Perangkat Lunak
Arduino IDE
Library UIPEthernet (untuk dukungan ENC28J60)
Diagram Rangkaian
Masukkan gambar diagram rangkaian Anda di sini, jika tersedia.

Instalasi dan Pengaturan
Pengaturan Perangkat Keras:

Hubungkan modul ENC28J60 ke Arduino menggunakan pin SPI (MISO, MOSI, SCK) dan atur pin CS (Chip Select).
Sambungkan sensor suhu LM35 ke pin analog di Arduino (misalnya A0).
Pengaturan Perangkat Lunak:

Instal library UIPEthernet di Arduino IDE (Sketch > Include Library > Manage Libraries...).
Salin dan tempel sketch Arduino yang disediakan (temperature_monitor_enc28j60.ino) ke Arduino IDE.
Sesuaikan alamat MAC dan alamat IP dalam sketch sesuai dengan konfigurasi jaringan Anda.
Unggah Sketch:

Unggah sketch ke papan Arduino Anda menggunakan Arduino IDE.
Mengakses Antarmuka Web:

Setelah sketch diunggah dan Arduino terhubung ke jaringan, buka web browser.
Masukkan alamat IP yang diberikan ke Arduino di bilah alamat browser.
Anda akan melihat halaman web yang menampilkan suhu saat ini dan informasi tambahan.
Detail Proyek
Arduino secara terus-menerus membaca suhu dari sensor LM35.
Berdasarkan pembacaan suhu, LED yang terhubung ke Arduino dinyalakan untuk menunjukkan rentang suhu secara visual.
Server web yang dibangun dengan Arduino merespons permintaan HTTP dari klien (web browser) dan melayani halaman HTML sederhana yang menampilkan suhu.
Troubleshooting
Tidak Ada Tanggapan dari Arduino:

Periksa koneksi Ethernet dan pastikan Arduino telah berhasil mendapatkan alamat IP dari jaringan Anda.
Verifikasi pengaturan alamat MAC dan alamat IP dalam sketch.
Pembacaan Suhu Tidak Tepat:

Pastikan sensor LM35 terhubung dengan benar dan dikalibrasi jika diperlukan.
Periksa pembacaan analog dan logika konversi dalam sketch Arduino.
Halaman Web Tidak Tampil:

Konfirmasi bahwa modul Ethernet diinisialisasi dengan benar dalam fungsi setup pada sketch Arduino.
Periksa kode HTML dalam sketch untuk memastikan formatnya sudah benar dan dikirimkan dalam respons terhadap permintaan HTTP.
