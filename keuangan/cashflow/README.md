---
judul: "Cashflow — Pencatatan Transaksi Harian"
versi: "1.0"
tanggal_review: "2026-07-23"
type: dokumentasi-sistem
modul: cashflow
tags:
  - keuangan
  - cashflow
  - catatan
status: stabil
---

# Cashflow

Modul ini adalah **tempat mencatat transaksi harian** berdasarkan kategori yang sudah didefinisikan di [[keuangan/struktur-pengeluaran]].

Bukan tempat untuk mendefinisikan ulang kategori — gunakan kategori yang sudah ada. Kalau bingung masuk kategori mana, ikuti alur di [[keuangan/struktur-pengeluaran/README]].

---

## Prinsip Modul

1. **Catat, jangan pikir ulang.** Tugas modul ini hanya mencatat. Proses kategorisasi ditentukan oleh aturan di [[keuangan/struktur-pengeluaran/README]].
2. **Satu baris = satu transaksi.** Tidak ada agregasi dalam satu baris.
3. **Konsisten dengan glosarium.** Semua istilah (kategori, jenis transaksi) harus cocok dengan definisi di [[keuangan/glosarium]].

---

## Aturan Pencatatan

| Aturan | Detail |
|---|---|
| Setiap transaksi harus punya kategori | Pilih salah satu dari 5 kategori struktur-pengeluaran |
| Format tanggal: YYYY-MM-DD | Biar sorting kronologis konsisten |
| Nominal dalam Rupiah | Tulis angka saja, tanpa titik (contoh: `25000`) |
| Deskripsi seminimal mungkin | Cukup jelas buat diingat 6 bulan kemudian |
| Satu file per bulan | Format: `2026-07.md`, `2026-08.md`, dst |

---

## Struktur Folder

```
cashflow/
├── README.md
├── 2026-07.md
├── 2026-08.md
└── ...
```

---

## Format Baris Transaksi

```
YYYY-MM-DD | kategori     | nominal  | deskripsi
```

Contoh:

```
2026-07-01 | rutin         | 25000    | Nasi padang lunch
2026-07-01 | rutin         | 100000   | Bensin motor
2026-07-02 | sosial        | 200000   | Amplop nikah teman
2026-07-03 | darurat       | 50000    | Tambal ban bocor
2026-07-05 | berkala       | 800000   | Pajak STNK tahunan
2026-07-06 | tidak-rutin   | 150000   | Beli baju di Shopee
```

> **Penting:** Nama kategori harus ditulis **sama persis** dengan nama folder di [[keuangan/struktur-pengeluaran]]:
> - `rutin` → pengeluaran-rutin
> - `tidak-rutin` → pengeluaran-tidak-rutin
> - `berkala` → berkala
> - `darurat` → darurat
> - `sosial` → sosial

---

## Cara Membuat File Bulanan

1. Copy template di bawah
2. Simpan sebagai `YYYY-MM.md` (contoh: `2026-08.md`)
3. Mulai catat transaksi harian

### Template

```markdown
# Cashflow — YYYY-MM

## Transaksi

| Tanggal     | Kategori     | Nominal  | Deskripsi          |
|-------------|--------------|----------|--------------------|
| YYYY-MM-DD  | kategori     | 0        | deskripsi singkat  |

## Ringkasan Akhir Bulan

| Kategori       | Total        |
|----------------|--------------|
| Rutin          | 0            |
| Tidak Rutin    | 0            |
| Berkala        | 0            |
| Darurat        | 0            |
| Sosial         | 0            |
| **Total**      | **0**        |
```

---

## Pertanyaan Saat Bingung

Gunakan saat ragu cara mencatat:

- [ ] Apakah transaksi ini sudah jelas kategorinya? (kalau tidak → cek [[keuangan/struktur-pengeluaran/README]])
- [ ] Apakah format tanggal sudah YYYY-MM-DD?
- [ ] Apakah nominal ditulis dalam Rupiah tanpa titik/koma?
- [ ] Apakah nama kategori sesuai dengan yang ada di struktur-pengeluaran?
- [ ] Apakah deskripsi cukup jelas tanpa terlalu panjang?
