Adelita Daeli_4525210049

Sesi 2 — Enkapsulasi dan Penjagaan Invariant
Proyek ini merupakan latihan pemrograman berorientasi objek (OOP) yang berfokus pada konsep enkapsulasi dan penjagaan invariant (aturan kevalidan data objek) menggunakan dua bahasa pemrograman, yaitu Java dan PHP.

📌 Deskripsi Masalah
Sistem akademik mencatat data mahasiswa dengan ketentuan sebagai berikut:
1. Atribut Utama: NIM, Nama, dan tiga komponen nilai (Tugas, UTS, dan UAS).
2. Immutable NIM: NIM tidak boleh berubah setelah mahasiswa terdaftar (menggunakan final di Java dan readonly di PHP).
3. Validasi Invariant Nilai: Setiap komponen nilai wajib berada di dalam rentang inklusif 0 sampai 100.
4.  Perhitungan Nilai Akhir: Dihitung menggunakan bobot tetap:Tugas:
   * $30\%$ ($\text{BOBOT\_TUGAS} = 0.30$)
   * UTS: $30\%$ ($\text{BOBOT\_UTS} = 0.30$)
   * UAS: $40\%$ ($\text{BOBOT\_UAS} = 0.40$)
6. Konversi Huruf Mutu:$\ge 80 \rightarrow$ "A"$\ge 70 \rightarrow$ "B"$\ge 60 \rightarrow$ "C"$\ge 50 \rightarrow$ "D"Lainnya $\rightarrow$ "E"
📂 Struktur Berkas
 * analisis.md — Daftar spesifikasi invariant dan aturan validasi objek.
 * Mahasiswa.java — Implementasi kelas dalam bahasa Java.
 * Mahasiswa.php — Implementasi kelas dalam bahasa PHP 8+.

**Output**
![Deskripsi Gambar](../image/After/mahasiswaj1.jpeg)
![Deskripsi Gambar](../images/After/mahasiswaj2.jpeg)
![Deskripsi Gambar](../images/After/mahasiswap1.jpeg)
![Deskripsi Gambar](../images/After/mahasiswap2.jpeg)
![Deskripsi Gambar](../images/After/mahasiswap3.jpeg)
![Deskripsi Gambar](../images/After/mainj1.jpeg)
![Deskripsi Gambar](../images/After/mainp1.jpeg)

 
 🚀 Cara Menjalankan1. 
 1. Java (Mahasiswa.java)Pastikan Anda sudah menginstal Java Development Kit (JDK 8 atau yang lebih baru).
 # Kompilasi
javac Mahasiswa.java
# Jalankan (jika ditambahkan method main pengujian)
java Mahasiswa

 2. PHP (Mahasiswa.php)Pastikan PHP versi 8.0 atau yang lebih baru terinstal (mendukung fitur Constructor Property Promotion dan readonly).
 # Jalankan skrip dengan PHP CLI
php Mahasiswa.php

🛡️ Penjagaan Invariant (Invariant Guard)Setiap upaya untuk memasukkan data yang melanggar aturan (seperti NIM kosong atau nilai negatif/di atas 100) akan langsung digagalkan pada tahap konstruksi objek dengan melempar IllegalArgumentException (Java) atau InvalidArgumentException (PHP). Hal ini menjamin bahwa objek Mahasiswa tidak pernah berada dalam kondisi tidak sah (invalid state).
