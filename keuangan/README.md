---
judul: "Modul Keuangan — Dokumentasi Sistem"
versi: "1.0"
tanggal_review: "2026-07-23"
---

# Modul Keuangan

Ini adalah root folder untuk dokumentasi sistem keuangan. Bukan aplikasi, bukan catatan transaksi — ini adalah **dokumentasi sistem** yang berisi aturan, definisi, prinsip, dan struktur untuk mengelola keputusan finansial secara konsisten.

---

## Filosofi

Dokumentasi ini dibangun dengan keyakinan bahwa:

1. **Sistem yang baik adalah sistem yang sederhana.** Definisi yang jelas, hubungan yang eksplisit, dan aturan yang minimal.
2. **Konsistensi > kebenaran mutlak.** Tidak ada kategori yang sempurna, yang ada adalah kategori yang dipahami bersama. Lebih baik salah secara konsisten daripada benar tapi membingungkan.
3. **Dokumentasi untuk masa depan.** Setiap bagian dibuat dengan asumsi bahwa pembaca adalah diri kita sendiri di 6 bulan yang akan datang, yang sudah lupa kenapa suatu keputusan diambil.

---

## Hubungan Antar Modul

```text
keuangan/
├── README.md                   ← panduan ini
├── glosarium.md                ← acuan istilah sistem
├── struktur-pengeluaran/       ← kategorisasi transaksi keluar
│   ├── pengeluaran-rutin/
│   ├── pengeluaran-tidak-rutin/
│   ├── berkala/
│   ├── darurat/
│   └── sosial/
└── <modul lain>                ← (belum ada)
```

Setiap modul di folder `keuangan/`:

- Bersifat **self-contained**: bisa dimengerti tanpa harus baca modul lain
- Terikat oleh **glosarium global**: semua istilah yang dipakai di semua modul harus konsisten dengan definisi di `glosarium.md`
- Wajib memiliki `README.md` sendiri yang menjelaskan bagaimana modul tersebut bekerja

---

## Prinsip Modular

| Prinsip | Penjelasan |
|---|---|
| Satu domain per folder | Setiap folder mencakup satu domain fungsional (pengeluaran, pemasukan, investasi, dll) |
| Independen | Sebuah modul tidak boleh bergantung pada detail internal modul lain |
| Expansibel | Modul baru tidak boleh membutuhkan perubahan pada modul yang sudah stabil |
| Testable | Definisi di setiap modul harus cukup konkret dan dapat diverifikasi |

## Prinsip Konsistensi

1. **Satu istilah = satu arti.** Tidak ada satu kata yang punya makna berbeda di modul berbeda (kecuali didefinisikan secara spesifik).
2. **Satu transaksi = satu kategori.** Tidak ada transaksi yang masuk ke dua folder/kelas/jenis sekaligus.
3. **Template seragam.** Semua file dokumentasi modul menggunakan template section yang sama (Tujuan, Definisi, Kriteria, Yang Termasuk, Yang Tidak Termasuk, Contoh, Pertanyaan Saat Bingung).
4. **Metadata YAML.** Setiap file memiliki judul, versi, dan tanggal_review di header.

## Single Source of Truth

Setiap fakta atau aturan hanya boleh didefinisikan di satu tempat:

| Fakta | Hanya ada di |
|---|---|
| Definisi istilah | glosarium.md |
| Kategori pengeluaran | struktur-pengeluaran/ |
| Aturan global per modul | README.md modul yang sesuai |
| Aturan global lintas modul | README.md ini |

Jika terjadi konflik antara sumber yang berbeda, aturan mengikuti prioritas:

1. Definisi di `glosarium.md` > definisi pada file dokumen modul
2. Aturan di dokumen root > aturan di dokumen subfolder modul > aturan di folder spesifik

---

## Memulai

Baca glosarium global dulu → masuk ke modul yang diinginkan → gunakan flowchart/pertanyaan di README modul untuk navigasi.

| Ingin | Buka |
|---|---|
| Memahami istilah | [glosarium.md](glosarium.md) |
| Mengkategorikan transaksi | [struktur-pengeluaran/README.md](struktur-pengeluaran) |
