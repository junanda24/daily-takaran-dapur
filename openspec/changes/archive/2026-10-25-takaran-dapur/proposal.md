# Takaran Dapur — Konverter Takaran Masakan Indonesia

## Apa & kenapa
Resep Indonesia menulis "1 gelas belimbing tepung", "3 sdm gula", "segenggam beras" — sementara resep modern menulis gram. Tukang masak rumahan tidak punya timbangan, dan konversi sendok-ke-gram BEDA tiap bahan (1 sdm tepung != 1 sdm gula). Takaran Dapur menyelesaikan itu: pilih bahan, masukkan takaran apa pun (sdm, sdt, gelas belimbing, cup, ml, gram, ons), langsung dapat padanannya di semua satuan, plus Skala Resep (kali 0,5x–3x) untuk masak porsi berbeda.

## Efek kejut
Satuan "gelas belimbing" — gelas legendaris tiap dapur Indonesia — diperlakukan sebagai satuan kelas satu, bukan catatan kaki. Orang akan senyum karena ada yang akhirnya serius mengurus gelas itu. Data berbasis densitas per bahan (bukan angka pukul rata), jadi hasilnya jujur: beda bahan, beda hasil.

## Bentuk output & backend
Web app statis, frontend-only, tanpa login/database. Tidak butuh backend: semua data (14 bahan + densitasnya) statis dan komputasi sepele di browser. Keputusan sadar: nilai adalah PERKIRAAN (densitas bervariasi menurut merek/kelembapan) dan itu ditulis jelas di aplikasi, bukan disembunyikan.
