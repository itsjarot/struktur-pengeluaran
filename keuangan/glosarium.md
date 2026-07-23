---
judul: "Glosarium — Sistem Keuangan"
versi: "1.0"
tanggal_review: "2026-07-23"
type: glosarium
modul: keuangan
tags:
  - keuangan
  - glosarium
  - acuan
status: stabil
---

# Glosarium

Acuan istilah sistem keuangan. Setiap istilah di sini menjadi **single source of truth** — semua modul harus menggunakan definisi yang sama.

> **Cara pakai:** Kalau baca modul tertentu dan nemu istilah yang kurang jelas, cari di sini. Kalau ketemu istilah baru yang belum ada di sini, tambahkan. Jangan ubah definisi tanpa update juga referensi di modul lain.

---

## A

### Anggaran
Rencana keuangan yang menetapkan batas alokasi dana untuk periode tertentu (biasanya bulanan atau tahunan). Bisa bersifat tetap atau fleksibel tergantung kategori.
- **Hubungan:** Terkait dengan kategori Pengeluaran (rutin, berkala, tidak rutin) untuk menentukan alokasi.

### Aset
Segala sesuatu yang memiliki nilai ekonomi dan dimiliki oleh individu. Mencakup uang tunai, tabungan, investasi, properti, kendaraan, dan lain-lain.
- **Hubungan:** Lawan dari Liabilitas. Tidak termasuk dalam cakupan modul Pengeluaran.

---

## B

### Berkala (Pengeluaran Berkala)
Lihat **Pengeluaran Berkala**.

---

## C

### Cashflow
Catatan kronologis seluruh transaksi (pengeluaran) yang terjadi dalam periode tertentu. Disusun per bulan dalam format tabel sederhana.
- **Tujuan:** Melacak ke mana uang keluar secara riil, sebagai bahan evaluasi dan laporan.
- **Kapan digunakan:** Setiap kali ada transaksi — catat di file cashflow bulan berjalan.
- **Modul:** [[keuangan/cashflow]]
- **Hubungan:** Setiap baris di cashflow harus merujuk ke salah satu kategori di [[keuangan/struktur-pengeluaran]]. Tanpa kategori, cashflow hanyalah daftar belanja tanpa makna.

---

## D

### Darurat (Pengeluaran Darurat)
Lihat **Pengeluaran Darurat**.

### Dana Darurat
Dana yang disisihkan khusus untuk menghadapi pengeluaran darurat. Idealnya mencakup 3-6 bulan biaya hidup rutin.
- **Hubungan:** Berelasi langsung dengan kategori [Darurat](#darurat-pengeluaran-darurat).

---

## K

### Kategori
Label pengelompokan yang digunakan untuk mengklasifikasikan transaksi finansial. Setiap kategori memiliki definisi, kriteria, dan batasan yang jelas.
- **Hubungan:** Satu transaksi hanya boleh memiliki **satu kategori utama**.

---

## L

### Liabilitas
Kewajiban finansial yang harus dibayar di masa depan. Mencakup utang, cicilan, tagihan yang belum dibayar.
- **Hubungan:** Beberapa Pengeluaran Berkala (cicilan KPR, KKB) memiliki unsur liabilitas.

---

## P

### Pengeluaran
Arus kas keluar — uang yang dibayarkan untuk memperoleh barang, jasa, atau memenuhi kewajiban.
- **Hubungan:** Lawan dari Pemasukan (belum didefinisikan dalam sistem ini). Terbagi menjadi 5 kategori.

### Pengeluaran Berkala
Pengeluaran yang terjadi secara periodik dengan interval lebih dari satu bulan dan umumnya memiliki tanggal jatuh tempo yang pasti.
- **Kriteria:** Interval >1 bulan, terjadwal, ada jatuh tempo.
- **Yang termasuk:** Pajak tahunan, asuransi, iuran tahunan.
- **Hubungan:** Berbeda dengan [Pengeluaran Rutin](#pengeluaran-rutin) pada intervalnya. Berbeda dengan [Pengeluaran Tidak Rutin](#pengeluaran-tidak-rutin) pada kepastian jadwal.
- **Modul:** [[keuangan/struktur-pengeluaran/berkala]]

### Pengeluaran Darurat
Pengeluaran yang tidak terduga, mendesak, dan harus segera dibayar.
- **Kriteria:** Tidak direncanakan, mendesak, ada risiko/kerugian jika ditunda.
- **Yang termasuk:** Biaya RS mendadak, perbaikan darurat, ban bocor.
- **Hubungan:** Tidak sama dengan [Pengeluaran Tidak Rutin](#pengeluaran-tidak-rutin) yang sifatnya bisa ditunda. Lawan dari kategori yang sudah direncanakan.
- **Modul:** [[keuangan/struktur-pengeluaran/darurat]]

### Pengeluaran Rutin
Pengeluaran yang terjadi berulang (mingguan/bulanan) dan dibutuhkan untuk menjalani kehidupan sehari-hari.
- **Kriteria:** Frekuensi tetap minimal 1x/bulan, dibutuhkan secara kontinu, nominal boleh naik-turun.
- **Yang termasuk:** Makan sehari-hari, bensin, token listrik, kuota internet.
- **Hubungan:** Berbeda dengan [Pengeluaran Tidak Rutin](#pengeluaran-tidak-rutin) pada aspek keberulangan dan urgensi. Berbeda dengan [Pengeluaran Berkala](#pengeluaran-berkala) pada interval (<1 bulan).
- **Modul:** [[keuangan/struktur-pengeluaran/pengeluaran-rutin]]

### Pengeluaran Sosial
Pengeluaran yang tujuan utamanya untuk kepentingan orang lain, hubungan sosial, atau berbagi.
- **Kriteria:** Penerima manfaat orang lain, motivasi memberi/relasi, tidak mengharapkan imbalan materi.
- **Yang termasuk:** Amplop nikah, sedekah, THR, traktir teman.
- **Hubungan:** Berbeda dengan kategori lain karena orientasinya ke orang lain, bukan ke diri sendiri.
- **Modul:** [[keuangan/struktur-pengeluaran/sosial]]

### Pengeluaran Tidak Rutin
Pengeluaran yang terjadi sewaktu-waktu, tidak terikat siklus harian/mingguan/bulanan, dan bersifat situasional atau keinginan.
- **Kriteria:** Frekuensi tidak menentu, bisa ditunda, lebih ke pilihan daripada kebutuhan.
- **Yang termasuk:** Beli baju, servis AC, tiket nonton, beli gadget.
- **Hubungan:** Kategori "sisa" — segala yang tidak masuk rutin, berkala, darurat, atau sosial.
- **Modul:** [[keuangan/struktur-pengeluaran/pengeluaran-tidak-rutin]]

---

## S

### Sosial (Pengeluaran Sosial)
Lihat **Pengeluaran Sosial**.

### Single Source of Truth (SSOT)
Prinsip bahwa setiap fakta atau aturan hanya didefinisikan di satu tempat dalam sistem dokumentasi. Lihat `keuangan/README.md`
- **Hubungan:** Berlaku untuk semua modul dalam folder keuangan.

---

## T

### Transaksi
Unit dasar dari sistem keuangan. Mewakili satu perpindahan uang (masuk atau keluar) pada satu waktu tertentu dengan nominal dan tujuan tertentu.
- **Aturan:** Satu transaksi hanya boleh memiliki **satu kategori**. Jika ragu, gunakan flowchart di [[keuangan/struktur-pengeluaran/README]].

### Tidak Rutin (Pengeluaran Tidak Rutin)
Lihat **Pengeluaran Tidak Rutin**.
