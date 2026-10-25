# Takaran Dapur — Konverter Takaran Masakan Indonesia

Resep Indonesia bilang "1 gelas belimbing tepung", resep modern bilang "106 gram".
Padahal 1 sendok tepung tidak sama beratnya dengan 1 sendok gula. Takaran Dapur
menyelesaikan kebingungan itu: pilih bahan, masukkan takaran apa pun (sdt, sdm,
gelas belimbing, cup, ml, gram, ons), langsung dapat padanannya — karena tiap
bahan punya densitas sendiri.

## Kenapa ide ini dipilih

Efek kejutnya ada di gelas belimbing: gelas legendaris yang ada di hampir tiap
dapur Indonesia akhirnya diperlakukan sebagai satuan kelas satu, bukan catatan
kaki. Tidak ada timbangan? Tidak masalah — sendok dan gelas di dapur sudah cukup.

## Fitur

- Konverter dua arah: bahan + jumlah + satuan asal → hasil di satuan target
  plus tabel padanan semua satuan.
- 14 bahan dengan densitas berbeda: tepung terigu, gula pasir, gula merah,
  mentega, minyak goreng, air, beras, tepung beras, tepung tapioka, cokelat
  bubuk, garam, santan, madu, susu bubuk.
- Satuan: sdt (5 ml), sdm (15 ml), gelas belimbing (200 ml), cup (240 ml),
  ml, gram, ons (100 g), kg. Tombol tukar satuan asal–target.
- Preset sekali ketuk (mis. "1 gelas belimbing tepung terigu").
- Skala Resep: tambah baris bahan + takaran, kalikan 0,5x/1x/1,5x/2x/3x/custom
  — tiap baris menampilkan hasil skala dalam satuan asal dan gram.
- Tombol salin hasil ("3 sdm gula pasir = 37,5 gram").
- Angka hasil animasi count-up + micro-interaction sendok bergoyang.
- Catatan jujur di aplikasi: semua nilai adalah PERKIRAAN.

## Cara pakai

Buka link artifact, pilih bahan, isi jumlah, pilih satuan asal dan target.
Untuk resep sekeluarga: buka Skala Resep, tambahkan semua bahan, pilih pengali.

## Cara mengembangkan dari source

Hasil export artifact ada di `src/` (file HTML mandiri hasil `artifact.export`).
Tidak ada build step, tidak ada backend, tidak ada dependensi: buka file HTML
di browser apa pun dan aplikasi langsung jalan.

## Tech stack

- Web app statis client-side (HTML/CSS/JavaScript), tanpa login, tanpa database.
- Model konversi: `gram = ml × densitas bahan` (densitas per bahan, g/ml):
  terigu 0,53; gula pasir 0,83; gula merah 0,92; mentega 0,96; minyak 0,91;
  air 1,00; beras 0,77; tepung beras 0,66; tapioka 0,53; cokelat bubuk 0,42;
  garam 1,20; santan 0,97; madu 1,42; susu bubuk 0,48.

## Struktur folder

```
2026-10-25-takaran-dapur/
├── README.md
├── src/                  # export artifact (HTML mandiri)
└── openspec/changes/archive/2026-10-25-takaran-dapur/
    ├── proposal.md
    ├── design.md
    ├── tasks.md
    └── specs/takaran-dapur/spec.md
```

## Link hasil

- Artifact: lihat kartu artifact `takaran-dapur` (link share menyusul setelah build selesai)
- Repo: https://github.com/junanda24/daily-takaran-dapur
- Tanggal rilis: 2026-10-25

## Catatan / temuan saat build

- Yang disengaja TIDAK dibuat: database resep tersimpan dan login — tidak
  dibutuhkan; konverter harus langsung pakai tanpa akun.
- Nilai adalah perkiraan: densitas nyata bervariasi menurut merek, kelembapan,
  dan cara mengisi sendok (munjung vs peres). Aplikasi menampilkan peringatan
  ini, bukan menyembunyikannya.
- Gelas belimbing diasumsikan 200 ml (ukuran umum gelas belimbing penuh);
  cup diasumsikan 240 ml (standar cup US).
