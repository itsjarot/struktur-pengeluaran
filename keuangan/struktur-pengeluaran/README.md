---
judul: "Aturan Global Dokumentasi Pengeluaran"
versi: "1.0"
tanggal_review: "2026-07-23"
---

# Aturan Global Dokumentasi Pengeluaran

Dokumen ini adalah **aturan main** untuk seluruh folder di `struktur-pengeluaran/`.  
Baca ini dulu sebelum mulai mengkategorikan transaksi.

---

## Aturan Besi: Satu Transaksi = Satu Kategori

Setiap transasi hanya boleh masuk **satu kategori utama**. Tidak ada transaksi yang masuk ke dua folder sekaligus.

> **Konsep Gerbong:** Anggap setiap kategori seperti gerbong kereta. Satu transaksi naik ke satu gerbong. Kalau ragu, ikuti alur tanya-jawab di bawah.

> Kalau terasa **sama kuat** antara dua kategori, gunakan `Pertanyaan Saat Bingung` di masing-masing file untuk memutuskan. Salah pilih tidak masalah — yang penting konsisten.

---

## Alur Tanya-Jawab: Menentukan Kategori Transaksi

Jawab pertanyaan **berurutan** dari atas. Berhenti di `Ya` pertama.

```
1. APAKAH INI DARURAT?
   → Apakah mendesak, tak terduga, dan butuh dibayar segera?
   │ Ya   → 📁 darurat/
   │ Tidak → lanjut ke 2

2. APAKAH TUJUANNYA MEMBERI ATAU RELASI?
   → Apakah ini untuk sedekah, hadiah, traktir, atau hubungan sosial?
   │ Ya   → 📁 sosial/
   │ Tidak → lanjut ke 3

3. APAKAH INI TERJADI BERULANG UNTUK KEBUTUHAN SEHARI-HARI?
   → Apakah ini pengeluaran yang muncul mingguan/bulanan dan diperlukan buat hidup normal?
   │ Ya   → 📁 pengeluaran-rutin/
   │ Tidak → lanjut ke 4

4. APAKAH INI TERJADI PERIODIK (>1 BULAN SEKALI)?
   → Apakah ini tagihan tahunan, iuran semester, atau langganan tahunan?
   │ Ya   → 📁 berkala/
   │ Tidak → 📁 pengeluaran-tidak-rutin/
```

---

## Template Setiap File

Setiap file Markdown di folder ini mengikuti struktur seragam:

| Bagian | Fungsi |
|---|---|
| Metadata | YAML front matter: judul, versi, tanggal_review |
| Prinsip Kategori | Filosofi kenapa kategori ini ada |
| Tujuan | Satu kalimat jelas tentang tujuan kategori |
| Definisi | Definisi formal |
| Kriteria | Syarat konkret masuk kategori ini |
| Ruang Lingkup | Batasan yang di-cover |
| Yang Termasuk | Daftar item konkret yang masuk |
| Yang Tidak Termasuk | Daftar item yang sering salah masuk (plus arahkan) |
| Contoh | 2-3 contoh real dengan ilustrasi |
| Pertanyaan Saat Bingung | Checklist untuk menentukan kategori |

---

## Cara Maintenance

- **Tanggal review** di metadata diupdate setiap kali definisi berubah.
- Kalau ada kategori baru, buat file baru dengan template yang sama, lalu update flowchart di README ini.
- Jangan hapus kategori yang sudah ada tanpa migrasi transaksi ke kategori lain.
