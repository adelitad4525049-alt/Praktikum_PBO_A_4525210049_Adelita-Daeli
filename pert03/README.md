Proyek RekeningBank (Java OOP)
Proyek ini adalah implementasi sederhana dari sistem pengelolaan rekening bank menggunakan bahasa pemrograman Java. Proyek ini dirancang untuk mempelajari konsep Pemrograman Berorientasi Objek (PPOB / OOP) tingkat lanjut di Java, khususnya mengenai constructor chaining (delegasi constructor), anggota statis (static), konstanta (final), serta penanganan eksepsi (exception handling).

📂 Struktur Kelas
Proyek ini terdiri dari dua kelas utama:

Main.java: Kelas utama (driver) yang menjalankan pengujian (skenario tes) untuk memastikan semua fungsi pada kelas RekeningBank berjalan dengan benar sesuai invariant yang ditentukan.

RekeningBank.java: Kelas cetak biru (blueprint) yang merepresentasikan entitas rekening bank beserta logika bisnisnya (validasi saldo, setor, tarik, administrasi, dan perhitungan bunga).

⚙️ Fitur dan Implementasi Utama (RekeningBank.java)
Konstanta Global (public static final):

bungatahunan = 0.025 (Suku bunga 2.5%)

biayaadministrasi = 5000 (Potongan biaya admin)

bataspenarikan_sekali = 5000000 (Batas maksimal penarikan dalam sekali transaksi)

Constructor & Delegasi (this(...)):

Menggunakan constructor chaining agar logika validasi terpusat pada satu constructor utama guna menghindari duplikasi kode.

Encapsulation & Invariant:

Menjaga agar saldo tidak pernah bernilai negatif.

Nomor rekening bersifat tetap (final) setelah objek berhasil dibuat.

Validasi ketat pada input setoran, penarikan, serta parameter pembuatan rekening.

Anggota Statis (static):

jumlahRekening: Variabel privat untuk melacak total objek rekening yang berhasil diinisialisasi.

getJumlahRekening() & bungaSetahun(double pokok): Method utilitas statis yang dapat dipanggil tanpa harus membuat instansiasi objek terlebih dahulu.

🚀 Cara Menjalankan Program
Pastikan Anda sudah menginstal Java Development Kit (JDK) di komputer Anda.

Simpan kedua berkas kode (Main.java dan RekeningBank.java) ke dalam satu direktori/folder yang sama.

Buka terminal atau command prompt pada folder tersebut.

Kompilasi program dengan perintah:

Bash
javac Main.java RekeningBank.java
Jalankan program dengan perintah:

Bash
java Main
🧪 Skenario Pengujian (Main)
Program pengujian di kelas Main mencakup:

Pengecekan penghitungan jumlah rekening secara akurat menggunakan method statis.

Pembuatan objek rekening dengan berbagai varian constructor.

Pengujian operasi penyetoran dana (setor).

Pengujian penarikan dana dengan simulasi penolakan jika melebihi saldo atau melewati batas penarikan maksimal (tarik).

Pengujian pemotongan biaya administrasi tanpa membuat saldo menjadi negatif (potongBiayaAdmin).

Perhitungan estimasi bunga tabungan dalam setahun menggunakan method utilitas statis.
