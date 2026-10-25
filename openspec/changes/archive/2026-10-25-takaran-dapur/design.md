# Design: Takaran Dapur
- Stack: web artifact statis (HTML/CSS/JS client-side), single-file section discipline (STATE satu objek, DATA densitas terpisah dari logic, RENDER murni, EVENTS tipis) sesuai ARCHITECTURE.md bagian web artifact statis.
- State: keranjang Lokal saja (pilihan bahan, jumlah, satuan, daftar skala resep). Tidak ada server state, tidak ada global store.
- Model data: tiap bahan = densitas g/ml. Volume satuan dalam ml; berat dalam gram. gram = ml * densitas.
- Densitas (g/ml, perkiraan standar baking): terigu 0,53; gula pasir 0,83; gula merah 0,92; mentega 0,96; minyak 0,91; air 1,00; beras 0,77; tepung beras 0,66; tapioka 0,53; cokelat bubuk 0,42; garam 1,20; santan 0,97; madu 1,42; susu bubuk 0,48.
- Visual: dapur hangat (krem + oranye bata + hijau daun), kartu bahan bergambar ikon, mobile-first. Delight: angka hasil count-up, sendok bergoyang saat nilai berubah.
- IP: semua ikon/grafis digambar via CSS/emoji generik, tanpa aset pihak ketiga.
