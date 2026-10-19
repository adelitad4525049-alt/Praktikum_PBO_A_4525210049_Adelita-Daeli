### Laporan Praktikum PBO - Sesi Polimorfisme & Pewarisan (Inheritance)
**Nama: Adelita Daeli**
**NPM : 4525210049**

Repositori ini berisi kumpulan latihan dan tugas praktikum Pemrograman Berorientasi Objek (PBO) yang berfokus pada penerapan Pewarisan (Inheritance), Kelas Abstrak (Abstract Class), Polimorfisme (Polymorphism), serta perbandingan implementasi kode menggunakan bahasa Java dan PHP.
    
    
📁 **Struktur & Daftar Program**
Berikut adalah ringkasan dari 11 program yang terdapat dalam praktikum ini:
1. Studi Kasus Pegawai & Gaji (Java)
    * Program 1 (Main.java - Pegawai): Menjalankan daftar pegawai (Pegawai Tetap dan Kontrak) beserta perhitungan beban gaji total secara polimorfik.
    * Program 2 (Pegawai.java & Turunannya): Kelas induk abstrak Pegawai dengan validasi penolakan gaji negatif serta penerapan method hitungGaji() dan toString().
2. Refaktorisasi Anti-Pattern ke Polimorfisme (Java & PHP)
    * Program 3 (AntiPattern.java): Contoh kode awal (Anti-Pattern) yang belum menerapkan polimorfisme (menggunakan pengecekan tipe instanceof secara manual dalam percabangan if-else).
    * Program 4 (AntiPatternRefaktor.java): Hasil refaktorisasi dari Anti-Pattern menjadi kode yang bersih menggunakan Interface dan struktur polimorfik.
3. Hierarki Bangun Datar (Java)
    * Program 5 (BangunDatar.java): Kelas abstrak induk yang mendefinisikan kontrak utama (luas() dan keliling()) beserta format cetak toString().
    * Program 6 (Lingkaran.java): Kelas turunan untuk menghitung luas dan keliling lingkaran lengkap dengan validasi parameter jari-jari > 0.
    * Program 7 (Persegi.java): Kelas turunan untuk menghitung luas dan keliling persegi dengan validasi parameter sisi > 0.
    * Program 8 (Segitiga.java): Kelas turunan untuk menghitung luas dan keliling segitiga siku-siku.
    * Program 9 (Trapesium.java): Kelas turunan untuk menghitung luas dan keliling trapesium.
    * Program 10 (Main.java - Bangun Datar): Driver code pengujian utama yang menerapkan Upcasting pada array BangunDatar[] serta contoh aman penggunaan Downcasting dengan pattern matching instanceof.
4. Hierarki Notifikasi (PHP)
    * Program 11 (main.php / Notifikasi.php): Latihan mandiri berbasis PHP (declare(strict_types=1)) yang menerapkan kelas abstrak Notifikasi dengan tiga kelas turunan (Email, SMS, dan WhatsApp) serta fungsi pengiriman polimorfik (kirimSemua()) tanpa pemeriksaan tipe sama sekali.
    
🚀 Cara Menjalankan ProgramMenjalankan Program JavaPastikan Anda berada di dalam direktori penyimpanan file sumber Java.Kompilasi semua file kelas:Bashjavac Main.java BangunDatar.java Lingkaran.java Persegi.java Segitiga.java Trapesium.java
Jalankan program utama:Bashjava Main
Menjalankan Program PHPPastikan PHP telah terinstal di komputer Anda.Jalankan skrip melalui terminal:Bashphp main.php


💡 Poin Pembelajaran Utama Menghindari Anti-Pattern: 
    Penambahan tipe data baru dalam kode polimorfik tidak memerlukan perubahan pada logika pemanggilan utama (bebas dari percabangan instanceof atau switch-case yang kaku).Kontrak Kelas Abstrak: Memastikan setiap kelas turunan wajib mengimplementasikan method spesifik (luas(), keliling(), kirim()) sesuai kontrak dari kelas induknya.Validasi Data: Setiap kelas turunan dilengkapi dengan proteksi konstruktor (IllegalArgumentException) untuk menolak nilai parameter yang tidak valid ($\le 0$).
