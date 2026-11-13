# Pincuk — demo tampilan kasir warung makan

**Jenis halaman:** aplikasi kasir (antrean nota, tombol menu, nota aktif, bayar dengan kembalian, rekap harian, menu dan harga, akun).

Demo tampilan statis untuk kasir warung makan, dibuat dengan HTML, CSS, dan JavaScript biasa tanpa server dan tanpa proses build. Nama "Pincuk" (cone daun pisang pembungkus nasi pecel), nama warung, nama orang, dan semua angka adalah fiktif. Alur dan logikanya mengikuti aplikasi kasir aslinya (nomor nota diulang tiap hari, menu diurutkan menurut kelarisan, pilihan uang diterima, rekap harian); yang dibuat ulang adalah tampilannya.

## Bagian

- **Kasir**: antrean nota di atas, tombol menu besar di tengah (yang paling laku paling besar), nota aktif seperti struk di bawah (di layar lebar dan HP miring di kolom kanan), ciri pelanggan dengan satu ketukan, total berjalan, dan tombol Bayar.
- **Lembar bayar**: Uang pas, pilihan uang diterima berwarna pecahan, kembalian, dan cap LUNAS.
- **Rekap**: pemasukan, jumlah nota lunas, waktu rata-rata per nota, terbuka dan batal, daftar terjual, nota selesai, dan unduh cadangan (berkas JSON dari data contoh).
- **Menu dan harga**: tambah item, ubah nama dan harga, hapus (hanya dinonaktifkan), aktifkan lagi, dengan pesan galat saat isian salah.
- **Akun dan cadangan**: masuk dan daftar (tiruan, dengan validasi), status pengiriman nota, rekap dari server, simulasi offline dan langganan berakhir, tema terang atau gelap.

## Konsep desain

- **Palet:** hijau daun pisang untuk header, krem kertas pembungkus untuk latar, kuning kunyit untuk tombol utama antrean, merah cabai untuk Bayar dan lencana jumlah.
- **Huruf:** Bricolage Grotesque untuk judul dan angka, DM Mono untuk harga dan keterangan.
- **Gaya:** tombol timbul yang menekan saat diketuk, nota berbentuk struk dengan tepi bergerigi, ikon makanan digambar sendiri sebagai SVG.
- **Tata letak:** satu kolom di HP (antrean, menu, nota), dua kolom di laptop dan HP miring (menu di kiri, nota di kanan).

## Cara melihat

Buka `index.html` dengan klik dua kali, atau jalankan lewat server lokal (mis. XAMPP) dan buka folder `pincuk-kasir`.

- Nyaman di lebar HP (320 px ke atas), HP miring, tablet, dan laptop.
- Tema mengikuti pengaturan perangkat; tambahkan `?tema=gelap` atau `?tema=terang` di alamat untuk memaksa, atau pakai tombol bulan/matahari di header.
- Coba: ketuk menu untuk menambah, ketuk **Bayar**, pilih uang diterima, lalu buka **Rekap**. Di **Akun** ada panel simulasi untuk mencoba keadaan offline dan langganan berakhir.
- Semua data hanya hidup di halaman dan kembali ke contoh saat dimuat ulang.

## Catatan teknis

- Satu berkas `index.html` (CSS dan JavaScript di dalamnya). Font Bricolage Grotesque dan DM Mono dimuat dari Google Fonts tanpa memblokir tampilan; bila gagal dimuat, halaman memakai font sistem.
- Tidak ada permintaan jaringan selain font, tidak ada kata sandi atau kunci apa pun di dalam berkas.
- Mengikuti `prefers-reduced-motion`; semua kontrol bisa dijangkau dengan keyboard (Esc menutup panel, tombol Back peramban juga menutup panel).

Demo: https://editorzash.github.io/demo_pincuk_kasir/
