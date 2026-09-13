# Vall Web & Tunnel
Vall Web & Tunnel adalah aplikasi Android mandiri yang berfungsi sebagai local web server (PHP) sekaligus manajemen Cloudflare Quick Tunnel otomatis, terinspirasi dari fungsionalitas KSWEB namun dikemas secara ringan dan praktis langsung di perangkat Android.
## Fitur Utama
 * **Local Web Server PHP (libphp.so):** Menjalankan server PHP lokal di berbagai nomor port pilihan dengan direktori root kustom tanpa memerlukan akses root sistem.
 * **Cloudflare Quick Tunnel (libcloudflared.so):** Menyediakan tautan publik instan berformat trycloudflare.com secara otomatis dengan opsi aktif/nonaktif (*HTTPS/HTTP toggle*) pada setiap host.
 * **Integrated File Manager & Code Editor:** Dilengkapi dengan penjelajah file rekursif, ikon format file berbasis vektor, bilah simbol koding cepat (simbol pemrograman umum seperti <, >, $, {, }), serta fitur buat, ubah nama, dan hapus berkas.
 * **Folder Picker Intuitif:** Memilih direktori dokumen web secara visual menggunakan antarmuka penjelajah folder interaktif tanpa harus mengetik jalur path secara manual.
 * **Splash Screen Beranimasi:** Layar pembuka (*splash screen*) dengan pemuatan GIF halus berlatar belakang warna tema aplikasi.
## Struktur Komponen Utama
 * **MainActivity.java**: Pusat kendali utama untuk menambah, menghapus, mengedit, serta menyalakan/mematikan daftar host server dan tunnel.
 * **TunnelService.java**: Layanan latar belakang (*Foreground Service*) yang mengeksekusi proses biner libphp.so dan libcloudflared.so secara bersamaan.
 * **EditorActivity.java**: Editor teks koding dengan bilah pintasan karakter khusus untuk mengedit file web secara langsung.
 * **FolderPickerActivity.java**: Antarmuka pemilih direktori penyimpanan eksternal.
 * **SplashActivity.java**: Aktivitas awal pemuatan animasi pembuka aplikasi.
## Persyaratan Sistem
 * **Arsitektur Perangkat:** ARM64 / AArch64 (mendukung sebagian besar ponsel Android modern).
 * **Versi Android:** Minimal Android 8.0 (Oreo) hingga versi terbaru.
 * **Izin Aplikasi:** Akses penyimpanan eksternal untuk membaca dan menulis file web (*Document Root*).
