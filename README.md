# Digital Haus — Countdown & Calendar Studio (v3)

Builder satu halaman untuk membuat countdown & kalender yang siap dipakai di Canva. v3 menambahkan **link Embed untuk Canva** (cara yang sama seperti TickCounter) dan fitur kustomisasi ala TickCounter.

## Mulai cepat
1. Ekstrak ZIP dan buka **index.html** di Chrome / browser lain.
2. Pilih Countdown atau Calendar, isi tanggal, jam, dan zona waktu.
3. Atur tema, warna, font, satuan waktu, background, dll.

## Cara memasukkan countdown BERGERAK ke Canva
Canva tidak bisa menjalankan countdown dari gambar PNG atau HTML mentah yang di-paste. Satu-satunya cara agar angkanya jalan adalah lewat **link Embed**:

1. **Hosting sekali saja.** Buka `app.netlify.com/drop`, tarik folder builder ini ke halaman itu (buat akun gratis supaya situsnya permanen). GitHub Pages / Cloudflare Pages juga bisa.
2. Tempel alamat situsnya (mis. `https://nama-kamu.netlify.app/`) di kolom **Alamat builder** — tersimpan otomatis.
3. Atur desain, lalu klik **Copy ke Canva — countdown bergerak**.
4. Di Canva: **Apps → Embed** → paste link → **Add to design**.

Tombol lain: **Share link**, **Embed code (iframe)** untuk website, **Buka share link** untuk mengetes. Countdown tampil bergerak saat desain Canva dipublikasikan sebagai website / dipresentasikan / dibuka lewat link; desain yang di-download sebagai PNG/PDF/video hanya menampilkan angka saat itu.

**Copy gambar PNG** tetap tersedia untuk gambar diam (kalender, atau snapshot countdown).

## Fitur countdown (ala TickCounter)
- Zona waktu acara (WIB/WITA/WIT dan zona dunia) — semua penonton melihat hitungan yang sama
- Jam sampai detik
- Satuan waktu bebas: tahun, bulan, minggu, hari, jam, menit, detik
- Arah tampilan horizontal / vertikal (vertikal cocok untuk desain portrait)
- Bahasa label & tanggal: English, Indonesia, Melayu, Español, Français, Deutsch, Português, Italiano
- Warna judul, angka, satuan terakhir, dan border + tebal border
- 12 background gradasi (juga di PNG & widget)
- Saat waktu habis: berhenti di nol / hitung naik (count-up) / ulangi tiap N detik–tahun, plus teks selesai
- Link opsional saat countdown diklik
- 8 font, tampil/sembunyikan tiap teks, 3 gaya angka (Cards, Clean, Pills)

## Bonus
- Calendar Builder: ekspor **.ICS** dan link Google Calendar.
- Pengaturan tersimpan lokal di browser (`localStorage`).
- Bisa dipasang sebagai web app (PWA). Setelah upload versi baru, refresh paksa agar service worker (v3) aktif.
- Font Google memakai font cadangan bila perangkat offline.

## Catatan teknis
- Link widget memuat seluruh pengaturan di URL (±1.100 karakter), tanpa server atau database. Perubahan desain = salin link baru.
- Halaman widget membangun tampilannya dengan `textContent` dan memvalidasi warna, URL, dan zona waktu, jadi input berbahaya tidak dieksekusi.
- v3 memperbaiki bug v2: link live sebelumnya menampilkan sisa tampilan builder di belakang widget.
