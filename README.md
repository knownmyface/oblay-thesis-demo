# DapurERP — ERP Warmindo (Warung Senja)

Sistem ERP sederhana untuk warung makan / Warmindo, dibuat untuk tugas akhir.
Bahasa Indonesia semua. Live demo: https://oblay-thesis-demo.vercel.app/

## Cara jalanin

- **Paling gampang:** buka `index.html` langsung di browser, atau buka link Vercel di atas.
- **Deploy sendiri ke Vercel:** import repo ini di Vercel, framework pilih "Other", tanpa build command.
- Tanpa login, tanpa install apa-apa. Satu file HTML mandiri (termasuk CSS + JS di dalamnya).

## Halaman (11 halaman terpisah)

Ringkasan, Kasir, Menu & bahan, Resep & produksi, Pembelian, Supplier,
Pelanggan, Karyawan, Kas & biaya, Laporan, Pengaturan.

## Fitur

- **Mode mulai dari nol:** semua angka mulai Rp 0, teman/owner input sendiri dari awal.
- **Kasir:** tombol "+ Transaksi baru" buka form (nama pelanggan/meja, menu, jumlah, status).
  Simpan → transaksi tercatat, angka Ringkasan ikut berubah.
- **Stok otomatis:** penjualan di Kasir memotong stok bahan sesuai resep
  (misal Kopi Susu → kopi, susu, gula berkurang). Pembelian menambah stok.
  Stok di bawah minimum muncul di "Bahan perlu dibeli" + tombol Beli.
  Stok tidak cukup → transaksi diblokir + peringatan bahan yang kurang.
- **Edit / Hapus:** tiap menu, bahan, dan baris resep bisa diedit (form terisi data lama)
  dan dihapus (pakai konfirmasi). Hapus menu ikut menghapus resepnya.
- **Grafik "Penjualan minggu ini":** dihitung dari transaksi yang diinput
  (Sen–Min, minggu 2–8 Nov 2026), bar hari ini oranye + label nominal.
- **Laporan:** tombol "Buat Laporan PDF Bulanan" export semua bagian dalam satu PDF.
- **Tutup Buku:** di halaman Laporan. Wajib export PDF dulu baru tombol aktif.
  Setelah dikonfirmasi, transaksi/pembelian/kas bulan itu dibersihkan
  (bulan baru mulai Rp 0), PDF bulan itu tersimpan di "Riwayat Laporan".
  Menu, resep, bahan + stok saat ini, supplier, pelanggan, karyawan tetap ada.

## Catatan data

- Versi ini (preview statis) menyimpan data selama sesi di browser saja —
  refresh halaman akan mengembalikan ke mode mulai dari nol.
- Versi live nanti: colok Supabase (gratis, 500 MB — cukup bertahun-tahun
  untuk ukuran warkop, ~5 MB/bulan). Tabel: transaksi, menu, bahan, resep,
  pembelian, supplier, pelanggan, karyawan, kas.
- Data demo awal: Warung Senja, Admin Senja, Rabu 4 November 2026.

## Struktur repo

- `index.html` — seluruh aplikasi (HTML + CSS + JS) dalam satu file.
- `README.md` — file ini.
