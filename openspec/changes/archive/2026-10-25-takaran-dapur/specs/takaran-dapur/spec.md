# Spec: Takaran Dapur

## SHALL
- SHALL: konverter dua arah — WHEN pengguna memilih bahan + jumlah + satuan asal, THEN aplikasi menampilkan hasil di satuan target DAN tabel padanan semua satuan (volume + berat).
- SHALL: 14 bahan dengan densitas berbeda: tepung terigu, gula pasir, gula merah, mentega, minyak goreng, air, beras, tepung beras, tepung tapioka, cokelat bubuk, garam, santan, madu, susu bubuk.
- SHALL: satuan: sdt (5 ml), sdm (15 ml), gelas belimbing (200 ml), cup (240 ml), ml, gram, ons (100 g), kg.
- SHALL: konversi volume<->berat memakai densitas bahan; konversi berat<->berat dan volume<->volume tidak bergantung bahan.
- SHALL: Skala Resep — WHEN pengguna menambah baris bahan + takaran lalu memilih pengali (0,5x/1x/1,5x/2x/3x/custom), THEN semua baris diskalakan dan ditampilkan dalam satuan asal + gram.
- SHALL: preset cepat ("1 gelas belimbing tepung", "3 sdm gula", dll) sekali ketuk mengisi konverter.
- SHALL: tombol salin hasil; label jelas bahwa semua nilai adalah perkiraan.
- SHALL: mobile-friendly, copy Bahasa Indonesia natural, tanpa lorem ipsum, tanpa placeholder palsu, tanpa fungsi mati.
- SHALL: momen delight — animasi count-up pada hasil dan micro-interaction saat konversi berubah.
