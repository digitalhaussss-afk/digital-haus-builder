# Digital Haus — Countdown & Calendar Studio

Web builder (installable PWA) for beautiful Canva-ready countdown and calendar widgets.

## Cara pakai
1. Buka `index.html` melalui browser untuk mencoba builder.
2. Pilih **Countdown** atau **Calendar**, lalu isi tanggal, teks, warna, dan gaya.
3. Tekan **Copy ke Canva**, paste di editor Canva. Jika copy gambar tidak diizinkan browser, builder otomatis mengunduh PNG transparan. Gunakan **Uploads → Upload files** di Canva.
4. Countdown PNG hanyalah *snapshot* (tidak bergerak). Untuk hitung mundur langsung, tekan **Live Widget HTML**, upload file HTML hasil ekspor ke hosting HTTPS yang menghasilkan URL publik, lalu coba **Canva → Apps → Embed** dan masukkan URL. Dukungan URL/jenis desain bergantung Canva.
5. Pada Calendar Builder, tersedia juga file `.ics` dan tombol Google Calendar.

## Deploy
Upload seluruh isi folder ini ke GitHub Pages, Netlify, atau hosting statis lainnya. Lalu bagikan URL hasil hostingnya. File `manifest.webmanifest` dan `sw.js` memungkinkan pemasangan sebagai web app (PWA) di browser yang mendukung. Browser biasanya membutuhkan HTTPS untuk fitur clipboard dan instalasi PWA.

## Catatan
- Tidak ada akun / database / backend; data desain disimpan di browser perangkat.
- Font Google akan menggunakan fallback bawaan perangkat bila offline.
- Tanggal/jam event memakai zona waktu perangkat saat widget HTML diekspor (widget timer menyimpan waktu UTC absolut, sehingga benar pada browser tamu di zona waktu berbeda).
- Widget HTML terpisah perlu dihosting pada URL publik untuk percobaan embed di Canva. Menyalin HTML mentah ke Canva tidak didukung.
